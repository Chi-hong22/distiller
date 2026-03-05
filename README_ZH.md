<div align="center">



# Distiller

[![Agent Skill](https://img.shields.io/badge/Agent-Skill-blue.svg?style=for-the-badge)](https://github.com)
[![Markdown](https://img.shields.io/badge/Markdown-Obsidian-purple.svg?style=for-the-badge&logo=markdown)](https://obsidian.md/)
[![No Dependencies](https://img.shields.io/badge/Dependencies-None-brightgreen.svg?style=for-the-badge)](#)

<br/>

<i>"知识不应只是流过你的指尖，让 Distiller 帮你留住它们。"</i>

<br/>

[English](./README.md) | [简体中文](./README_ZH.md)

Distiller 是一个独立的 Agent Skill 工具，用于将你与 AI 的每一次高质量技术对话，沉淀为结构化、可检索、可复用的个人知识库。

</div>

---

## 为什么需要 Distiller

- **沉淀结对经验**: 昨晚刚刚排查出的诡异 Bug，今天换个项目又从头查起。
- **解决知识碎片化**: 学到的新架构、新写法语境全在历史对话里，难以二次查找。
- **转化技术肌肉**: AI 给出的精彩重构方案，自动回顾上下文并提取核心决策。
- **兼容本地知识库**: 生成完美兼容 Obsidian 的高质量 Markdown 笔记。

---

## 核心特性

- **场景化提炼**: 拒绝千篇一律的总结。系统内置 5 大真实开发场景（项目收尾、Bug 复盘、代码重构、技术学习、通用兜底），根据对话特征自动切换提取侧重点。
- **克制与真实**: 遵循“提取不诠释”原则，绝不凭空捏造。每条结论都会标注置信度（高/中/低），保留最原汁原味的技术现场。
- **无缝接入知识库**: 标准化的 `YAML Frontmatter` 和层级标签体系，天然支持 Obsidian 等本地双链笔记软件。
- **温故知新**: 内置智能检索脚本。提炼前自动搜索历史笔记，你可以选择“补充到已有文档”或“创建新文档”，让知识产生复利。
- **纯粹且轻量**: 零外部依赖，仅需系统自带的 Python 环境，开箱即用。

---

## 极简上手指南

### 1. 唤醒 Distiller

在你觉得“这次对话很有价值”时，向 AI 助手发送以下任意指令：

```text
distill
extract distilled knowledge
retrospective
what did I learn
```

### 2. 交互式沉淀（AI 将引导你完成）

唤醒后，Distiller 会自动执行以下流程，你只需做几个简单的选择：

1. **确认提炼范围**: 是总结当前这一次对话，还是回顾今天的所有对话？
2. **确认场景**: AI 会自动为你匹配最合适的场景（例如：*看来我们在排查一个 Bug，使用“Bug 复盘”模板可以吗？*）。
3. **确认存储位置**: 保存到你的 Obsidian 仓库，还是当前项目目录下？
4. **生成与审查**: AI 将呈现排版精美的总结文档，并在你点头确认后，正式落盘保存。

---

## 提炼场景一览

Distiller 就像一位经验丰富的技术 Leader，针对不同情况问出最核心的问题：

| 触发场景 | Distiller 会帮你记录什么？ |
| :--- | :--- |
| **Bug 复盘** | 错误画像、根本原因推导链、快速定位方法、如何预防。 |
| **代码重构** | 原始代码的“坏味道”、重构遵循的设计原则、前后对比与收益。 |
| **技术学习** | 新技术的概念地图、高频 API 速查、最适用的业务场景。 |
| **项目收尾** | 关键架构决策记录、沉淀出的可复用模块、踩坑与避坑指南。 |
| **通用兜底** | 核心发现、关键决策背后的权衡（Trade-off）。 |

---

## 严谨的标签体系

为了保证你的知识库不会随时间推移变成“垃圾场”，Distiller 强制推行多维度的标签管理机制：

- **基础标识**: 所有提炼生成的文档固定包含 `distilled`，方便全局索引。
- **场景维度**: 如 `scene/bug-retrospective`，一秒定位所有排错记录。
- **技术维度**: 如 `tech/python`、`tech/react`，按技术栈无限扩展。
- **主题维度**: 如 `topic/concurrency`（并发）、`topic/architecture`（架构）。
- **难度分级**: `difficulty/beginner`、`intermediate` 或 `advanced`。

---

## 项目内部结构

如果你想深入了解或定制 Distiller，展开下方的结构地图：

<details>
<summary><b>点击展开项目结构地图</b></summary>
<br>

```text
distiller/
├── SKILL.md                        - 技能的主入口，定义了完整的引导工作流
├── assets/
│   └── distiller-frontmatter.md   - 规范化的 Obsidian YAML 头部模板
├── scripts/
│   └── search_distiller.py        - 核心搜索脚本，基于词频帮你找出相关的历史笔记
└── references/
    ├── tags-taxonomy.md            - 标签分类学指南
    ├── scene-project-wrapup.md    - [场景模板] 项目/迭代收尾
    ├── scene-bug-retrospective.md - [场景模板] Bug 深度复盘
    ├── scene-refactoring.md       - [场景模板] 代码重构与演进
    ├── scene-tech-learning.md     - [场景模板] 新技术探索与学习
    └── scene-universal.md         - [场景模板] 通用知识沉淀
```

</details>

<br>

<div align="center">
  <i>"不要让每一次精彩的代码重构，随着聊天窗口的关闭而消散。"</i>
</div>