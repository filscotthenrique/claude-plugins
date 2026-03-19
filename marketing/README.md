# Abeam Marketing Plugin

Marketing operations toolkit for Abeam — a pilot-first platform for general aviation.

## Architecture

One skill (`marketer`) with structured data files and prose references, organized by domain. 9 commands for content workflows.

### Skill: `marketer`

The single marketing knowledge base. Contains core voice guidelines in SKILL.md, with progressive disclosure via `data/` (structured, queryable) and `reference/` (prose).

```
skills/marketer/
├── SKILL.md                      # Voice, do/don't, terminology, competitor rules, resource directory
├── data/                         # Structured queryable data
│   ├── taglines.json             # Taglines by category/audience/status
│   ├── audience-profiles.json    # 5 personas with demographics, pain points, messaging
│   ├── platform-specs.json       # Character limits, image sizes, cadence per platform
│   ├── product-state.jsonl       # Auto-maintained by /finalize pipeline
│   └── experiment-log.csv        # Content performance tracking
└── reference/                    # Prose reference by domain
    ├── product-knowledge.md      # Pipeline pointers, translation filter, claim rules
    ├── feature-inventory.md      # Product lines, pricing, origin story
    ├── competitive-landscape.md  # Competitor facts and positioning
    ├── website-copy-patterns.md  # Hero, feature, coming-soon page patterns
    ├── boilerplate-copy.md       # Standard descriptions (25/50/100 words)
    └── experiment-guide.md       # How to use the experiment log
```

### Commands (9)

| Command | Purpose |
|---------|---------|
| `/copy-rewrite` | Rewrite marketing site copy from a ticket spec |
| `/social-post` | Generate platform-specific social media copy |
| `/copy-generator` | High-volume copy variations (taglines, hooks, bios) |
| `/release-announce` | Complete release marketing package |
| `/blog-outline` | SEO blog post outline |
| `/app-store-copy` | App Store listing optimization |
| `/email-draft` | Marketing email copy |
| `/forum-response` | Community response drafts |
| `/performance-review` | Analyze experiment log performance |

## Integration with Main Repo

### Product State Pipeline

The `/finalize` command in the main repo includes a `marketing-state` agent that automatically appends user-facing feature changes to `data/product-state.jsonl`. This means the marketing plugin's product knowledge stays current as a side-effect of the normal development workflow.

```
Code → /finalize → marketing-state agent → product-state.jsonl → marketer skill reads it
```

### Content Generation Pipeline

The main repo's `/content-generate` skill produces extraction artifacts, changelogs, blog drafts, and release notes. The marketer skill's `reference/product-knowledge.md` points to these outputs for determining current product state.

## Data Format Rationale

| Format | Used For | Why |
|--------|----------|-----|
| JSON | Taglines, personas, platform specs | Filtered, queried, updated programmatically |
| JSONL | Product state | Append-only, one entry per feature shipped |
| CSV | Experiment log | Tabular, aggregated by column |
| Markdown | Voice guidelines, competitive context, copy patterns | Prose, read linearly |
