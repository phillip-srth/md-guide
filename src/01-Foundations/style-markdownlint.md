# Style and markdownlint 🧹

markdownlint catches style problems before review. It removes avoidable noise: inconsistent headings, missing blank
lines, duplicate titles, bad list indentation, and unlabelled code fences.

## Install

```powershell
npm install --save-dev markdownlint-cli2
```

Run it:

```powershell
npx markdownlint-cli2 "**/*.md" "#public" "#node_modules"
```

## Recommended Configuration

```json
{
  "default": true,
  "line-length": {
    "line_length": 120,
    "code_blocks": false,
    "tables": false
  },
  "no-duplicate-heading": {
    "siblings_only": true
  },
  "no-inline-html": {
    "allowed_elements": ["br", "img", "details", "summary", "kbd"]
  },
  "first-line-h1": false
}
```

| Rule | Decision | Reason |
| --- | --- | --- |
| `MD013/line-length` | Keep a 120-character limit. | Long lines are hard to review. |
| `MD024/no-duplicate-heading` | Allow repeated headings in different sections. | Repeated lower level headings are normal. |
| `MD033/no-inline-html` | Allow a few HTML tags. | `details`, `summary`, `kbd`, and `img` are useful. |
| `MD041/first-line-h1` | Disable first-line heading enforcement. | mdBook `SUMMARY.md` is special. |

## Team Style Rules

- One idea per paragraph.
- Prefer active voice: "Run the command" instead of "The command should be run".
- Use sentence case for headings.
- Use `code formatting` for file paths, commands, flags, package names, and identifiers.
- Use relative links for local docs.
- Add alt text to images.

## Pre-commit Hook

```yaml
repos:
  - repo: https://github.com/DavidAnson/markdownlint-cli2
    rev: v0.13.0
    hooks:
      - id: markdownlint-cli2
        args:
          - --config
          - .markdownlint.json
```

Pin versions in real projects. Floating versions make failures harder to reproduce.
