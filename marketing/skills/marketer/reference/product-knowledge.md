# Product Knowledge

How to determine what Abeam can do right now and what's coming.

## Where to Find Current Product State

| Source | Location | What It Tells You |
|--------|----------|-------------------|
| **Product state log** | `data/product-state.jsonl` | Append-only log of user-facing features, auto-maintained by `/finalize` |
| **What's New** | `web/apps/marketing/content/whats-new/` | User-facing release entries (YNAB-style timeline) |
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
| apple (AbeamSync) | Offline-First Sync | Works without connectivity, syncs when you're back |
| objectives, progress | Training Progress | XP bar, milestones, goal completion — see where you are |
| passkeys, webauthn | Passkey Login | Passwordless, secure, one tap to sign in |

## What NOT to Claim (Durable Rules)

These apply regardless of what ships:
- No Android app exists. "iPhone, iPad, and the web" is accurate.
- Abeam is NOT an EFB. It's a logbook and pilot management platform.
- Do NOT compare directly to ForeFlight — they solve different primary problems.
- Only claim features that have shipped or are in the current release candidate.
- For "coming soon" features, reference the roadmap ticket status and use future tense with a timeline.
- Do NOT claim flight planning features (ForeFlight's territory).
- No ADS-B integration or synthetic vision.
- **No field-level conflict resolution.** The sync system uses whole-record last-write-wins. Do NOT claim "field-level merge," "smart conflict resolution," "conflict resolution UI," or "three-way merge." The system is simple: upload first, then download. Last write wins at the record level.
- **No "conflict-free" claims.** Conflicts are handled by last-write-wins, not eliminated. Do not say "never lose data" — say "your data syncs automatically" or "works offline, syncs when you're back."

## AbeamSync — Offline-First Sync (Updated 2026-03-25)

AbeamSync is the offline-first data layer for Abeam Pilot on iOS. It is fully implemented (Phases 1-3 complete).

### What it does (marketing-safe claims)
- **Offline logbook**: Create and edit logbook entries without connectivity. They sync automatically when you're back online.
- **Delta sync**: Only downloads what changed since last sync — not the entire logbook every time. Important for pilots at remote airfields on cellular.
- **Background sync**: Keeps data fresh even when the app is backgrounded (via iOS BGTaskScheduler).
- **Batch upload**: Create 50 entries offline, they all sync in one HTTP request on reconnect.
- **Transparent sync status**: Per-row sync status indicators in the logbook list. Pilots see a pending-upload icon on entries waiting to sync. No other aviation app shows this.
- **Offline banner**: Clear indicator when the app is disconnected.
- **Manual sync**: "Sync Now" button in Data & Sync settings for pilots who want explicit control.
- **CFI signature integrity**: SHA-256 hash verification ensures signed entries haven't been tampered with. Compliant with AC 120-78B electronic signature guidance.

### Marketing angles
- **Differentiator**: "Your logbook works at 8,000 feet with no cell service" — no competing logbook app offers transparent offline sync with per-row status indicators.
- **Trust angle**: Entry hash verification means CFI signatures are cryptographically verifiable. This matters for DPEs and FSDO audits.
- **Performance**: Delta sync means the app is fast even on slow connections. Only changes download, not the whole logbook.
- **Pilot autonomy**: "Log the flight before the engine cools, sync when you're back in range."

### What NOT to claim about sync
- No field-level conflict resolution (see "What NOT to Claim" above)
- No real-time collaborative editing (this is a single-pilot logbook, not Google Docs)
- No web offline support (offline is iOS only; web requires connectivity)
- Do not say "never lose data" — say "works offline, syncs when you're back"

## Launch Scope Constraints (Updated 2026-03-25)

These clarify what is and is NOT available in the Abeam Pilot launch (Q2 2026):

**Scheduling is a school/club feature, not a pilot feature.** Individual pilots do not have a standalone booking flow. Scheduling only exists in the context of a flight school or club using Abeam. Do not claim "book lessons" or "schedule flights" in pilot-facing copy unless qualified with "at schools using Abeam."

**Document management IS a launch feature.** Pilots can upload and manage certificates, medicals, endorsements, checkout cards, and training documents. Use this in pilot-facing copy. "Your certificates and training docs, organized" is accurate.

**The homepage leads with pilot messaging, not flight school ops.** The brand tagline is "Built for the way you fly." The homepage showcases: (1) Digital Logbook, (2) Currency Tracking, (3) Document Management. Flight school features (scheduling, fleet management) are secondary — linked from feature pages, not the hero.

**Avoid "OS" and "operating system" in marketing copy.** The brand voice guide explicitly lists these as taglines to avoid — "too techy for this audience."

**Offline-first is an iOS feature, not a web feature.** The AbeamSync offline-first architecture only applies to the iOS app. The web app requires connectivity. Do not claim "works offline on every device" — qualify with "on your iPhone and iPad."

**Training progress is a shipped feature.** XP-based progress tracking, training goals (PPL, IR, CPL), milestone markers, and goal completion celebrations are live on both iOS and web. "See your progress toward your next certificate" is accurate now.

**Passkey login is a shipped feature.** WebAuthn/passkey authentication works on iOS and web. "Sign in with a tap" is accurate. Do not call it "biometric login" — passkeys may use biometrics but that's a device-level detail, not an Abeam feature.

**"Founding partner" program is retired.** All founding partner language, preferred pricing, and early adopter pricing references have been removed from the marketing site. Do not resurrect this language in any new content. The CTA is "Join the Waitlist."

**The logbook is free forever.** Not a trial, not freemium bait. The logbook specifically will always be free for individual pilots. Other features introduced in the future (instructor tools, school management) may have costs, but the core pilot logbook is permanently free. Be precise: "Free for pilots — forever" when discussing the logbook. Don't extend this claim to all Abeam products.
