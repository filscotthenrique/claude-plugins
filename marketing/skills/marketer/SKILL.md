---
name: marketer
description: >
  Abeam's comprehensive marketing knowledge base. Use this skill whenever writing, drafting,
  reviewing, or editing any marketing content for Abeam — social media posts, App Store copy,
  blog posts, email newsletters, forum responses, ad copy, landing page text, press blurbs,
  taglines, or any public-facing communication. Also use when the user asks to: "check the voice,"
  "review tone," "pick a tagline," "find a hook," "write a headline," or mentions brand consistency,
  audience targeting ("student pilots," "CFIs," "flight school owners"), platform formatting
  ("character limit," "image size," "hashtag strategy"), product capabilities ("what features
  do we have," "what's live," "what's coming"), competitive positioning, or content performance.
  If in doubt about whether Abeam marketing is involved, use this skill.
---

# Abeam Marketing Guide

Abeam is a pilot-first platform for general aviation. This skill is the single source of truth for writing Abeam marketing content.

## The voice in one line

**Sound like a knowledgeable friend at the airport who happens to build software.**

Not a SaaS marketing page. Not an airline safety briefing. Not a Silicon Valley pitch deck. A real pilot, talking to real pilots, about tools that make their flying lives easier.

## Core principles

**Be direct and plain-spoken.** Say "log your flights in seconds," not "leverage our streamlined flight-logging solution." Aviation runs on clear communication — so does Abeam's copy.

**Respect the audience.** Student pilots are spending serious money and taking real risk. Weekend flyers are passionate about something most people don't understand. Instructors are running small businesses on thin margins. Never talk down, never patronize, never assume ignorance.

**Understate and overdeliver.** Pilots are skeptical people. Overclaiming erodes trust instantly. If the feature is good, describe it simply and let the reader draw their own conclusion. "Upload your medical once. We track your currency automatically." — that's more persuasive than any superlative.

**Be authentic about who we are.** Abeam is built by a pilot, in Colorado, because the existing tools weren't good enough. That origin story is a strength. Use it naturally, not as a constant refrain.

**Humor is welcome, but grounded.** Self-deprecating beats clever wordplay. Hangar talk beats advertising copy. If a joke would land at a fly-in breakfast, it'll work. If it sounds like a copywriter wrote it, cut it.

## The do / don't table

This is the single most important reference. When in doubt, check a draft against these pairs:

| Do | Don't |
|---|---|
| "Log your flights in seconds" | "Leverage our streamlined flight-logging solution" |
| "We built this because we needed it" | "Our team identified a market opportunity" |
| "Works on your iPhone, your iPad, and the web" | "Omnichannel cross-platform experience" |
| "Upload your medical once" | "Seamlessly integrate your certification documents" |
| "No contracts. Cancel anytime." | "Flexible subscription management options" |
| "Built for Part 61 flexibility" | "Adaptive training framework architecture" |
| "Your data stays with you" | "Robust data portability and interoperability" |
| "See all your students at a glance" | "Comprehensive student lifecycle management" |
| "Share your study materials in one tap" | "Deploy instructional assets via our content distribution pipeline" |

The pattern: use the words a pilot would use talking to another pilot. If a phrase could appear in a generic B2B SaaS blog post, rewrite it.

## Aviation terminology

Use correct aviation terms. This is non-negotiable — getting terminology wrong destroys credibility with this audience instantly.

- **METAR**, not "weather data feed" or "weather conditions report"
- **Currency**, not "certification status" or "compliance tracking"
- **ACS** (Airman Certification Standards), not "skills framework" or "testing rubric"
- **BFR** / **Flight Review**, not "recertification" or "proficiency check"
- **Part 61** / **Part 141**, not "training pathway" or "regulation type"
- **CFI**, not "flight teacher" or "aviation educator"
- **Checkride**, not "practical test" or "final examination"
- **Tail number**, not "aircraft identifier" or "registration code"
- **Ramp**, not "tarmac" (tarmac is an airline/media term that GA pilots notice)
- **FBO**, not "airport service center"
- **Logbook**, not "flight journal" or "flight record"

When writing about features, map them to how pilots actually talk: "currency tracking" not "compliance monitoring," "digital hangar" not "aircraft asset management."

## Platform availability

**Abeam Pilot** is available on **iOS and the web**. There is no Android app — it's on the roadmap but not available yet, likely tied to European market expansion. "Works on your iPhone, your iPad, and the web" is accurate. "Works on every device" or "iOS, Android, and web" is not.

## Competitor mentions

**Default: do not mention competitors by name.** Focus on what Abeam does. Let pilots draw their own comparisons.

Only name a competitor when ALL of these are true:
1. The user explicitly asks for a comparison or the content format requires it.
2. You can verify the claim as factual. If unsure, say so or direct the reader to check the competitor's site.
3. The comparison highlights something Abeam does better or differently.

For detailed competitor data, load `reference/competitive-landscape.md`.

## Primary tagline

**"Built for the way you fly."**

This is the brand tagline. Use it as the anchor. It works across all audiences and products.

## Data Files & References

Load these when the task requires them:

| File | When to Load | What It Contains |
|------|-------------|------------------|
| `data/taglines.json` | Needs a hook, headline, tagline, or App Store subtitle | Full tagline library, filterable by category/audience/status. Includes avoid-patterns. |
| `data/audience-profiles.json` | Writing for a specific persona, choosing messaging angle, or audience question | 5 personas with demographics, pain points, messaging hooks, tone, channels, budgets |
| `data/platform-specs.json` | Formatting for a specific platform (character limits, image sizes, cadence) | Instagram, TikTok, Reddit, LinkedIn, X, YouTube, App Store, Email, Blog specs |
| `data/product-state.jsonl` | Checking what features have shipped (auto-maintained by /finalize) | Append-only log of user-facing features with dates and scopes |
| `data/experiment-log.csv` | Generating content (check what's worked), logging post performance | Performance tracking: likes, comments, shares, impressions, qualitative notes |
| `reference/product-knowledge.md` | Checking what can be claimed, translating technical→marketing, "what NOT to claim" | Pipeline pointers, translation filter, scope-to-feature mapping, durable claim rules |
| `reference/feature-inventory.md` | Product lines, pricing, origin story, platform availability | Stable facts that rarely change |
| `reference/competitive-landscape.md` | Comparison content, competitive positioning, forum responses about alternatives | Competitor facts: ForeFlight, LogTen/Pilotbase, FSP, MyFlightbook, Flight Circle, Pilot Partner |
| `reference/website-copy-patterns.md` | Writing or rewriting marketing site pages | Hero, feature, coming-soon, persona page patterns, CTA conventions |
| `reference/boilerplate-copy.md` | Bios, about sections, press materials, partnership descriptions | Standard descriptions at 25, 50, and 100 words |
| `reference/experiment-guide.md` | Logging post performance, analyzing content patterns, "what's working" questions | How to use experiment-log.csv, analysis dimensions, pattern tracking |
