# Padel39

Single-page video microsite for Padel39. A full-screen, scroll-snap video reel served from GitHub Pages.

**Live site:** https://climateinsiders.github.io/padel39/

## How it works

`index.html` is a self-contained page (inline CSS + JS, no build step). It plays five
full-screen clips in a vertical scroll-snap reel: the video in view autoplays muted and
loops, a global sound toggle un-mutes the active clip, and progress dots track position.

Everything is served from the repo root so the relative `<source src="...">` references
resolve on the same origin. **Do not move the videos into a subfolder** or the reel breaks.

## Files (all in repo root)

| File | Purpose |
|------|---------|
| `index.html` | The site |
| `padel39-logo-white.png` | White logo lockup, used in the header |
| `favicon.png` | Browser tab icon (arrow mark) |
| `place-to-be.mp4` | Panel 1 — hero clip |
| `aerial.mp4` | Panel 2 — aerial view |
| `largest-club.mp4` | Panel 3 — largest padel club in Texas |
| `full-club.mp4` | Panel 4 — full club vibe |
| `sports-bar.mp4` | Panel 5 — sports bar |

Keep each `.mp4` under 100 MB (GitHub's hard limit for regular files). Git LFS is **not**
used, because GitHub Pages serves the LFS pointer file instead of the actual video.

## Deployment

Hosted on GitHub Pages from the `main` branch, root folder (`/`). Any push to `main`
redeploys automatically.
