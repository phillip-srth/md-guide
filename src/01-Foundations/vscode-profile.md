# VS Code Writing Profile

VS Code can become a strong Markdown editor with a dedicated profile. A separate profile keeps writing settings from
interfering with normal coding settings.

## Recommended Extensions

| Extension | Purpose |
| --- | --- |
| `DavidAnson.vscode-markdownlint` | Lint Markdown while editing. |
| `bierner.markdown-mermaid` | Preview Mermaid diagrams. |
| `jebbs.plantuml` | Preview PlantUML diagrams. |
| `yzhang.markdown-all-in-one` | Authoring helpers and table formatting. |
| `streetsidesoftware.code-spell-checker` | Catch spelling mistakes in prose and code terms. |

## Workspace Settings

Create `.vscode/settings.json`:

```json
{
  "editor.wordWrap": "on",
  "editor.rulers": [120],
  "editor.tabSize": 2,
  "files.trimTrailingWhitespace": true,
  "files.insertFinalNewline": true,
  "markdown.validate.enabled": true,
  "markdownlint.config": {
    "extends": ".markdownlint.json"
  },
  "cSpell.words": [
    "CommonMark",
    "Docs-as-Code",
    "markdownlint",
    "mdBook",
    "PlantUML"
  ]
}
```

## Useful Shortcuts

| Action | Windows Shortcut | Why It Helps |
| --- | --- | --- |
| Open preview | `Ctrl` + `Shift` + `V` | Check rendered output quickly. |
| Open preview to side | `Ctrl` + `K`, then `V` | Write and preview side by side. |
| Format document | `Shift` + `Alt` + `F` | Format tables and lists. |
| Quick fix | `Ctrl` + `.` | Apply lint fixes when available. |

## Preview Strategy

| Level | Tool | Use Case |
| --- | --- | --- |
| Editor preview | VS Code Markdown preview | Fast feedback while typing. |
| Book preview | `mdbook serve --open` | Verify navigation, theme, search, and MathJax. |
| CI build | GitHub Actions or another pipeline | Verify the same checks reviewers will trust. |

Do not rely only on the editor preview. VS Code, GitHub, and mdBook render some features differently.
