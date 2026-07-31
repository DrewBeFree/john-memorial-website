# John Memorial Website — Workspace State

**Repo / Path:** `/home/drew/workspace/john-memorial-website/`  
**Source Materials:** `/mnt/data/Documents/12-john/` (source for memorial content, photos, site assets)  
**Website Project:** Dedicated workspace for developing and maintaining the public John memorial website (distinct from private investigation share at john.drewbefree.com)  
**Created:** 2026-07-31

## Current Status
- Project initialized per workspace standardization and versioned with local git.
- Obituary text saved to `content/obituary.txt`.
- Premium public memorial website created at `index.html` using the supplied watercolor portrait as the hero image.
- Hero image copied to `assets/John.png` from WebUI attachment `/home/drew/.hermes/webui/attachments/93bf2a5a1914/John.png`.
- Current design direction: top-of-the-line, art-forward, warm editorial memorial site with polished typography, responsive layout, hero portrait, QR-code concert context, slideshow, memorial service video link, obituary, donation information, and survivors section.
- New content direction implemented: this is a QR-code destination from a poster at a tribute concert for John at Ponce City Market in Atlanta.
- The July 8 memorial service is treated as a past event; copy no longer presents it as upcoming.
- Prominent sincere thanks added for David Collins Band and Shatoya.
- Memorial service video link added: `https://vimeo.com/event/6037295/dece23c342?fl=so&fe=fs`.
- First-pass slideshow experience added with hero portrait + text slides. Real photo slides are pending because `/mnt/data/Documents/12-john/memorial-photos/` currently contains only `.gitkeep`.
- This is intended to be a separate public site on a different subdomain or possibly its own full domain; do not treat it as a subpath of the private `john-share` investigation archive.
- Source materials (memorial-photos, evidence-photos, static HTML scaffolding) exist in `/mnt/data/Documents/12-john/`.
- `memorial-photos/` and `.private/` curation rules apply: keep sensitive/private items filesystem-only unless explicitly requested for public site.
- Related existing: `john-share` (private PIN-protected archive site), `memorial-project` (stub).

## Versioning
- Local git repo initialized in `/home/drew/workspace/john-memorial-website/`.
- Back up `index.html` before major rewrites into `versions/` with descriptive names.
- Current HTML snapshot: `versions/index-premium-obituary-baseline-20260731.html` — premium memorial page before QR-code tribute concert revisions.
- See `VERSIONING.md`.

## Tasks
- Backlog maintained in `TASKS.md`.
- Completed: QR/concert-facing copy, David Collins Band and Shatoya thanks, Vimeo memorial service video card/link, first-pass slideshow shell, updated hero CTA hierarchy, historical memorial-service wording.
- Still open: curate public photo set, add final captions, choose launch domain/subdomain, generate production QR code.

## Verification
- `index.html` written successfully: 37,605 bytes after QR-code tribute concert revision.
- `assets/John.png` exists and is a valid PNG: 1054 × 1405 RGB.
- `assets/favicon.svg` added and linked.
- Local HTML asset check passed: no missing local `src`/`href` references.
- Content checks passed for: `Ponce City Market`, `David Collins Band`, `Shatoya`, Vimeo memorial service URL, `View photo slideshow`, and `Watch memorial service`.
- Temporary local preview served successfully on `127.0.0.1:41731`.
- Chrome headless screenshot captured at `preview-home-updated.png`; visual inspection confirmed tribute concert context and thanks are visible above the fold/lower hero area, with no obvious broken image, text overlap, or contrast problem.

## Next Steps / Open Items
- Curate public-safe real photos for slideshow. Current `memorial-photos/` folder has no usable images yet.
- Decide final domain/subdomain and hosting target.
- Generate QR code after final production URL is chosen.
- Consider adding tribute / guestbook functionality. If public submissions are needed, static HTML will require a small server/backend or third-party form service.
- Decide whether to keep this as static HTML or migrate into a framework before launch.
- Read STATE.md before any work; append changes after each session.

**Update this file after every session.**