---
supplier_id: clawhub-skills
name: ClawHub Skills Platform
repo: https://clawhub.ai
stars: N/A
license: Mixed
type: platform
platforms:
  - openclaw
  - claude-code
indexed_at: 2026-03-10
skills_count: 22004+
note: "数量最大的 Skills 平台，社区驱动，向量语义搜索"
---

# ClawHub Skills Platform

全球最大的 Skills 分发平台，22,000+ Skills，向量语义搜索，社区驱动。

## 概述

- **平台**：https://clawhub.ai
- **Skills 数量**：22,004+
- **作者数**：8,260+
- **License**：Mixed（各 Skill 独立）
- **类型**：Skills 分发平台
- **搜索方式**：向量语义搜索

## 核心特点

1. **数量最大** - 22,004+ Skills
2. **社区驱动** - 8,260+ 作者
3. **智能搜索** - 向量语义匹配
4. **版本管理** - npm 式版本控制
5. **安全审核** - VirusTotal + OpenClaw 评级

---

## 🔥 热门榜单（Top 15）

### 按下载量排序

| 排名 | Skill | 功能描述 | 分类 |
|:----:|-------|---------|------|
| 1 | **self-improving-agent** | 自我改进，持续学习 | Agent |
| 2 | **Tavily Web Search** | AI 优化网页搜索 | 搜索 |
| 3 | **Find Skills** | 发现安装 Skills | 工具 |
| 4 | **Gog (Google Workspace)** | Google 办公套件 | 办公 |
| 5 | **Summarize** | 总结 URL/文件 | 文档 |
| 6 | **GitHub** | GitHub CLI 交互 | 开发 |
| 7 | **Polymarket** | 预测市场查询 | 金融 |
| 8 | **ultimate-agent** | 终极 Agent 增强 | Agent |
| 9 | **Notion** | Notion API | 办公 |
| 10 | **nano-pdf** | PDF 自然语言编辑 | 文档 |
| 11 | **Nano Banana Pro** | 图片生成编辑 | 多媒体 |
| 12 | **Composio** | 100+ API 集成 | 集成 |
| 13 | **Obsidian** | Obsidian 自动化 | 知识管理 |
| 14 | **humanize** | 去除 AI 写作痕迹 | 写作 |
| 15 | **knowledge-graph** | 知识图谱内存 | 记忆 |

---

## 🔍 技术亮点

### 1. 向量语义搜索

**传统搜索：**
```
搜索关键词："document"
结果：包含 "document" 字符串的 Skills
```

**向量语义搜索：**
```
搜索意图：处理文档
结果：
  - pdf (PDF 处理)
  - docx (Word 处理)
  - summarize (文档总结)
  - nano-pdf (PDF 编辑)
```

**优势：**
- 理解搜索意图
- 跨语言搜索
- 相似性推荐

### 2. 版本管理

**npm 式版本控制：**
```json
{
  "name": "self-improving-agent",
  "version": "2.3.1",
  "dependencies": {
    "knowledge-graph": "^1.0.0"
  }
}
```

**版本操作：**
```bash
# 安装特定版本
clawhub install self-improving-agent@2.3.1

# 更新到最新版
clawhub update self-improving-agent

# 查看版本历史
clawhub info self-improving-agent --versions
```

### 3. 安全审核

**三层安全机制：**

1. **nonSuspicious 过滤**
   ```
   URL: https://clawhub.ai/skills?nonSuspicious=true
   ```

2. **VirusTotal 扫描**
   - 自动扫描所有上传文件
   - 检测恶意代码

3. **OpenClaw 评级**
   - 安全评级：A/B/C/D
   - 社区反馈
   - 使用统计

---

## 📦 获取方式

### 方式 1：官网浏览（推荐）

**热门榜单：**
```
https://clawhub.ai/skills?sort=downloads&nonSuspicious=true
```

**参数说明：**
- `sort=downloads` - 按下载量排序
- `sort=stars` - 按 Stars 排序
- `sort=recent` - 按最近更新排序
- `nonSuspicious=true` - 过滤可疑 Skills

### 方式 2：CLI 工具

**安装：**
```bash
npm i -g clawhub
```

**登录（推荐）：**
```bash
clawhub login
```

**常用命令：**
```bash
# 搜索（向量语义搜索）
clawhub search "AI 搜索"

# 浏览最新
clawhub explore --limit 10

# 查看详情
clawhub inspect self-improving-agent

# 安装
clawhub install self-improving-agent

# 批量安装
clawhub install tavily-search github-cli

# 更新
clawhub update --all

# 列出已安装
clawhub list

# 卸载
clawhub uninstall <skill-slug>
```

**⚠️ 速率限制：**
- 匿名用户：严格限制
- 登录用户：宽松限制
- 频繁请求会触发 `Rate limit exceeded`

### 方式 3：本地仓库分析

**已下载完整备份：**
- 路径：`skill-research/clawhub-skills/`
- 规模：8,260 作者，22,004+ Skills，1.5G
- 结构：`skills/<作者>/<skill-name>/SKILL.md`

**分析方法：**
```bash
# 查看 Skill 数量
find skills -name "SKILL.md" | wc -l

# 查看元数据
find skills -name "_meta.json" -exec cat {} \;

# 搜索特定作者
ls -la skills/anthropics/

# 搜索特定 Skill
find skills -name "self-improving-agent"
```

---

## 📂 Skills 分类

### 1. Agent 增强（Agent Enhancement）
- **self-improving-agent** - 自我改进
- **ultimate-agent** - 终极增强
- **proactive-agent** - 主动式 Agent

### 2. 搜索能力（Search）
- **Tavily Web Search** - AI 优化搜索
- **Find Skills** - Skills 发现
- **perplexity-search** - Perplexity 集成

### 3. 办公集成（Office Integration）
- **Gog (Google Workspace)** - Google 办公
- **Notion** - Notion API
- **Slack** - Slack 集成
- **Trello** - 看板管理

### 4. 开发工具（Development）
- **GitHub** - GitHub CLI
- **Obsidian** - Obsidian 自动化
- **git-operations** - Git 操作

### 5. 文档处理（Document Processing）
- **Summarize** - 文档总结
- **nano-pdf** - PDF 编辑
- **document-converter** - 文档转换

### 6. 多媒体（Multimedia）
- **Nano Banana Pro** - 图片编辑
- **video-frames** - 视频处理
- **audio-transcription** - 音频转文字

### 7. API 集成（API Integration）
- **Composio** - 100+ API
- **zapier-integration** - Zapier 集成
- **api-gateway** - API 网关

### 8. 知识管理（Knowledge Management）
- **knowledge-graph** - 知识图谱
- **memory-bank** - 记忆库
- **context-engineering** - 上下文工程

### 9. 写作工具（Writing Tools）
- **humanize** - 去除 AI 痕迹
- **content-writer** - 内容写作
- **grammar-checker** - 语法检查

### 10. 金融工具（Finance）
- **Polymarket** - 预测市场
- **stock-analyzer** - 股票分析
- **crypto-tracker** - 加密货币追踪

---

## 💡 使用建议

### 1. 新手入门

**推荐 Skills（必装）：**
1. **self-improving-agent** - 持续学习改进
2. **Tavily Web Search** - 增强搜索能力
3. **Find Skills** - 发现更多 Skills
4. **Summarize** - 文档总结
5. **GitHub** - 开发必备

### 2. 开发者

**推荐 Skills：**
1. **GitHub** - Git 操作
2. **self-improving-agent** - 自我改进
3. **knowledge-graph** - 知识管理
4. **Obsidian** - 笔记自动化
5. **Composio** - API 集成

### 3. 内容创作者

**推荐 Skills：**
1. **humanize** - 内容人性化
2. **Summarize** - 内容总结
3. **Nano Banana Pro** - 图片编辑
4. **Notion** - 内容管理
5. **Gog** - 文档协作

### 4. 企业用户

**推荐 Skills：**
1. **Gog (Google Workspace)** - 办公套件
2. **Notion** - 知识管理
3. **Slack** - 团队协作
4. **Composio** - API 集成
5. **knowledge-graph** - 企业知识库

---

## 🔄 更新频率

- **新 Skills**：每天新增
- **热门榜单**：每周更新
- **安全审核**：持续进行
- **版本更新**：按需发布

---

## 🔗 相关链接

- **官网**：https://clawhub.ai
- **热门榜单**：https://clawhub.ai/skills?sort=downloads&nonSuspicious=true
- **CLI 工具**：https://www.npmjs.com/package/clawhub
- **文档**：https://docs.clawhub.ai

---

## 📊 对比分析

| 特性 | ClawHub | Anthropic Skills | awesome-claude-skills |
|------|---------|------------------|----------------------|
| **Skills 数量** | 22,004+ | 17 | 30+ |
| **搜索方式** | 向量语义 | 手动 | 手动 |
| **版本管理** | ✅ npm 式 | ❌ | ❌ |
| **安全审核** | ✅ 三层 | ⚠️ | ⚠️ |
| **社区活跃度** | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ |

---

## ⚠️ 注意事项

### 1. 速率限制
- 匿名用户严格限制
- 建议登录后使用
- 避免频繁请求

### 2. 质量参差
- 22,000+ Skills 质量不一
- 使用 `nonSuspicious=true` 过滤
- 查看 Stars 和下载量

### 3. 安全审核
- 检查 OpenClaw 评级
- 查看社区反馈
- 审查 Skill 源码

### 4. 依赖管理
- 注意 Skill 依赖
- 检查兼容性
- 避免版本冲突

---

## 🎯 适用场景

- **快速发现** - 寻找合适的 Skills
- **功能扩展** - 快速增强 Agent 能力
- **社区贡献** - 分享自己的 Skills
- **实验尝试** - 测试新 Skills
- **生产使用** - 经过审核的高质量 Skills

---

## 🚀 未来规划

- [ ] 增加更多筛选条件
- [ ] 改进搜索算法
- [ ] 增强 CLI 功能
- [ ] 提供更多 API
- [ ] 改进安全审核

---

_更新时间：2026-03-10_
_维护者：ClawHub Team_
_优先级：P1（重点跟踪）_
