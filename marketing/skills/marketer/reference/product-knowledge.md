# Product Knowledge

How to determine what Abeam can do right now and what's coming.

## Where to Find Current Product State

| Source | Location | What It Tells You |
|--------|----------|-------------------|
| **Product state log** | `data/product-state.jsonl` | Append-only log of user-facing features, auto-maintained by `/finalize` |
| **Changelog** | `web/apps/marketing/content/drafts/changelog/CHANGELOG.md` | Full technical changelog with scope prefixes |
| **Recent commits** | `git log --since="3 months ago" --oneline --grep="feat"` | Raw feature commit history |
| **Roadmap tickets** | `.claude/docs/roadmap/` | What is planned, in progress, or completed |
| **Extraction artifacts** | `.claude/skills/content-generate/templates/extraction-artifact.schema.json` | JSON schema for structured feature data |

## The Translation Filter

Not everything in the changelog is marketing-worthy. Apply this filter:

1. **Is it user-facing?** Internal refactors, test improvements, CI changes → skip
2. **Does a pilot care?** Database optimization → no. Faster logbook loading → yes
3. **Can we demo it?** If there's no visible UI or behavior change, it's not marketing copy

## Scope-to-Feature Mapping

| Git Scope | Marketing Feature Name | Marketing Angle |
|-----------|----------------------|-----------------|
| logbook | Digital Logbook | Speed, simplicity, Part 61 support |
| currency | Currency Tracking | Never wonder if you're current |
| aircraft | Digital Hangar | Every tail number, every detail |
| scheduling | Smart Scheduling | Real-time, conflict detection |
| metar, weather | Live Weather | Home airport METAR on dashboard |
| certificates | Certificate Storage | Upload once, access anywhere |
| references | Built-in References | FARs, AIM in your pocket |
| endorsements | Digital Endorsements | Stored properly, always accessible |
| documents | Document Management | Certificates, medicals, training docs — upload once, access anywhere |
| members | Member Management | Invite system, roles, profiles |

## What NOT to Claim (Durable Rules)

These apply regardless of what ships:
- No Android app exists. "iPhone, iPad, and the web" is accurate.
- Abeam is NOT an EFB. It's a logbook and pilot management platform.
- Do NOT compare directly to ForeFlight — they solve different primary problems.
- Only claim features that have shipped or are in the current release candidate.
- For "coming soon" features, reference the roadmap ticket status and use future tense with a timeline.
- Do NOT claim flight planning features (ForeFlight's territory).
- No ADS-B integration or synthetic vision.

## Launch Scope Constraints (Updated 2026-03-19)

These clarify what is and is NOT available in the Abeam Pilot launch (Q2 2026):

**Scheduling is a school/club feature, not a pilot feature.** Individual pilots do not have a standalone booking flow. Scheduling only exists in the context of a flight school or club using Abeam. Do not claim "book lessons" or "schedule flights" in pilot-facing copy unless qualified with "at schools using Abeam."

**Document management IS a launch feature.** Pilots can upload and manage certificates, medicals, endorsements, checkout cards, and training documents. Use this in pilot-facing copy. "Your certificates and training docs, organized" is accurate.

**The homepage leads with pilot messaging, not flight school ops.** The brand tagline is "Built for the way you fly." The homepage showcases: (1) Digital Logbook, (2) Currency Tracking, (3) Document Management. Flight school features (scheduling, fleet management) are secondary — linked from feature pages, not the hero.

**Avoid "OS" and "operating system" in marketing copy.** The brand voice guide explicitly lists these as taglines to avoid — "too techy for this audience."
