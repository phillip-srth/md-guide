# Content Review

> **Note:** This is a work in progress. The content is not final and may change significantly before publication.

Content review is where documentation becomes useful. Automation can prove the site builds, but humans must verify that
the page answers the right question.

## Review Order

Review in this order:

1. Correctness.
1. Completeness.
1. Structure.
1. Clarity.
1. Style.

Do not start with commas and formatting when the technical explanation is wrong.

## Reviewer Checklist

```markdown
# Documentation Review Checklist

- [ ] The page has one clear purpose.
- [ ] The target reader is obvious.
- [ ] Commands and examples are current.
- [ ] Prerequisites are stated before steps.
- [ ] Steps are ordered correctly.
- [ ] Warnings appear before dangerous actions.
- [ ] Links point to maintained pages.
- [ ] Diagrams match the text.
- [ ] The page is included in navigation when appropriate.
- [ ] The change passes automated checks.
```

## Pull Request Comments

Weak:

```text
This is confusing.
```

Better:

```text
This section says to run `mdbook build`, but it does not say where the command should be run. Please state that it runs
from the repository root.
```

## Content Freshness

Documentation decays when systems change. Use these signals to find stale pages:

- The page references old package versions.
- Screenshots no longer match the UI.
- Commands use deprecated flags.
- The owner team no longer exists.
- A page has not changed while the system it documents has changed many times.
