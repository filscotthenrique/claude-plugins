# Website Copy Patterns

Patterns for writing marketing site copy for Abeam. Use alongside the marketer skill's voice guidelines and product-knowledge reference for accuracy.

## Hero Sections

The hero is the first thing a visitor sees.

### Hero Copy Formula
1. **Headline**: Tagline or hook (under 10 words) — pull from data/taglines.json
2. **Subhead**: One sentence explaining who it's for and what they get
3. **CTA**: One primary button, optional secondary
4. **Trust signal**: "Free. No credit card." or "Built by a pilot in Colorado."

### Rules
- Lead with the brand tagline or a feature-specific hook
- Supporting copy: 1-2 sentences max. Describe what the user GETS, not what Abeam IS
- Avoid feature lists in the hero — save details for below the fold

### Example
> **Built for the way you fly.**
> Your logbook, your currency, your weather — one app, on your iPhone, your iPad, and the web.
> [Join the Waitlist] [See the Roadmap]

## Feature Pages

Each feature page follows a consistent structure:
1. **Feature hero**: Feature-specific tagline + 1-sentence benefit
2. **Problem statement**: The pain point this solves (use audience pain points from data/audience-profiles.json)
3. **Solution walkthrough**: 3-4 capabilities with screenshots
4. **Social proof** (when available): Testimonials or stats
5. **CTA**: Primary conversion action

### Feature Copy Rules
- Every feature claim must be verifiable against the changelog or product-state.jsonl
- Use present tense for shipped features: "Abeam tracks your currency automatically"
- Use future tense WITH timeline for unshipped: "Coming Q3 2026"
- Never use "will" without a timeline indicator
- **Don't list regulatory coverage as a benefit.** "Every FAA category," "all FAR references," "complete endorsement library" — pilots assume any decent tool handles these. Lead with what the pilot GETS (speed, simplicity, sync, freedom) not what the software COVERS (categories, regulations, form fields).

## "Coming Soon" Framing

For features not yet built (Operations page, some instructor tools):

### Rules
- **Prominent status badge**: "Coming Q4 2026" or "Under Development" at the top
- **Future tense throughout**: "will include", "we're building"
- **Keep the vision**: The pain point is real even if the solution isn't built yet
- **CTA shift**: "Help Us Build This" or "Shape What We Build" instead of "Get Started"
- **Pain points are still valid**: "39% of aviation invoices are paid late" remains true

### Formula
> **[Feature Name]** — Coming [Quarter Year]
> [Pain point — present tense, the problem is real NOW]
> [Vision — future tense, what we're building]
> [CTA: "Join the waitlist to shape this"]

## Persona Landing Pages

Pages like /for/students, /for/instructors, /for/flight-schools:

1. **Persona-specific hero**: Lead with their biggest pain point
2. **Feature mapping**: Show which Abeam features solve THEIR problems
3. **Persona-matched tone**: Student = warm, CFI = empathetic about admin, School = ROI
4. **Testimonial** (when available): From someone in that role
5. **CTA**: Persona-appropriate ("Start Free" for students, "See Pricing" for schools)

### Rules
- Load the persona from data/audience-profiles.json
- Lead with their #1 pain point, not a generic feature list
- Use their language: students say "checkride," schools say "utilization"
- Don't show features irrelevant to this persona

## Section Headers

Section headers should be benefit-oriented, not feature-oriented:

| Bad (Feature-Oriented) | Good (Benefit-Oriented) |
|------------------------|------------------------|
| "Currency Tracking" | "Never wonder 'am I current?' again" |
| "Digital Logbook" | "Log a flight before the engine cools" |
| "Aircraft Management" | "Your aircraft, digitized" |
| "Smart Scheduling" | "Real-time scheduling that syncs in seconds" |

Pull benefit-oriented headers from data/taglines.json when possible.

## CTA Conventions

| Context | CTA Text | Notes |
|---------|----------|-------|
| Pre-launch homepage | "Join the Waitlist" | Primary |
| Pre-launch feature page | "Join the Waitlist" | Same |
| Coming-soon feature | "Help Shape This" or "Get Early Access" | Forward-looking |
| Post-launch homepage | "Download Free" or "Get Started Free" | Direct |
| Instructor page | "See Pricing" or "Start Your Trial" | ROI-oriented |
| School page | "Schedule a Demo" or "See Pricing" | Enterprise pattern |

**NEVER use:** "Become a Founding Partner," "Lock in founding partner rates," or any founding partner language. This program has been retired.

## Product Naming in Comparisons

When comparing to competitors on feature-specific pages, use the product name ("Pilot", "Instruct") not the company name. On general/brand pages, use "Abeam."

| Context | Name | Example |
|---------|------|---------|
| Logbook feature page | "Pilot" | "See How Pilot Stacks Up" |
| Currency feature page | "Pilot" | "How Pilot Tracks Your Currency" |
| Instructor feature page | "Instruct" | "What Makes Instruct Different" |
| Homepage / general | "Abeam" | "Built for the way you fly" |
| Footer / about | "Abeam" | "Tools for general aviation" |

## Internal Linking

Every page should link to 2-3 related pages:

| Page Type | Link To |
|-----------|---------|
| Feature page | Related features, relevant persona page |
| Persona page | Features relevant to this persona, pricing |
| Homepage | Feature pages, roadmap, about |
| Blog post | Related features, other posts |

## "Now + Coming" Pattern for Persona Pages

When a persona page covers features at different stages of development (e.g., instructors page where some features ship in Q2 and others in Q3), split into explicit sections:

### Formula
```
## What you get now
[Features available at launch — present tense, confident]

## What's coming with [Product Name] ([Quarter Year])
[Features under development — future tense, with timeline]
```

### Rules
- Always lead with what's available NOW — don't bury real features under "coming soon" items
- Use clear visual separation (headings, badges, or dividers) between now and coming
- "Now" section uses present tense: "Track your currency automatically"
- "Coming" section uses future tense with specific timeline: "Coming Q3 2026"
- This pattern is especially important for the Instructors page (Abeam Pilot ships Q2, Abeam Instruct ships Q3) and Students page (some features depend on school adoption)

### Example (Instructors)
> **What you get now (Abeam Pilot)**
> Digital logbook for tracking instruction hours, currency tracking including CFI REED, mobile access
>
> **Coming with Abeam Instruct (Q3 2026)**
> Student CRM, ACS progress tracking, digital endorsements, structured debriefs

---

## Progress Disclosure Language

When discussing features at various stages:

| Stage | Language Pattern | Example |
|-------|-----------------|---------|
| Shipped | Present tense, factual | "Abeam tracks your currency automatically" |
| In current release | Present tense | "Log flights on your iPhone, iPad, and the web" |
| Building now (this quarter) | "Launching [timeframe]" | "Launching Summer 2026" |
| Next quarter | "Coming [Quarter Year]" | "Coming Q3 2026" |
| Planned (2+ quarters out) | "On our roadmap" | "On our roadmap for Q4 2026" |
| Aspirational / no timeline | "We're exploring" | "We're exploring maintenance tracking" |

---

## Content Hub (/learn + /whats-new)

The marketing site has two content areas:

### /learn — Article Library

All long-form content lives here. Four categories, filterable via client-side pills:

| Category | Content Type | Examples |
|----------|-------------|---------|
| Tutorials | How-to guides, migration guides | "Migrate from ForeFlight," "Review Auto-Generated Entries" |
| What's New | Feature announcements, release articles | "Introducing Scheduling" |
| Company | Behind-the-scenes, roadmap, updates | "Introducing Abeam" |
| User Stories | Testimonials, case studies, pilot profiles | (future) |

### /whats-new — Release Timeline

A YNAB-inspired timeline of releases. NOT an article collection — it's a structured product page that links OUT to articles, videos, feature walkthroughs, and demos. Each entry has: date, platform badges (Web/iOS), headline, description, highlights, and action links.

A feature launch might produce:
- A What's New timeline entry (structured card)
- A tutorial in /learn/tutorials/ ("How to use the new feature")
- A blog post in /learn/ with category "What's New"

The timeline entry links to all of these.

### Content Copy Rules
- Tutorial titles: imperative or "How to..." — "How to Migrate Your Logbook from ForeFlight"
- Blog posts: descriptive — "Introducing Scheduling for Flight Schools"
- What's New entries: short, feature-focused — "January Platform Update"
- All content should have keyword-rich `seoTitle` and `seoDescription` frontmatter for search
