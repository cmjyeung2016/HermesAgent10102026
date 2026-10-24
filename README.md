# Hermes Agent — Todo List

A modern, fully self-contained **Todo List** web app. One HTML file, zero
dependencies — open it in any browser and it works (data persists locally via
`localStorage`).

## Features

- **Add** tasks (Enter or the + button)
- **Mark done** with an animated checkbox
- **Delete** with a slide-out animation
- Filters: All / Active / Completed (with counts)
- Inline editing (double-click a task)
- Progress bar + completion percentage
- Light / dark theme (auto-detects system, manual toggle)
- Responsive + accessible (ARIA, focus states, reduced-motion support)

## Run locally

No build step — just open `index.html`:

```
open index.html      # macOS
xdg-open index.html  # Linux
```

## Deploy (GitHub Pages)

This repo ships a CI/CD workflow (`.github/workflows/deploy.yml`) that
auto-builds and deploys to GitHub Pages on every push to `main` (and can be
run manually). Pages is configured to use the "GitHub Actions" source.

> Public URL: https://cmjyeung2016.github.io/HermesAgent10102026/
