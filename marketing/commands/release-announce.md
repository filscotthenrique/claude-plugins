---
description: Generate a complete release marketing package from a release summary
allowed-tools: Read, Write, Edit, Grep, Glob, Bash
argument-hint: [path to release summary or describe changes]
---

Generate a complete release marketing package for Abeam.

This is the primary output of the Git-to-marketing pipeline. It takes a release summary (what changed) and produces ready-to-publish marketing content across all channels.

**Before writing anything**, load the `marketer` skill by reading its SKILL.md, then read these data/reference files:
- `marketer/data/taglines.json` — for feature-specific hooks and taglines
- `marketer/data/audience-profiles.json` — to tailor content for different segments
- `marketer/data/platform-specs.json` — for format requirements per channel
- `marketer/data/experiment-log.csv` — check what angles have worked for similar features
- `marketer/reference/product-knowledge.md` — to verify accuracy and identify what's new vs existing

**Gather the release information:**

If $ARGUMENTS points to a file, read it. Otherwise, ask:
1. **What changed?** New features, improvements, bug fixes — describe what a user would notice.
2. **Which audiences does this affect?** Student pilots, private pilots, CFIs, all users?
3. **Which channels should we create content for?** All, or a specific subset?
4. **Is this a major or minor release?** Major = full marketing package. Minor = What's New + social.

**Generate the package:**

### 1. App Store "What's New" copy
- Under 500 characters
- Clean, scannable, factual
- Feature names match the app UI

### 2. Social media posts (per platform requested)
- **Instagram**: Feed post caption with hashtags. Consider whether a carousel or reel makes more sense.
- **LinkedIn**: Founder-voice announcement. More reflective, "here's what we built and why."
- **X/Twitter**: Concise announcement. Thread if multiple features.
- **Reddit**: Only if the release is significant enough to warrant a post on r/flying. Draft as a founder update, not a product announcement.
- **TikTok**: Script outline for a quick walkthrough or "new feature" reveal.

### 3. Blog post (for major releases)
- Full draft or detailed outline depending on release size
- SEO-optimized title and meta description
- Naturally integrates the new feature into Abeam's broader story

### 4. Email announcement
- Subject line options (3)
- Preview text
- Body (200–400 words)
- Segmented versions if the feature matters more to one audience

### 5. Suggested taglines for the new feature
- 3–5 tagline options specific to this feature/update
- Note which existing taglines from the library could be adapted

### 6. Product state verification
- Verify that `data/product-state.jsonl` includes entries for this release's features
- If the `/finalize` pipeline has already run, entries should exist automatically
- If entries are missing, append them to `data/product-state.jsonl` following the JSONL schema: `{"date":"YYYY-MM-DD","scope":"...","feature":"...","type":"feature","description":"...","commits":["..."]}`

**Output format:**
- Each section clearly labeled and formatted for its target platform
- Product-knowledge update at the end, clearly marked as "proposed — review before merging"
- Note: "All content is draft. Review and personalize before publishing."
