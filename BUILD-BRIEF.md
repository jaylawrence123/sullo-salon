# SULLO SALON — BUILD BRIEF (read this first)

You are building the Sullo Salon & Day Spa homepage. Static HTML/CSS/JS, deployed to Netlify or Cloudflare. Mobile-first.

## READ THESE FILES IN THIS ORDER, BEFORE WRITING ANY CODE
1. **PRODUCT.md** — who/what/why, brand voice, anti-references, strategic principles. (impeccable skill context)
2. **DESIGN.md** — the visual system: exact color tokens, Hanken Grotesk type scale, components, do's/don'ts. Tokens are NORMATIVE — use these exact hex values and type settings, do not invent your own.
3. **COPY.md** — final, approved copy for every section. Use verbatim. Do not rewrite.
4. **This file (BUILD-BRIEF.md)** — build order, rules, integrations, redirect map.

Also load the impeccable skill (design law) and claude-seo skill (SEO/AEO) if available.

## HOW WE BUILD: SECTION BY SECTION — STOP FOR APPROVAL BETWEEN EACH
**Do NOT build the whole homepage in one shot.** Build ONE section at a time, in the order below. After each section: show it (mobile 390px first), then STOP and wait for explicit approval before starting the next. This is non-negotiable — a one-shot full build produced unusable drift last time.

Sections 1–10 are already fully designed and approved (mockups exist). Reproduce them faithfully from the specs — do NOT redesign, reinterpret, or "improve" them. If something is ambiguous, ask, don't guess.

## BUILD ORDER (the homepage spine — locked)
1. **Hero** — nav (text logo "sullo" + phone + burger); hero photo with eyebrow (★★★★★ 4.5 · 93 Google reviews) directly above headline, Book + pink Call CTAs above the fold ON the photo; below photo a WHITE/PAPER (snow) band with "SULLO" in solid BLACK Hanken 900 (full word, not pink, not over photo); then 3-cell trust ribbon (39 Years / Glamour Top 10 U.S. / Goldwell Platinum).
2. **Services** — directly under hero. IMAGE TILES (photo + name over scrim), NOT text rows. 6 equal square tiles + 1 full-width 7th: Color & Balayage (flag: Most booked), Extensions (flag: #1 in Fort Lauderdale), Hair, Facials, Makeup, Nails, "Waxing & more" full-width.
3. **Marquee** — moving auto-scroll black strip, pink ✦ separators, entity terms. Pause on prefers-reduced-motion.
4. **Proof line** — credential HIERARCHY (not flat grid): big Glamour lead block, then hairline-divided supporting rows.
5. **The Work** — editorial masonry, ~8 results, mixed heights in 2 clean columns, tiny captions.
6. **Reviews** — DARK (ink) background; aggregate 4.5★/93 leads; 2 story quotes EACH paired with a result photo.
7. **Team** — owner-led hierarchy: Heather + Matteo large lead cards, others as 2-up cards.
8. **Visit** — photo → map → Google/Waze/Apple directions buttons → NAP + hours.
9. **Final CTA** — full-bleed photo close, wordmark bookend, reason line at the button.
10. **Footer** — pink book nudge → structured footer (Explore/Services/Visit/Contact) → socials → legal.

## SECTION BREAKS / COLOR RHYTHM
Section breaks are handled by BACKGROUND COLOR SHIFTS, not dividers (editorial approach).
- Primary surface = `snow #FDFCFA`. Alternate band = `paper #FAF7F0`. Deeper alt = `bone-warm #EAE1D0`. Dark punctuation = `ink #16140F`.
- Alternate snow/paper between adjacent light sections so they separate without lines.
- Add a thin rule + small section number (e.g. "03 — The Work") ONLY where two SAME-color sections touch (Services→Work). Don't divider every section.

## BOOKING (critical)
Booking platform is TBD (client is integrating a new system). Build ONE reusable "Book" CTA component pointing at a SINGLE configurable URL/variable (e.g. `BOOKING_URL`). Every Book button + the Call→tel link + the chatbot's booking action all reference this one variable. When the platform is chosen, it's a one-line swap. Do NOT build an embedded calendar.

## CHATBOT (flag — build a mount point)
The client has a custom chatbot to add later. Build a placeholder mount point (bottom-right launcher) that does NOT collide with the sticky mobile Book/Call bar — coordinate them in the bottom cluster so they don't overlap in the thumb zone. The bot will (a) be fed this site's content as its knowledge base, and (b) book appointments via the same `BOOKING_URL` once live. Leave clean hooks; don't build the bot itself.

## SEO / AEO REQUIREMENTS
- Schema markup: `LocalBusiness` (NAP + hours + geo), `Review` + `AggregateRating` (4.5 / 93), `Service` for each service.
- Descriptive + local image alt-text on every image (e.g. "Hand-painted balayage by a master colorist, Sullo Salon Fort Lauderdale"), never "salon photo."
- Semantic HTML, fast Core Web Vitals (static map image not heavy embed; lazy-load below-fold images; preload Hanken 900 + 400 only).
- Run the claude-seo skill after build for the full audit.

## REDIRECT MAP (preserve 39 years of domain authority — DO NOT orphan any indexed URL)
Currently indexed URLs — each must KEEP its slug or 301-redirect to its new home:
- `/about-us/` → keep or → `/about`
- `/our-team/` → keep or → `/team`
- `/contact-us/` → keep or → `/contact` (or merge into Visit)
- `/gallery/` → keep
- `/hair-extensions/` → keep (high-value, already ranks) → `/extensions`
- `/hair/` → keep
- `/facials/` → keep
- `/makeup/` → keep
- `/nails/` → keep
- `/waxing/` → keep
- `/work-with-us/` → keep or → `/careers`
NET-NEW pages (submit to Google Search Console after launch): `/color` or `/balayage` (Color & Balayage — broken out, did not exist before).
Use Netlify `_redirects` or Cloudflare equivalent. 301 (permanent), never 302.

## PLACEHOLDERS / PENDING CLIENT INPUTS (do not block; mark clearly)
- **Logo:** real vector pending from client. Use text "sullo" in Hanken 900 in nav/footer until supplied. (Hero "SULLO" is display type, not the logo.)
- **Photos:** all images are placeholders. Each image slot has a shot-spec comment in COPY.md / mockups — keep these as comments so the client knows what to shoot. Use representative stock until real photos arrive.
- **Reviews:** featured review text is PLACEHOLDER. Build must use REAL verbatim Google reviews (legal + schema requirement). Pull via Google API or client-supplied.
- **Hours:** CLIENT-VERIFY. Their site and Google currently disagree. Do NOT publish hours until confirmed.
- **Award wording:** confirm exact phrasing of Glamour/Sun-Sentinel/Gold Coast/CBS claims with client before publish.

## TYPE & PALETTE QUICK REF (full detail in DESIGN.md)
- Font: Hanken Grotesk only (one family). Display = weight 900, letter-spacing -0.055em, line-height 0.8. Body = 400, 17px, lh 1.6. Labels = 700 caps, letter-spacing 0.16em.
- Colors: ink #16140F, snow #FDFCFA (primary surface), paper #FAF7F0 (alt), bone-warm #EAE1D0, bone #F4F0E9, pink #EB82A0 (accent ONLY ≤10%, never field/wordmark), pink-text #A33B59 (readable pink text), pink-deep #5A2235, line #D8D0C0, muted #8A8270.
- Never pure #000 or #fff. Pink is accent only.
