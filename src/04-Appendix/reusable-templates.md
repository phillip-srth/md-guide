# Reusable Templates

Copy these templates into real projects and adapt them to your team's workflow.

## Documentation Page Template

```markdown
# Page Title

One short paragraph explaining what this page helps the reader do.

## Prerequisites

- Required tool, permission, or context

## Steps

1. Run the command.
1. Verify the result.
1. Commit the change.

## Troubleshooting

| Symptom | Cause | Fix |
| --- | --- | --- |
| Build fails | Missing dependency | Install the documented version |

## See Also

- [Related page](related-page.md)
```

## Architecture Decision Record Template

```markdown
# ADR 0000: Title

## Status

Proposed

## Context

Describe the problem, constraints, and forces.

## Decision

Describe the chosen option.

## Consequences

- Positive consequence
- Negative consequence
- Follow-up work
```

## Pull Request Documentation Checklist

```markdown
## Documentation

- [ ] New behavior is documented.
- [ ] Changed behavior updates existing docs.
- [ ] Breaking changes include migration notes.
- [ ] Examples were tested.
- [ ] Diagrams or screenshots are updated.
- [ ] `mdbook build` passes locally or in CI.
```

## Final Advice

Start small and automate early. A simple, accurate documentation site with linting and a working build is better than an
ambitious documentation platform that nobody can maintain.
