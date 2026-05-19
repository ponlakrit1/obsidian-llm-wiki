# Lint Skill

**Lint** performs a health check on the wiki. Produces a prioritized issue report and offers to fix housekeeping items.

## Workflow

1. **Build inventory** — start with `index.md`, scan `wiki/` for unlisted files, review `CLAUDE.md` for convention violations
2. **Check all issue categories** (see below)
3. **Produce prioritized report** — structured as **Critical / Should Fix / Nice to Have**
4. **Ask which to fix** before making any changes
5. **Append to `log.md`** — findings, what was fixed, what was deferred

## Issue Categories

- **Orphan pages** — wiki pages with no inbound links from other wiki pages
- **Missing cross-references** — entity or concept mentioned in a page body but not wikilinked
- **Stale pages** — `sources` frontmatter grew but the body wasn't updated
- **Unflagged contradictions** — conflicting claims across pages without `> [!WARNING]` callouts
- **Concept stubs** — concepts mentioned in passing but no page exists
- **Index gaps** — pages that exist in `wiki/` but aren't listed in `index.md`, or vice versa
- **Overview drift** — `wiki/overview.md` doesn't reflect the current wiki state (new entities/concepts exist that it ignores)

## Design Principle

Signal over noise: a focused list of things that actually matter is more useful than an exhaustive list of minor issues. Housekeeping fixes (index gaps, broken links) can be automated; contradictions, stale claims, and overview drift typically require human judgment.
