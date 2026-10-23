# Discipline Desk

Source for the [Discipline Desk](https://claude.ai/artifact/5T5d2EFUMrDgsitkw5eNuf) Claude artifact — a daily
discipline board with top-three priorities, non-negotiable habits, a focus timer, parking lot, evening review,
a five-week score heatmap, Google Calendar events and a Claude-built day plan.

- `index.html` — the page body as published (the artifact service adds the `<!doctype>`/`<head>` skeleton at publish time).
- `artifact.json` — the artifact URL and the runtime capabilities the page declares (`db`, `mcp` → Google Calendar
  `list_events`, `sample`, `user`).

## Updating the live artifact

Edit `index.html`, then ask Claude Code to republish it to the URL in `artifact.json`. Claude reads the live
version first and merges any changes made on claude.ai before publishing, so edits in either place aren't lost.
