# xiaoyu-skills API 规范

本文档定义 xiaoyu-skills 的 API 接口，供 [assistant-mcp](https://github.com/maplefeng-a/assistant-mcp) 集成使用。

## 概述

API 基于 HTTP/REST，返回 JSON 格式数据。

## 接口列表

### 1. 获取所有供应商

```http
GET /suppliers
```

**Response:**
```json
{
  "suppliers": [
    {
      "id": "anthropic",
      "name": "Anthropic Official Skills",
      "repo": "https://github.com/anthropics/skills",
      "stars": 85947,
      "license": "Apache-2.0",
      "platforms": ["claude-code", "claude-api", "openclaw"],
      "indexed_at": "2026-03-07"
    },
    {
      "id": "openai",
      "name": "OpenAI Codex Skills",
      "repo": "https://github.com/openai/skills",
      "stars": 11931,
      "license": "MIT",
      "platforms": ["codex", "openclaw"],
      "indexed_at": "2026-03-07"
    }
  ],
  "total": 4
}
```

### 2. 获取供应商详情

```http
GET /suppliers/:id
```

**Response:**
```json
{
  "id": "anthropic",
  "name": "Anthropic Official Skills",
  "repo": "https://github.com/anthropics/skills",
  "stars": 85947,
  "license": "Apache-2.0",
  "platforms": ["claude-code", "claude-api", "openclaw"],
  "indexed_at": "2026-03-07",
  "commit": "main",
  "description": "Anthropic 官方维护的 Agent Skills 仓库...",
  "quality_rating": 5
}
```

### 3. 获取供应商的 Skills

```http
GET /suppliers/:id/skills
```

**Response:**
```json
{
  "supplier_id": "anthropic",
  "skills": [
    {
      "name": "docx",
      "description": "创建、读取、编辑、转换 Word 文档 (.docx)",
      "category": "文档",
      "license": "Proprietary"
    },
    {
      "name": "pdf",
      "description": "PDF 处理与分析",
      "category": "文档",
      "license": "Proprietary"
    }
  ],
  "total": 17
}
```

### 4. 跨供应商搜索 Skills

```http
GET /skills/search?q=keyword&platform=openclaw&category=文档
```

**Query Parameters:**
- `q` (required): 搜索关键词
- `platform` (optional): 平台过滤 (openclaw, claude-code, codex)
- `category` (optional): 分类过滤

**Response:**
```json
{
  "query": "document",
  "results": [
    {
      "supplier_id": "anthropic",
      "supplier_name": "Anthropic Official Skills",
      "name": "docx",
      "description": "创建、读取、编辑、转换 Word 文档 (.docx)",
      "category": "文档",
      "relevance": 0.95
    },
    {
      "supplier_id": "anthropic",
      "supplier_name": "Anthropic Official Skills",
      "name": "pdf",
      "description": "PDF 处理与分析",
      "category": "文档",
      "relevance": 0.92
    },
    {
      "supplier_id": "openai",
      "supplier_name": "OpenAI Codex Skills",
      "name": "doc",
      "description": "文档创建与管理",
      "category": "文档",
      "relevance": 0.88
    }
  ],
  "total": 5
}
```

### 5. 获取 xiaoyu 自研 Skills

```http
GET /xiaoyu/skills
```

**Response:**
```json
{
  "skills": [
    {
      "name": "xiaoyu-knowledge-learning",
      "version": "1.0.0",
      "description": "围绕主题开展研究学习的闭环 skill...",
      "status": "released",
      "updated": "2026-03-07"
    }
  ],
  "total": 1
}
```

### 6. 获取 xiaoyu Skill 详情

```http
GET /xiaoyu/skills/:name
```

**Response:**
```json
{
  "name": "xiaoyu-knowledge-learning",
  "version": "1.0.0",
  "description": "围绕主题开展研究学习的闭环 skill...",
  "content": "# Knowledge Learning Loop\n\n...",
  "changelog": [
    {
      "version": "1.0.0",
      "date": "2026-03-07",
      "note": "初始版本，从 knowledge-learning-loop 迁移"
    }
  ],
  "compatibility": {
    "platforms": ["openclaw"],
    "tools": ["memory_search", "read", "write", "edit", "web_search", "web_fetch", "exec"]
  }
}
```

### 7. 获取 xiaoyu Skill 特定版本

```http
GET /xiaoyu/skills/:name/:version
```

**Response:** 同上，返回指定版本的内容

## 数据格式

### Supplier

```typescript
interface Supplier {
  id: string;              // 供应商 ID
  name: string;            // 显示名称
  repo: string;            // 仓库 URL
  stars: number;           // GitHub Stars
  license: string;         // 许可证
  platforms: string[];     // 支持的平台
  indexed_at: string;      // 索引日期 (YYYY-MM-DD)
  commit?: string;         // Git commit
  description?: string;    // 描述
  quality_rating?: number; // 质量评分 (1-5)
}
```

### Skill

```typescript
interface Skill {
  name: string;            // Skill 名称
  version?: string;        // 版本号（xiaoyu skills）
  description: string;     // 描述
  category?: string;       // 分类
  license?: string;        // 许可证
  content?: string;        // SKILL.md 完整内容
  changelog?: Changelog[]; // 变更历史
  compatibility?: {        // 兼容性
    platforms: string[];
    tools?: string[];
  };
}
```

### Changelog

```typescript
interface Changelog {
  version: string;   // 版本号
  date: string;      // 发布日期
  note: string;      // 变更说明
}
```

## 错误响应

```json
{
  "error": {
    "code": "NOT_FOUND",
    "message": "Supplier not found: unknown"
  }
}
```

**Error Codes:**
- `NOT_FOUND`: 资源不存在
- `INVALID_QUERY`: 查询参数无效
- `INTERNAL_ERROR`: 服务器内部错误

## 实现建议

1. **数据源**：解析 `suppliers/*.md` 和 `skills/*/SKILL.md` 文件
2. **缓存**：建议缓存解析结果，定期刷新
3. **搜索**：可使用简单的关键词匹配，或集成 Elasticsearch
4. **版本控制**：通过 Git Tag 获取历史版本
