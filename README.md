# AI Team in 3 Days — Show Notes Site

Companion show-notes site for the **AI Team in 3 Days** course inside the [AI Business Growth Academy](https://academy.trulyauthenticmarketing.com).

🔗 **Live:** https://ai-team-in-3-days-show-notes.vercel.app

## What this is

A simple TAM-branded link-tree landing page that serves as:

- **Show notes from Chris's videos** — drop the URL in your YouTube descriptions, viewers click through to the full lessons
- **A quick-jump menu during recording** — Chris hits each day-card on camera while live-streaming
- **A persistent landing page** for anyone who wants to revisit the course material

## Routes

| URL | What it is |
|---|---|
| `/` | TAM-branded landing — link tree with Day 1/2/3 cards + resources |
| `/day-1.html` | Day 1 master-slides deck (4 lessons, 30 slides) |
| `/day-2.html` | Day 2 master-slides deck (3 lessons, 22 slides) |
| `/day-3.html` | Day 3 master-slides deck (3 lessons, 22 slides) |

Each deck is a single self-contained HTML file (master-slides format: paper typography + isometric scenes + scroll-snap navigation).

## Hosting

**Vercel** (auto-deploys from GitHub on every push to `main`).

- **Production URL:** https://ai-team-in-3-days-show-notes.vercel.app
- **Project:** `keepinitgreen93s-projects/ai-team-in-3-days-show-notes`
- **Build:** static, no framework — Vercel auto-detects raw HTML files at root

To trigger a redeploy: edit any file → `git commit` → `git push origin main`. Vercel rebuilds + deploys in ~10 sec.

## Where the source lives

- **This repo (`keepinitgreen93/ai-team-in-3-days-show-notes`)** is the version-controlled source for the show-notes site itself
- **The decks (`day-1.html`, `day-2.html`, `day-3.html`) are duplicated here** from the source-of-truth course folder at `Business Success Coach/programs-courses/ai-business-growth-academy/3-day-ai-hires-sprint/decks/`. When the decks are edited there, copy them to this repo + push.
- **The skills + templates** (Brain Builder, Chief of Staff, Agent Map, etc.) are NOT here — those live in [keepinitgreen93/ai-team-in-3-days](https://github.com/keepinitgreen93/ai-team-in-3-days) (the public Claude Code marketplace + git-clone-able templates).

## Sync workflow

When the decks update in the main course folder:

```bash
SRC="C:/Users/Gem en Eye/Documents/Claude Code Workspace/Business Success Coach/programs-courses/ai-business-growth-academy/3-day-ai-hires-sprint/decks"
cd ~/dev/ai-team-show-notes
cp "$SRC/day-1.html" "$SRC/day-2.html" "$SRC/day-3.html" .
git add -A && git commit -m "deck update from source" && git push
# Vercel auto-deploys in ~10 sec
```

## Custom domain

Currently served at the default `*.vercel.app` URL. To attach a custom domain (e.g., `firstthree.ai` or `aiteamin3days.com`):

1. Vercel dashboard → project → Settings → Domains → Add
2. Update DNS at the registrar to point at Vercel
3. Vercel auto-provisions SSL

## Course details

- **Course:** AI Team in 3 Days · 10 lessons across 3 days · ~3.5 hrs
- **Inside:** [AI Business Growth Academy](https://academy.trulyauthenticmarketing.com) — $1 trial · $97/mo
- **Demo client:** [Plant Based Tone](https://plantbasedtone.com) — Toni's wellness brand
- **Format:** Pre-recorded lessons + optional monthly live cohort kickoffs

## License

MIT — match the marketplace repo. Fork it, swap the brand, ship your own course site.

## About

Built by [Truly Authentic Marketing](https://trulyauthenticmarketing.com) for [Product Champ](https://productchamp.com) Academy members.
