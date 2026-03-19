---
description: Generate a social media post for Abeam
allowed-tools: Read, Write, Edit, Grep, Glob
argument-hint: [platform] [feature or topic]
---

Generate a social media post for Abeam.

**Before writing anything**, load the `marketer` skill by reading its SKILL.md, then read these data files:
- `marketer/data/taglines.json` — for hooks and one-liners to build from
- `marketer/data/platform-specs.json` — for the target platform's character limits, hashtag strategy, and formatting
- `marketer/data/audience-profiles.json` — if a specific audience is mentioned
- `marketer/data/experiment-log.csv` — check what's worked before on this platform
- `marketer/reference/product-knowledge.md` — if product claims need verification

**Gather these inputs** (ask if not provided in $ARGUMENTS):
1. **Platform**: Instagram, TikTok, Reddit, LinkedIn, X, or multiple
2. **Feature or topic**: Which Abeam feature or angle to highlight
3. **Target audience**: Student pilots, private pilots, CFIs, general, or let me pick
4. **Any specific constraints**: Screenshot to reference, event tie-in, thread vs single post

**Generate the post:**
- Use proper formatting for the platform (capitalization, hashtags, length, emoji conventions)
- Lead with a hook — the first line determines whether anyone reads the rest
- Pull from the tagline library for the closing line or CTA
- If generating for multiple platforms, adapt the message for each — don't just cross-post the same text
- Include a note about whether the experiment log has relevant patterns for this platform/feature combo

**Output format:**
- The post copy, formatted exactly as it would appear on the platform
- A brief note on which tagline/angle was used and why
- Reminder: "Review and personalize before posting."

If generating for Reddit, always include the founder disclosure line.
