---
name: pineapple-design-system-hci-472-final
source_file: Pineapple Design System — HCI 472 Final
source_page: Designs
generated_at: 2026-11-18T00:47:42.372Z
---

# Pineapple Design System — HCI 472 Final Design Guidelines

## Source
- Figma file: Pineapple Design System — HCI 472 Final
- Figma page: Designs
- Extracted at: 2026-11-18T00:47:42.372Z

## Brand
- Product: Pineapple — a healthcare navigation app (book care, check insurance coverage, estimate costs) from my UX portfolio case study.
- Owner mark: my personal "Chay :)" logo, used in the navbar and footer.
- Voice: plain, specific, research-backed. Editorial layout: big light headlines, bracketed labels, huge numerals, lime / pink / green marquee bands.

## Variable Collections
- Primitives
- Tokens

## Color Tokens
- Neutral/White: #FFFFFF
- Ink/900: #0A0A0A
- Ink/700: #2B2B2B
- Grey/500: #6B6B6B
- Grey/400: #8A8A8A
- Grey/200: #E5E5E5
- Grey/50: #F7F7F7
- Lime/500: #ADF801
- Lime/300: #CCFF5C
- Pink/500: #EE55B6
- Green/500: #6BFD03
- Primitives/color/neutral/0: #FFFFFF
- Tokens/color/bg/default: alias(color/neutral/0)
- Tokens/color/bg/subtle: alias(color/grey/50)
- Tokens/color/bg/inverse: alias(color/ink/900)
- Tokens/color/bg/accent-subtle: alias(color/lime/500)
- Tokens/color/text/primary: alias(color/ink/900)
- Tokens/color/text/secondary: alias(color/grey/500)
- Tokens/color/text/inverse: alias(color/neutral/0)
- Tokens/color/text/accent: alias(color/ink/900)
- Tokens/color/text/accent-on-dark: alias(color/lime/500)
- Tokens/color/border/default: alias(color/grey/200)
- Tokens/color/border/strong: alias(color/ink/900)
- Tokens/color/action/primary: alias(color/ink/900)
- Tokens/color/action/primary-hover: alias(color/ink/700)
- Tokens/color/action/accent: alias(color/lime/500)
- Tokens/color/action/accent-hover: alias(color/lime/300)
- Primitives/color/ink/900: #0A0A0A
- Primitives/color/ink/700: #2B2B2B
- Primitives/color/grey/500: #6B6B6B
- Primitives/color/grey/400: #8A8A8A
- Primitives/color/grey/200: #E5E5E5
- Primitives/color/grey/50: #F7F7F7
- Primitives/color/lime/500: #ADF801
- Primitives/color/lime/300: #CCFF5C
- Primitives/color/pink/500: #EE55B6
- Primitives/color/green/500: #6BFD03

## Typography Tokens
- Display/Desktop: Outfit Light, 90px / 100%, tracking -4%
- Display/Numeral: Outfit Light, 96px / 90%, tracking -4%
- Display/Giant: Outfit Light, 300px / 85%, tracking -5%
- Heading/H1: Outfit Regular, 57px / 105%, tracking -3%
- Heading/H2: Outfit Regular, 48px / 110%, tracking -3%
- Heading/H3: Outfit Regular, 40px / 115%, tracking -2%
- Heading/H4: Outfit Regular, 33px / 120%, tracking -1%
- Heading/H5: Outfit Regular, 25px / 125%, tracking -1%
- Heading/Statement: Outfit Medium, 35px / 125%, tracking -1%
- Heading/Ghost: Outfit Light, 25px / 125%, tracking -1%
- Body/Lead: DM Sans Regular, 19px / 155%, tracking 0px
- Body/Regular: DM Sans Regular, 16px / 160%, tracking 0px
- Body/Emphasis: DM Sans Italic, 16px / 160%, tracking 0px
- Body/Strong: DM Sans SemiBold, 16px / 160%, tracking 0px
- Body/Link: DM Sans Medium, 16px / 160%, tracking 0px
- Body/Small: DM Sans Regular, 13px / 150%, tracking 0px
- Label/Overline: DM Sans Medium, 13px / 140%, tracking 0.5px
- Label/Button: DM Sans Medium, 14px / 100%, tracking 0.5px
- Label/Meta: DM Sans Medium, 12px / 130%, tracking 2%

## Spacing Tokens
- Primitives/space/1: 4
- Primitives/space/2: 8
- Primitives/space/3: 16
- Primitives/space/4: 24
- Primitives/space/5: 48
- Primitives/space/6: 96

## Radius Tokens
- Primitives/radius/sm: 0
- Primitives/radius/md: 0
- Primitives/radius/lg: 0
- Primitives/radius/pill: 2

## Motion Tokens
- No motion variables found.

## Effect Styles
- Shadow/Card: none

## Grid Styles
- No local grid styles found.
- Layout grids applied directly on the design frames (Bootstrap 5):
  - Desktop 1440: 12 columns, 24px gutter, 72px margin
  - Tablet 768: 12 columns, 24px gutter, 36px margin
  - Phone 390: 12 columns, 24px gutter, 12px margin

## Component Families
Components live on the Figma page "Foundations and Components" (this export was run from "Designs", so the plugin listed none). Added by hand after extraction:
- Logo — Version: Color / Black / Reverse / White (plus Mark, Favicon and App icon frames)
- Button — Style: Primary / Secondary / Accent × State: Default / Hover
- Badge — Style: Neutral / Accent / Inverse
- Nav Link — State: Default / Active
- Navbar — Device: Desktop / Mobile
- Text Block — Style: Plain / Highlight
- Service Row — Layout: Inline / Stacked
- Marquee — Color: Lime / Pink / Green
- Footer — Device: Desktop / Tablet / Mobile
- Single components: Section Header, Meta Item, Meta Strip, Card / Process, Photo

### Web implementation (Bootstrap)
#### Navbar (`.navbar.navbar-expand-lg.sticky-top`)
White, 1px bottom hairline, 80px tall desktop / 64px mobile. Color logo left; grey links + Primary button right. Active link: ink SemiBold with a 24×2px ink underline and `aria-current="page"`. Square bordered toggler below 992px.

#### Button (`.btn`)
2px radius, padding 12px 20px, DM Sans Medium 14px uppercase, ↗ arrow after the label (CSS `::after`), min height 44px.
- Primary: ink fill, white text; hover Ink 700.
- Secondary ("Learn more", `.btn-light-sv`): Grey 50 fill, ink text; hover Grey 200.
- Accent: lime fill, ink text; hover Lime 300.
Hover nudges the arrow 2px up-right (off under reduced motion). Focus: 2px white + 2px ink ring.

#### Process step (`.step-sv`) and Project card (`.card-sv`)
Step: 1px ink rule on top, 24px padding, Outfit Light 96px numeral ("1."), H5 title, grey body. Project card: flat, no border/radius/shadow, ink cover image with mark, lime badge, H4 title, body, Secondary button; whole card is one link.

#### Others
Badge (Neutral = plain caps, Accent = lime, Inverse = ink with lime text), Section Header (bracket label + H2 + lead), Meta Item (hairline top, label + strong value), Text Block (H5 + body; Plain or Highlight — Highlight has a 1px ink left rule), Figure (16:9, square, small grey caption), Marquee (lime band, scrolling caps text), Footer (ink, reverse logo, lime links).

## Logo
- Personal logo: "Chay" wordmark (Outfit Medium, outlined) + a smile mark — a sideways ":)" in a lime circle.
- Versions: Color (ink + lime), Black, Reverse (white + lime on ink), White, Mark only, Favicon (ink tile, 16/32/64/180), App icons (lime, light).
- Navbar uses the Color logo; footer uses Reverse.
- Minimum width 96px; clear space = half the smile's diameter.

## Page pattern — Case study (Pineapple)
Navbar (Color logo) → Hero ("( UX case study … )" aside, 90px light H1 "Pineapple: healthcare access, made clear.", lead, Meta Strip) → Intro (ghost kicker "How might we…", HMW statement, phone screen panel + The problem / The approach text blocks) → Process intro (centered 90px H2 + "( Process )") → 1. Research & Synthesis (3 service rows, persona images) → lime marquee → 2. Ideation & Iteration (Version 1–3 rows, paper / v2 / v3 screens) → pink marquee → 3. Core Features (4 rows, doctor / bill / insurance screens) → green marquee → What we learned ? (usability testing, lesson statement, tall screen) → What testing revealed (two text blocks + wide hero image) → Footer (CTA + Meta Strip).
Screens sit on Grey 50 panels with object-fit: contain so phone mockups are never cropped.

## Accessibility
- Body contrast ≥ 4.5:1 (ink on white 19.8:1; Grey 500 on white 5.3:1). Grey 400 (3.5:1) only for large ghost text.
- Light weights only at 40px and above.
- Visible focus on every interactive element; hit targets ≥ 44×44px.
- Marquee is decorative (`aria-hidden`) and stops under `prefers-reduced-motion`.
- Semantic landmarks, one `h1` per page, step numerals hidden from screen readers.

## Editing Notes
- Token names match across Figma variables, this file and the CSS custom properties (`Tokens/color/text/primary` → `--sv-text-primary`).
- Keep token names synchronized with Figma styles and variables.
