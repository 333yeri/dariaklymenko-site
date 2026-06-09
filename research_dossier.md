# CINEMATIC WEB DESIGN — RESEARCH DOSSIER
## For: Daria Klymenko Cinematic Landing Page
## Researched: June 9, 2026

---

## 1. WHAT'S WINNING IN 2025-2026

### Awwwards Data (Q1 2026)
- **61%** of Site of the Day winners are immersive 3D experiences (up from 23% in 2024)
- **Creativity scores**: 3D sites average 8.7/10 vs 6.4/10 for flat layouts
- **Top stack**: Three.js + GSAP ScrollTrigger + custom post-processing
- **Judging shift**: "Judges score ambition, not just aesthetics. The browser is a rendering engine, not a document viewer."

### Key Trends
- **Scroll-driven narrative arcs** — camera spline paths, scroll checkpoints, normalized scroll position (0→1) as master timeline
- **Narrative pacing** — easing curves + scroll-velocity thresholds. Fast scroll = abbreviated transitions. Slow scroll = hidden details
- **Spatial composition** — depth, parallax, volumetric fog over flat grids
- **Dark mode as default** — not inverted colors, but thoughtful contrast + accessible typography
- **Editorial typography** — grotesque-serif voice, bold display type, cinematic filmstrip sliders
- **5 scenes max** — visitors want 2-3 minute experiences, not 10

### What Separates Good from Great
- **Camera animation systems** drive narrative progression
- **Adaptive pacing** — intentional speed control
- **Real-time ray marching**, GPU fluid simulations, procedural environments
- **Progressive enhancement** — graceful degradation on mobile

---

## 2. DARK CINEMATIC DESIGN PATTERNS

### From Award-Winning Dark Sites
- **Black + white minimalism** — Yanchen portfolio (ex-Apple): scroll-triggered animations, parallax, creative typography
- **Dark + gold accents** — luxury brands: white and gold text on dark backgrounds
- **Dark + warm earth tones** — the sweet spot for Daria: warm clay/sand on dark bark/charcoal
- **Interactive headers** — dynamic, not static
- **Text and intro animations** — staggered reveals, not everything at once
- **Custom cursor** — subtle brand reinforcement
- **Sticky/fixed navigation** — appears on scroll, transparent on hero

### Dark Design Principles
1. Dark mode ≠ inverted colors. Requires thoughtful contrast ratios
2. Typography must be bolder on dark backgrounds (font-weight + letter-spacing)
3. Accent colors pop more on dark — gold, warm clay, sage all sing on dark
4. Negative space is even more critical on dark — breathing room prevents visual fatigue
5. Gradients and glow effects add depth without images

---

## 3. EDITORIAL TYPOGRAPHY TRENDS

### What's Working
- **Serif + sans pairing** remains dominant for editorial/luxury
- **Display serifs** for headlines: Cormorant Garamond, Playfair Display, custom serifs
- **Clean sans** for body: Inter, Helvetica Neue, custom grotesque
- **Bold and experimental typography** — oversized headlines, mixed weights
- **Letter-spacing** — generous tracking on uppercase labels, tight on headlines
- **Type as hero** — typography IS the design, not decoration

### For Daria Specifically
- **Cormorant Garamond** (light/regular) — more cinematic than Playfair Display, thinner strokes, more elegant
- **Inter** (regular/medium) — clean, modern, highly legible
- **Letter-spacing**: +0.08em on uppercase labels, -0.02em on large headlines
- **Weight contrast**: Light (300) for display, Regular (400) for body — avoid bold

---

## 4. SCROLL-DRIVEN NARRATIVE TECHNIQUES

### The Winning Formula
1. **Normalized scroll position (0→1)** as master timeline
2. **Scroll checkpoints** trigger: content reveals, particle effects, camera rotations
3. **Easing curves** — ease-out for reveals, ease-in-out for transitions
4. **Scroll-velocity thresholds** — fast vs slow scroll = different experiences
5. **5 scenes maximum** — focused narrative arc

### Implementation (No WebGL Required)
- **IntersectionObserver** for scroll-triggered reveals (fade-up, slide-in)
- **CSS `scroll-behavior: smooth`** for buttery scrolling
- **Parallax via `transform: translateY()`** at different speeds per layer
- **Sticky sections** for horizontal scroll effects within vertical scroll
- **Opacity transitions** tied to scroll position for crossfade between sections

### What to Avoid
- Scroll-jacking (overriding native scroll behavior)
- Too many animations competing for attention
- Heavy 3D that kills mobile performance
- Animation for animation's sake — every motion must serve the narrative

---

## 5. COLOR STRATEGY FOR DARIA

### Her Current Palette (Keep)
- `#C4875A` — warm terracotta clay (primary accent)
- `#2C2018` — bark dark brown (text, dark sections)
- `#E8D5B7` — sand (borders, subtle backgrounds)
- `#FAF6F0` — sand-lt warm cream (light backgrounds)
- `#7C9B7A` — muted sage green (secondary accent)

### Cinematic Extensions (Add)
- `#1A1410` — charcoal (immersive dark sections, deeper than bark)
- `#FFF8EF` — warm white (text on dark, creamier than pure white)
- `#C4A35A` — antique gold (cinematic accent, bridges clay and sand)
- `#3D2B1F` — espresso (midpoint between bark and charcoal)

### Color Application
- **Dark sections**: charcoal bg + warm white text + gold accents + clay CTAs
- **Light sections**: cream bg + bark text + clay accents + sage secondary
- **Transitions**: dark→light sections create cinematic rhythm (like scene changes)
- **Gradients**: clay→gold for CTAs, charcoal→transparent for hero overlays

---

## 6. SECTION-BY-SECTION CINEMATIC STRATEGY

### Hero (Scene 1 — The Hook)
- Full viewport, charcoal background
- Film grain texture overlay (CSS noise)
- Text stagger reveal on load (4 lines, 200ms delay each)
- Radial gold glow behind headline
- Scroll indicator with animated line
- No image — typography and atmosphere only

### For Who (Scene 2 — The Mirror)
- Dark background continues
- 3 cards: light text on slightly lighter dark (not pure black)
- Staggered reveal on scroll
- Each card = one client type (sustainable, ethical fashion, values-led)

### Story/About (Scene 3 — The Reveal)
- Transition to light (cream background)
- Editorial layout: photo left, text right
- Gold accent line on photo border
- Pull quote from Daria in large serif

### Preview Grid (Scene 4 — The Proof)
- Back to dark
- 9 branded content-type tiles (no stock photos)
- Her gradients only — clay, sand, sage, gold
- Hover: subtle scale + glow

### Process (Scene 5 — The Path)
- Light background
- 3 steps with gold timeline connector
- Minimal, clean, editorial

### Pricing (Scene 6 — The Investment)
- Dark background
- 3 tiers, center tier featured (gold border, "Most Popular")
- Clean typography, no decoration

### CTA + Forms (Scene 7 — The Close)
- Dual CTA: "Apply" (serious) + "Free Audit" (warm lead)
- Light background for forms
- Dark for CTA banner

---

## 7. TECHNICAL APPROACH

### Stack
- Pure HTML/CSS/JS — no frameworks, no dependencies
- Google Fonts: Cormorant Garamond + Inter
- CSS custom properties for all tokens
- IntersectionObserver for scroll reveals
- CSS animations for hero load sequence
- No WebGL, no Three.js — performance-first

### Performance Budget
- < 50KB HTML/CSS (no external CSS frameworks)
- No images in hero (CSS gradients + typography only)
- System font fallback if Google Fonts fail
- 60fps animations only (transform + opacity only, no layout triggers)
- Mobile-first: all animations reduce on `@prefers-reduced-motion`

### Browser Support
- Modern browsers (Chrome, Safari, Firefox, Edge)
- Graceful degradation: no animation = still looks great
- Mobile: all scroll effects work on touch

---

## 8. WHAT MAKES THIS CINEMATIC (NOT JUST "PREMIUM")

1. **Narrative arc** — beginning (hook), middle (proof), end (CTA)
2. **Pacing** — dark/light alternation creates rhythm like scene changes
3. **Typography as voice** — Cormorant Garamond at display sizes IS the brand
4. **Atmosphere** — film grain, glow effects, generous negative space
5. **Restraint** — only 2-3 "wow" moments, everything else is clean editorial
6. **Scroll as film** — each scroll reveals the next "frame" of the story
7. **Color as emotion** → dark = intimate, light = open, gold = premium

---

## 9. ANTI-PATTERNS (WHAT WE'RE NOT DOING)

- ❌ Centered hero with equal margins and a stock photo
- ❌ Generic glossy gradients
- ❌ Bad anatomy (AI-generated people)
- ❌ Over-saturated lighting
- ❌ Scroll-jacking
- ❌ 3D for 3D's sake
- ❌ Fake testimonials
- ❌ Lorem ipsum
- ❌ More than 2 typefaces
- ❌ More than 3 colors (plus neutrals)
- ❌ Animation that doesn't serve the narrative
- ❌ Heavy frameworks (React, Vue, etc. for a landing page)

---

## 10. SUCCESS CRITERIA

- **8.0+ on self-assessment** before shipping
- **< 3 second load** on 4G
- **60fps** on mid-range devices
- **Mobile-first** — looks intentional on phone, not broken
- **Narrative clarity** — someone understands what Daria does within 5 seconds
- **Emotional response** — "this feels different" not "this looks nice"
