# YouTube Viral SEO — an agentic AI skill

An AI-agent skill for creators building a **career** on YouTube, not just uploading to it. At its core it does the work of a growth analyst on every video: it **analyzes the video, scores it, and hands back a complete upload pack** — ranked titles, an SEO description, tags and hashtags — tuned to how the YouTube algorithm actually promotes content: click-through rate × average view duration on long-form, and swipe-through rate, percentage viewed and loopability on Shorts.

Around that core, the skill runs the whole career system: channel foundations, a content pipeline that never starts from a blank page, growth engines beyond single videos, a monetization path, channel protection, and the sustainability habits that keep creators from quitting in the flat months.

No view promises, no income promises. What it maximizes is the odds.

## What it does

1. **Watches the video first.** Probes the file, samples frames densely (every 2 seconds on a Short, every 20 seconds plus scene changes on long-form), and transcribes the audio — so every claim in the SEO copy matches what the video actually says and shows, and pacing is only ever judged from frames actually sampled.
2. **Audits the hook and retention.** Shorts are judged on the first 3 seconds; long-form on the first 30. It maps open loops, pattern interrupts, dead stretches, and whether the ending loops (Shorts) or chains into the next video (long-form).
3. **Scores it.** A five-part scorecard — Hook, Curiosity gap, Retention structure, Payoff, Shareability — each with evidence, plus the **top 3 fixes tied to exact timestamps**.
4. **Writes titles that earn the click.** Generates 8–10 candidates, ranks them, and recommends one + two alternates. Keywords front-loaded, one idea per title, nothing the video can't back up.
5. **Builds the description for search and suggested.** Keyword in the first sentence, payoff expansion, chapters on long-form (first at 0:00, each at least 10 seconds), and the channel's standing block and hashtags.
6. **Spends the tag budget in the right order.** Primary keyword, close variants, long-tail question forms, niche terms, series/channel terms — inside YouTube's 500-character tag limit. Up to three hashtags display above the title (the skill budgets all three), and more than 15 in total gets every hashtag ignored — the skill counts before it finishes.
7. **Directs the thumbnail / cover frame** and recommends a **posting window** based on the audience's geography, plus a ready-to-post **pinned comment**.

## Output

A single paste-ready upload pack, saved beside the video:

- Recommended title + 2 alternates
- Full description
- Tag list (comma-separated)
- Hashtag line
- Pinned comment
- Thumbnail direction (long-form) or cover frame pick (Shorts)
- End-screen spec — which video it points to, and from what second (long-form)
- Playlist placement
- Community post draft (for channels with Posts access)
- Posting window — with the scorecard and top fixes above it

## Example (illustrative)

Input: a 52-second faceless history Short — *"What if the Library of Alexandria never burned?"* — narration transcript + video file supplied.

Scorecard (excerpt — scores relative to the channel's own recent Shorts):

| Axis | Score | Evidence |
| --- | --- | --- |
| Hook | 6/10 | The boldest line ("We lost 700 years of science in one night") lands at 0:09; the first 3 seconds are a slow fade-in. |
| Curiosity gap | 8/10 | Title asks a question the video genuinely answers at 0:31. |
| Retention structure | 7/10 | New beat every ~4s; one dead stretch 0:22–0:29 with no visual change. |
| Payoff | 8/10 | The scroll-count reveal is specific and sendable. |
| Shareability | 7/10 | "Send this to someone who loves books" writes itself. |

Top fix: move the 0:09 line to 0:00 and open on the burning-shelf frame — the hook *is* the video's best line; it is just buried.

Titles, ranked:

1. **What If the Library of Alexandria Never Burned?**
2. One Fire Erased 700 Years of Science
3. The Night Humanity Lost Its Memory

The full pack (description, tags within budget, three hashtags, pinned comment — *"Which lost invention do you wish had survived?"* — cover frame, posting window) follows the Output shape above.

## The career system around the video

- **Channel foundations** — a three-legged niche test (demand × differentiation × a hundred videos of depth), the one-viewer promise, complete channel identity (including a banner that survives the phone crop), and a persistent `channel-profile.md` the agent maintains across sessions.
- **A content system, not random uploads** — two or three content pillars, an idea bank fed by comments, search demand and niche outliers, deliberate series design, a holdable cadence, and batched production with a finished-video buffer.
- **Growth beyond single videos** — the Shorts/search → series → returning-viewer funnel, balancing the search and browse engines, cross-platform repurposing, right-sized collaborations, and community habits that make viewers return on purpose.
- **Monetization** — the Partner Program gates as milestones, a revenue stack ordered by what a small channel can actually reach (ads → affiliates → products → sponsors), sponsor readiness with provable numbers, and honest career-money hygiene.
- **Protection** — copyright and Content ID as a hard system, the reused-content bar faceless and AI-assisted channels must clear, and account security (2FA, permissions, phishing, backups) treated like the business it is.
- **Sustainability** — a monthly career review ritual, slump diagnosis instead of panic pivots, evidence thresholds for changing direction, and burnout protection as career infrastructure.

## Guardrails

- **Never writes metadata the video doesn't support.** Misleading titles and tags violate YouTube policy, destroy retention, and train the algorithm to bury a channel.
- **Never advises buying subscribers, views, watch hours or engagement** — botted or incentivized traffic violates platform terms, poisons every later analytics decision, and can end monetization permanently.
- **No engagement bait, no keyword stuffing**, anywhere.
- **Scores are not view predictions** — they compare the video against what the algorithm rewards, and the skill says so plainly.
- If the video itself is weak, the skill says that too — and names the one change that would matter most, instead of hiding it under strong SEO.

## Install

This is a [Muse](https://muse.ai)-style agent skill. Copy this folder into your agent's custom skills directory:

```
~/workspace/custom-skills/youtube_viral_seo/
├── SKILL.md
└── skill.yaml
```

Then ask your agent to use it: *"Run the YouTube Viral SEO skill on this video"* — or just hand it a video and ask for an upload pack. Other agent frameworks use different skill folders; the two files are self-contained, so place them wherever your agent loads skills from.

## Requirements for full video analysis

- `ffprobe` / `ffmpeg` (metadata + frame grabs)
- A whisper transcription setup (e.g. faster-whisper) — optional; the skill also works from a script or transcript alone, and marks the analysis as script-based when it never saw the cut.

## Files

| File | Purpose |
| --- | --- |
| `SKILL.md` | The skill itself — the full analysis and packaging playbook the agent follows. |
| `skill.yaml` | Skill descriptor (name, title, description, category). |
| `references/niches.md` | The niche catalog: 26 families and every major sub-niche, with relative RPM tier, competition and faceless viability. |
| `README.md` | This file. |
| `LICENSE` | MIT license. |

## License

MIT — see [LICENSE](LICENSE).
