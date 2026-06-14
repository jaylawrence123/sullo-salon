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

---

## Pages

| Page | Path | Status |
|------|------|--------|
| Home | `/` | Done |
| About | `/about-us/` | Done |
| Our Team | `/our-team/` | Done |
| Gallery | `/gallery/` | Not started |
| Contact | `/contact-us/` | Not started |
| Work With Us | `/work-with-us/` | Not started |
| Hair | `/hair/` | Not started |
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

---

## Team Roster Pattern (`/our-team/`)

- **Owners (Heather + Matteo):** featured flex-row layout, alternating photo side, full bio, tags
- **Staff (7):** horizontal roster rows — 80×80 photo thumb + role/name column + tag pills
- No bio paragraphs on roster rows — tags communicate credentials
- Placeholder initials for Kelly Mitchell (KM), Jonathan Rivera (JR), Shannon (S)

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
- [ ] Propagate footer to /about-us/ and /our-team/
- [ ] Build remaining pages: gallery, contact, work-with-us, 6 service pages
- [ ] Client approval → merge dev to master
