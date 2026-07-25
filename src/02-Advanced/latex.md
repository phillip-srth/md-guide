# LaTeX and Math

LaTeX-style math is useful when documentation includes formulas, algorithms, complexity notes, statistics, or engineering
calculations.

mdBook can render math through MathJax when `mathjax-support = true` is enabled in `book.toml`.

## Inline Math

```markdown
The algorithm runs in \\(O(n \log n)\\) time.
```

Rendered:

The algorithm runs in \\(O(n \log n)\\) time.

## Block Math

```markdown
\\[
availability = \frac{total\ time - downtime}{total\ time}
\\]
```

Rendered:

\\[
availability = \frac{total\ time - downtime}{total\ time}
\\]

## When to Use Math

| Topic | Example |
| --- | --- |
| Performance | \\(O(n)\\), \\(O(n^2)\\), latency percentiles |
| Reliability | Availability, error budgets, retry limits |
| Security | Entropy, probability, token expiry |
| Data | Aggregation, normalization, intervals |

Avoid math when plain prose is clearer.

## Style

- Explain variables before using them.
- Keep formulas close to examples.
- Prefer named equations only in formal reference material.
- Test the final rendered site, because math support varies between renderers.
