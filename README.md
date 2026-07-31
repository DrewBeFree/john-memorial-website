# John Memorial Website

Premium public memorial website for John Fitzrobert Webb.

This project is separate from the private `john-share` investigation archive. It is intended for a public QR-code link on tribute materials, including the tribute concert at Ponce City Market in Atlanta.

## Current artifact

- `index.html` — static premium memorial landing page
- `assets/John.png` — hero watercolor portrait
- `assets/favicon.svg` — site icon
- `content/obituary.txt` — source obituary text
- `TASKS.md` — project task backlog

## Preview locally

```bash
python3 -m http.server 41731 --bind 127.0.0.1
# open http://127.0.0.1:41731/
```

## Important content rules

- This is a public memorial site, not the private investigation archive.
- Treat service details as historical/past event copy.
- Keep private/sensitive material out of the public site unless Drew explicitly approves it.
- Curate `memorial-photos/` carefully; `.private/` stays filesystem-only unless explicitly requested.
