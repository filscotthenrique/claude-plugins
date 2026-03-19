---
description: Create an SEO blog post outline for Abeam
allowed-tools: Read, Write, Edit, Grep, Glob
argument-hint: [keyword or topic]
---

Create a structured blog post outline optimized for search.

**Before writing anything**, load the `marketer` skill by reading its SKILL.md, then read these data/reference files:
- `marketer/data/taglines.json` — for potential headlines and hooks
- `marketer/data/audience-profiles.json` — for the target reader's perspective
- `marketer/data/platform-specs.json` — for blog formatting best practices
- `marketer/reference/competitive-landscape.md` — for differentiation and comparison opportunities
- `marketer/reference/product-knowledge.md` — for accurate product details

**Gather these inputs** (ask if not provided in $ARGUMENTS):
1. **Target keyword or topic**: e.g., "best free pilot logbook app" or "how to track pilot currency"
2. **Content type**: comparison, how-to guide, listicle, opinion/thought leadership, or product feature deep-dive
3. **Target audience**: Which persona is the primary reader?
4. **Word count target**: Standard (1,000–1,500), deep-dive (2,000–2,500), or pillar (3,000+)

**Generate the outline:**

1. **Title options** (3): SEO-optimized, under 60 characters, include the target keyword
2. **Meta description**: 150–160 characters, compelling and keyword-rich
3. **Introduction** (100–150 words): Hook, problem statement, what the reader will learn
4. **Section breakdown**: H2 and H3 structure with:
   - Key points to cover in each section
   - Where to naturally mention Abeam (never forced — the content should be genuinely helpful)
   - Competitive differentiation opportunities (factual, not trashy)
   - Internal link opportunities to product pages or other posts
5. **Conclusion + CTA**: Summary and clear next step
6. **SEO notes**: Related keywords to include, potential featured snippet opportunity, internal/external linking strategy

**For comparison content** (e.g., "ForeFlight vs Abeam"):
- Be factual and fair about competitors (load `reference/competitive-landscape.md`)
- Include Abeam's limitations honestly — credibility matters more than spin
- Structure for featured snippet capture (tables, bullet comparisons)

**Output format:**
- Complete outline in markdown, ready to write from
- SEO notes section at the end
