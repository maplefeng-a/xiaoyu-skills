---
supplier_id: openai
name: OpenAI Codex Skills
repo: https://github.com/openai/skills
stars: 11931
license: MIT
platforms:
  - codex
  - openclaw
indexed_at: 2026-03-07
commit: main
---

# OpenAI Codex Skills

OpenAI 官方维护的 Codex CLI Skills 目录，聚焦工程开发、部署、协作场景。

## 概述

- **仓库**：https://github.com/openai/skills
- **Stars**：11.9k ⭐
- **License**：MIT（大部分）
- **规范**：[agentskills.io](https://agentskills.io)

## Skills 列表

### 系统 Skills（自动安装）

| name | description | category |
|------|-------------|----------|
| skill-installer | 安装和管理其他 skills | 系统 |
| skill-creator | 创建新 skills | 系统 |
| openai-docs | OpenAI 文档查询 | 系统 |

### 精选 Skills

| name | description | category |
|------|-------------|----------|
| doc | 文档创建与管理 | 文档 |
| pdf | PDF 处理 | 文档 |
| slides | 幻灯片创建 | 文档 |
| spreadsheet | 电子表格操作 | 文档 |
| playwright | Playwright 自动化测试 | 开发 |
| playwright-interactive | 交互式 Playwright 测试 | 开发 |
| figma | Figma 设计集成 | 设计 |
| figma-implement-design | 实现 Figma 设计 | 设计 |
| screenshot | 网页截图工具 | 工具 |
| imagegen | 图像生成 | 创意 |
| sora | Sora 视频生成 | 创意 |
| speech | 语音合成 | 音频 |
| transcribe | 语音转文字 | 音频 |
| jupyter-notebook | Jupyter Notebook 操作 | 数据 |
| aspnet-core | ASP.NET Core 开发 | 开发 |
| chatgpt-apps | ChatGPT 应用开发 | 开发 |
| develop-web-game | Web 游戏开发 | 开发 |
| winui-app | Windows UI 应用开发 | 开发 |

### 部署 Skills

| name | description | category |
|------|-------------|----------|
| vercel-deploy | Vercel 部署 | 部署 |
| netlify-deploy | Netlify 部署 | 部署 |
| cloudflare-deploy | Cloudflare 部署 | 部署 |
| render-deploy | Render 部署 | 部署 |

### 协作 Skills

| name | description | category |
|------|-------------|----------|
| notion-meeting-intelligence | Notion 会议智能 | 协作 |
| notion-knowledge-capture | Notion 知识捕获 | 协作 |
| notion-research-documentation | Notion 研究文档 | 协作 |
| notion-spec-to-implementation | Notion 规格到实现 | 协作 |
| linear | Linear 项目管理 | 协作 |
| sentry | Sentry 错误监控 | 监控 |
| gh-address-comments | GitHub 处理 PR 评论 | 开发 |
| gh-fix-ci | GitHub 修复 CI | 开发 |

### 安全 Skills

| name | description | category |
|------|-------------|----------|
| security-best-practices | 安全最佳实践 | 安全 |
| security-ownership-map | 安全所有权映射 | 安全 |
| security-threat-model | 威胁建模 | 安全 |

### 其他

| name | description | category |
|------|-------------|----------|
| yeet | 快速分享代码片段 | 工具 |

## 安装方式

### Codex CLI

```bash
# 安装精选 skill
$skill-installer gh-address-comments

# 安装实验性 skill
$skill-installer install the create-plan skill from the .experimental folder

# 从 GitHub URL 安装
$skill-installer install https://github.com/openai/skills/tree/main/skills/.experimental/create-plan
```

### OpenClaw

```bash
# 克隆到 skills 目录
cd ~/.openclaw/skills
git clone https://github.com/openai/skills.git openai-official
```

## 目录结构

```
openai/skills/
├── skills/
│   ├── .system/         # 3 个系统 skills（自动安装）
│   ├── .curated/        # 35 个精选 skills
│   └── .experimental/   # 实验性 skills
├── README.md
└── contributing.md
```

## 质量评价

⭐⭐⭐⭐ **官方维护，聚焦工程场景**

- 部署类 skills 丰富（Vercel/Netlify/Cloudflare/Render）
- 安全类 skills 独特（威胁建模、所有权映射）
- Notion/Linear 等协作工具集成完善
- 部分 skills 仍在实验阶段

## 相关链接

- [Codex Skills 文档](https://developers.openai.com/codex/skills)
- [创建自定义 Skills](https://developers.openai.com/codex/skills/create-skill)
- [Agent Skills 规范](https://agentskills.io)
