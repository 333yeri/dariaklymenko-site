# Daria Klymenko — Cinematic Taste Profile
## Generated June 9, 2026

---

## DESIGN THESIS
"Social media for brands with a soul. The site should feel like discovering someone who finally gets it — relief, recognition, quiet confidence."

---

## COLOR SYSTEM

### Base (Her existing palette — evolved)
| Token | Hex | Role |
|---|---|---|
| bark | #2C2018 | Primary dark — text, dark sections |
| clay | #C8997A | Primary warm — CTAs, highlights |
| sand | #E8D5B7 | Secondary warm — borders, subtle bg |
| sand-lt | #FAF6F0 | Light background |
| sage | #7B9B7A | Accent organic — sparingly |

### Cinematic Additions
| Token | Hex | Role |
|---|---|---|
| gold | #C4A35A | Cinematic accent — gold text on dark, reveals, hero moments |
| charcoal | #1A1410 | Richer dark than bark — hero, immersive sections |
| cream | #FFF8EF | Warmer white — text on dark, breathing room |

### CINEMATIC ACCENT RATIONALE
- #C4A35A (antique gold): Sits between her warm clay and dark bark. Adds richness.
- Works on both light and dark sections.
- Film-grade warmth without being yellow or brassy.
- Used for: hero typography accent, dividers, hover states, scroll indicator, key UI moments.

### Reserved for dark sections only
- charcoal (#1A1410) replaces bark in immersive/hero moments
- cream (#FFF8EF) replaces sand-lt for text on dark
- gold (#C4A35A) for highlights on dark

---

## TYPOGRAPHY

### New Pairing
- **Headlines:** Cormorant Garamond (serif) — lighter weight, wider tracking, more cinematic than Playfair Display
- **Body + UI:** Inter (sans) — kept, it works

### Scale (editorial, generous)
| Level | Size (desktop) | Weight | Tracking | Role |
|---|---|---|---|---|
| Display | 72-96px | Light 300 | +0.02em | Hero headline |
| h1 | 48-56px | Regular 400 | +0.01em | Section titles |
| h2 | 32-40px | Medium 500 | 0 | Sub-section |
| h3 | 20-24px | SemiBold 600 | +0.03em | Caps labels, prices |
| Body | 16-18px | Regular 400 | 0 | Paragraphs |
| Small | 13-14px | Medium 500 | +0.05em | Labels, nav, meta |

### Rules
- Never more than 2 font sizes in view at once
- Wide tracking on caps labels (process steps, section overlines)
- Light weight on large display type — elegance over boldness
- Line-height: 1.6 for body, 1.1 for headlines

---

## SPACING & LAYOUT

### Grid
- Max container: 1200px (expanded from 1120px for cinematic feel)
- Outer padding: 32px desktop, 20px mobile
- Section padding: 120px-160px vertical (generous breathing room)
- Between sections: use color contrast, not just spacing

### Radii
- Cards: 16px (slightly larger, softer)
- Buttons: 999px (pill, unchanged)
- Images: 4px (sharp, editorial — no rounding on photos)

---

## CINEMATIC PRINCIPLES

### Scroll
- Smooth scroll (CSS `scroll-behavior: smooth`)
- Parallax on hero image and section divider images ONLY
- Reveal on scroll (fade + translateY) for section content
- No scroll-snap — free scroll feels more editorial
- Scroll-driven opacity on fixed elements (header fades to dark bg)

### Animation Approach: Selective Cinematic
- **Hero:** Full treatment — text stagger reveal on load, parallax background, gold accent line draws in
- **Section dividers:** Parallax image reveal as you scroll past
- **Content:** Simple fade-up on scroll into view (Intersection Observer)
- **Micro:** Hover states only — no looping, no bouncing, no auto-animate
- **Zero:** No 3D transforms, no particle effects, no WebGL, no cursor-follow

### Image Treatment
- No stock photos
- Real Daria content only (her face, her work, her words)
- If no image exists: use abstract gold-on-dark geometric instead of placeholder
- Images never rounded (editorial sharpness)

---

## SECTION ARCHITECTURE

1. **Urgency Strip** (fixed, thin, top)
2. **Nav** (transparent → dark on scroll)
3. **Hero** (full viewport, cinematic, parallax bg, stagger text reveal)
4. **For Who** (dark bg, 3 cards, gold accents)
5. **Story/About** (light bg, text-heavy, editorial layout, horizontal scroll gallery)
6. **Preview — The Grid** (dark bg, 6-9 content tiles, no images — branded color tiles)
7. **How It Works** (light bg, 3-step horizontal timeline)
8. **Pricing** (dark bg, 3 tiers with gold featured card)
9. **FAQ** (light bg, accordion)
10. **CTA Banner** (dark bg, full-width, strong single line)
11. **Footer** (minimal, dark)

---

## OFFERING POSITIONING (defined by the site)

Based on cinematic language, the offering crystallizes as:
**"Instagram presence for brands with purpose"**

Not just "social media management." Not just "content."
The site should make Daria's positioning clear through design language:
- She's strategic (not just a poster)
- She's visual (not just a scheduler)
- She's selective (not for everyone)

The "Apply" vs "Free Audit" dual CTA captures this:
- Apply = "I'm ready to invest in my brand" (serious clients)
- Free Audit = "I'm curious, show me what you see" (warm lead)

---

## ANTI-PATTERNS (what this site is NOT)
- No generic gradient backgrounds
- No stock photography
- No testimonials from people who aren't real clients
- No "trusted by" logo bar with brands she hasn't worked with
- No chat widgets
- No cookie banner (not needed for this use case)
- No popups
- No "limited time offer" countdown timer
- No 5-step process (3 max)
- No feature list with icons (strategy isn't a feature list)
