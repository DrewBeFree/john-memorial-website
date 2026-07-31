# John Memorial Website — Workspace State

**Repo / Path:** `/home/drew/workspace/john-memorial-website/`  
**Source Materials:** `/mnt/data/Documents/12-john/` (source for memorial content, photos, site assets)  
**Website Project:** Dedicated workspace for developing and maintaining the public John memorial website (distinct from private investigation share at john.drewbefree.com)  
**Created:** 2026-07-31

## Current Status
- Project initialized per workspace standardization and now versioned with local git.
- Obituary text saved to `content/obituary.txt`.
- Premium public memorial website created at `index.html` using the supplied watercolor portrait as the hero image.
- Hero image copied to `assets/John.png` from WebUI attachment `/home/drew/.hermes/webui/attachments/93bf2a5a1914/John.png`.
- Current design direction: top-of-the-line, art-forward, warm editorial memorial site with polished typography, responsive layout, hero portrait, obituary, celebration details, donation information, and survivors section.
- New content direction: this will be a QR-code destination from a poster at a tribute concert for John at Ponce City Market in Atlanta.
- The July 8 memorial service is in the past; copy must not present it as an upcoming event.
- Include a prominent sincere thanks to David Collins Band and Shatoya.
- Include the memorial service video link: `https://vimeo.com/event/6037295/dece23c342?fl=so&fe=fs`.
- Create a slideshow experience using only curated public-safe images.
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
- Backlog created in `TASKS.md`.
- Immediate priorities: revise QR/concert-facing copy, thank David Collins Band and Shatoya, add Vimeo memorial service video link, build slideshow, curate public images.

## Verification
- `index.html` written successfully: 23,109 bytes after premium redesign and favicon link.
- `assets/John.png` exists and is a valid PNG: 1054 × 1405 RGB.
- `assets/favicon.svg` added and linked.
- Local HTML asset check passed: no missing local `src`/`href` references.
- Temporary local preview served successfully on `127.0.0.1:41731`; preview server was stopped after verification.
- Chrome headless screenshot captured at `preview-home.png`; visual inspection found no broken image, text overlap, or obvious contrast/layout problems.

## Next Steps / Open Items
- Implement the QR-code tribute concert revision from `TASKS.md`.
- Decide final domain/subdomain and hosting target.
- Curate public memorial content vs private investigation materials.
- Add photo gallery/slideshow section using curated public images from `memorial-photos/`.
- Consider adding tribute / guestbook functionality. If public submissions are needed, static HTML will require a small server/backend or third-party form service.
- Decide whether to keep this as static HTML or migrate into a framework before launch.
- Read STATE.md before any work; append changes after each session.

**Update this file after every session.**