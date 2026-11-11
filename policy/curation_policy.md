# Talk Digest Curation Policy

A talk is **published** as a digest only when all of the following hold:

1. A transcript is available (prefer the archived transcript linked from the intake record).
2. The transcript has at least 120 words (whitespace-separated tokens).
3. The transcript mentions at least one keyword of the declared track (case-insensitive substring).

Otherwise the talk is **rejected**. The reason is the first failing rule, in order:

- `transcript_unavailable` - no transcript could be obtained.
- `insufficient_content` - fewer than 120 words.
- `off_topic` - enough words but no keyword of the declared track.

## Track keywords

| Track | Keywords |
|-------|----------|
| `ai-ml` | neural, model, training, inference, transformer, dataset |
| `web-dev` | javascript, browser, frontend, react, css, accessibility |
| `infra` | kubernetes, deployment, container, pipeline, cloud, observability |
| `security` | vulnerability, attack, encryption, authentication, threat |

## Publishing

- Digest file: `digests/<submission_id>.md`, with front matter fields
  `submission_id`, `video_url`, `title`, `track`, `word_count`, followed by
  `## Summary` and a `## Key takeaways` list of at least three bullets.
- Curation report: `reports/curation_report.json`.
- Rejected talks with priority `high` get a follow-up issue titled
  `Follow-up: <submission_id>`.
