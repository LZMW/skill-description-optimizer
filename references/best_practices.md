# Skill Description 编写最佳实践

> 本文档基于官方高品质skill学习整理，提供 skill description 编写的核心标准、模板和技巧。

---

## 核心原则

> **Description 是 Claude 判断是否使用 skill 的唯一依据**
>
> - Claude 只读取 `name` + `description`
> - 必须包含 "what" + "when"
> - 所有触发信息必须在 description 中，不要放在 body

---

## SDS 标准（硬性规则）

| 规则 | 要求 |
|------|------|
| 格式 | 单行英文、引号包裹 |
| 长度 | < 1024 字符（推荐 180-330） |
| 禁止 | `<` 或 `>` 字符 |

---

## 万能公式

```
[功能概述] + [触发条件] + [场景列表] + [兜底条款]
```

### 公式详解

| 组成部分 | 说明 | 常用表达 |
|---------|------|----------|
| **功能概述** | 一句话说明核心功能 | Comprehensive X, Toolkit for, Guide for |
| **触发条件** | 何时使用 | When Claude needs to, Use when |
| **场景列表** | 具体用例 | (1)... (2)... 或 (examples include...) |
| **兜底条款** | 覆盖未列出场景 | or any other... / or when... |

---

## 五大模板（按场景选择）

### 模板 1: 文件处理类 ⭐⭐⭐⭐⭐

```
Comprehensive [domain] creation, editing, and analysis with support for [features].
When Claude needs to work with [filetypes] for:
(1) [Scenario 1], (2) [Scenario 2], (3) [Scenario 3], (4) [Scenario 4], or any other [domain] tasks
```

**示例**:
```yaml
description: "Comprehensive document creation, editing, and analysis with support for tracked changes, comments, formatting preservation, and text extraction. When Claude needs to work with professional documents (.docx files) for: (1) Creating new documents, (2) Modifying or editing content, (3) Working with tracked changes, (4) Adding comments, or any other document tasks"
```

**关键点**: 编号列表 + 兜底条款

---

### 模板 2: 工具/测试类 ⭐⭐⭐⭐

```
Toolkit for [function] using [technology].
Supports [capability 1], [capability 2], [capability 3], and [capability 4].
```

**示例**:
```yaml
description: "Toolkit for interacting with and testing local web applications using Playwright. Supports verifying frontend functionality, debugging UI behavior, capturing browser screenshots, and viewing browser logs."
```

**关键点**: Toolkit + Supports + 技术栈

---

### 模板 3: 设计/创意类 ⭐⭐⭐⭐⭐

```
Create [quality] [output] with [features].
Use this skill when the user asks to [actions] (examples include [examples], or when [catch-all]).
[Value proposition].
```

**示例**:
```yaml
description: "Create distinctive, production-grade frontend interfaces with high design quality. Use this skill when the user asks to build web components, pages, artifacts, posters, or applications (examples include websites, landing pages, dashboards, React components, HTML/CSS layouts, or when styling/beautifying any web UI). Generates creative, polished code that avoids generic AI aesthetics."
```

**关键点**: 括号示例 + 价值主张 + 否定约束

---

### 模板 4: 元技能/指导类 ⭐⭐⭐⭐

```
Guide for creating [adjective] [noun] that [purpose].
Use when [action], whether in [variant 1] ([framework 1]) or [variant 2] ([framework 2]).
```

**示例**:
```yaml
description: "Guide for creating high-quality MCP (Model Context Protocol) servers that enable LLMs to interact with external services through well-designed tools. Use when building MCP servers to integrate external APIs or services, whether in Python (FastMCP) or Node/TypeScript (MCP SDK)."
```

**关键点**: Guide + 技术栈标注 + 展开缩写

---

### 模板 5: 平台特定类 ⭐⭐⭐⭐

```
Knowledge and utilities for [action] optimized for [platform].
Provides [feature 1], [feature 2], and [feature 3].
Use when [trigger phrase] like "[concrete example in quotes]".
```

**示例**:
```yaml
description: "Knowledge and utilities for creating animated GIFs optimized for Slack. Provides constraints, validation tools, and animation concepts. Use when users request animated GIFs for Slack like \"make me a GIF of X doing Y for Slack.\""
```

**关键点**: 平台名称 + 引号示例

---

## 七大技巧

| 技巧 | 说明 | 示例 |
|------|------|------|
| **1. 编号列表** | 用 (1)(2)(3) 清晰列举场景 | for: (1) Creating, (2) Editing, (3) Analyzing |
| **2. 括号示例** | 用括号提供具体示例 | (examples include websites, dashboards...) |
| **3. 关键词重复** | 核心词出现 2-5 次 | PDF × 5 次, Slack × 3 次 |
| **4. 技术栈标注** | 括号内标注框架 | Python (FastMCP), Node (MCP SDK) |
| **5. 兜底条款** | 覆盖未列出场景 | or any other document tasks |
| **6. 否定约束** | 说明不做什么 | avoids generic AI aesthetics |
| **7. 排除条件** | 明确不适用场景 | not for simple single-file artifacts |

---

## 触发短语库

### 触发条件短语

| 短语 | 适用场景 |
|------|----------|
| "When Claude needs to" | 文件处理 |
| "Use when" | 通用 |
| "Use this skill when the user asks to" | 用户明确请求 |
| "This skill should be used when users want to" | 用户意图 |

### 开篇形容词

| 形容词 | 适用类型 |
|--------|--------|
| Comprehensive | 全功能技能 |
| Production-grade | 高质量输出 |
| High-quality | 专业工具 |
| Distinctive | 创意类 |

### 定位词

| 定位词 | 适用场景 |
|--------|--------|
| Guide | 指导性 |
| Toolkit | 工具集合 |
| Comprehensive | 全面覆盖 |
| Knowledge and utilities | 知识+工具 |

---

## 质量检查清单

### 格式检查 ✅

- [ ] 单行英文
- [ ] 引号包裹
- [ ] < 1024 字符（推荐 180-330）
- [ ] 不包含 `<` 或 `>`

### 内容检查 ✅

- [ ] 包含 "what skill does"
- [ ] 包含 "when to use"
- [ ] 有具体触发场景（编号或示例）
- [ ] 有兜底条款
- [ ] 指定技术/格式（如适用）
- [ ] 触发词 5+ 个

---

## 数据指标（基于 8 个官方 skills）

| 指标 | 平均值 | 推荐范围 |
|------|--------|----------|
| 字符数 | 242 | 180-330 |
| 词数 | 34 | 23-47 |
| 触发场景数 | 3.5 | 3-7 |

**长度分类**:
- **短** (170-220): 单一目的技能
- **中** (220-280): 2-4 个触发场景
- **长** (280-330): 5+ 个触发场景

---

## 常见错误

| 错误 | 问题 | 正确做法 |
|------|------|----------|
| 触发信息放 body | Claude 看不到 | 所有触发信息放 description |
| 过于简略 | "PDF tool" | 包含功能 + 触发场景 |
| 过于冗长 | > 1024 字符 | 控制在 180-330 字符 |
| 缺少触发条件 | 没说何时使用 | 必须有 "When/Use when" |
| 缺少兜底条款 | 只列固定场景 | 添加 "or any other..." |

---

## 快速参考

### 文件处理类
```yaml
description: "Comprehensive [filetype] creation, editing, and analysis with support for [features]. When Claude needs to work with [filetypes] for: (1) [Scenario 1], (2) [Scenario 2], (3) [Scenario 3], or any other [domain] tasks"
```

### 工具类
```yaml
description: "Toolkit for [function] using [technology]. Supports [capability 1], [capability 2], [capability 3], and [capability 4]."
```

### 设计/创意类
```yaml
description: "Create [quality] [output] with [features]. Use this skill when the user asks to [actions] (examples include [examples], or when [catch-all]). [Value proposition]."
```

### 元技能类
```yaml
description: "Guide for creating [adjective] [noun] that [purpose]. Use when [action], whether in [variant 1] ([framework 1]) or [variant 2] ([framework 2])."
```

---

## 总结

编写高触发率 skill description 的关键：

1. **选择合适的模板** - 5 种模板对应不同场景
2. **使用编号列表** - 多场景技能首选
3. **添加兜底条款** - 覆盖未列出的相关场景
4. **重复关键词** - 核心词出现 2-5 次
5. **控制长度** - 180-330 字符最佳
6. **指定技术栈** - 括号标注具体框架
7. **提供价值主张** - 说明差异化优势

**万能公式**: `[功能概述] + [触发条件] + [场景列表] + [兜底条款]`
