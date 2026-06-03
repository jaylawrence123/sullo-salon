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
| 1 | Hero (nav + photo/video + wordmark + trust ribbon) | ✅ Done |
| 2 | Services (image tiles, 6 square + 1 full-width) | ✅ Done |
| 3 | Marquee (ink strip, auto-scroll) | ✅ Done |
| 4 | Proof line (Glamour lead + 4-stat grid) | ✅ Done |
| 5 | The Work (masonry gallery, 8 images) | ✅ Done |
| 6 | Reviews (dark section, story quotes) | ⬜ Next |
| 7 | Team (owner-led hierarchy) | ⬜ |
| 8 | Visit (map + directions + NAP + hours) | ⬜ |
| 9 | Final CTA (full-bleed close) | ⬜ |
| 10 | Footer (links + legal) | ⬜ |

---

## Pending Client Inputs

- **Photos:** All image slots are `placehold.co` placeholders with shot specs in HTML comments. Swap `src` when real photos arrive.
- **Hero video:** `sullo-salon-hero-video.mp4` is live. Placeholder image fallback remains for reduced-motion users.
- **Booking URL:** Set `BOOKING_URL` in the `<script>` block at the bottom of `index.html`. Currently `'#'`.
- **Reviews:** Section 6 uses placeholder text. Must be replaced with real verbatim Google reviews (legal + schema requirement).
- **Hours:** Do NOT publish until client verifies — site and Google currently disagree.
- **Award wording:** CLIENT-VERIFY all Glamour/Sun-Sentinel/Gold Coast/CBS claims before publish.
- **Logo:** Using text "sullo" in Hanken 900. Real vector pending from client.
- **Chatbot:** Mount point built (`#chatbot-launcher`, hidden). Wire when platform is chosen.

---

## Design Tokens (DESIGN.md)

```
ink        #16140F   primary text + dark sections
ink-soft   #2B251C   button hover
snow       #FDFCFA   primary surface
paper      #FAF7F0   alternate band
bone-warm  #EAE1D0   placeholder fallback bg
bone       #F4F0E9   text on dark
pink       #EB82A0   accent fills only (≤10% of any view)
pink-soft  #E8A9BD   pill backgrounds
pink-text  #A33B59   readable pink on light bg
pink-deep  #5A2235   text on pink fills
line       #D8D0C0   hairline rules
muted      #8A8270   secondary/meta text
```

Font: **Hanken Grotesk** only. Display = 900 / -0.055em / lh 0.8. Body = 400 / 17px / lh 1.6. Labels = 700 / caps / 0.16em.

---

## SEO / AEO (post-build)

- Schema: LocalBusiness + AggregateRating + Service — add before launch
- Run claude-seo audit after all 10 sections are built
- Submit `/color` (net-new) to Google Search Console after launch

## Redirects (preserve domain authority)

Add `_redirects` file for Netlify before launch. See `BUILD-BRIEF.md` for full map.
