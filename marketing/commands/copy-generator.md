---
description: Generate high-volume marketing copy variations — taglines, descriptions, hooks, bios, and more
allowed-tools: Read, Write, Edit, Grep, Glob
argument-hint: [taglines | descriptions | hooks | bios | headlines] [feature or theme]
---

Generate a large volume of marketing copy variations for Abeam. The goal is quantity — produce enough options that the best ones can be hand-picked and added to the tagline library or used directly.

**Before writing anything**, load these skills by reading their SKILL.md files:
- `brand-voice` — for voice, tone, and the do/don't table
- `tagline-library` — to understand existing taglines and avoid duplicating them
- `product-knowledge` — for accurate product details
- `audience-profiles` — if generating for a specific persona

**Determine the output type** from $ARGUMENTS (ask if not provided):

1. **Taglines** — Short, punchy lines (5–12 words). Brand-level or feature-specific.
2. **Descriptions** — Longer copy at specified lengths (25 words, 50 words, 100 words, one paragraph, etc.).
3. **Hooks** — Opening lines for social posts, emails, or blog intros. The line that makes someone stop scrolling.
4. **Bios** — Social media bios, App Store subtitle options, about-page blurbs at various lengths.
5. **Headlines** — Blog post titles, landing page headers, email subject lines.
6. **CTAs** — Calls to action at various energy levels (soft, direct, urgent).

**Gather inputs:**
- **Theme or feature**: What should the copy be about? A specific feature (currency tracking, digital hangar, METAR), a brand angle (built by a pilot, free tier, cross-platform), or general brand.
- **Target audience** (optional): Student pilots, private pilots, CFIs, general. Defaults to general if not specified.
- **Quantity**: How many variations? Default to 25 per batch. Can go higher — 50, 100. The user is curating, so more is better.
- **Length constraint** (for descriptions): 25 words, 50 words, 100 words, one sentence, one paragraph, etc.
- **Tone dial** (optional): Where on the spectrum? Options:
  - Understated → Confident → Bold
  - Casual → Professional
  - Warm → Direct
  - Default: the Abeam sweet spot (understated, casual, warm)

**Generation approach:**

Produce variations by systematically varying these dimensions:
- **Angle**: What's the entry point? The problem it solves, the feeling it creates, the origin story, the technical capability, the comparison to alternatives, the simplicity.
- **Structure**: Statement, question, command, fragment, two-part (setup + payoff), call-and-response.
- **Register**: Hangar talk, app store polish, founder voice, community voice, headline energy.
- **Specificity**: Abstract ("Built for the way you fly") vs concrete ("Log a flight in 12 seconds").
- **Emotional tone**: Confidence, relief, belonging, frustration-resolution, aspiration, humor.

Don't self-censor during generation. The user is picking favorites — include lines you're not sure about. A line that sounds risky might be exactly what lands.

**Rules:**
- Do NOT repeat existing taglines from the tagline-library skill verbatim. Reference them to understand the voice, then generate new ones.
- Do NOT use anything from the "taglines to avoid" list (no "all-in-one," "next-gen," "disrupting aviation," etc.).
- Do NOT mention Android. "iPhone, iPad, and the web" is the platform reality.
- Do NOT use SaaS jargon. Every line should pass the do/don't table test.
- DO use correct aviation terminology naturally (METAR, currency, BFR, checkride, ramp, FBO, tail number).
- DO include some lines that are edgy, funny, or unexpected — the user can always cut them.

**Output format:**

Organize by variation type, numbered for easy reference:

```
## [Theme] — Taglines (25 variations)

### Angle: Problem it solves
1. ...
2. ...
3. ...

### Angle: How it feels
4. ...
5. ...
6. ...

### Angle: Origin story
7. ...
8. ...

### Angle: Simplicity / speed
9. ...
10. ...

### Angle: Community / belonging
11. ...
12. ...

### Angle: Unexpected / edgy
13. ...
14. ...

[etc.]
```

After generating, add a brief note:
- "My top 5 from this batch" — flag the ones you think are strongest
- "These push the boundary" — flag any that are edgy or might not land
- "These are variations on existing library lines" — flag any that riff on current taglines

**When the user selects favorites**, update the tagline library automatically:

1. Read the current `tagline-library` SKILL.md at `skills/tagline-library/SKILL.md`
2. For each selected line, determine the best category (existing category if it fits, or propose a new one)
3. Append the new lines to the appropriate category sections in the tagline library
4. If a line doesn't fit an existing category, create a new section with a clear heading
5. Add a brief note next to new lines indicating they were generated in this session — e.g., `(added March 2026)` — so the user can track what's new vs original
6. Also update the brand-voice reference file at `skills/brand-voice/references/tagline-library.md` to stay in sync
7. Show the user the diff of what was added and where

If the user hasn't selected specific lines yet, ask: "Which ones do you want to keep? Give me the numbers and I'll add them to the tagline library."
