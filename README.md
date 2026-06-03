# Sullo Salon & Day Spa — Homepage

Static HTML/CSS/JS homepage. Deploy to Netlify or Cloudflare Pages.

**Local:** `C:\Users\Jay\Documents\sullo-salon`
**GitHub:** https://github.com/jaylawrence123/sullo-salon
**Live:** TBD

---

## Stack

- Single `index.html` — all CSS inline in `<style>`, all JS inline in `<script>`
- Font: **Satoshi** via Fontshare CDN (400/500/700/900) — replaced Hanken Grotesk
- No frameworks, no build step, no dependencies
- Deploy: drag `index.html` + `sullo-salon-hero-video.mp4` to Netlify/Cloudflare

---

## Build Status

| # | Section | Status |
|---|---------|--------|
| 1 | Hero (announce bar + nav + video + wordmark + trust ribbon + sticky bar) | ✅ Done |
| 2 | Services (6 square tiles + 1 full-width — all real photos) | ✅ Done |
| 3 | Marquee (ink strip, auto-scroll) | ✅ Done |
| 4 | Proof line (Glamour lead + 2×2 / 4-col stat grid) | ✅ Done |
| 5 | The Work (masonry gallery — all 8 real photos) | ✅ Done |
| 6 | Reviews (ink section — 2 real Google reviews + photos) | ✅ Done |
| 7 | Team (Heather + Matteo lead cards, 4 supporting) | ✅ Done |
| — | About (origin story + 4-stat grid) | ✅ Done |
| 8 | Visit (storefront photo + map embed + directions + NAP + hours) | ✅ Done |
| 9 | Final CTA (full-bleed photo + copy + Book CTA) | ✅ Done |
| 10 | Footer (pink nudge + centered nav grid + socials + legal) | ✅ Done |

**All sections complete. Pre-launch checklist below.**

---

## Pending Client Inputs

- **Booking URL:** Set `BOOKING_URL` in `<script>` block at bottom of `index.html`. Currently `'#'`.
- **Reviews:** 2 real Google reviews live (Skyla Petrillo, Stephanie Vogelgesang Felton). Add more as needed.
- **Team portraits:** 6 placeholder images (Heather, Matteo, Taiilor, Kristen, Pam, Carolyn) — shot specs in HTML comments.
- **Award wording:** CLIENT-VERIFY all Glamour/Sun-Sentinel/Gold Coast/CBS claims.
- **Logo:** CSS typographic wordmark in place (su/ll/o size treatment). Real vector pending — needs clean transparent PNG or SVG from client.
- **Chatbot:** Mount point built (`#chatbot-launcher`, hidden). Wire when platform chosen.
- **Social URLs:** Confirm real handles for Facebook, Pinterest, Yelp.
- **Visit photo gap:** White gap on mobile storefront photo — flagged in HTML, revisit with real photo.
- **Work gallery desktop gap:** Bottom-left gap in 3-col masonry — flagged in HTML.

---

## Pre-Launch Checklist

- [ ] Swap `BOOKING_URL` variable (one line in `<script>`)
- [ ] Verify award wording with client
- [ ] Confirm social media handles/URLs
- [ ] Add JSON-LD schema (LocalBusiness + AggregateRating + Service)
- [ ] Create `_redirects` file (see BUILD-BRIEF.md for full map)
- [ ] Submit `/color` to Google Search Console (net-new page)
- [ ] Wire chatbot when platform is chosen
- [ ] Swap team portrait placeholders with real photos
- [ ] Supply real logo (transparent PNG or SVG)
- [ ] Confirm Google Business Profile reviews URL for "Read all 93 reviews →" link

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
pink-soft  #F2A4BD   lighter pink — pills, bar, nudge strip, Call button
line       #D8D0C0   hairline rules
muted      #8A8270   secondary/meta text
```

Font: **Satoshi** (Fontshare). 400/700/900. Replaced Hanken Grotesk site-wide.
Wordmark: `su` at `clamp(4.5rem, 25vw, 9rem)`, `ll` at `clamp(5.5rem, 30vw, 10rem)` with `vertical-align: -0.12em`, stagger reveal animation on scroll.

---

## SEO / AEO (post-build)

- Schema: LocalBusiness + AggregateRating + Service — add before launch
- Run claude-seo audit
- Submit `/color` (net-new) to Google Search Console after launch

## Redirects (preserve domain authority)

Add `_redirects` file for Netlify before launch. See `BUILD-BRIEF.md` for full map.
