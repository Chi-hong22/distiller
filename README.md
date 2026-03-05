<div align="center">

# Distiller

[![Agent Skill](https://img.shields.io/badge/Agent-Skill-blue.svg?style=for-the-badge)](https://github.com) [![Markdown](https://img.shields.io/badge/Markdown-Obsidian-purple.svg?style=for-the-badge&logo=markdown)](https://obsidian.md/) [![No Dependencies](https://img.shields.io/badge/Dependencies-None-brightgreen.svg?style=for-the-badge)](#)

<br/>
<i>"Knowledge shouldn't just slip through your fingertips; let Distiller capture it."</i>
<br/>

[English](./README.md) | [简体中文](./README_ZH.md)

Distiller is a standalone Agent Skill tool designed to distill your high-quality technical conversations with AI into a structured, searchable, and reusable personal knowledge base.

</div>

---

## Why Distiller

- **Preserve pair-programming experience**: The obscure bug you debugged last night shouldn't be investigated from scratch today.
- **Solve knowledge fragmentation**: New architectures and syntaxes learned often get buried in chat history, making them hard to find later.
- **Build technical muscle**: Brilliant refactoring proposals from AI need to be systematically captured, not just copy-pasted.
- **Compatible with local knowledge bases**: Generates high-quality Markdown notes that are perfectly compatible with Obsidian.

---

## Core Features

- **Scene-based Extraction**: Rejects generic summaries. Built-in 5 real-world development scenes (Project Wrap-up, Bug Retrospective, Code Refactoring, Tech Learning, Universal) to automatically switch extraction focus based on conversation context.
- **Restrained & Authentic**: Strictly follows the "extract, don't interpret" principle. No hallucinations. Every extracted point is marked with a confidence level (high/medium/low) to preserve the original technical context.
- **Seamless Integration**: Standardized `YAML Frontmatter` and hierarchical tag taxonomy, natively supporting local bidirectional linking tools like Obsidian.
- **Review & Reinforce**: Built-in smart search script. Before extracting, it automatically searches historical notes, allowing you to choose whether to "append to existing" or "create a new" document, building compounded knowledge.
- **Pure & Lightweight**: Zero external dependencies, runs out of the box with the system's built-in Python environment.

---

## Quick Start

### 1. Wake up Distiller

When you feel "this conversation is valuable", send any of the following commands to your AI assistant:

```text
distill
extract distilled knowledge
retrospective
what did I learn
```

### 2. Interactive Extraction (Guided by AI)

Once awakened, Distiller will automatically execute the following workflow. You just need to make a few simple choices:

1. **Confirm Scope**: Summarize the current conversation, or all conversations today?
2. **Confirm Scene**: AI will automatically match the most suitable scene (e.g., *It seems we are debugging a bug, can we use the "Bug Retrospective" template?*).
3. **Confirm Storage**: Save to your Obsidian vault, or the current project directory?
4. **Generate & Review**: AI will present a beautifully formatted summary document and save it only after your confirmation.

---

## Extraction Scenes

Distiller acts like an experienced Tech Lead, asking the most critical questions tailored to the situation:

| Trigger Scene | What Distiller Captures |
| :--- | :--- |
| **Bug Retrospective** | Bug profile, root cause chain, quick location methods, and prevention strategies. |
| **Code Refactoring** | "Code smells" of the original code, applied design principles, and before/after comparison with benefits. |
| **Tech Learning** | Concept maps of new tech, high-frequency API cheat sheets, and best applicable scenarios. |
| **Project Wrap-up** | Key architectural decision records, reusable modules, and pitfalls to avoid. |
| **Universal** | Core findings and trade-offs behind key decisions. |

---

## Strict Tag Taxonomy

To prevent your knowledge base from turning into a dumping ground over time, Distiller enforces a multi-dimensional tag management mechanism:

- **Base Tag**: All extracted documents must include `distilled` for global indexing.
- **Scene Dimension**: e.g., `scene/bug-retrospective`, locating all debugging records in a second.
- **Tech Dimension**: e.g., `tech/python`, `tech/react`, infinitely extensible by tech stack.
- **Topic Dimension**: e.g., `topic/concurrency`, `topic/architecture`.
- **Difficulty Level**: `difficulty/beginner`, `intermediate`, or `advanced`.

---

## Project Structure

If you want to dive deeper or customize Distiller, unfold the structure map below:

<details>
<summary><b>Click to expand project structure map</b></summary>
<br>

```text
distiller/
├── SKILL.md                        - Main entry of the skill, defines the guided workflow
├── assets/
│   └── distiller-frontmatter.md   - Standardized Obsidian YAML header template
├── scripts/
│   └── search_distiller.py        - Core search script, finds related historical notes using word frequency
└── references/
    ├── tags-taxonomy.md            - Tag taxonomy guide
    ├── scene-project-wrapup.md    - [Scene Template] Project/iteration wrap-up
    ├── scene-bug-retrospective.md - [Scene Template] In-depth bug retrospective
    ├── scene-refactoring.md       - [Scene Template] Code refactoring and evolution
    ├── scene-tech-learning.md     - [Scene Template] Exploring and learning new tech
    └── scene-universal.md         - [Scene Template] Universal knowledge extraction
```

</details>

<br>

<div align="center">
  <i>"Don't let brilliant refactorings fade away with closed chat windows."</i>
</div>