# Versioning Notes

This project is tracked in local git. Keep changes small and commit after each meaningful design/content milestone.

## HTML snapshots

Before major rewrites, copy the current `index.html` into `versions/` with a descriptive name.

Current snapshots:

- `versions/index-premium-obituary-baseline-20260731.html` — premium memorial page using the supplied watercolor hero portrait, before QR-code tribute concert revisions.

## Git workflow

```bash
git status
git add .
git commit -m "Describe milestone"
```

Use git commits for real version history; use `versions/` only for human-friendly HTML snapshots that are easy to open directly.
