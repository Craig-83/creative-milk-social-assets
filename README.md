# Creative Milk — social assets

Organic social creatives for **Creative Milk** (`creative-milk.com.au`), consumed by
`routines/presence-loop.md` in the `scale-ops` repo.

## Why this repo is public

Facebook fetches post images **server-side** from `raw.githubusercontent.com`. A private repo's
raw URLs require an auth token, which Facebook does not have and which would expire — the fetch
fails and the post is withheld. Every brand asset repo in this fleet is public for the same
reason (`Craig-83/scalesites-social-assets`, `scalepoint-social-assets`, `scalesites-au-social-assets`).

**This is a publish surface, not a working store.** Only creatives that are going out publicly
belong here. Master files, paid-ad creative, unreleased variants and anything client-connected
live in the **private** `Craig-83/creative-milk-assets`. Do not mirror that repo into this one.

## How the loop uses these

`presence-loop` builds an image URL as `<creative base> + <the queue row's Local Image Path>`,
fetches it, and only sets the row's Image URL on a **real HTTP 200 with an image content-type**.
A 404 leaves the row untouched and unpublished — it never guesses a URL. So the filename in the
Notion row must match the filename here **exactly**.

Creative base:
```
https://raw.githubusercontent.com/Craig-83/creative-milk-social-assets/main/
```

## What's here

Posts **11–52** of a 52-post series. Posts 1–10 were published between 16 June and 7 July 2026
from a manually scheduled batch and are deliberately **not** included — the series resumes at 11.

Filenames are `post<NN>_Line<A|B|C>_<slug>.jpg`, carried over unchanged from the source set so
the queue's `Local Image Path` values keep working:

- **Line A — Straight Talk**: photoreal cinematic surreal, animal-in-business-wear house style
- **Line B — Industry Spotlight**: dark minimal typographic, no people or animals
- **Line C — The Build**: as Line B, build/case-study framing

All are 4:5 portrait masters (1080×1350) with a central 1080×1080 safe zone, so the same frame
crops cleanly to square and landscape.
