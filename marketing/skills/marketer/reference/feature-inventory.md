# Feature Inventory

Stable product facts for Abeam. Feature-level details are now derived from the product pipeline (see product-knowledge.md); this file captures durable product structure, pricing, platform availability, and positioning constraints.

**Last updated:** 2026-03-25 (pre-launch)
**Launch target:** Late June 2026

## Product Line

Abeam has two products at different stages:

**Abeam Pilot** (Free — launching Q2 2026)
The pilot app. Free for all pilots, forever. The logbook will always be free — this is not a trial. Key capabilities:
- Digital logbook with offline-first sync (iOS)
- Currency tracking with automatic expiry reminders
- Training progress with XP-based milestones and goal completion
- Live METAR weather on dashboard
- Document management (certificates, medicals, endorsements)
- Passkey authentication (passwordless sign-in)
- Built-in regulatory references (FARs, AIM)
- Digital hangar for aircraft management

**Abeam Instruct** (Paid, separate app — launching Q3-Q4 2026)
A dedicated app for instructors. Not an add-on or upgrade to Abeam Pilot — it's an independent product. Student management, digital endorsements, resource sharing, CRM, debrief workflows. A CFI would use both Abeam Pilot (for their own logbook) and Abeam Instruct (for managing students).

## Platform Availability

- **iOS** (iPhone and iPad): Yes — includes offline-first sync (works without connectivity)
- **Web**: Yes — requires connectivity (no offline mode)
- **Android**: No. Long-term roadmap, likely tied to European market expansion. Do not mention Android availability in marketing copy. Be honest if asked: "It's on the roadmap but not available yet."

"Works on your iPhone, your iPad, and the web" — accurate.
"Works on every device" — not accurate.
"Works offline on your iPhone and iPad" — accurate.
"Works offline on every platform" — not accurate (web requires connectivity).

## Pricing

**Abeam Pilot:** Free for individual pilots — forever. The logbook will always be free. No hour limits. No credit card required. This is not a trial or freemium bait. Future features outside the logbook may have costs, but the core pilot logbook is permanently free.

**Abeam Instruct:** Paid, pricing TBD. Separate app. Positioned to be affordable for CFIs building hours on thin margins. "Less than a single ground lesson."

**Abeam for schools:** Pricing TBD. Transparent — no "talk to sales" required. Monthly, no contracts.

## Brand Hierarchy

- **Highland Software** — the company (legal entity)
- **Abeam** — the brand and platform
- **Abeam Pilot** — the free pilot product (logbook, currency, aircraft)
- **Abeam Instruct** — the separate paid instructor app

The web app is "Abeam" and houses all products. Feature pages reference specific products ("Abeam Pilot," "Abeam Instruct"). The brand name in general contexts is just "Abeam."

## Origin Story

Abeam is built by people who love flying, in Colorado, because the existing tools weren't good enough. The product comes from genuine frustration with the fragmented, outdated tools available to GA pilots. This is a strength — use it naturally.

"Made in Colorado by people who love flying."
"Made at the airport, not in a boardroom."

## What NOT to Claim

- No Android app exists. Don't imply it does.
- Abeam Instruct is not launched yet. Don't describe instructor features as available.
- No flight planning features (that's ForeFlight's territory, not ours).
- No ADS-B integration or synthetic vision.
- Abeam is not an EFB. It's a logbook and pilot management platform.
- Don't compare the product to ForeFlight as a direct competitor — they solve different primary problems.
- No field-level conflict resolution. Sync uses whole-record last-write-wins. Do not claim "smart merge," "field-level merge," or "conflict resolution UI."
- Web app does not work offline. Only iOS has offline-first sync.
- Do not claim "real-time collaborative editing" — this is a single-pilot logbook.
- **No "founding partner" language.** Do not reference "founding partners," "founding partner program," "preferred pricing," or "early adopter pricing." This program has been retired. Use "Join the Waitlist" as the primary CTA.
- **Abeam Instruct is not an "add-on" or "upgrade."** It's a separate paid app. Do not say "upgrade to Instruct" — a CFI uses both Pilot and Instruct as independent products.

## Updating This File

After each release, update this file with:
1. New products or tiers that ship (move from "planned" to launched)
2. Updated pricing if it changes
3. Platform availability changes
4. Any positioning constraints added or removed

Feature-level changes should be captured via the product pipeline (product-state.jsonl) rather than edited here.
