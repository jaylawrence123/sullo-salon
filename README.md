# Sullo Salon & Day Spa — Homepage

Static HTML/CSS/JS homepage. Deploy to Netlify or Cloudflare Pages.

**Local:** `C:\Users\Jay\Documents\sullo-salon`
**GitHub:** https://github.com/jaylawrence123/sullo-salon
**Live:** TBD

---

## Stack

- Single `index.html` — all CSS inline in `<style>`, all JS inline in `<script>`
- Font: **Satoshi** via Fontshare CDN (400/500/700/900)
- No frameworks, no build step, no dependencies
- Deploy: drag `index.html` + `sullo-salon-hero-video.mp4` to Netlify/Cloudflare

---

## Build Status

| # | Section | Status |
|---|---------|--------|
| 1 | Hero (announce bar + nav + video + wordmark + pink pill rating + sticky bar) | Done |
| 2 | Services (6 square + 1 full-width — all real photos) | Done |
| 3 | Marquee (ink strip, auto-scroll) | Done |
| 4 | Why Sullo (Glamour headline + 3-stat grid + About CTA) | Done |
| 5 | The Work (16:9 video + editorial CSS Grid — all 8 real photos) | Done |
| 6 | Reviews (ink section — 2 real Google reviews + photos) | Done |
| 7 | Team (all 6 real portraits — Heather/Matteo leads, 4 supporting) | Done |
| 8 | Visit (storefront photo + map + directions + NAP + hours) | Done |
| 9 | Final CTA (pink Book button + demoted call text link) | Done |
| 10 | Footer (pink nudge + centered nav + socials + legal) | Done |

**All sections complete. No placeholder images except hero fallback.**

---

## Pending Client Inputs

- **Booking URL:** Set `BOOKING_URL` in `<script>` at bottom of `index.html`. Currently `'#'`.
- **Hero fallback image:** One placeholder remains — "master colorist mid-work, warm editorial, vertical crop"
- **Award wording:** CLIENT-VERIFY Sun-Sentinel, Gold Coast, CBS claims before publish
- **Logo:** CSS typographic wordmark in place. Real vector (transparent PNG or SVG) pending.
- **Social URLs:** Confirm real handles for Facebook, Pinterest, Yelp
- **Google Business Profile URL:** For "Read all 93 reviews" link in Reviews section
- **Visit photo gap:** White gap on mobile storefront photo — revisit with real photo

---

## Pre-Launch Checklist

- [ ] Swap `BOOKING_URL` variable (one line in `<script>`)
- [ ] Supply hero fallback image
- [ ] Verify award wording with client
- [ ] Confirm social media handles/URLs
- [ ] Confirm Google Business Profile reviews URL
- [ ] Add JSON-LD schema (LocalBusiness + AggregateRating + Service)
- [ ] Create `_redirects` file (see redirect map below)
- [ ] Submit `/color` to Google Search Console (net-new page)
- [ ] Wire chatbot when platform is chosen
- [ ] Supply real logo (transparent PNG or SVG)

---

## Design Tokens

```
ink        #16140F   primary text + dark sections
ink-soft   #2B251C   button hover
snow       #FDFCFA   primary surface
paper      #FAF7F0   alternate band
bone-warm  #EAE1D0   placeholder fallback bg
bone       #F4F0E9   text on dark
pink       #EF87AA   brand pink — final CTA button only
pink-soft  #F2A4BD   pills, bar, nudge strip, Call button
line       #D8D0C0   hairline rules
muted      #8A8270   secondary/meta text
```

---

## Redirect Map (Netlify `_redirects`)

```
/about-us/        /about       301
/our-team/        /team        301
/contact-us/      /contact     301
/hair-extensions/ /extensions  301
/work-with-us/    /careers     301
```

Keep as-is: `/gallery/`, `/hair/`, `/facials/`, `/makeup/`, `/nails/`, `/waxing/`
Net-new — submit to Search Console after launch: `/color`
