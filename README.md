# Second Brain Wiki

A personal knowledge base maintained by an LLM agent. You source and explore; the agent writes, cross-references, and keeps everything current.

## How It Works

Raw sources go into `raw/`. The agent reads them, extracts key information, and compiles it into structured, interlinked pages in `wiki/`. Knowledge accumulates — each new source updates existing pages, flags contradictions, and strengthens the synthesis. Nothing gets re-derived from scratch on every question.

## Structure

```
vault/
├── CLAUDE.md        ← agent operating schema (page formats, workflows, conventions)
├── index.md         ← full content catalog
├── log.md           ← append-only record of every ingest, query, and audit
├── raw/             ← your source documents (immutable — agent never modifies these)
│   └── assets/      ← downloaded images and attachments
└── wiki/
    ├── overview.md  ← living synthesis of the whole wiki
    ├── entities/    ← people, orgs, places, products, events
    ├── concepts/    ← ideas, theories, frameworks, themes
    ├── sources/     ← one summary page per ingested source
    └── outputs/     ← filed analyses, comparisons, syntheses
```

## Usage

Open this vault in Claude Code (`claude` in the vault directory). The agent loads `CLAUDE.md` automatically and knows what to do.

| Command | What happens |
|---|---|
| `ingest [file]` | Agent reads the source, discusses takeaways, writes all pages |
| `what do we know about X?` | Agent searches the wiki and synthesizes an answer |
| `compare X and Y` | Produces a comparison, offers to file it as an output page |
| `lint` | Audits the wiki — orphans, stale pages, missing links, contradictions |
| `file this` | Saves the current answer as a permanent output page |
| `update overview` | Regenerates `wiki/overview.md` from the current wiki state |
| `what should I read next?` | Suggests sources based on gaps in the wiki |

## Adding Sources

1. Drop any document into `raw/` — articles clipped with [Obsidian Web Clipper](https://obsidian.md/clipper), PDFs, transcripts, notes, data files
2. Say `ingest [filename]`
3. The agent surfaces the key takeaways and asks about emphasis
4. It writes the source summary, updates entity and concept pages, and logs everything

Good answers can be filed back into the wiki as output pages — your explorations compound just like ingested sources do.

## Browsing

Open in Obsidian for the full experience: graph view shows the link structure, Dataview queries work against page frontmatter, and the file tree mirrors the folder layout above.
