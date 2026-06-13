# Sullo Salon & Day Spa — Homepage

Static HTML/CSS/JS homepage. Deploy to Netlify or Cloudflare Pages.

**Local:** `C:\Users\Jay\Documents\sullo-salon`
**GitHub:** https://github.com/jaylawrence123/sullo-salon
**Live:** https://sullo-salon.netlify.app (master branch, auto-deploys)

---

## Stack

- Single `index.html` — all CSS inline in `<style>`, all JS inline in `<script>`
- Font: **Satoshi** — self-hosted woff2 in `fonts/` (400/500/700/900). NOT from CDN.
- No frameworks, no build step, no dependencies
- Deploy: push to master → Netlify auto-deploys

---

## Theme Toggle

A pink/classic toggle is built into the nav on all breakpoints.

- Button: `[data-theme-toggle]` — always visible in nav (where phone number was)
- Attribute: `data-theme="pink"` on `<html>` — all pink overrides scoped to this
- Persistence: `localStorage` key `sullo-theme`
- Label: "Pink" / "Classic" — switches on toggle

Pink mode overrides are complete for sections S1–S8. S9 and S10 pending.

---

## Build Status

| # | Section | Classic | Pink Mode |
|---|---------|---------|-----------|
| 1 | Hero (announce bar + nav + video + wordmark + sticky bar) | Done | Done |
| 2 | Services (6 square + 1 full-width — all real photos) | Done | Done |
| 3 | Marquee (ink strip, auto-scroll) | Done | Done |
| 4 | Why Sullo (video bg + frosted glass stats) | Done | Done |
| 5 | The Work (editorial CSS Grid — all 8 real photos) | Done | Done |
| 6 | Reviews (ink section — 2 real Google reviews + photos) | Done | Done |
| 7 | Team (all 6 real portraits — Heather/Matteo leads, 4 supporting) | Done | Done |
| 8 | Visit (storefront photo + map + directions + NAP + hours) | Done | Done |
| 9 | Final CTA (press quote photo section) | Done | Pending |
| 10 | Footer (nudge strip + ink body + socials + legal) | Done | Pending |

---

## Pending Client Inputs

- **Booking URL:** Set `BOOKING_URL` in `<script>` at bottom of `index.html`. Currently `'#'`.
- **Award wording:** CLIENT-VERIFY Sun-Sentinel, Gold Coast, CBS claims before publish
- **Logo:** CSS typographic wordmark in place. Real vector (transparent PNG or SVG) pending.
- **Social URLs:** Confirm real handles for Facebook, Pinterest, Yelp
- **Google Business Profile URL:** For "Read all 93 reviews" link in Reviews section

---

## Pre-Launch Checklist

- [ ] Swap `BOOKING_URL` variable (one line in `<script>`)
- [ ] Verify award wording with client
- [ ] Confirm social media handles/URLs
- [ ] Confirm Google Business Profile reviews URL
- [ ] Add JSON-LD schema (LocalBusiness + AggregateRating + Service)
- [ ] Wire chatbot when platform is chosen
- [ ] Supply real logo (transparent PNG or SVG)
- [ ] Complete S9 + S10 pink mode overrides
- [ ] Client approval on pink toggle before launch

---

## Design Tokens

```
ink        #16140F   primary text + dark sections
snow       #FDFCFA   primary surface + light text on dark
paper      #FAF7F0   alternate band (classic mode)
bone       #F4F0E9   warm light surface (classic mode)
pink       #EF87AA   brand pink — accents, pills, toggle theme
line       #D8D0C0   hairline rules (classic mode)
muted      #8A8270   secondary/meta text (classic mode)
```

---

## Sitemap — Preserve All Existing URLs

No redirects. Keep every slug identical to the current live site to protect Google indexing and link equity.

| Page | URL |
|------|-----|
| Home | `/` |
| About | `/about-us/` |
| Hair Extensions | `/hair-extensions/` |
| Hair | `/hair/` |
| Facials | `/facials/` |
| Makeup | `/makeup/` |
| Nails | `/nails/` |
| Waxing | `/waxing/` |
| Our Team | `/our-team/` |
| Gallery | `/gallery/` |
| Work with us | `/work-with-us/` |
| Contact | `/contact-us/` |
