# xiaoyu-skills

> xiaoyu 生态的 Skills 聚合与分发中心

## 📦 仓库结构

```
xiaoyu-skills/
├── suppliers/           # Skills 供应商索引（带摘要）
│   ├── official/        # 官方仓库（Anthropic, OpenAI）
│   ├── community/       # 社区仓库
│   └── niche/           # 细分领域
├── skills/              # xiaoyu 自研 Skills
├── templates/           # Skill 模板
└── docs/                # 文档
```

## 🎯 用途

1. **Skills 发现**：索引优秀的第三方 skills 供应商
2. **Skills 分发**：沉淀 xiaoyu 智能体生态的自研 skills
3. **API 支持**：为 [assistant-mcp](https://github.com/maplefeng-a/assistant-mcp) 提供统一的 skills 查询接口

## 🚀 快速开始

### 安装 Skill

```bash
# 通过 OpenClaw 安装
/plugin install xiaoyu-knowledge-learning@maplefeng-a/xiaoyu-skills

# 通过 Claude Code 安装
/plugin install xiaoyu-knowledge-learning@xiaoyu-skills
```

### 浏览 Skills

- [官方 Skills](suppliers/official/) - Anthropic / OpenAI 官方维护
- [社区 Skills](suppliers/community/) - 高质量社区仓库
- [xiaoyu Skills](skills/) - xiaoyu 自研 skills

## 📋 供应商列表

| 供应商 | 类型 | Stars | Skills 数量 |
|--------|------|-------|-------------|
| [Anthropic](suppliers/official/anthropic.md) | 官方 | 85.9k | 17 |
| [OpenAI](suppliers/official/openai.md) | 官方 | 11.9k | 38+ |
| [awesome-claude-code](suppliers/community/awesome-claude-code.md) | 社区 | 26.6k | - |
| [antigravity-awesome-skills](suppliers/community/antigravity-awesome-skills.md) | 社区 | 21.0k | 1000+ |

## 🔌 API 规范

本仓库遵循 [Agent Skills](https://agentskills.io) 开放规范。

### 供应商文档格式

每个供应商文档包含 YAML 元数据 + Markdown 内容：

```yaml
---
supplier_id: anthropic
name: Anthropic Official Skills
repo: https://github.com/anthropics/skills
stars: 85947
license: Apache-2.0
platforms: [claude-code, claude-api, openclaw]
indexed_at: 2026-03-07
---

# Skills 列表

| name | description | category |
|------|-------------|----------|
| docx | 创建、读取、编辑 Word 文档 | 文档 |
| ... | ... | ... |
```

### 查询接口

```typescript
// GET /suppliers - 获取所有供应商
// GET /suppliers/:id/skills - 获取供应商的所有 skills
// GET /skills/search?q=keyword - 跨供应商搜索
```

详见 [docs/api-spec.md](docs/api-spec.md)

## 🏷️ 版本管理

- 每个 skill 独立版本（语义化版本）
- 统一 [CHANGELOG.md](CHANGELOG.md) 记录变更
- Git Tag 格式：`skills/<skill-name>/v<version>`

## 🤝 贡献

1. Fork 本仓库
2. 添加新的 skill 或供应商索引
3. 提交 PR

## 📄 License

- 自研 Skills：Apache-2.0
- 供应商索引：CC BY 4.0
