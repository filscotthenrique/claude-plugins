---
description: Analyze the experiment log and review content performance
allowed-tools: Read, Write, Edit, Grep, Glob, Bash
argument-hint: [time range or platform filter]
---

Analyze Abeam's marketing content performance using the experiment log.

**Before doing anything**, load these skills by reading their SKILL.md files:
- `experiment-memory` — for how to read and analyze the log
- `platform-specs` — for benchmark expectations per platform

**Read the experiment log:**
Look for `experiment-log.csv` in the working directory. If it doesn't exist, let the user know and offer to create it.

**Gather optional filters** from $ARGUMENTS:
- **Time range**: "last week," "last 30 days," "March," or all-time
- **Platform filter**: Instagram only, Reddit only, etc.
- **Feature filter**: Posts about a specific feature
- **Specific question**: "What's our best-performing content type?" etc.

**Analyze and present:**

1. **Summary stats**: Total posts logged, posts per platform, average engagement by platform
2. **Top performers**: The 3–5 posts with the highest engagement (relative to platform benchmarks)
3. **Underperformers**: Posts that fell flat — and hypotheses about why
4. **Pattern analysis**:
   - Which features generate the most interest?
   - Which taglines/angles land best?
   - Which content types outperform (reels vs feed, comments vs posts)?
   - Any platform-specific patterns?
   - Day-of-week or time-of-day patterns?
5. **Recommendations**:
   - "Do more of this" — specific, actionable suggestions
   - "Stop doing this" — what's not working
   - "Try this" — untested angles or platforms worth experimenting with

**Output format:**
- Structured analysis with clear sections
- Specific post references (date, platform, angle) for top/bottom performers
- 3–5 concrete recommendations for the next content cycle

If the log has fewer than 10 entries, note that it's too early for reliable patterns and suggest continuing to log consistently.
