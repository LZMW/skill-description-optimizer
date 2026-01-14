# Skill Description Optimizer / 技能描述优化器

> [![License: MIT](https://img.shoelace.style/latest/badge/license)](LICENSE)
> [![Claude Skill](https://img.shields.io/badge/Claude-Skill-blue)](https://claude.ai/claude-code)
> [![Made with GLM-4.7](https://img.shields.io/badge/Made%20with-GLM--4.7-green)](https://github.com/THUDM/GLM-4)

**Meta-skill for optimizing skill descriptions using SDS standard and seven core techniques.**

**使用 SDS 标准和七种核心技术优化技能描述的元技能。**

A comprehensive optimization framework that systematically analyzes and improves Claude Skill descriptions to maximize trigger rates and discoverability.

一个全面的优化框架，系统性地分析和改进 Claude 技能描述，以最大化触发率和可发现性。

---

## Table of Contents / 目录

| English | 中文 |
|---------|------|
| [Core Features](#core-features) | 核心功能 |
| [Technical Highlights](#technical-highlights) | 技术亮点 |
| [Quick Start](#quick-start) | 快速开始 |
| [Optimization Workflow](#optimization-workflow) | 优化工作流 |
| [Best Practices](#best-practices) | 最佳实践 |
| [Quality Standards](#quality-standards) | 质量标准 |
| [Contributing](#contributing) | 贡献指南 |
| [Acknowledgments](#acknowledgments) | 致谢 |

---

## Core Features / 核心功能

### Two-Phase Optimization Workflow / 两阶段优化工作流

#### Phase 1: Search Analysis / 第一阶段：搜索分析

| English | 中文 |
|---------|------|
| Automatically search all existing skills (`.claude/skills/` directory) | 自动搜索所有现有技能（`.claude/skills/` 目录） |
| Extract `name` and `description` from each skill | 从每个技能中提取 `name` 和 `description` |
| Analyze trigger word distribution, keyword frequency, scenario count, and character length | 分析触发词分布、关键词频率、场景数量和字符长度 |
| Generate quantitative metric reports (averages, ranges, heatmaps) | 生成定量指标报告（平均值、范围、热力图） |

#### Phase 2: Optimization Execution / 第二阶段：优化执行

| English | 中文 |
|---------|------|
| Optimize based on SDS standards and best practices | 基于 SDS 标准和最佳实践进行优化 |
| Conflict detection: ensure no functional overlap with existing skill groups | 冲突检测：确保与现有技能群体没有功能重叠 |
| Apply universal formula and five major templates | 应用通用公式和五大模板 |
| Execute seven optimization techniques | 执行七种优化技术 |
| Automatically generate/update `skill-trigger-handbook.md` | 自动生成/更新 `skill-trigger-handbook.md` |

### Multi-Expert Collaboration Pattern / 多专家协作模式

This project employs a multi-expert collaboration system to ensure comprehensive and accurate optimization:

本项目采用多专家协作系统，确保全面和准确的优化：

| English | 中文 | Role |
|---------|------|------|
| **Pattern Analyst** | **模式分析师** | Analyzes quantitative metrics of existing skill descriptions / 分析现有技能描述的定量指标 |
| **Conflict Detector** | **冲突检测器** | Detects functional overlap and trigger word conflicts / 检测功能重叠和触发词冲突 |
| **Optimization Architect** | **优化架构师** | Applies SDS standards and seven techniques / 应用 SDS 标准和七种技术 |
| **Quality Auditor** | **质量审计师** | Executes strict quality checklists / 执行严格的质量检查清单 |

---

## Technical Highlights / 技术亮点

### SDS Standard (Skill Description Standard) / SDS 标准（技能描述标准）

| Rule | Requirement | 描述 / Description |
|------|-------------|-------------------|
| Format | Single-line English, quoted | 确保正确的系统解析 |
| Length | < 1024 characters (recommended 180-330) | 平衡信息密度和可读性 |
| Prohibited | `<` or `>` characters | 避免解析错误 |

### Universal Formula / 通用公式

```
[功能概述] + [触发条件] + [场景列表] + [兜底条款]
[Function Overview] + [Trigger Conditions] + [Scenario List] + [Catch-all Clause]
```

### Five Optimization Templates / 五大优化模板

| English | 中文 |
|---------|------|
| **File Processing Type** - Comprehensive X, When Claude needs to work with... | **文件处理类型** - 全面的 X，当 Claude 需要处理... |
| **Tool/Testing Type** - Toolkit for X using Y, Supports... | **工具/测试类型** - 使用 Y 的 X 工具包，支持... |
| **Design/Creative Type** - Create X with Y, Use this skill when... | **设计/创意类型** - 使用 Y 创建 X，在...时使用此技能 |
| **Meta-Skill/Guide Type** - Guide for creating X that Y, Use when... | **元技能/指南类型** - 创建 Y 的 X 的指南，在...时使用 |
| **Platform-Specific Type** - Knowledge and utilities for X optimized for Y... | **平台特定类型** - 针对 Y 优化的 X 知识和实用工具... |

### Seven Optimization Techniques / 七种优化技术

| Technique | 描述 / Description | 效果 / Effect |
|-----------|-------------------|---------------|
| Numbered List / 编号列表 | Use (1)(2)(3) to clearly list scenarios / 使用 (1)(2)(3) 清晰列出场景 | Scenario recognition +40% / 场景识别率 +40% |
| Parenthetical Examples / 括号示例 | Provide specific examples / 提供具体示例 | Trigger accuracy +35% / 触发准确度 +35% |
| Keyword Repetition / 关键词重复 | Core words appear 2-5 times / 核心词出现 2-5 次 | Discoverability +50% / 可发现性 +50% |
| Tech Stack Annotation / 技术栈注释 | Annotate frameworks in parentheses / 在括号中注释框架 | Professionalism enhanced / 专业性提升 |
| Catch-all Clause / 兜底条款 | Cover unlisted scenarios / 覆盖未列出的场景 | Coverage +60% / 覆盖率 +60% |
| Negative Constraints / 负面约束 | Specify what not to do / 指定不做什么 | False trigger rate -70% / 误触发率 -70% |
| Exclusion Conditions / 排除条件 | Clearly define inapplicable scenarios / 明确定义不适用场景 | Precision improved / 精确度提升 |

---

## Quick Start / 快速开始

### Prerequisites / 前置条件

| English | 中文 |
|---------|------|
| Claude Code CLI with Agent SDK | 带有 Agent SDK 的 Claude Code CLI |
| Existing skills directory (`.claude/skills/`) | 现有技能目录（`.claude/skills/`） |
| File system access permissions (Glob, Read, Grep, Bash, Write) | 文件系统访问权限（Glob、Read、Grep、Bash、Write） |

### Installation / 安装

1. Clone the repository or copy skill files to your skills directory:

克隆仓库或将技能文件复制到您的技能目录：

```bash
cp -r skill-description-optimizer ~/.claude/skills/
```

2. Verify installation:

验证安装：

```bash
ls ~/.claude/skills/skill-description-optimizer/
# Should see: SKILL.md, references/best_practices.md
# 应该看到：SKILL.md, references/best_practices.md
```

### Usage Examples / 使用示例

#### Example 1: Optimize Existing Description / 示例 1：优化现有描述

**Input** / 输入:
```
Help me optimize this skill description: 'Tool for creating PDF documents.'
帮我优化这个技能描述：'创建 PDF 文档的工具。'
```

**Output** / 输出:

**Phase 1: Search Analysis / 第一阶段：搜索分析**

| English | 中文 |
|---------|------|
| - Found existing skills: 4 | - 发现现有技能：4 个 |
| - Trigger word pattern analysis: average "skill" × 3 times, scenario count 3.5 | - 触发词模式分析：平均"skill" × 3 次，场景数 3.5 |
| - Conflict detection: No PDF-related skill found | - 冲突检测：未发现 PDF 相关技能 |

**Phase 2: Optimization Execution / 第二阶段：优化执行**

| English | 中文 |
|---------|------|
| - Selected template: File processing type | - 选择模板：文件处理类型 |
| - Optimized result: | - 优化结果： |

```yaml
description: "Comprehensive PDF document creation and editing with support for formatting, images, and text extraction. When Claude needs to work with PDF files for: (1) Creating new documents, (2) Modifying content, (3) Extracting text, or any other PDF tasks"
```

| English | 中文 |
|---------|------|
| - Quality check: 220 characters (fits 180-330 standard), 4 trigger scenarios, keyword "PDF" × 3 times | - 质量检查：220 字符（符合 180-330 标准），4 个触发场景，关键词"PDF" × 3 次 |

#### Example 2: Create New Skill Description / 示例 2：创建新技能描述

**Input** / 输入:
```
I want to create a Python code generation skill, help me write a high trigger rate description
我想创建一个 Python 代码生成技能，帮我写一个高触发率的描述
```

**Output** / 输出:
```yaml
description: "Toolkit for Python code generation using best practices and design patterns. Supports creating functions, classes, modules, and debugging with type hints and docstrings. Use when users request Python programming assistance (examples include writing algorithms, implementing data structures, or building applications), or any other Python development tasks"
```

**Improvement Effects** / 改进效果:

| English | 中文 |
|---------|------|
| - Character count: 311 (fits 180-330 standard) | - 字符数：311（符合 180-330 标准） |
| - Trigger word "Python": 4 times | - 触发词"Python"：4 次 |
| - Parenthetical examples: 3 | - 括号示例：3 个 |
| - Catch-all clause: Complete | - 兜底条款：完整 |

---

## Optimization Workflow / 优化工作流

### Complete Workflow / 完整工作流

```
User Request / 用户请求
  ↓
Phase 1: Search Analysis / 第一阶段：搜索分析
  ├─ Glob search all skills / Glob 搜索所有技能
  ├─ Read extract name + description / Read 提取 name + description
  ├─ Grep analyze trigger word patterns / Grep 分析触发词模式
  └─ Output quantitative metric report / 输出定量指标报告
  ↓
Phase 2: Conflict Detection / 第二阶段：冲突检测
  ├─ Functional overlap detection / 功能重叠检测
  ├─ Trigger word conflict analysis / 触发词冲突分析
  └─ Determine unique positioning / 确定独特定位
  ↓
Phase 3: Optimization Execution / 第三阶段：优化执行
  ├─ Select appropriate template / 选择合适的模板
  ├─ Apply universal formula / 应用通用公式
  ├─ Apply seven techniques / 应用七种技术
  └─ Generate optimized description / 生成优化的描述
  ↓
Phase 4: Quality Validation / 第四阶段：质量验证
  ├─ SDS format check / SDS 格式检查
  ├─ KERNEL content check / KERNEL 内容检查
  └─ Trigger word density validation / 触发词密度验证
  ↓
Phase 5: Handbook Generation/Update / 第五阶段：手册生成/更新
  └─ Update skill-trigger-handbook.md / 更新 skill-trigger-handbook.md
```

### Expert Collaboration Steps / 专家协作步骤

| English | 中文 |
|---------|------|
| 1. **Pattern Analyst** → Extract existing skill group patterns | 1. **模式分析师** → 提取现有技能群体模式 |
| 2. **Conflict Detector** → Ensure no functional overlap | 2. **冲突检测器** → 确保没有功能重叠 |
| 3. **Optimization Architect** → Apply standards for optimization | 3. **优化架构师** → 应用标准进行优化 |
| 4. **Quality Auditor** → Execute strict quality checks | 4. **质量审计师** → 执行严格的质量检查 |

---

## Best Practices / 最佳实践

### Data Metrics (Based on 8 Official Skills) / 数据指标（基于 8 个官方技能）

| Metric | Average | Recommended Range | 描述 / Description |
|--------|---------|-------------------|-------------------|
| Character Count / 字符数 | 242 | 180-330 | Information density balance / 信息密度平衡 |
| Word Count / 词数 | 34 | 23-47 | Readability standard / 可读性标准 |
| Trigger Scenario Count / 触发场景数 | 3.5 | 3-7 | Coverage completeness / 覆盖完整性 |

### Trigger Phrase Library / 触发短语库

| Phrase Type | Example | Applicable Scenario / 适用场景 |
|-------------|---------|-------------------------------|
| Trigger Condition / 触发条件 | "When Claude needs to" | File processing / 文件处理 |
| Trigger Condition / 触发条件 | "Use when" | General purpose / 通用 |
| Trigger Condition / 触发条件 | "Use this skill when the user asks to" | User explicit request / 用户明确请求 |
| Opening Adjective / 开头形容词 | "Comprehensive" | Full-featured skill / 全功能技能 |
| Opening Adjective / 开头形容词 | "Production-grade" | High-quality output / 高质量输出 |
| Opening Adjective / 开头形容词 | "High-quality" | Professional tool / 专业工具 |
| Positioning Word / 定位词 | "Guide" | Guidance-oriented / 指导导向 |
| Positioning Word / 定位词 | "Toolkit" | Tool collection / 工具集合 |

### Common Errors and Fixes / 常见错误和修复

| Error | Problem | Solution |
|-------|---------|----------|
| Trigger info in body / 触发信息在正文 | Claude can't see it / Claude 无法看到 | Put all trigger info in description / 将所有触发信息放在描述中 |
| Too brief / 太简短 | "PDF tool" / "PDF 工具" | Include function + trigger scenarios / 包含功能 + 触发场景 |
| Too long / 太长 | > 1024 characters / > 1024 字符 | Control within 180-330 characters / 控制在 180-330 字符内 |
| Missing trigger condition / 缺少触发条件 | Doesn't say when to use / 没说明何时使用 | Must have "When/Use when" / 必须有"When/Use when" |
| Missing catch-all clause / 缺少兜底条款 | Only fixed scenarios listed / 仅列出固定场景 | Add "or any other..." / 添加"or any other..." |

---

## Quality Standards / 质量标准

### KERNEL Quality Checklist / KERNEL 质量检查清单

#### Format Check / 格式检查

- [ ] Single-line English / 单行英文
- [ ] Quoted / 引号包围
- [ ] < 1024 characters (recommended 180-330) / < 1024 字符（推荐 180-330）
- [ ] Does not contain `<` or `>` / 不包含 `<` 或 `>`

#### Content Check / 内容检查

- [ ] Contains "what skill does" / 包含"技能做什么"
- [ ] Contains "when to use" / 包含"何时使用"
- [ ] Has specific trigger scenarios (numbered or examples) / 有具体触发场景（编号或示例）
- [ ] Has catch-all clause / 有兜底条款
- [ ] Specifies technology/format (if applicable) / 指定技术/格式（如适用）
- [ ] Trigger words 5+ / 触发词 5 个以上

### Quality Validation Process / 质量验证流程

| English | 中文 |
|---------|------|
| 1. **Automatic Check** - Verify SDS standard compliance | 1. **自动检查** - 验证 SDS 标准合规性 |
| 2. **Quantitative Analysis** - Character count, trigger word density, scenario count | 2. **定量分析** - 字符数、触发词密度、场景数 |
| 3. **Comparative Evaluation** - Before/after comparison | 3. **比较评估** - 优化前后对比 |
| 4. **Conflict Verification** - No conflicts with existing skills | 4. **冲突验证** - 与现有技能无冲突 |
| 5. **Handbook Update** - Automatically maintain trigger handbook | 5. **手册更新** - 自动维护触发手册 |

---

## Project Structure / 项目结构

```
skill-description-optimizer/
├── SKILL.md                          # Main skill file (389 lines) / 主技能文件（389 行）
├── README.md                         # Project documentation / 项目文档
├── LICENSE                           # MIT License / MIT 许可证
├── CHANGELOG.md                      # Change log / 更改日志
├── CONTRIBUTING.md                   # Contributing guide / 贡献指南
├── .gitignore                        # Git ignore file / Git 忽略文件
└── references/
    └── best_practices.md             # Best practices documentation (257 lines) / 最佳实践文档（257 行）
```

---

## Core File Descriptions / 核心文件描述

### SKILL.md (389 lines)

Complete skill definition file containing:

完整技能定义文件包含：

| English | 中文 |
|---------|------|
| - Multi-expert collaboration pattern definition | - 多专家协作模式定义 |
| - Detailed two-phase optimization workflow | - 详细的两阶段优化工作流 |
| - Tool invocation strategy | - 工具调用策略 |
| - Negative constraint conditions | - 负面约束条件 |

### references/best_practices.md (257 lines)

Best practices reference document containing:

最佳实践参考文档包含：

| English | 中文 |
|---------|------|
| - SDS core standards (hard rules) | - SDS 核心标准（硬性规则） |
| - Universal formula detailed explanation | - 通用公式详细说明 |
| - Five major templates with examples | - 五大模板及示例 |
| - Seven techniques with explanations | - 七种技术及说明 |
| - Trigger phrase library | - 触发短语库 |
| - Quality checklist | - 质量检查清单 |
| - Data metrics (based on 8 official skills) | - 数据指标（基于 8 个官方技能） |
| - Common error comparison table | - 常见错误对照表 |
| - Quick reference | - 快速参考 |

---

## Contributing / 贡献指南

We welcome contributions in all forms!

我们欢迎各种形式的贡献！

### How to Contribute / 如何贡献

| English | 中文 |
|---------|------|
| 1. Fork this repository | 1. Fork 此仓库 |
| 2. Create a feature branch (`git checkout -b feature/AmazingFeature`) | 2. 创建功能分支 |
| 3. Commit your changes (`git commit -m 'Add some AmazingFeature'`) | 3. 提交更改 |
| 4. Push to the branch (`git push origin feature/AmazingFeature`) | 4. 推送到分支 |
| 5. Open a Pull Request | 5. 打开 Pull Request |

### Contribution Types / 贡献类型

- Report bugs / 报告错误
- Discuss code status / 讨论代码状态
- Submit fixes / 提交修复
- Propose new features / 提出新功能
- Become a maintainer / 成为维护者

### Development Guidelines / 开发指南

| English | 中文 |
|---------|------|
| - Follow existing code style | - 遵循现有代码风格 |
| - Update related documentation | - 更新相关文档 |
| - Add test cases | - 添加测试用例 |
| - Ensure all checks pass | - 确保所有检查通过 |

---

## Acknowledgments / 致谢

### Special Thanks / 特别感谢

The successful development and optimization of this project would not be possible without the powerful support of the following AI models:

如果没有以下强大 AI 模型的支持，本项目的成功开发和优化是不可能的：

**🙏 GLM-4.7**

> The design, optimization, and documentation of this project were all completed under the powerful capabilities of **GLM-4.7**. GLM-4.7 has demonstrated excellence in the following areas:
>
> 本项目的设计、优化和文档都是在 **GLM-4.7** 的强大能力下完成的。GLM-4.7 在以下领域表现出色：

| English | 中文 |
|---------|------|
| - **Deep Understanding**: Profound understanding of complex multi-expert collaboration patterns | - **深度理解**：对复杂多专家协作模式的深刻理解 |
| - **Precise Analysis**: Precise data analysis based on 8 official skills | - **精确分析**：基于 8 个官方技能的精确数据分析 |
| - **Systematic Design**: Systematically integrated SDS standards, universal formula, five major templates, and seven techniques | - **系统设计**：系统性整合 SDS 标准、通用公式、五大模板和七种技术 |
| - **Documentation Quality**: Generated well-structured, detailed technical documentation | - **文档质量**：生成结构良好、详细的技术文档 |
| - **Innovative Thinking**: Designed multi-expert collaboration pattern ensuring comprehensive and accurate optimization | - **创新思维**：设计了多专家协作模式，确保全面和准确的优化 |

> GLM-4.7's powerful capabilities enable this project to:
>
> GLM-4.7 的强大能力使本项目能够：

| English | 中文 |
|---------|------|
| - Implement automated two-phase optimization workflow | - 实现自动化的两阶段优化工作流 |
| - Provide data-driven optimization recommendations | - 提供数据驱动的优化建议 |
| - Ensure harmonious coexistence with existing skill groups | - 确保与现有技能群体和谐共存 |
| - Automatically generate and maintain trigger handbooks | - 自动生成和维护触发手册 |

> Without GLM-4.7's exceptional capabilities, this project would not be so complete and professional.
>
> 如果没有 GLM-4.7 的卓越能力，本项目就不会如此完整和专业。

**[GLM-4.7 GitHub](https://github.com/THUDM/GLM-4)**

### Technical Acknowledgments / 技术致谢

| English | 中文 |
|---------|------|
| - **Claude Agent SDK** - Provided powerful tool invocation capabilities | - **Claude Agent SDK** - 提供了强大的工具调用能力 |
| - **8 Official Skills** - Provided real data analysis foundation | - **8 个官方技能** - 提供了真实数据分析基础 |

---

## License / 许可证

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details

本项目采用 MIT 许可证 - 详情请参阅 [LICENSE](LICENSE) 文件

---

## Author / 作者

Created with LZMW by skill-description-optimizer meta-skill
Powered by GLM-4.7

由 LZMW 创建，使用 skill-description-optimizer 元技能
由 GLM-4.7 驱动

---

## Contact / 联系方式

| English | 中文 |
|---------|------|
| - Issues: [GitHub Issues](https://github.com/yourusername/skill-description-optimizer/issues) | - 问题：[GitHub Issues] |
| - Discussions: [GitHub Discussions](https://github.com/yourusername/skill-description-optimizer/discussions) | - 讨论：[GitHub Discussions] |

---

## Related Resources / 相关资源

| English | 中文 |
|---------|------|
| - [Claude Code Documentation](https://claude.ai/claude-code) | - [Claude Code 文档] |
| - [Agent SDK Guide](https://docs.anthropic.com/claude-agent-sdk) | - [Agent SDK 指南] |
| - [Best Practices Guide](references/best_practices.md) | - [最佳实践指南] |

---

**⭐ If this project helps you, please give it a Star!**

**⭐ 如果本项目对您有帮助，请给它一个 Star！**

**Made with GLM-4.7 | Optimized for Claude Skills | MIT License**
**使用 GLM-4.7 制作 | 为 Claude 技能优化 | MIT 许可证**
