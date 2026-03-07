# 知识卡片模板

## 必需结构

```markdown
---
id: <uuid>
type: concept | howto | reference | overview
title: <标题>
status: active | draft | deprecated
aliases:
  - <别名1>
  - <别名2>
tags:
  - <标签1>
  - <标签2>
refs:
  - <源码引用或文档链接>
---

# <标题>

> 一句话定位

## 一句话

<用一句话说明这个概念/模块的核心作用>

## 核心定位

- **特点1**：说明
- **特点2**：说明
- **特点3**：说明

## 架构/结构

<可选：用图示或代码说明结构>

## 核心实现

```java
// 关键代码片段
```

## API 详解

| 方法 | 返回类型 | 说明 |
|------|----------|------|
| `method1()` | `Type` | 说明 |

## 使用示例

```java
// 实际使用示例
```

## 源码位置

`io.agentscope.xxx.Xxx`

## 关联

- [[相关知识卡片1]]
- [[相关知识卡片2]]
```

## 字段说明

| 字段 | 必需 | 说明 |
|------|------|------|
| `id` | ✅ | UUID，唯一标识 |
| `type` | ✅ | concept/howto/reference/overview |
| `title` | ✅ | 卡片标题 |
| `status` | ✅ | active/draft/deprecated |
| `aliases` | ❌ | 别名列表，便于搜索 |
| `tags` | ❌ | 标签列表 |
| `refs` | ❌ | 源码或文档引用 |

## type 选择指南

| type | 适用场景 |
|------|----------|
| concept | 概念解释、架构说明 |
| howto | 操作指南、使用方法 |
| reference | API 参考、配置说明 |
| overview | 概览、导航、知识地图 |
