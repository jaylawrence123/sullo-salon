# Sullo Salon & Day Spa — Homepage

Static HTML/CSS/JS homepage. Deploy to Netlify or Cloudflare Pages.

**Local:** `C:\Users\Jay\Documents\sullo-salon`
**GitHub:** https://github.com/jaylawrence123/sullo-salon
**Live:** TBD

---

## Stack

- Single `index.html` — all CSS inline in `<style>`, all JS inline in `<script>`
- Font: Hanken Grotesk via Google Fonts (400/700/900)
- No frameworks, no build step, no dependencies
- Deploy: drag `index.html` + `sullo-salon-hero-video.mp4` to Netlify/Cloudflare

---

## Build Status

| # | Section | Status |
|---|---------|--------|
| 1 | Hero (nav + video + wordmark + trust ribbon + sticky bar) | ✅ Done |
| 2 | Services (image tiles — 6 square + 1 full-width, real ibb.co photos) | ✅ Done |
| 3 | Marquee (ink strip, auto-scroll, pink ✦ separators) | ✅ Done |
| 4 | Proof line (Glamour lead + 2×2 / 4-col stat grid) | ✅ Done |
| 5 | The Work (2-col masonry gallery, 8 images) | ✅ Done |
| 6 | Reviews (ink section, 4.5★ aggregate, 2 story pairs) | ✅ Done |
| 7 | Team (Heather + Matteo lead cards, 4 supporting) | ✅ Done |
| 8 | Visit (storefront photo + map embed + directions + NAP + hours) | ✅ Done |
| 9 | Final CTA (full-bleed photo + copy + Book CTA) | ✅ Done |
| 10 | Footer (pink nudge + nav grid + socials + legal) | ✅ Done |

**All 10 sections complete. Pre-launch checklist below.**

---

## Pending Client Inputs

- **Photos:** Work gallery (8 slots), team portraits (6 slots), final CTA still using real photo. Shot specs in HTML comments throughout.
- **Hero video:** `sullo-salon-hero-video.mp4` live. Placeholder image fallback for reduced-motion users.
- **Booking URL:** Set `BOOKING_URL` in `<script>` block at bottom of `index.html`. Currently `'#'`.
- **Reviews:** Section 6 uses PLACEHOLDER text. Must be replaced with real verbatim Google reviews before launch (legal + schema requirement).
- **Award wording:** CLIENT-VERIFY all Glamour/Sun-Sentinel/Gold Coast/CBS claims.
- **Logo:** Text "sullo" in Hanken 900. Real vector pending.
- **Chatbot:** Mount point built (`#chatbot-launcher`, hidden). Wire when platform chosen.
- **Visit photo gap:** White gap on left/right of storefront photo on mobile — flagged in HTML comment. Likely ibb.co image dimension issue; revisit with real photo.
- **Work gallery gap:** Bottom-left gap in 3-col desktop masonry (uneven 8-image distribution). Fix when real photos arrive.
- **Social URLs:** Facebook, Pinterest, Yelp links are placeholder paths — confirm real handles with client.

---

## Pre-Launch Checklist

- [ ] Swap `BOOKING_URL` variable
- [ ] Replace placeholder review text with real Google reviews
- [ ] Verify award wording with client
- [ ] Confirm social media handles/URLs
- [ ] Add JSON-LD schema (LocalBusiness + AggregateRating + Service)
- [ ] Create `_redirects` file (see BUILD-BRIEF.md for full map)
- [ ] Submit `/color` to Google Search Console (net-new page)
- [ ] Wire chatbot when platform is chosen
- [ ] Swap placeholder images with real client photos
- [ ] Confirm hours with client (currently from Google — may disagree with site)
- [ ] Supply real logo vector

---

## Design Tokens

```
ink        #16140F   primary text + dark sections
ink-soft   #2B251C   button hover
snow       #FDFCFA   primary surface
paper      #FAF7F0   alternate band
bone-warm  #EAE1D0   placeholder fallback bg
bone       #F4F0E9   text on dark
pink       #EF87AA   brand pink (sampled from building) — accent fills only
pink-soft  #F2A4BD   lighter pink — pills, announcement bar, nudge strip
pink-text  #A33B59   readable pink type on light bg
pink-deep  #5A2235   text on pink fills
line       #D8D0C0   hairline rules
muted      #8A8270   secondary/meta text
```

Font: **Hanken Grotesk** only. Display = 900 / -0.055em / lh 0.8. Body = 400 / 17px / lh 1.6. Labels = 700 / caps / 0.16em.

---

## SEO / AEO (post-build)

- Schema: LocalBusiness + AggregateRating + Service — add before launch
- Run claude-seo audit
- Submit `/color` (net-new) to Google Search Console after launch

## Redirects (preserve domain authority)

Add `_redirects` file for Netlify before launch. See `BUILD-BRIEF.md` for full map.
