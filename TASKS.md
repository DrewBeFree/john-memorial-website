# John Memorial Website — Tasks

Source of truth for the public John memorial website backlog.

## Immediate Priority

- [ ] Revise event copy for QR-code tribute concert context
  - The July 8 memorial service is in the past; do not present it as upcoming.
  - Position this site as the destination for people scanning a QR code from a poster at a tribute concert for John.
  - Mention the tribute concert at Ponce City Market in Atlanta.

- [ ] Add special thanks section
  - Thank David Collins Band prominently.
  - Thank Shatoya prominently.
  - Tone: warm, sincere, not corporate.

- [ ] Add memorial service video section
  - Include link to memorial service video: https://vimeo.com/event/6037295/dece23c342?fl=so&fe=fs
  - Decide whether to embed Vimeo iframe or use a polished outbound video card/button.
  - Ensure mobile QR visitors can open it easily.

- [ ] Create slideshow experience
  - Use curated public-safe images only.
  - Candidate source folder: `/mnt/data/Documents/12-john/memorial-photos/`.
  - Do not use `.private/` or evidence/investigation images without explicit approval.
  - Support mobile-first viewing for concert attendees.

## Design / UX

- [ ] Update hero and CTA hierarchy for concert visitors
  - Primary CTA: view slideshow / remember John.
  - Secondary CTA: watch memorial service video.
  - Keep obituary available, but lower priority than memorial/concert content.

- [ ] Add QR-code landing polish
  - Fast first load.
  - Clear above-the-fold message for people arriving from a poster.
  - Big touch targets.
  - Avoid heavy autoplay or anything disruptive at a live event.

- [ ] Add responsive slideshow controls
  - Previous / next buttons.
  - Swipe support if practical.
  - Pause/play if auto-advance is used.
  - Respect `prefers-reduced-motion`.

- [ ] Consider adding music/life sections
  - Highlight piano, drums, creativity, faith, and friendship.
  - Avoid filler; use only real copy or clearly marked draft copy.

## Content / Curation

- [ ] Curate public image set
  - Review available `memorial-photos/` assets.
  - Copy only approved public images into this repo under `assets/slideshow/`.
  - Keep originals untouched.

- [ ] Add captions if available
  - Names/dates/locations only if confirmed.
  - Otherwise use simple non-specific captions or no captions.

- [ ] Update obituary section wording
  - Preserve obituary text.
  - Change service details from event announcement to historical remembrance.
  - Keep donation information to The Extension.

## Launch / Deployment

- [ ] Choose final domain/subdomain
  - Options: separate subdomain or full domain.
  - Do not host as a subpath of the private `john-share` archive unless explicitly directed.

- [ ] Decide static vs server-backed features
  - Static HTML is enough for QR landing, obituary, slideshow, and video link.
  - Guestbook/tributes require a backend or trusted form service.

- [ ] Generate QR code once final URL is chosen
  - Use final production URL only.
  - Save QR asset in `assets/qr/`.
  - Test scan on phone before poster print.

- [ ] Production verification
  - Test desktop and mobile viewport.
  - Verify all links and images.
  - Verify Vimeo link opens.
  - Confirm no private/investigation material is exposed.

## Done / Completed

- [x] Create dedicated workspace project.
- [x] Add obituary source text.
- [x] Add supplied watercolor hero image.
- [x] Create premium first-pass static memorial landing page.
- [x] Initialize local git repository.
