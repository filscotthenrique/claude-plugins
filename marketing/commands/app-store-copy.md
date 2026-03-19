---
description: Optimize Abeam's App Store listing or write What's New copy
allowed-tools: Read, Write, Edit, Grep, Glob
argument-hint: [what's-new | full-listing | keywords]
---

Generate or optimize App Store copy for Abeam Pilot.

**Before writing anything**, load the `marketer` skill by reading its SKILL.md, then read these data/reference files:
- `marketer/data/taglines.json` — for subtitle options and supporting taglines
- `marketer/data/platform-specs.json` — for App Store character limits and formatting rules
- `marketer/reference/product-knowledge.md` — for accurate feature descriptions
- `marketer/reference/competitive-landscape.md` — for keyword and positioning opportunities

**Determine the task** from $ARGUMENTS:
- **what's-new**: Write "What's New" release notes for a specific update
- **full-listing**: Optimize the full listing (title, subtitle, description, keywords)
- **keywords**: Research and suggest keyword field optimization

**For What's New copy:**
- Ask what changed in this release (or read a release summary file if provided)
- Keep under 500 characters for readability
- Clean, scannable, factual. Short paragraphs or dashes.
- Feature names must match what the user sees in the app
- No marketing fluff — this is a utility read, not a sales pitch

**For full listing optimization:**
- Title: "Abeam Pilot" (30 chars max)
- Subtitle: Pick from `data/taglines.json` App Store subtitles or propose new (30 chars max)
- Description: Front-load the value prop. First 3 lines visible before "more." Max 4,000 chars.
- Keywords: 100 characters total, comma-separated, no spaces after commas, singular forms, no duplicates. Cross-reference competitor keywords.

**For keyword research:**
- Analyze competitor listings for keyword opportunities
- Identify high-intent searches Abeam should target
- Suggest keyword field optimization (100 char limit)

**Output format:**
- The copy, formatted with character counts for each field
- Notes on keyword strategy or competitive positioning if relevant
