---
supplier_id: superpowers
name: Superpowers (obra)
repo: https://github.com/obra/superpowers
stars: 高星
license: Apache-2.0
type: workflow
platforms:
  - claude-code
  - openclaw
indexed_at: 2026-03-10
commit: main
skills_count: 14
note: "工作流完整的 Skills，强调 TDD 和子代理开发"
---

# Superpowers (obra)

高质量工作流 Skills 合集，由 obra 维护，强调 TDD 和子代理驱动开发。

## 概述

- **仓库**：https://github.com/obra/superpowers
- **Stars**：高星 ⭐
- **License**：Apache-2.0
- **类型**：工作流 Skills
- **Skills 数量**：14
- **特点**：工作流完整，TDD+子代理

## 核心特点

1. **工作流完整** - 覆盖完整开发流程
2. **TDD 强制** - 红绿重构，不写测试删代码
3. **子代理模式** - 独立子代理 + 双阶段审查
4. **苏格拉底式** - 不直接写代码，先澄清需求
5. **最佳实践** - 强调工程化实践

---

## 🎯 核心 Skills（14个）

### 1. brainstorming - 苏格拉底式设计提炼

**功能：**
- 不直接写代码
- 通过提问澄清需求
- 渐进式需求细化

**使用场景：**
- 新项目启动
- 需求不明确时
- 设计方案讨论

**工作流程：**
```
用户需求
  ↓
提问澄清（Socratic questioning）
  ↓
需求细化
  ↓
设计方案
  ↓
实现计划
```

### 2. using-git-worktrees - 隔离工作区

**功能：**
- 创建隔离的 Git worktree
- 避免分支冲突
- 并行开发多个特性

**使用场景：**
- 多任务并行开发
- 紧急 Bug 修复
- 实验性特性开发

**命令示例：**
```bash
# 创建新 worktree
git worktree add ../feature-branch feature

# 切换 worktree
cd ../feature-branch

# 删除 worktree
git worktree remove ../feature-branch
```

### 3. writing-plans - 详细实现计划

**功能：**
- 生成详细实现计划
- 分解复杂任务
- 识别依赖关系

**计划格式：**
```markdown
## 任务：实现用户认证

### 阶段 1：数据库设计（2h）
- [ ] 创建 users 表
- [ ] 设计密码加密方案
- [ ] 添加索引

### 阶段 2：API 开发（4h）
- [ ] POST /api/register
- [ ] POST /api/login
- [ ] POST /api/logout

### 阶段 3：测试（2h）
- [ ] 单元测试
- [ ] 集成测试
- [ ] E2E 测试
```

### 4. subagent-driven-development - 子代理驱动开发

**功能：**
- 创建独立子代理
- 双阶段代码审查
- 自动化质量保证

**工作流程：**
```
主代理（规划）
  ↓
子代理 1（实现）
  ↓
子代理 2（审查）
  ↓
主代理（整合）
```

**双阶段审查：**
1. **第一阶段** - 代码质量审查
2. **第二阶段** - 架构设计审查

### 5. test-driven-development - 红绿重构 TDD

**功能：**
- 强制执行 TDD 流程
- 红绿重构循环
- 不写测试删代码

**TDD 循环：**
```
🔴 Red - 编写失败测试
  ↓
🟢 Green - 编写最小实现
  ↓
🔵 Refactor - 重构代码
  ↓
重复
```

**强制规则：**
- ❌ 不写测试 = 删除代码
- ✅ 测试先行
- ✅ 最小实现

### 6. requesting-code-review - 代码审查请求

**功能：**
- 生成代码审查请求
- 自动化审查清单
- 提供改进建议

**审查清单：**
- [ ] 代码风格一致性
- [ ] 测试覆盖率
- [ ] 性能优化
- [ ] 安全检查
- [ ] 文档完整性

### 7. finishing-a-development-branch - 分支完成

**功能：**
- 自动化分支完成流程
- 清理临时文件
- 生成发布说明

**完成流程：**
```
运行所有测试
  ↓
更新文档
  ↓
生成 CHANGELOG
  ↓
创建 PR
  ↓
清理分支
```

---

## 📂 完整 Skills 列表

| # | Skill | 功能 | 类型 |
|---|-------|------|------|
| 1 | brainstorming | 苏格拉底式设计提炼 | 规划 |
| 2 | using-git-worktrees | 隔离工作区 | 工具 |
| 3 | writing-plans | 详细实现计划 | 规划 |
| 4 | subagent-driven-development | 子代理驱动开发 | 开发 |
| 5 | test-driven-development | 红绿重构 TDD | 测试 |
| 6 | requesting-code-review | 代码审查请求 | 审查 |
| 7 | finishing-a-development-branch | 分支完成 | 发布 |
| 8 | debugging-workflow | 调试工作流 | 调试 |
| 9 | refactoring-strategies | 重构策略 | 重构 |
| 10 | documentation-generator | 文档生成器 | 文档 |
| 11 | dependency-management | 依赖管理 | 工具 |
| 12 | performance-optimization | 性能优化 | 优化 |
| 13 | security-audit | 安全审计 | 安全 |
| 14 | deployment-automation | 部署自动化 | 部署 |

---

## 🔍 技术亮点

### 1. 苏格拉底式对话

**传统方式：**
```
用户：实现登录功能
Agent：好的，开始编写代码...
```

**苏格拉底式：**
```
用户：实现登录功能
Agent：
  1. 需要支持哪些登录方式？（邮箱/手机/第三方）
  2. 密码加密用什么算法？
  3. Session 还是 JWT？
  4. 需要记住我功能吗？
  5. 密码重置流程是怎样的？
```

### 2. 子代理模式

**架构：**
```
主代理（Orchestrator）
  ├─ 子代理 1（实现者）
  ├─ 子代理 2（审查者）
  └─ 子代理 3（测试者）
```

**优势：**
- 职责分离
- 双重检查
- 质量保证

### 3. TDD 强制执行

**规则：**
```python
# ❌ 错误：没有测试
def add(a, b):
    return a + b

# ✅ 正确：测试先行
def test_add():
    assert add(1, 2) == 3

def add(a, b):
    return a + b
```

---

## 💡 使用建议

### 1. 完整工作流

**推荐流程：**
```
1. brainstorming（澄清需求）
   ↓
2. writing-plans（制定计划）
   ↓
3. using-git-worktrees（创建隔离环境）
   ↓
4. subagent-driven-development（子代理开发）
   ↓
5. test-driven-development（TDD 实现）
   ↓
6. requesting-code-review（代码审查）
   ↓
7. finishing-a-development-branch（分支完成）
```

### 2. 选择性使用

**最小集合：**
- brainstorming
- test-driven-development
- requesting-code-review

**推荐集合：**
- brainstorming
- writing-plans
- test-driven-development
- subagent-driven-development
- requesting-code-review

### 3. 团队协作

**团队规范：**
- 所有 PR 必须经过 TDD 流程
- 必须通过代码审查
- 使用 worktrees 隔离开发

---

## 🔄 更新频率

- **主仓库**：持续更新
- **新增 Skills**：按需添加
- **Bug 修复**：及时响应

---

## 🔗 相关链接

- **GitHub 仓库**：https://github.com/obra/superpowers
- **文档**：https://github.com/obra/superpowers/blob/main/README.md
- **示例项目**：https://github.com/obra/superpowers/tree/main/examples

---

## 📊 对比分析

| 特性 | superpowers | Anthropic Skills | awesome-claude-skills |
|------|-------------|------------------|----------------------|
| **Skills 数量** | 14 | 17 | 30+ |
| **工作流完整性** | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐ |
| **TDD 支持** | ⭐⭐⭐⭐⭐ | ⭐⭐ | ⭐⭐⭐ |
| **子代理模式** | ⭐⭐⭐⭐⭐ | ⭐ | ⭐⭐ |
| **工程化** | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐ |

---

## 🎯 适用场景

- **专业开发者** - 完整开发流程
- **团队协作** - 规范化开发
- **高质量项目** - TDD 强制执行
- **复杂项目** - 子代理模式
- **敏捷开发** - 迭代优化

---

## ⚠️ 注意事项

1. **学习曲线** - 需要熟悉工作流
2. **严格执行** - TDD 规则强制
3. **团队配合** - 需要团队统一采用
4. **工具依赖** - 需要 Git worktrees 支持

---

_更新时间：2026-03-10_
_维护者：obra_
_优先级：P1（重点跟踪）_
