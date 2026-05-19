# Ingest Skill

**Ingest** processes new sources into this wiki. Triggered when the user wants to absorb material into the wiki rather than receive a one-off summary.

## Workflow

1. **Read the raw source** — file in `raw/`. Never create, edit, or delete files in `raw/`.
2. **Surface and discuss** — send one short message: the 3–5 most important takeaways, and ask if there's a particular angle to emphasize. Keep it tight; don't monologue.
3. **Write source page** — `wiki/sources/<slug>.md`
4. **Identify all entities** — people, orgs, places, products, events mentioned
5. **Identify all concepts** — ideas, frameworks, theories introduced or developed
6. **Update entity pages** — check `wiki/entities/`. Update if exists, create if not.
7. **Update concept pages** — check `wiki/concepts/`. Update if exists, create if not.
8. **Flag contradictions** — if the source conflicts with existing claims, add `> [!WARNING]` callouts to affected pages
9. **Update `wiki/overview.md`** — if this source materially shifts the big picture
10. **Update `index.md`** — add new pages, update counts and "last updated" line
11. **Append to `log.md`** — one entry listing every file touched

## Key Principles

- Use wikilinks (`[[wiki/path/slug|Display Name]]`) on first mention of any entity or concept that has a page
- Cite sources; don't assert claims without attribution
- Flag contradictions inline rather than silently overwriting
- Keep source pages as immutable summaries; synthesize across sources on entity/concept pages
- A single ingest typically touches 5–15 pages

## Wiki Structure

```
wiki/
├── overview.md        ← living synthesis
├── entities/          ← people, orgs, places, products, events
├── concepts/          ← ideas, theories, frameworks, themes
├── sources/           ← one summary page per ingested raw source
└── outputs/           ← filed analyses, comparisons, syntheses
```

## Conventions

Consult `CLAUDE.md` for page formats, frontmatter schemas, naming conventions, and log/index format requirements.
