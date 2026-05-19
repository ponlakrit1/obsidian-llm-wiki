# Query Skill

**Query** answers questions by reading the wiki — not by guessing, but by finding relevant pages, synthesizing what they say, and citing sources.

## Workflow

1. **Read `index.md`** to identify relevant pages
2. **Read the relevant wiki pages** — sources, entities, concepts — and follow wikilinks 1–2 levels deep
3. **Synthesize an answer** with `[[wikilinks]]` as inline citations
4. **Offer to file** — end with: "Should I file this as an output page?" If yes, write `wiki/outputs/<slug>.md`, then update `index.md` and append to `log.md`
5. **Surface gaps** — if the answer reveals something uninvestigated, note it: "Gap: no source yet covers X."

## Core Principle

Answers are grounded in the user's actual wiki, not general training data. Always cite specific pages so the user can verify and explore context. When the wiki lacks information, acknowledge the gap rather than fill it with guesses. Surface contradictions instead of arbitrating between them.

## Conventions

Consult `CLAUDE.md` for output page format, frontmatter schema, and wikilink conventions.
