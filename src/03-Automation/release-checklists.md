# Release Checklists

> **Note:** This is a work in progress. The content is not final and may change significantly before publication.

Release checklists protect documentation from becoming an afterthought.

## Release Documentation Checklist

```markdown
# Release Documentation Checklist

## Scope

- [ ] Release name and version are known.
- [ ] User-visible changes are listed.
- [ ] Breaking changes are identified.
- [ ] Migration steps are documented.

## Documentation

- [ ] Getting started guide still works.
- [ ] API reference is updated.
- [ ] Screenshots or diagrams are current.
- [ ] Known issues are documented.
- [ ] Troubleshooting section covers new failure modes.

## Verification

- [ ] markdownlint passes.
- [ ] `mdbook build` passes.
- [ ] Internal links pass.
- [ ] Content owner approved the changes.
```

## Release Notes Template

```markdown
# Release Notes: 1.4.0

Release date: 2026-06-10

## Highlights

- Added Markdown linting to the documentation pipeline.
- Added mdBook deployment to GitHub Pages.

## Breaking Changes

None.

## Documentation

- [Markdown Basics](./01-Foundations/markdown-basics.md)
- [CI Automation](./03-Automation/ci-automation.md)
```

## Good Checklist Design

Weak:

```markdown
- [ ] Documentation is good.
```

Better:

```markdown
- [ ] The deployment guide was tested on a clean machine.
```
