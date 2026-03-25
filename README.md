# Theology

Theological research monorepo. Confessional 1689 Reformed Baptist framework.

## Topics

- **[prenup](prenup/)** — Christian marriage contract research
- **[monarchy](monarchy/)** — Monarchy and political theology
- **[semper-virgo](semper-virgo/)** — Perpetual virginity of Mary

## Repository Structure

Every topic follows the same directory layout:

```text
topic-name/
├── README.md                        # Topic overview, thesis direction, status
├── research/
│   ├── references/                  # Source material — CSVs, PDFs, primary texts
│   │   ├── scripture.csv            # Biblical passages relevant to the topic
│   │   ├── patristic.csv            # Church Fathers sources
│   │   └── ...                      # Additional categories as needed
│   └── *.md                         # Narrative research notes and analysis
├── drafts/                          # Working drafts of written output
│   └── *.md
└── thesis/                          # Finalized or near-final arguments
    └── *.md
```

### Conventions

- **One topic per directory.** Don't mix research across topics in the same files.
- **CSVs for source catalogs.** Each CSV collects sources of a particular type
  (Scripture, patristic, Puritan, modern, etc.) with columns for the figure, work,
  relevant quote, stance, and reference notes.
- **Markdown for analysis.** Narrative research notes, commentary, and argumentation
  go in `.md` files under `research/` or `drafts/`/`thesis/`.
- **GitHub Issues for research tracking.** Each topic has issues labeled with its
  topic name (e.g., `prenup`, `monarchy`, `semper-virgo`). One issue per source
  category — mirrors the reference CSVs but includes research questions and gaps.
- **Cross-references welcome.** Topics overlap (e.g., the same Church Father may
  appear in multiple topics). Use issue references (`#N`) and relative paths to
  link across topics rather than duplicating content.

### Adding a new topic

1. Create a directory: `new-topic/`
2. Add a `README.md` with the topic overview and thesis direction
3. Create `research/references/` and seed it with at least one source CSV
4. Ask a maintainer to create the GitHub issue label
5. Open research issues following the pattern of existing topics
6. Update this README's Topics list

## Development

```bash
make check   # lint all markdown
make fix     # auto-fix markdown issues
```

All markdown must pass [markdownlint](https://github.com/DavidAnson/markdownlint)
with the repo's `.markdownlint.yaml` config before merging. Line length limit is
120 characters.
