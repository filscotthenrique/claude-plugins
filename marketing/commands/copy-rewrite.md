---
description: Rewrite marketing site copy based on a ticket specification
allowed-tools: Read, Write, Edit, Grep, Glob, Bash
argument-hint: [ticket number or path]
---

Rewrite marketing site copy for a specific page, guided by a Marketing Copy Update ticket.

**Before writing anything**, load the `marketer` skill by reading its SKILL.md, then read these files based on the task:

- `marketer/data/taglines.json` — for taglines and hooks to use in headers and heroes
- `marketer/data/audience-profiles.json` — if the ticket targets a specific persona
- `marketer/reference/product-knowledge.md` — for claim verification rules
- `marketer/reference/feature-inventory.md` — for product lines, pricing, origin story
- `marketer/reference/website-copy-patterns.md` — for page structure patterns (hero, feature, coming-soon, persona)

**Resolve the ticket:**

If $ARGUMENTS is a number (e.g., "4"), find the ticket at:
`.claude/docs/roadmap/marketing/marketing-copy-update/🎫 [N] *.md`

Use glob matching: `.claude/docs/roadmap/marketing/marketing-copy-update/*[N]*`

If $ARGUMENTS is a file path, read that file directly.

If no argument is provided, list available tickets from the `marketing-copy-update/` directory and ask which one to work on.

**Read the ticket and extract:**
1. **Files to modify** — the ticket lists specific source file paths
2. **Tasks** — checkbox items describing what to change
3. **Acceptance criteria** — what "done" looks like
4. **Messaging references** — tagline requirements, persona references, framework guidance
5. **Screenshot TODOs** — which visuals need replacing (may be blocked by ticket [11])

**For each file in the ticket:**

1. Read the current source file in the main repo
2. Identify all copy strings — JSX text content, title/description props, meta tags, section headers, CTA button text
3. For each string the ticket says to change:
   - Draft new copy following the marketer skill's voice guidelines
   - If the ticket references a specific tagline, pull it from `data/taglines.json`
   - If the ticket specifies an audience, load that persona's messaging hooks from `data/audience-profiles.json`
   - Apply website-copy-patterns for the page type (hero, feature, coming-soon, persona)
4. Present changes as a before/after diff for each component or section
5. For SEO meta descriptions and titles, show character counts

**Verify product claims:**

For every feature claim in the new copy:
- Check against the main repo changelog: `web/apps/marketing/content/drafts/changelog/CHANGELOG.md`
- Check `data/product-state.jsonl` for shipped features
- Check roadmap ticket status if the copy references planned features
- Flag any claim that cannot be verified as shipped or in-progress

**Output format:**

Present changes grouped by component/section within each file:

```
## File: web/apps/marketing/src/components/landing/HeroSection.tsx

### Hero Tagline
- **Before**: "A Modern OS for General Aviation. Software That Just Works."
- **After**: "Built for the way you fly."
- **Source**: Brand tagline (data/taglines.json, category: brand)

### Supporting Copy
- **Before**: [current text]
- **After**: [new text]
- **Rationale**: [which persona/pain-point this addresses]

### Timeline Badge
- **Before**: "Coming 2026"
- **After**: "Launching Summer 2026"
- **Verified**: Matches roadmap Q2 2026 target

## SEO Meta (index.astro)
- **Title** (52 chars): "Abeam — Built for the Way You Fly | Pilot Logbook & Currency"
- **Description** (148 chars): "Free pilot logbook, automatic currency tracking, and live weather on iPhone, iPad, and the web. Built by a pilot in Colorado."
```

After the user approves the changes, apply them to the source files.

**Post-rewrite checklist:**
- Remind the user to run `/seo-audit` after all copy changes in a ticket are complete
- Note any screenshot placeholders that still need replacing (blocked by ticket [11])
- If the ticket has acceptance criteria checkboxes, list which ones are now satisfied
