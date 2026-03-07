# xiaoyu 自研 Skills

本目录包含 xiaoyu 智能体生态的自研 skills。

## 📋 Skills 列表

| name | version | description | status |
|------|---------|-------------|--------|
| xiaoyu-knowledge-learning | 1.0.0 | 围绕主题开展研究学习的闭环 skill | ✅ 已发布 |
| xiaoyu-dev | - | 开发辅助 | 🚧 计划中 |
| xiaoyu-task-manage | - | 任务管理 | 🚧 计划中 |
| xiaoyu-skill-manager | - | Skill 管理 | 🚧 计划中 |

## 🚀 安装方式

### OpenClaw

```bash
# 克隆仓库
git clone https://github.com/maplefeng-a/xiaoyu-skills.git

# 复制 skill 到 OpenClaw skills 目录
cp -r xiaoyu-skills/skills/xiaoyu-knowledge-learning ~/.openclaw/skills/
```

### Claude Code

```bash
# 作为 plugin 安装
/plugin install xiaoyu-knowledge-learning@maplefeng-a/xiaoyu-skills
```

## 📝 创建新 Skill

1. 使用模板创建：
```bash
cp -r templates/skill-template skills/my-new-skill
```

2. 编辑 `SKILL.md`：
```yaml
---
name: my-new-skill
version: 1.0.0
description: 描述这个 skill 的功能和触发条件
---
```

3. 更新 `CHANGELOG.md`

4. 提交 PR

## 🎯 设计原则

1. **遵循 agentskills.io 规范**
2. **description 要详细**：包含功能 + 触发条件
3. **三层加载**：metadata → body → resources
4. **版本独立**：每个 skill 独立版本号
