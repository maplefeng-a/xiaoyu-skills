# Skills 供应商索引

本目录收录优秀的 Agent Skills 供应商，每个供应商包含：
- 基本信息（仓库、Stars、License）
- Skills 列表（带摘要）
- 安装方式

## 📊 供应商总览

| ID | 名称 | 类型 | Stars | Skills | 平台 |
|----|------|------|-------|--------|------|
| anthropic | [Anthropic Official](official/anthropic.md) | 官方 | 85.9k | 17 | claude-code, claude-api, openclaw |
| openai | [OpenAI Codex](official/openai.md) | 官方 | 11.9k | 38+ | codex, openclaw |
| awesome-claude-code | [Awesome Claude Code](community/awesome-claude-code.md) | 社区 | 26.6k | - | claude-code |
| antigravity-skills | [Antigravity Awesome Skills](community/antigravity-awesome-skills.md) | 社区 | 21.0k | 1000+ | claude-code, codex, cursor |

## 🗂️ 目录结构

```
suppliers/
├── official/        # 官方仓库
│   ├── anthropic.md
│   └── openai.md
├── community/       # 社区仓库
│   ├── awesome-claude-code.md
│   └── antigravity-awesome-skills.md
└── niche/           # 细分领域
    └── (待添加)
```

## 📝 文档格式

每个供应商文档包含：

```yaml
---
# YAML 元数据（供程序解析）
supplier_id: anthropic
name: Anthropic Official Skills
repo: https://github.com/anthropics/skills
stars: 85947
license: Apache-2.0
platforms: [claude-code, claude-api, openclaw]
indexed_at: 2026-03-07
---

# Markdown 内容（供人类阅读）
## 概述
...

## Skills 列表
| name | description | category |
|------|-------------|----------|
| ... | ... | ... |
```

## 🔌 API 接口

本索引为 [assistant-mcp](https://github.com/maplefeng-a/assistant-mcp) 提供数据源：

```typescript
// 获取所有供应商
GET /suppliers
Response: { suppliers: [...] }

// 获取供应商的 skills
GET /suppliers/:id/skills
Response: { skills: [...] }

// 跨供应商搜索
GET /skills/search?q=document
Response: { results: [...] }
```

## 🔄 更新频率

- **官方仓库**：每周检查更新
- **社区仓库**：每月检查更新
- **细分领域**：按需更新

## 📮 添加新供应商

1. 在对应目录创建 `<supplier-id>.md`
2. 填写 YAML 元数据
3. 列出 Skills 清单
4. 提交 PR
