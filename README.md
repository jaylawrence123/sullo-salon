# Sullo Salon & Day Spa

Static HTML/CSS/JS website. Deploy to Netlify via master branch.

**Local:** `C:\Users\Jay\Documents\sullo-salon`
**GitHub:** https://github.com/jaylawrence123/sullo-salon
**Live:** https://sullo-salon.netlify.app (master branch, auto-deploys)
**Work branch:** `dev` — never push directly to master without client approval

---

## Stack

- One `index.html` per page — all CSS inline in `<style>`, all JS inline in `<script>`
- Font: **Satoshi** — self-hosted woff2 in `fonts/` (400/500/700/900). NOT from CDN.
- No frameworks, no build step, no dependencies

---

## Theme Toggle

Pink/classic toggle in nav, all pages.

- Button: `[data-theme-toggle]`
- Attribute: `data-theme="pink"` on `<html>`
- Persistence: `localStorage` key `sullo-theme`
- All pink overrides scoped to `[data-theme="pink"]`
- **Rule:** `.nav-right .theme-toggle` must be `display:inline-flex` in base CSS on every page — never `display:none`. Toggle is visible in the nav on mobile AND desktop.

---

## Pages

| Page | Path | Status |
|------|------|--------|
| Home | `/` | Done |
| About | `/about-us/` | Done |
| Our Team | `/our-team/` | Done |
| Gallery | `/gallery/` | Done |
| Contact | `/contact-us/` | Done |
| Work With Us | `/work-with-us/` | Done |
| Hair | `/hair/` | Done |
| Color &amp; Balayage | `/color/` | Done |
| Hair Extensions | `/hair-extensions/` | Not started |
| Facials | `/facials/` | Not started |
| Makeup | `/makeup/` | Not started |
| Nails | `/nails/` | Not started |
| Waxing | `/waxing/` | Not started |

---

## Homepage Sections

| # | Section | Status | Pink Mode |
|---|---------|--------|-----------|
| 1 | Hero (announce bar + nav + video + wordmark + sticky bar) | Done | Done |
| 2 | Services (6 square + 1 full-width tiles) | Done | Done |
| 3 | Marquee | Done | Done |
| 4 | Why Sullo (video bg + frosted glass stats) | Done | Done |
| 5 | The Work (8 gallery photos) | Done | Done |
| 6 | Reviews (2 real Google reviews) | Done | Done |
| 7 | Team (Meet the team preview) | Done | Done |
| 8 | Visit (map + NAP + hours) | Done | Done |
| 9 | Footer CTA (photo bg, frosted CTAs) | Done | Done |
| 10 | Footer | Done | Done |

---

## Footer Pattern (apply to all pages)

- Small sullo wordmark centered at top (`.footer-logo-wm` with `.footer-logo-sm`/`.footer-logo-lg`)
- Tagline: "Salon · Day Spa · Est. 1986"
- Info strip (centered column stack):
  - **Explore:** links in a horizontal row
  - **Visit:** address line 1, phone line 2
  - **Follow:** 4 SVG icons (Instagram / Facebook / Pinterest / Yelp)
- Large sullo wordmark: `clamp(4.5rem,25vw,9rem)` / `clamp(5.5rem,30vw,10rem)` — bone on ink, same as hero band
- "Salon · Day Spa" below wordmark
- Pink mode: wordmark turns `var(--pink)`
- Legal bar: copyright + Privacy + Designmynt
- **Font sizes are mobile-first; larger desktop sizes live in `@media (min-width: 768px)` only — never touch base sizes**

---

## Visit Section — Desktop Notes

- Left column: photo (420px fixed) + NAP block + pinned `.visit-book` CTA at bottom
- `.visit-nap` is `flex:1; flex-direction:column` — fills remaining left-column height
- `.visit-book` is `display:none` on mobile, `display:block` on desktop — full-width ink "Book an appointment →" pinned via `margin-top:auto`
- Pink mode: `.visit-book-btn` → pink bg, ink text
- Right column: map (`flex:1`) fills height; directions buttons hidden on desktop (`display:none`)

---

## Team Roster Pattern (`/our-team/`)

- **Owners (Heather + Matteo):** featured flex-row layout, alternating photo side, full bio, tags
- **Staff (7):** horizontal roster rows — 80×80 photo thumb + role/name column + tag pills
- No bio paragraphs on roster rows — tags communicate credentials
- Placeholder initials for Kelly Mitchell (KM), Jonathan Rivera (JR), Shannon (S)

---

## Contact Page Pattern (`/contact-us/`)

- Page header: bone bg, eyebrow "Get in touch" + h1
- Two-column layout: form left (`flex:1`), info panel right (`360px` fixed on desktop), stacks on mobile
- Form fields: name + phone (side by side ≥480px), email, service dropdown, message, submit
- Form submission: Web3Forms — swap `REPLACE_WITH_WEB3FORMS_KEY` in the hidden input
- Success state: form hides, `.form-success` shown (no page redirect)
- **Form labels:** `var(--pink)` in classic mode, `var(--snow)` in pink mode
- **Form fields in pink mode:** `var(--snow)` background so they read against the pink form wrap
- Info panel: Visit (address + map link), Reach us (phone + email), Hours table
- Pink mode info panel: ink background, bone/snow text

---

## Gallery Page Pattern (`/gallery/`)

- Page header: eyebrow "The work" + h1 headline
- Sticky filter bar: `position:sticky; top:56px` mobile / `top:64px` desktop, `z-index:90`
- 6 tabs (Hair & Color, Extensions, Facials & Spa, Makeup, Nails, Waxing) — **no "All" tab**
- Active tab: `is-active` class, pink `border-bottom`, ink text
- Pink mode: filter bar → pink bg, inactive tabs `rgba(22,20,15,0.8)`, active → ink border-bottom
- Per-section carousels: `scroll-snap-type:x mandatory`, cards `72vw` mobile / `300px` desktop, `aspect-ratio:3/4`
- No `padding-bottom` on `.gallery-track` — last section only gets `padding-bottom: var(--xl)` via `.gallery-section:last-child .gallery-track`
- `scroll-margin-top` on sections: `106px` mobile / `118px` desktop (nav + filter bar)
- Lightbox: pure JS, `position:fixed; inset:0`, closes on X / overlay / Escape
- Pink mode sections: all → `var(--ink)` bg (no alternating)
- IntersectionObserver updates active filter tab on scroll (`rootMargin: '-20% 0px -70% 0px'`)

---

## Design Rules

- **Hero overlays:** The dark ink gradient on `.hero::after` and `.service-header::before` is the same in both classic and pink theme. Never add a `[data-theme="pink"]` override for the gradient. Only subcopy color may need a pink-mode tweak.
- **Desktop styles:** Every mobile-first CSS block needs real desktop overrides in `@media (min-width: 768px)` — larger type (+30–50%), more padding, bigger column gaps. Mobile values must not carry through unchanged.
- **Nav toggle:** Always `display:inline-flex` in base CSS — see Theme Toggle above.

---

## Design Tokens

```
ink        #16140F   primary text + dark sections
snow       #FDFCFA   primary surface + light text on dark
paper      #FAF7F0   alternate warm band
bone       #F4F0E9   warm light surface
bone-warm  #EAE1D0   warmer surface variant
pink       #EF87AA   brand pink — accents, pills, theme toggle
line       #D8D0C0   hairline rules
muted      #8A8270   secondary/meta text
```

---

## Pending Client Inputs

- **Booking URL:** Set `BOOKING_URL` const in `<script>` at bottom of each page. Currently `'#'`.
- **Team photos:** Kelly Mitchell, Jonathan Rivera, Shannon — placeholders in place
- **Award wording:** CLIENT-VERIFY Sun-Sentinel, Gold Coast, CBS claims before publish
- **Logo:** CSS typographic wordmark in use. Real vector pending.
- **Social URLs:** Confirm Facebook, Pinterest, Yelp handles
- **Google Business Profile URL:** For "Read all 93 reviews" link

---

## Pre-Launch Checklist

- [ ] Swap `BOOKING_URL` on all pages
- [ ] Supply team photos (Kelly, Jonathan, Shannon)
- [ ] Verify award wording with client
- [ ] Confirm social media handles/URLs
- [ ] Confirm Google Business Profile URL
- [ ] Add JSON-LD schema (LocalBusiness + AggregateRating)
- [ ] Add Web3Forms key to `/contact-us/` and `/work-with-us/` (replace `REPLACE_WITH_WEB3FORMS_KEY`)
- [ ] Build remaining pages: 6 service pages
- [ ] Client approval → merge dev to master
