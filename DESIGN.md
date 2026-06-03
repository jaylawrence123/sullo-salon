---
name: Sullo Salon & Day Spa
description: Warm structural / light-brutalist brand site for a 39-year Fort Lauderdale salon — confident, refined, established.
colors:
  ink: "#16140F"
  ink-soft: "#2B251C"
  bone: "#F4F0E9"
  bone-warm: "#EAE1D0"
  snow: "#FDFCFA"
  paper: "#FAF7F0"
  pink: "#EB82A0"
  pink-soft: "#E8A9BD"
  pink-text: "#A33B59"
  pink-deep: "#5A2235"
  line: "#D8D0C0"
  muted: "#8A8270"
typography:
  display:
    fontFamily: "'Hanken Grotesk', system-ui, sans-serif"
    fontSize: "clamp(4.5rem, 26vw, 9rem)"
    fontWeight: 900
    lineHeight: 0.8
    letterSpacing: "-0.055em"
  h1:
    fontFamily: "'Hanken Grotesk', system-ui, sans-serif"
    fontSize: "clamp(1.75rem, 6vw, 3rem)"
    fontWeight: 700
    lineHeight: 1.08
    letterSpacing: "-0.02em"
  h2:
    fontFamily: "'Hanken Grotesk', system-ui, sans-serif"
    fontSize: "clamp(1.4rem, 4.5vw, 2.25rem)"
    fontWeight: 700
    lineHeight: 1.15
    letterSpacing: "-0.015em"
  lead:
    fontFamily: "'Hanken Grotesk', system-ui, sans-serif"
    fontSize: "clamp(1.25rem, 3vw, 1.5rem)"
    fontWeight: 600
    lineHeight: 1.25
    letterSpacing: "normal"
  body:
    fontFamily: "'Hanken Grotesk', system-ui, sans-serif"
    fontSize: "1.0625rem"
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: "normal"
  label:
    fontFamily: "'Hanken Grotesk', system-ui, sans-serif"
    fontSize: "0.6875rem"
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: "0.16em"
rounded:
  none: "0px"
  sm: "2px"
  pill: "999px"
spacing:
  xs: "8px"
  sm: "16px"
  md: "24px"
  lg: "40px"
  xl: "64px"
  xxl: "96px"
components:
  button-primary:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.bone}"
    typography: "{typography.label}"
    rounded: "{rounded.sm}"
    padding: "16px 32px"
  button-primary-hover:
    backgroundColor: "{colors.ink-soft}"
    textColor: "{colors.bone}"
  button-secondary:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.ink}"
    typography: "{typography.label}"
    rounded: "{rounded.none}"
    padding: "16px 4px"
  pill-accent:
    backgroundColor: "{colors.pink-soft}"
    textColor: "{colors.pink-deep}"
    typography: "{typography.label}"
    rounded: "{rounded.pill}"
    padding: "6px 14px"
  marquee:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.bone}"
    typography: "{typography.label}"
    padding: "13px 0"
---

## Overview

Sullo is a warm structural / light-brutalist brand site. The voice is **confident, refined, established** — a 39-year salon with nothing to prove. The structure does the confident, brutalist work (honest visible grid, hairline rules, oversized typography, generous negative space, sharp corners); warmth comes from real photography, a warm-black/warm-white palette, and a single disciplined pink accent. The reference lane is deliberately *between* cold web-brutalism and saturated editorial-serif — both of which are explicit anti-references.

Color strategy: **Restrained-plus.** A near-monochrome warm black-and-white system carries 90%+ of every surface; the brand pink appears as a controlled accent (≤10% of any view) — a nod to the storefront, never the field, never the wordmark, never glittery or gradient. This is the discipline that makes pink read premium instead of cheap.

Theme: **light.** Physical scene that forces it — a woman on her phone in Fort Lauderdale daylight, mid-afternoon, deciding whether this salon is good enough to book. Warm paper, not screen-dark. Dark sections (marquee, footer, occasional full-bleed) are punctuation, not the canvas.

Type: **one family, Hanken Grotesk, free + self-hostable.** The personality comes from the *setting*, not an exotic face — weight 900 at extreme negative tracking for display, lighter weights for everything else. One family = cohesive, fast, no licensing. (Optional premium upgrade path, client's call: swap display to a licensed grotesque like Söhne / GT America / Neue Montreal, self-hosted, via a single CSS variable. Not required; Hanken ships.)

## Colors

Never use pure `#000` or `#fff`. Every neutral is warm-tinted toward the brand.

- **ink `#16140F`** — primary text, dark sections, primary buttons, the hero wordmark. A warm near-black.
- **ink-soft `#2B251C`** — button hover, secondary dark surfaces.
- **snow `#FDFCFA`** — PRIMARY surface. A near-white with just a whisper of warmth — reads crisp/gallery-clean to the eye but never clashes with the warm black and pink. This is the default page background.
- **paper `#FAF7F0`** — ALTERNATE band. Slightly warmer/creamier than snow; used for every other content section so adjacent sections separate by color shift alone (the editorial section-break move) without needing a divider.
- **bone `#F4F0E9`** — warm-white used for text on dark surfaces, and the hero knockout band.
- **bone-warm `#EAE1D0`** — the warmest neutral; deeper alt band for sections that need more separation (e.g. proof line, visit).
- **pink `#EB82A0`** — the real storefront pink (sampled). Accent ONLY: large fills, the connecting detail in the wordmark area, decorative marks. **Fails contrast for small text — never use for body or small labels.**
- **pink-soft `#E8A9BD`** — softer accent fills (e.g. the rating pill background).
- **pink-text `#A33B59`** — the accessible pink for any pink-colored *text* on light backgrounds (passes AA at normal sizes). Use this, not `#EB82A0`, whenever pink must be readable type.
- **pink-deep `#5A2235`** — text sitting on a pink/pink-soft fill.
- **line `#D8D0C0`** — hairline rules and dividers (the structural grid lines).
- **muted `#8A8270`** — secondary/meta text, captions.

Contrast: ink on bone/paper passes AAA. bone on ink passes AAA. pink-deep on pink-soft passes AA. pink (#EB82A0) is large-graphic-only.

## Typography

One family, Hanken Grotesk, loaded weights 400/500/600/700/900. `font-display: swap`; preload the 900 (above-the-fold display) and 400 (body) weights only.

- **display** — the hero "SULLO" and major section openers. Weight 900, `letter-spacing: -0.055em`, `line-height: 0.8`. Set huge; let it break the grid / bleed off edges intentionally. The tight tracking is non-negotiable — it's what makes a utility grotesque read as a custom wordmark.
- **h1 / h2** — section headlines, weight 700, tight (-0.02 to -0.015em).
- **lead** — the one-sentence value statements under headlines, weight 600.
- **body** — 17px, weight 400, line-height 1.6, max measure 65–70ch.
- **label** — the ALL-CAPS structural microtext (kickers, marquee, button text, credentials), weight 700, `letter-spacing: 0.16em`. Caps reserved for labels only — never body.

Scale ratio ≥1.25 between steps; no muddy in-between sizes. Hierarchy through weight + scale contrast, not color.

## Elevation

Light-brutalist = **flat.** No drop shadows, no glassmorphism, no gradient surfaces. Depth comes from:

- **Hairline rules** (`1px solid {colors.line}`) as honest structural dividers — full borders only, never single-side colored stripes.
- **Background steps** between bone / paper / bone-warm to separate zones without borders.
- **Dark inversion** (ink sections) for emphasis blocks (marquee, footer, occasional feature).
- **Image as plane** — photography sits flush in the grid, sharp-cornered, as a structural block, not a floated shadowed card.

One permitted exception: a sticky mobile booking bar may use a single subtle top hairline to separate it from content. No blur.

## Components

Sharp corners are the default (`rounded.none` / `sm: 2px`). The only pill (`rounded.pill`) is the accent rating/credential chip — a deliberate soft note against the hard grid.

- **button-primary** — ink fill, bone text, 2px corners, caps label. The booking CTA. Hover → ink-soft. This is the single reusable handoff component; its `href` is one configurable booking URL (booking platform TBD — wire once, swap in one place). Full-width in mobile thumb zone; a persistent sticky variant pins to the bottom on scroll.
- **button-secondary** — flat, underlined-on-hover text button for tertiary actions ("Our work"). No box.
- **pill-accent** — pink-soft fill, pink-deep text, the ONE rounded element. Used for rating ("★ 4.5 · 93 reviews") and small credential flags. Sparing.
- **marquee** — ink bar, bone caps label text, slow auto-scroll of real entity terms (Balayage · Goldwell Platinum · Great Lengths · Olaplex · Keratin · Bridal). Doubles as SEO/AEO entity signal. Pauses on `prefers-reduced-motion`.
- **hero** — full-bleed photo with a gradient scrim top+bottom; kicker + one-line head + rating pill float top-left; the display wordmark sits bottom-left and overlaps the photo's lower edge (the Pixie/Zazz mechanism). On mobile, image leads first.
- **rule-grid** — hairline-divided rows/columns as the visible structural skeleton for content sections (services, credentials, team). The grid is meant to be *seen*.

Motion: entrance reveals only (staggered fade/translate on scroll via IntersectionObserver), ease-out-quint, no bounce. Never animate layout properties. All motion gated by `prefers-reduced-motion`.

## Do's and Don'ts

**Do**
- Design every screen at 390px first; reorder blocks so a face/result + social proof land in the first 1.5s on mobile.
- Keep pink under ~10% of any view; use pink-text for readable pink type, pink for fills only.
- Let the display wordmark be huge and break the grid — confidence is in the scale.
- Show real work and real Google reviews as load-bearing content; specify exact shot per image slot until client photos arrive.
- Use full-border hairlines and background steps for structure; keep it flat.
- Route every path to the single booking CTA component.

**Don't**
- No hot-pink/glittery fields, gradients on pink, or pink wordmark. (Anti-reference #1.)
- No cold/corporate/sterile minimalism; no clinical blue. Warmth is mandatory.
- No Squarespace-template smell: no centered icon-title-subtitle card stacks, no evenly-distributed timid palette.
- No editorial-serif cliché (display italic serif + mono labels + ruled columns) and no reflex fonts (Fraunces, Playfair, Cormorant, Inter, DM, Syne, Space Grotesk, etc.).
- No drop shadows, glass, or single-side colored border stripes.
- No color block where a hero photo belongs — ship imagery.
