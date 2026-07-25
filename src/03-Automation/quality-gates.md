# Quality Gates

> **Note:** This is a work in progress. The content is not final and may change significantly before publication.

A quality gate is an automated or manual rule that must pass before documentation is accepted.

## Minimum Gates

| Gate | Automated | Purpose |
| --- | --- | --- |
| Markdown lint | Yes | Keep source readable and consistent. |
| Static site build | Yes | Prove the website can be generated. |
| Link check | Yes | Prevent broken navigation. |
| Content review | Manual | Verify accuracy and usefulness. |
| Release checklist | Manual plus automated evidence | Ensure release docs are complete. |

## Gate Severity

| Severity | Example | Merge Policy |
| --- | --- | --- |
| Blocking | Site build fails | Do not merge. |
| Blocking | Broken internal link | Do not merge. |
| Warning | One external link times out | Retry or document exception. |
| Warning | Minor spelling issue in draft page | Fix before release branch. |
| Advisory | Style preference | Mention in review, avoid blocking. |

## Definition of Done

Before a documentation task is complete:

- The page exists in navigation.
- Examples are current.
- Images and diagrams have useful alt text or surrounding explanation.
- Local build passes.
- CI gates pass.
- A reviewer has checked technical accuracy.
