# Product

## Register

brand

This is a brand/marketing site: the design IS the product. The site's job is to build trust and desire, then hand off to the salon's external booking system. Booking is the #1 conversion goal, but the booking transaction itself lives in a third-party tool (being integrated — TBD). Every "Book" CTA on the site is a single reusable component pointing at one configurable URL, so the booking platform can be swapped in one place once finalized. Do not build calendar/scheduling logic into the static site.

## Users

Sullo Salon & Day Spa is a 39-year-old institution on North Federal Highway in Fort Lauderdale, FL. The site serves four overlapping audiences, and the central design tension is holding all of them at once:

- **Loyal 40+ regulars (heritage core).** Have trusted Sullo for years, often follow a specific stylist. They need the site to feel like the same trusted place, only better — never alienated by something that reads as a gimmick.
- **Younger, trend-driven new clients.** Discover salons via Instagram/Google on mobile. They judge in ~5 seconds on a phone and need to see current, high-quality work to believe Sullo is for them too.
- **Affluent newcomers to Fort Lauderdale.** Searching "best hair salon / colorist / balayage near me." Need fast proof of authority and quality.
- **Bridal / special-occasion.** Higher-intent, higher-value, researching for a specific event.

Primary context of use: **mobile, often from social or a Google search, deciding whether this salon is good enough and trustworthy enough to book.** The job to be done: "Convince me you do exceptional work, prove others trust you, and get me to an appointment with as little friction as possible."

Success (6 months), in priority order:
1. More booked appointments (the north-star metric)
2. Rank #1 in Google and in AI/answer-engine search (Gemini, ChatGPT)
3. Attract higher-end clientele
4. Look premium enough to support raising prices

## Product Purpose

Replace a dated, conversion-dead WordPress site that actively undermines a strong brand. The current site cannot capture a single online booking (every "Book Now" links to "#"), displays zero of its 93 Google reviews, has near-empty service pages, and leans on a hot-pink storefront aesthetic that reads "discount spa" rather than "39-year master-colorist institution."

The new site must convert the brand's real, underused authority into bookings and search dominance. That authority is genuine and should be central: 39 years in business; founded by Phyllis Sullo, carried on by master stylists Heather Marino and Matteo Spatafora (40+ years each); Goldwell Platinum salon; Great Lengths & Olaplex certified; voted #1 by the Sun-Sentinel; Gold Coast Magazine Best of South Florida; featured on the CBS Morning Show; named by Glamour one of the ten best salons in the country. 4.5★ across 93 Google reviews.

## Brand Personality

**Three words: confident, refined, established.**

Voice and tone: assured without bragging, warm without being saccharine, expert without jargon. Speaks like a salon that has nothing to prove because the work and the decades speak for themselves. Uses plain, human language a real client would use ("master colorists," "balayage," "the same colorist for twelve years"), not spa-marketing fluff ("indulge in a journey of relaxation").

Emotional goals: a first-time mobile visitor should feel, in order — *this place is the real deal* (authority), *people genuinely love it here* (trust/proof), *I can see myself here* (desire), *booking is easy* (low friction).

The defining tension to design INTO, not away from: **heritage AND current.** It must reassure a 12-year regular and impress a 26-year-old discovering it on Instagram in the same view.

## Anti-references

Hard nos, confirmed by the owner:

- **Hot-pink / glittery "cheap spa" look.** The single biggest risk. Their storefront is a saturated coral-pink (#EB82A0); leaning into that as a dominant color reads discount, not premium. Pink is permitted ONLY as a disciplined, minor accent against a black-and-white system — never the field, never the wordmark, never glittery or gradient.
- **Cold, corporate, sterile.** No stock-corporate minimalism, no clinical med-spa blue, no soulless grids. Warmth is mandatory.
- **Generic Squarespace/Wix salon templates.** No centered-stack hero with icon-title-subtitle cards. No template smell. Must pass the "how was this made?" test, not "which AI/template made this?"
- **Trying-too-hard trendy that ages fast.** No effect-for-effect's-sake, no fad layouts that will read as "2026" in eighteen months. Confidence over novelty.

Also avoid (per impeccable skill, saturated AI-reflex lanes): editorial-serif-magazine cliché (display italic serif + mono labels + ruled columns), and pure cold web-brutalism. Our lane threads between them.

## Strategic Design Principles

1. **Mobile-first, always.** Most traffic is a phone from social/search. Every layout is designed at 390px first; desktop is the enhancement. Reorder content blocks for mobile so a real result/face and social proof hit within the first 1.5 seconds.
2. **Work and proof do the selling.** Real photography and real Google reviews are load-bearing, not decoration. A solid color block where a hero image belongs is a bug. (Photography to be supplied by client; build with representative placeholders that specify exactly what shot goes where.)
3. **Every path leads to one booking handoff.** Single reusable "Book" CTA component → one configurable booking URL. Persistent thumb-zone access on mobile.
4. **Warm structural / light-brutalist lane.** Honest visible grid, oversized confident typography, hairline rules, generous space — but warmed by photography and a non-cold palette. Structure signals confidence; warmth signals welcome.
5. **Authority is content, not ornament.** The credentials (39 years, Glamour, Goldwell Platinum, master colorists, 4.5★/93) are woven through as substance search engines and answer engines can cite — not a logo bar.
6. **Built for SEO + AEO from the structure up.** Content is question-answering, entity-rich, schema-ready, and locally grounded so it ranks in Google and gets cited by Gemini/ChatGPT. (Executed via the claude-seo skill during the Claude Code build.)
7. **Preserve 39 years of domain authority.** Every currently-indexed URL is either kept or 301-redirected. No orphaned pages. New pages flagged for Search Console submission. (Full redirect map in the build brief.)

## Accessibility & Inclusion

- Target WCAG 2.1 AA.
- The brand pink (#EB82A0) fails contrast for small text; never use it for body text or small UI labels. Derive a darker pink (TBD in DESIGN.md) for any pink-on-light text use; reserve #EB82A0 for large fills/accents only.
- Honor prefers-reduced-motion: scroll/entrance animation is enhancement, never required to understand or use the page.
- Minimum 44px tap targets; legible body type on small screens; thumb-zone primary actions.
