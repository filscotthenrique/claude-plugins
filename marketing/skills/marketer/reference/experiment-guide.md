# Abeam Experiment Memory

The experiment log tracks every marketing post, its performance, and what we learn from it. This is how Abeam builds institutional memory about what resonates with the pilot community.

## The experiment log file

The log is a CSV file stored at: `data/experiment-log.csv`

**Columns:**

| Column | Type | Description |
|--------|------|-------------|
| date | YYYY-MM-DD | Date published |
| platform | text | instagram, tiktok, reddit, linkedin, x, youtube, blog, email, app-store |
| content_type | text | feed-post, reel, story, comment, thread, video, short, article, newsletter, release-note |
| feature_highlighted | text | logbook, currency, metar, hangar, certificates, general, instructor, free-tier |
| tagline_or_angle | text | The hook or tagline used (quote the key line) |
| audience_target | text | student-pilot, private-pilot, cfi, school-owner, general |
| link | text | URL to the post (if public) |
| likes | number | Like/upvote count at time of logging |
| comments | number | Comment/reply count |
| shares | number | Share/retweet/repost count |
| saves | number | Save/bookmark count (Instagram, Reddit) |
| impressions | number | Reach/impressions if available |
| qualitative_notes | text | What worked, what didn't, notable comments, tone observations |

## How to log a post

When the user says "log this post" or provides performance data:

1. Read the existing `data/experiment-log.csv` (create it with headers if it doesn't exist)
2. Append a new row with all available data. Leave cells empty for unavailable metrics.
3. Always include `date`, `platform`, `content_type`, and `tagline_or_angle` at minimum.
4. Ask the user for qualitative notes — "anything notable about how this performed?"

## How to reference the log when generating new content

Before generating content, check the experiment log for relevant patterns:

1. **Same platform**: What's performed well on this platform before?
2. **Same feature**: If highlighting a specific feature, how did past posts about it perform?
3. **Same audience**: What angles resonated with this persona in the past?
4. **What to avoid**: Any angles or formats that consistently underperformed?

Mention relevant patterns briefly when presenting the draft: "METAR posts tend to get 2-3x engagement on Instagram, so I leaned into the weather dashboard angle."

## How to analyze patterns

When the user asks for a performance review or says "what's working":

1. Read the full `data/experiment-log.csv`
2. Analyze by these dimensions:
   - **By platform**: Which platforms get the most engagement per post?
   - **By feature**: Which product features generate the most interest?
   - **By angle/tagline**: Which messaging hooks land best?
   - **By content type**: Do reels outperform feed posts? Do comments outperform original posts?
   - **By audience**: Which persona-targeted content performs best?
3. Identify top performers and underperformers
4. Look for patterns: time of day, day of week, format, length
5. Recommend what to do more of and what to stop doing

Present findings as concrete recommendations, not just data summaries.

## Pattern tracking over time

As the log grows, watch for these compounding insights:

- **Feature resonance**: Which Abeam features are the community most excited about? This should influence product roadmap priority, not just marketing.
- **Platform fit**: Some messages work on Reddit but not Instagram, and vice versa. Don't cross-post blindly.
- **Audience response**: Student pilots may engage with different content than private pilots. Track this to inform audience targeting.
- **Seasonal patterns**: Aviation has seasonal cycles (spring = training season, summer = fly-ins, winter = ground school). Watch for engagement patterns tied to the flying calendar.
- **Competitor moments**: When ForeFlight raises prices or Pilotbase rebrands, does engagement spike on Abeam content? Track these external events.

## Starting the log

If the experiment log doesn't exist yet:

1. Create `data/experiment-log.csv` with the column headers above
2. If the user has any existing posts (even if no metrics), backfill what's available
3. Start logging from today — the value compounds over time

The log is most valuable after 4-6 weeks of consistent entries. Don't draw major conclusions from fewer than 10-15 data points.
