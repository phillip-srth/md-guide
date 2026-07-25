# Markdown Basics

Markdown is a lightweight markup language. Its main strength is that the source is readable before it is rendered.
That makes it ideal for code reviews, Git history, and long-lived project documentation.

## Headings

Use headings to create structure, not just larger text.

```markdown
# Page Title

## Main Section

### Subsection
```

Recommended rules:

| Rule | Why |
| --- | --- |
| Use exactly one `#` heading per page. | It gives the page one clear topic. |
| Do not skip levels. | Jumping from `##` to `####` makes navigation confusing. |
| Keep headings specific. | `Database Migration` is better than `Details`. |

## Paragraphs and Emphasis

A blank line starts a new paragraph.

```markdown
Use **bold** for important terms.
Use _italic_ for light emphasis.
Use `inline code` for commands, file names, flags, and identifiers.
```

Prefer restraint. If everything is bold, nothing is important.

## Lists

Use unordered lists for related items:

```markdown
- Install dependencies.
- Run the tests.
- Build the documentation.
```

Use ordered lists when sequence matters:

```markdown
1. Create a branch.
1. Make the change.
1. Open a pull request.
```

Use task lists for trackable work:

```markdown
- [x] Update API reference.
- [x] Add migration notes.
- [ ] Get reviewer approval.
```

## Links and Images

Use meaningful link text:

```markdown
[Read the mdBook documentation](https://rust-lang.github.io/mdBook/)
```

Add useful alt text to images:

```markdown
![Architecture diagram showing app, API, and database](../assets/project-structure.svg)
```

## Tables

Tables are best for comparison, not layout.

| Syntax | Use For | Example |
| --- | --- | --- |
| `**text**` | Strong emphasis | **Important** |
| `` `code` `` | Inline code | `dotnet test` |
| `[text](url)` | Links | [mdBook](https://rust-lang.github.io/mdBook/) |

Keep tables small. Large tables are hard to read on mobile and painful to review in Git diffs.

## Code Blocks

Always add a language to fenced code blocks.

````markdown
```powershell
mdbook build
```
````

This enables syntax highlighting and helps tools understand the content.

## Markdown Dialects

| Dialect | Typical Features | Where You See It |
| --- | --- | --- |
| CommonMark | Core Markdown syntax | Many parsers and static site generators |
| GitHub Flavored Markdown | Tables, task lists, strikethrough | GitHub issues, PRs, and README files |
| Renderer-specific Markdown | Callouts, tabs, includes | mdBook plugins, MkDocs Material, Docusaurus |

Use portable Markdown for core content and isolate renderer-specific features to places where you intentionally depend on
that renderer.
