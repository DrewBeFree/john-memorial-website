# John Memorial Website — Tasks

Source of truth for the public John memorial website backlog.

## Immediate Priority

- [x] Revise event copy for QR-code tribute concert context
  - The July 8 memorial service is in the past; do not present it as upcoming.
  - Position this site as the destination for people scanning a QR code from a poster at a tribute concert for John.
  - Mention the tribute concert at Ponce City Market in Atlanta.
  - Implemented in hero and tribute concert section.

- [x] Add special thanks section
  - Thank David Collins Band prominently.
  - Thank Shatoya prominently.
  - Tone: warm, sincere, not corporate.
  - Implemented in the Ponce City Market tribute concert card.

- [x] Add memorial service video section
  - Include link to memorial service video: https://vimeo.com/event/6037295/dece23c342?fl=so&fe=fs
  - Implemented as a polished outbound Vimeo video card/button rather than iframe embed, so QR/mobile visitors can open it reliably.
  - Ensure mobile QR visitors can open it easily.

- [x] Create slideshow experience
  - Functional slideshow section added with previous/next controls, dots, keyboard arrow support, and auto-advance.
  - Current slides use the hero portrait plus tasteful text slides because `/mnt/data/Documents/12-john/memorial-photos/` currently contains only `.gitkeep`.
  - Replace/add slides once public-safe photos are curated.

## Design / UX

- [x] Update hero and CTA hierarchy for concert visitors
  - Primary CTA: view photo slideshow.
  - Secondary CTA: watch memorial service video.
  - Obituary remains available but lower priority than memorial/concert content.

- [x] Add QR-code landing polish
  - Clear above-the-fold message for people arriving from a poster.
  - Big touch targets.
  - Avoided autoplay audio/video and disruptive behavior at a live event.

- [x] Add responsive slideshow controls
  - Previous / next buttons.
  - Dot navigation.
  - Keyboard arrow support.
  - Auto-advance every 7 seconds.
  - `prefers-reduced-motion` respected globally for CSS motion.

- [x] Consider adding music/life sections
  - Current cards highlight music, creativity, servant’s heart, and loyal friendship using obituary-based copy.

## Content / Curation

- [ ] Curate public image set
  - Review available `memorial-photos/` assets.
  - Current status: `/mnt/data/Documents/12-john/memorial-photos/` only contains `.gitkeep`, so there are no public photos to copy yet.
  - Copy only approved public images into this repo under `assets/slideshow/`.
  - Keep originals untouched.

- [ ] Add captions if available
  - Names/dates/locations only if confirmed.
  - Otherwise use simple non-specific captions or no captions.
  - Blocked until public image set exists.

- [x] Update obituary section wording
  - Preserved obituary text.
  - Changed service details from event announcement to historical remembrance.
  - Kept donation information to The Extension.

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
- [x] Implement QR-code tribute concert context.
- [x] Add David Collins Band and Shatoya thanks.
- [x] Add memorial service video link/card.
- [x] Add first-pass slideshow shell.
