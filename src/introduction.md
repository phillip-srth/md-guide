# Markdown Docs-as-Code Guide

Markdown is a strong choice for code documentation because it is readable as plain text, reviewable in pull requests,
portable across tools, and easy to automate.

This book takes you from basic Markdown syntax to a production-ready Docs-as-Code workflow:

1. Write **clear Markdown**, enforcing style with **markdownlint**.
1. Organize documentation like source code with a [Docs-as-Code](./01-Foundations/docs-as-code-setup.md) setup.
1. Configure **VS Code** for **fast authoring**.
1. Add **diagrams** with **Mermaid** and **PlantUML**.
1. Add **math** with **LaTeX** syntax.
1. Render a **static website** with **mdBook**.
1. Protect quality with **CI**, **review**, and **release checklists**.

![Docs-as-Code workflow](./assets/docs-as-code-flow.svg)

## Who This Is For

This guide is written for junior developers who already know source control basics and want documentation that can
live next to code without becoming stale.

The examples use GitHub, VS Code, markdownlint, Mermaid, PlantUML, LaTeX-style math, and mdBook. The same principles
also transfer to GitLab, Azure DevOps and other documentation stacks.

## What Good Looks Like

| Quality | Meaning | Example |
| --- | --- | --- |
| Accurate | The docs match the current system. | API examples are tested in CI. |
| Navigable | Readers can find answers quickly. | A clear table of contents and stable file names. |
| Reviewable | Changes are visible in pull requests. | Markdown diffs show exactly what changed. |
| Automatable | Formatting, links, and builds run in CI. | Pull requests fail when links break. |
| Maintainable | Ownership and release rules are explicit. | A release checklist includes documentation steps. |

> Documentation is part of the product. Treat it with the same discipline as code.

## Recommended Learning Path

Read the chapters in order if Markdown is new to you. If you already know how to write Markdown, start with
[Style and markdownlint](./01-Foundations/style-markdownlint.md), then continue with diagrams, automation, and quality gates.

<!--
<details>
<summary>Fast path for a team lead</summary>

1. Copy the lint configuration from this repository.
1. Create a small `src/` documentation structure with an owner for every section.
1. Add `mdbook build`, Markdown linting, and link checking to CI.
1. Make documentation review part of the pull request definition of done.

</details>
-->