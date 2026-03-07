---
supplier_id: anthropic
name: Anthropic Official Skills
repo: https://github.com/anthropics/skills
stars: 85947
license: Apache-2.0 (部分 Proprietary)
platforms:
  - claude-code
  - claude-api
  - claude-ai
  - openclaw
indexed_at: 2026-03-07
commit: main
---

# Anthropic Official Skills

Anthropic 官方维护的 Agent Skills 仓库，包含文档处理、开发工具、设计创意等生产级 skills。

## 概述

- **仓库**：https://github.com/anthropics/skills
- **Stars**：85.9k ⭐
- **License**：Apache-2.0（示例 skills）/ Proprietary（文档 skills）
- **规范**：[agentskills.io](https://agentskills.io)

## Skills 列表

| name | description | category | license |
|------|-------------|----------|---------|
| docx | 创建、读取、编辑、转换 Word 文档 (.docx) | 文档 | Proprietary |
| pdf | PDF 处理与分析 | 文档 | Proprietary |
| pptx | PowerPoint 创建与编辑 | 文档 | Proprietary |
| xlsx | Excel 电子表格创建与操作 | 文档 | Proprietary |
| mcp-builder | 构建 MCP (Model Context Protocol) 服务器 | 开发 | Apache-2.0 |
| skill-creator | 创建、修改、优化 Agent Skills | 开发 | Apache-2.0 |
| claude-api | Claude API 使用指南与最佳实践 | 开发 | Apache-2.0 |
| webapp-testing | Web 应用测试与自动化 | 开发 | Apache-2.0 |
| web-artifacts-builder | 构建 Web artifacts | 开发 | Apache-2.0 |
| algorithmic-art | 算法艺术生成 | 创意 | Apache-2.0 |
| canvas-design | Canvas 设计工具 | 创意 | Apache-2.0 |
| theme-factory | 主题工厂 - 创建一致的设计主题 | 创意 | Apache-2.0 |
| frontend-design | 前端设计指南 | 创意 | Apache-2.0 |
| brand-guidelines | 品牌指南应用 | 企业 | Apache-2.0 |
| internal-comms | 内部沟通模板与指南 | 企业 | Apache-2.0 |
| doc-coauthoring | 文档协作流程 | 企业 | Apache-2.0 |
| slack-gif-creator | Slack GIF 创建工具 | 工具 | Apache-2.0 |

## 安装方式

### Claude Code

```bash
# 添加为 marketplace
/plugin marketplace add anthropics/skills

# 安装文档 skills
/plugin install document-skills@anthropic-agent-skills

# 安装示例 skills
/plugin install example-skills@anthropic-agent-skills
```

### OpenClaw

```bash
# 克隆到 skills 目录
cd ~/.openclaw/skills
git clone https://github.com/anthropics/skills.git anthropic-official
```

### Claude API

通过 [Skills API](https://docs.claude.com/en/api/skills-guide) 上传使用。

## 目录结构

```
anthropics/skills/
├── skills/              # 17 个 skills
│   ├── docx/
│   ├── pdf/
│   ├── pptx/
│   ├── xlsx/
│   ├── mcp-builder/
│   └── ...
├── spec/                # Agent Skills 规范
├── template/            # Skill 模板
└── README.md
```

## 质量评价

⭐⭐⭐⭐⭐ **官方维护，生产级质量**

- 文档 skills (docx/pdf/pptx/xlsx) 已在 Claude 产品中广泛使用
- 遵循 agentskills.io 开放规范
- 包含完整的 skill-creator 工具链
- 定期更新，社区活跃

## 相关链接

- [Agent Skills 规范](https://agentskills.io)
- [Claude Skills 文档](https://support.claude.com/en/articles/12512176-what-are-skills)
- [创建自定义 Skills](https://support.claude.com/en/articles/12512198-creating-custom-skills)
