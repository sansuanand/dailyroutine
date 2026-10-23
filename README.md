# Discipline Desk

Source for the [Discipline Desk](https://claude.ai/artifact/5T5d2EFUMrDgsitkw5eNuf) Claude artifact — a daily
discipline board with top-three priorities, non-negotiable habits, a focus timer, parking lot, evening review,
a five-week score heatmap, Google Calendar events and a Claude-built day plan.

## The big three

Every day has three must-dos, shown as tiles at the top. Together they're 40% of the daily score.

- **MCAT today**: that day's checklist from the [Mcat 2.0](https://claude.ai/artifact/82ydXA23NpzgnRDB2ggDci) plan
  (daily protocol, weekly UWorld / CARS / Anki targets, breaks, full-lengths, taper). The plan is copied into the
  `<script id="mcat-plan">` JSON block in `index.html`. When the MCAT plan changes, ask Claude to re-sync that block.
- **Morning case**: Claude writes one consulting case a day. The case type and industry rotate. You clarify,
  structure, do the math and give a recommendation, then get graded feedback.
- **RREB1 review**: a daily writing minimum (45 min by default), words and notes, section status, deadline
  countdown (draft to Dr. Ishii Oct 30, final Nov 13) and a streak. Focus blocks set to "RREB1 review" add their
  minutes automatically.

- `index.html` — the page body as published (the artifact service adds the `<!doctype>`/`<head>` skeleton at publish time).
- `artifact.json` — the artifact URL and the runtime capabilities the page declares (`db`, `mcp` → Google Calendar
  `list_events`, `sample`, `user`).

## Updating the live artifact

Edit `index.html`, then ask Claude Code to republish it to the URL in `artifact.json`. Claude reads the live
version first and merges any changes made on claude.ai before publishing, so edits in either place aren't lost.
