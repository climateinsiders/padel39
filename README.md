# Padel39

Single-page video microsite for Padel39. A full-screen, scroll-snap video reel served from GitHub Pages.

**Live site:** https://climateinsiders.github.io/padel39/

## How it works

`index.html` is a self-contained page (inline CSS + JS, no build step). It plays eight
full-screen clips in a vertical scroll-snap reel, followed by a light "How we scale"
map slide and a contact panel: the video in view autoplays muted and loops, a global
sound toggle un-mutes the active clip, and progress dots track position. The map slide
carries a `light` class that flips the fixed header/dots to a dark treatment for legibility.

Everything is served from the repo root so the relative `<source src="...">` references
resolve on the same origin. **Do not move the videos into a subfolder** or the reel breaks.

## Files (all in repo root)

| File | Purpose |
|------|---------|
| `index.html` | The site |
| `padel39-logo-white.png` | White logo lockup, used in the header |
| `favicon.png` | Browser tab icon (arrow mark) |
| `us-map.svg` | US expansion map (phase-colored dots) for the "How we scale" slide |
| `place-to-be.mp4` | Panel 1 — hero clip |
| `amenities.mp4` | Panel 2 — club amenities ("the place to be in Austin") |
| `aerial.mp4` | Panel 3 — aerial view |
| `largest-club.mp4` | Panel 4 — largest padel club in Texas |
| `full-club.mp4` | Panel 5 — full club vibe |
| `sports-bar.mp4` | Panel 6 — sports bar |
| `tournaments.mp4` | Panel 7 — USA Padel 2000 tournament |
| `brand-collab.mp4` | Panel 8 — brand collabs |

Keep each `.mp4` under 100 MB (GitHub's hard limit for regular files). Git LFS is **not**
used, because GitHub Pages serves the LFS pointer file instead of the actual video.

## Deployment

Hosted on GitHub Pages from the `main` branch, root folder (`/`). Any push to `main`
redeploys automatically.
