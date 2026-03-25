# Theology

Theological research monorepo. Confessional 1689 Reformed Baptist framework.

## Topics

- **[prenup](prenup/)** — Christian marriage contract research
- **[monarchy](monarchy/)** — Monarchy and political theology
- **[semper-virgo](semper-virgo/)** — Perpetual virginity of Mary

## Structure

Each topic lives in its own directory with:

- `README.md` — topic overview and thesis
- `research/references/` — source material (CSVs, PDFs)
- `drafts/` or `thesis/` — written output

## Development

```bash
make check   # lint all markdown
make fix     # auto-fix markdown issues
```
