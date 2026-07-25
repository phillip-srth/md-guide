# Information Architecture

Information architecture is the structure that helps readers find the right page quickly.

## Start With Reader Tasks

Do not start by mirroring source folders. Start with reader questions.

| Reader | Main Questions |
| --- | --- |
| New apprentice | How do I run the project locally? Where do I ask for help? |
| Feature developer | How do I add a feature without breaking conventions? |
| Maintainer | Where are ownership, release, and troubleshooting rules? |
| Operator | How do I deploy, roll back, and recover? |

## Recommended Sections

```text
src/
├── 01-Foundations/
├── 02-Advanced/
├── 03-Automation/
├── 04-Appendix/
├── assets/
└── SUMMARY.md
```

## Progressive Disclosure

Put the most useful answer first, then add depth:

1. Start with the action or conclusion.
1. Show the command or example.
1. Explain why it works.
1. Link to deeper references.

## Navigation

In mdBook, navigation is controlled by `src/SUMMARY.md`:

```markdown
# Summary

[Introduction](01-Overview/introduction.md)

- [Markdown Basics](02-Foundations/markdown-basics.md)
- [Release Checklist](04-Automation/release-checklists.md)
```

Keep navigation shallow enough to scan. If a page is buried four levels deep, many readers will never find it.

## Architecture Decision Records

Use Architecture Decision Records, or ADRs, for important technical decisions.

```markdown
# ADR 0001: Use mdBook for Developer Documentation

## Status

Accepted

## Context

The team needs documentation that can be reviewed in pull requests and deployed as a static site.

## Decision

Use mdBook with Markdown sources stored in the repository.

## Consequences

- Documentation changes are versioned with code.
- The team must maintain `SUMMARY.md`.
- Renderer-specific features should be documented.
```
