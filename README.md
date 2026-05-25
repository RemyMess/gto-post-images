# gto-post-images

Public image host for GTO ecosystem social posts (LinkedIn, X, Threads, etc).

Each image is referenced from a draft in `gto_brain/departments/media/operations/drafts/` via the `imageSuggestion.filename` frontmatter field, and consumed by Buffer at publish time via the raw GitHub URL:

```
https://raw.githubusercontent.com/RemyMess/gto-post-images/main/<filename>
```

Pushes here are automated by `gto_brain/pipelines/publish/push-from-draft.js` — do not commit images manually unless you know what you're doing.

## File naming convention

`YYYY-MM-DD-<account>-<short-slug>.<ext>`

Examples:
- `2026-05-22-remy-x-equilibrium.png`
- `2026-05-23-remy-linkedin-hiring-auction.jpg`
- `2026-05-24-techgames-linkedin-recap.png`

This convention is enforced by the Content Writer bible (v2, §8.1) and mirrors the local draft frontmatter.

## Why a separate repo

The main `gto_brain` repo is private and contains internal operating context, brand strategy, and analytics. Public image-hosting for Buffer cannot live there. This repo is intentionally narrow: just images, public, append-only, indexed by filename.
