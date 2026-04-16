# OTLY 869 Design System

**Brand:** OTLY 869 — Affirmation-Led Apparel  
**Style:** Minimal Dark Luxury / Editorial Streetwear  
**Voice:** "Wear Your Resolve."  
**Last Updated:** April 17, 2026

---

## 🎨 Color Palette

### Core Surfaces
```css
--bg:          #F2F0E9    /* Neutral Bone — Main background (from design system) */
--surface:     #fbf9f2    /* Warm Off-White — Page surface */
--surface-2:   #ffffff    /* Pure White — Cards, product image backgrounds */
--surface-3:   #f6f4ec    /* Light Ecru — Subtle sections, thumbnail bg */
--surface-4:   #f0eee7    /* Taupe — Container bg, dividers */
--surface-5:   #eae8e1    /* Medium Taupe — High-contrast containers */
```

### Brand Colors
```css
--primary:     #000000    /* Pure Black — CTAs, headings, primary UI */
--on-primary:  #ffffff    /* White — Text on primary/black backgrounds */

--secondary:   #424242    /* Charcoal — Secondary buttons, icons */
--secondary-2: #5f5e5e    /* Medium Gray — Body text, secondary UI */

--tertiary:    #D9D7D0    /* Stone Taupe — Dividers, subtle accents, checked states */
--outline:     #cfc4c5    /* Warm Rose-Gray — Borders */
--outline-dim: rgba(207,196,197,0.30)  /* Subtle border tint */
```

### Text Colors
```css
--text:        #1b1c18    /* Deep Ink — Headings, primary text */
--text-2:      #5f5e5e    /* Medium Gray — Body text, secondary copy */
--text-3:      #888E95    /* Light Gray — Labels, captions, meta */
--text-variant:#4c4546    /* Warm Muted — On-surface-variant text */
```

### State Colors
```css
--error:       #ba1a1a    /* Error Red — Form validation */
--error-bg:    #ffdad6    /* Error Background */
--hover-bg:    rgba(0,0,0,0.04)   /* Hover overlay */
```

---

## 📐 Shadows

```css
--shadow-sm:   0 2px 8px rgba(27,28,24,0.05)      /* Subtle lift */
--shadow-md:   0 8px 32px rgba(27,28,24,0.09)     /* Card hover */
--shadow-lg:   0 24px 64px rgba(27,28,24,0.13)    /* Deep elevation */
--shadow-xl:   0 40px 80px rgba(27,28,24,0.16)    /* Modal, overlays */
```

---

## 🔠 Typography

### Font Families
```css
/* Headlines, product titles, CTAs, brand wordmark */
font-family: 'Space Grotesk', sans-serif;
/* Weights: 300 (Light), 400 (Regular), 500 (Medium), 600 (SemiBold), 700 (Bold) */

/* Body copy, labels, UI elements, metadata */
font-family: 'Inter', sans-serif;
/* Weights: 300 (Light), 400 (Regular), 500 (Medium), 600 (SemiBold), 700 (Bold) */
```

### Google Fonts Import
```css
@import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&family=Inter:wght@300;400;500;600;700&display=swap');
```

### Type Scale
```css
.t-9   { font-size: 9px;  }   /* Micro labels, tracking badges, meta */
.t-11  { font-size: 11px; }   /* Small labels, size indicators */
.t-12  { font-size: 12px; }   /* Breadcrumb, legal text */
.t-14  { font-size: 14px; }   /* Body text, captions */
.t-16  { font-size: 16px; }   /* Standard body */
.t-18  { font-size: 18px; }   /* Lead text */
.t-20  { font-size: 20px; }   /* Small headings */
.t-24  { font-size: 24px; }   /* Price, sub-headings */
.t-30  { font-size: 30px; }   /* Section headings */
.t-36  { font-size: 36px; }   /* Product titles (mobile) */
.t-48  { font-size: 48px; }   /* Product title (desktop) */
.t-64  { font-size: clamp(40px, 5vw, 64px); } /* Hero headline (responsive) */
```

### Usage Guidelines

**Headlines (Product Name, Section Titles):**
- Font: Space Grotesk
- Weight: 700 (Bold)
- Letter-spacing: -0.03em to -0.04em (very tight — editorial feel)
- Line-height: 1.0–1.1

**Body Text:**
- Font: Inter
- Weight: 400 (Regular)
- Font-size: 14–16px
- Line-height: 1.6–1.7
- Color: `--text-2` (#5f5e5e)

**Labels (Eyebrows, Size Tags, Tracking):**
- Font: Inter
- Weight: 600–700
- Text-transform: uppercase
- Letter-spacing: 0.15em–0.25em
- Font-size: 9–12px
- Color: `--primary` or `--text-3`

**Buttons:**
- Font: Space Grotesk
- Weight: 700 (Bold) for primary
- Font-size: 13–15px
- Letter-spacing: 0.1em–0.15em
- Text-transform: uppercase

---

## 📏 Spacing System (4px Grid)

```css
--sp-4:    4px
--sp-8:    8px
--sp-12:   12px
--sp-16:   16px
--sp-24:   24px
--sp-32:   32px
--sp-48:   48px
--sp-64:   64px
--sp-96:   96px
--sp-128:  128px
```

### Usage
- **Thumbnail gap:** 8–12px
- **Component gaps:** 12–16px
- **Card padding:** 24px
- **Section padding (desktop):** 64–128px top margin
- **Section padding (mobile):** 48–64px
- **Grid gaps:** 16–24px
- **Button padding:** 14–18px vertical, 24–32px horizontal
- **Announcement bar:** 8px vertical

---

## 🔲 Border Radius

```css
--r-none:  0px      /* Gallery images, main product frames — sharp edges intentional */
--r-sm:    2px      /* Minimal rounding — nav inputs, quantity counters */
--r:       4px      /* Subtle cards */
--r-lg:    8px      /* CTA bar (mobile), some cards */
--r-pill:  100px    /* Tags, badges */
```

### Usage
- **Primary CTA button:** `--r-none` (0px) — editorial/fashion flat aesthetic
- **Mobile bottom bar:** `--r-lg` (8px)
- **Gallery thumbnails:** `--r-none`
- **Product images:** `--r-none`
- **Size selector chips:** `--r-none` (square, brand-consistent)
- **Badges, tags:** `--r-pill`
- **Search inputs:** `--r-sm`

---

## 🎭 Animation & Transitions

### Timing Functions
```css
/* Natural deceleration — reveal, entrance */
cubic-bezier(0.22, 1, 0.36, 1)

/* Sharp exit */
cubic-bezier(0.55, 0, 1, 0.45)
```

### Transition Durations
```css
/* Instant feedback */
150ms  → Size/colour selection, hover color/border changes

/* Smooth transforms */
250ms–300ms  → Card lifts, image scale, nav hover

/* Reveal animations */
500ms–700ms  → Scroll-in reveals, image transitions

/* Gallery swap */
200ms  → Main image opacity fade on thumb click
```

### Common Transitions
```css
/* Button hover */
transition: opacity 0.2s ease;

/* Card image zoom */
transition: transform 0.6s ease;

/* Gallery main image */
transition: opacity 0.2s ease;

/* Colour/border state */
transition: all 0.15s ease;

/* Scroll reveal */
transition: opacity 0.6s ease, transform 0.6s ease;

/* Tab panels */
transition: none; /* instant — no layout shift on tab click */
```

### Respect Reduced Motion
```css
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}
```

---

## 📱 Responsive Breakpoints

```css
/* Mobile-first */
@media (max-width: 480px)  { /* Small phone — hero images, single col */ }
@media (max-width: 640px)  { /* Mobile — hide desktop nav */ }
@media (max-width: 768px)  { /* Tablet — 2-col grids */ }
@media (min-width: 1024px) { /* Desktop — side-by-side PDP layout */ }
@media (min-width: 1280px) { /* Large desktop — wider content, xl type */ }
```

### Container Max-Width
```css
.container {
  max-width: 1440px;
  margin: 0 auto;
  padding: 0 40px;  /* Desktop */
}

@media (max-width: 768px) {
  .container {
    padding: 0 24px;  /* Mobile */
  }
}
```

---

## 🎨 Component Patterns

### Buttons

#### Primary — Add to Basket
```css
.btn-primary {
  font-family: 'Space Grotesk', sans-serif;
  font-size: 14px;
  font-weight: 700;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  color: #ffffff;
  background: #000000;
  padding: 18px 32px;
  border-radius: 0;
  transition: opacity 0.2s ease;
}
.btn-primary:hover {
  opacity: 0.88;
}
```

#### Ghost / Wishlist
```css
.btn-ghost {
  font-family: 'Inter', sans-serif;
  font-size: 9px;
  font-weight: 700;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--text-2);
  padding: 0;
  background: transparent;
  border: none;
  transition: color 0.15s ease;
}
.btn-ghost:hover {
  color: var(--primary);
}
```

### Gallery

#### Thumbnail Strip (Desktop — vertical)
```css
.thumb-strip {
  display: flex;
  flex-direction: column;
  gap: 12px;
  width: 88px;  /* Desktop */
}

.thumb {
  aspect-ratio: 3/4;
  cursor: pointer;
  overflow: hidden;
}

.thumb.is-active {
  outline: 2px solid #000000;
  outline-offset: 2px;
}

.thumb:hover img {
  opacity: 1;
}
```

#### Main Hero Image
```css
.gallery-main {
  flex: 1;
  aspect-ratio: 3/4;
  overflow: hidden;
  background: var(--surface-3);
  cursor: zoom-in;
}

.gallery-main img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: opacity 0.2s ease;
}
```

### Size Selector Chips
```css
.size-btn {
  width: 48px;
  height: 48px;
  border: 1px solid var(--outline);
  font-size: 11px;
  font-weight: 700;
  font-family: 'Space Grotesk', sans-serif;
  color: var(--text-2);
  background: transparent;
  cursor: pointer;
  transition: all 0.15s ease;
}
.size-btn:hover {
  border-color: #000;
  color: #000;
}
.size-btn.is-active {
  background: #000;
  color: #fff;
  border-color: #000;
}
```

### Colour Swatch
```css
.colour-swatch {
  width: 36px;
  height: 36px;
  border-radius: 50%;
  cursor: pointer;
  transition: all 0.15s ease;
}
.colour-swatch.is-active {
  outline: 2px solid #000;
  outline-offset: 3px;
}
```

### Trust Badges
```css
.trust-item {
  display: flex;
  align-items: center;
  gap: 12px;
}
.trust-item .icon {
  font-size: 18px;  /* Material symbol */
  color: var(--text-variant);
}
.trust-item span {
  font-family: 'Inter', sans-serif;
  font-size: 9px;
  font-weight: 400;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  color: var(--text-2);
}
```

### Section Labels (Tabs / Headings)
```css
.section-eyebrow {
  font-family: 'Inter', sans-serif;
  font-size: 9px;
  font-weight: 700;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--primary);
  margin-bottom: 12px;
}

.section-title {
  font-family: 'Space Grotesk', sans-serif;
  font-size: clamp(24px, 3vw, 36px);
  font-weight: 700;
  letter-spacing: -0.03em;
  line-height: 1.05;
  color: var(--text);
  margin-bottom: 48px;
}
```

### Product Card (Related Products)
```css
.product-card {
  cursor: pointer;
}
.product-card .img-wrap {
  aspect-ratio: 3/4;
  background: var(--surface-3);
  overflow: hidden;
  margin-bottom: 16px;
}
.product-card img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.6s ease;
}
.product-card:hover img {
  transform: scale(1.04);
}
.product-card .name {
  font-family: 'Space Grotesk', sans-serif;
  font-size: 14px;
  font-weight: 700;
  color: var(--primary);
  margin-bottom: 4px;
}
.product-card .price {
  font-family: 'Inter', sans-serif;
  font-size: 9px;
  font-weight: 700;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--text-2);
}
```

---

## 🖼️ Image Guidelines

### Product Images
- **Source:** Printful print-on-demand mockups (auto-generated per variant)
- **Format:** JPG/WebP from Printful CDN
- **Aspect ratio:** 3:4 (portrait) — consistent across all product thumbnails
- **Background:** Clean white or neutral studio background
- **Alt text:** Required format: `{brand} {product name} — {variant colour}`

### Hero/Full-width Images
- **Aspect ratio:** 4:5 (mobile hero), 3:4 (desktop main gallery)
- **Object-fit:** cover (always fills container)

### Fallback Images
- Every `<img>` tag must include an `onerror` fallback
- Fallback source: Stitch lh3.googleusercontent.com URLs (already generated)

---

## 📋 PDP Layout Specification

### Desktop (≥1024px)

```
[12-column grid]
├── Col 1–7 (58%): Gallery
│   ├── Vertical thumb strip — 88px wide, gap 12px
│   └── Main hero image — flex: 1, aspect 3:4, sticky scroll
└── Col 8–12 (42%): Summary
    ├── Product title (Space Grotesk, 48px, tracking -0.03em)
    ├── Price (Space Grotesk, 24px)
    ├── Short description (Inter 14px, max-width 360px)
    ├── Colour selector + label
    ├── Size chips + size guide link
    ├── Qty + Add to Basket CTA
    ├── Wishlist link
    └── Trust badges (4 items)
    [position: sticky, top: 104px]
```

### Mobile (<1024px)

```
[Single column]
├── Full-width hero image (aspect 4:5)
├── Horizontal thumbnail strip (overflow-x: scroll, no scrollbar)
├── Product title (Space Grotesk, 36px)
├── Price
├── Colour selector
├── Size chips (2×2 grid or flex wrap)
├── Trust badges (condensed)
├── Details accordion (Description / Shipping / Returns)
├── Related products (horizontal scroll, w-56 cards)
└── [Fixed] Bottom bar: price + "Add to Basket" (backdrop-blur)
```

---

## ♿ Accessibility

### Color Contrast
- **Body text (#5f5e5e on #fbf9f2):** ✅ Passes WCAG AA (≥4.5:1)
- **Headings (#1b1c18 on #fbf9f2):** ✅ Passes WCAG AAA (≥7:1)
- **CTA text (white on #000000):** ✅ 21:1 (maximum)
- **Labels (#5f5e5e on #f6f4ec):** ✅ Passes AA

### Interactive Elements
- `:focus-visible` outline on all interactive elements
- Minimum touch target: 44×44px
- `cursor: pointer` on all clickable elements
- `aria-label` on icon-only buttons

---

## 🏗️ Layout Grid

### Desktop (≥1024px)
```css
/* PDP top section */
grid-template-columns: 7fr 5fr;  /* ~58% gallery / 42% summary */
gap: 80px;

/* Related products */
grid-template-columns: repeat(4, 1fr);
gap: 32px;

/* Footer */
grid-template-columns: 2fr 1fr 1fr;
gap: 48px;
```

### Tablet (≤768px)
```css
/* Related products */
grid-template-columns: repeat(2, 1fr);
gap: 24px;
```

### Mobile (≤640px)
```css
/* Everything single column */
grid-template-columns: 1fr;

/* Related products → horizontal scroll instead */
display: flex;
overflow-x: auto;
gap: 16px;
```

---

## 🎯 OTLY 869 Content Guidelines

### Product Naming
- All caps for brand references: "OTLY 869"
- Title case for product names: "Signature Disco Tee", "R&B Heritage Tee"
- Avoid generic names: not "Black T-Shirt" → "Disco Tee — Black"

### Body Copy
- Keep descriptions emotionally resonant but short (2–3 sentences max)
- Reference cultural anchors: Caribbean heritage, music culture, identity, resilience
- End product copy with a brand sign-off where space allows: **"OTLY 869 — Wear Your Resolve."**

### Labels / Tags
- All uppercase, wide letter-spacing (0.15–0.2em)
- Common: "MADE TO ORDER", "FREE UK SHIPPING OVER £75", "SECURE CHECKOUT"
- Avoid: discount-culture language like "SALE", "50% OFF" — undercuts premium positioning

### Price Format
- UK Pounds, no trailing zeros: `£29.99` not `£29.990`
- From prices: `from £29.99` (when multiple variants)

### CTAs
- Primary: `ADD TO BASKET` (not "Buy Now", not "Add to Cart")
- Secondary: `SAVE TO WISHLIST`
- Size guide: `Size Guide` (sentence case, underlined link)

---

## 🔧 Technical Stack (Mockup)

- **HTML/CSS/JS:** Vanilla (no frameworks)
- **CSS framework:** Tailwind CSS v3 (CDN) — utility-first for rapid mockup
- **Icons:** Material Symbols Outlined (Google Font, weight 300)
- **Fonts:** Google Fonts CDN (Space Grotesk + Inter)
- **Images:** Printful CDN URLs (production), Stitch lh3 fallbacks (mockup)

### Production (WooCommerce / Woodmart)
- Woodmart theme v7.x + WooCommerce
- Woodmart Single Product Builder for layout
- CSS overrides via Woodmart > Custom CSS (scoped to `.product` or `.woocommerce`)
- No jQuery — use Woodmart's existing JS hooks where available

---

## 📋 Quick Reference

### Most Used Colors
```
Primary CTA:        #000000  (--primary)
Page background:    #fbf9f2  (--surface)
Section bg:         #f6f4ec  (--surface-3)
Primary text:       #1b1c18  (--text)
Secondary text:     #5f5e5e  (--text-2)
Borders:            #cfc4c5  (--outline)
Tertiary/Accent:    #D9D7D0  (--tertiary)
```

### Most Used Spacing
```
Card / section gap:    16–24px
Section margin-top:    96–128px (desktop), 48–64px (mobile)
Button padding:        18px × 32px
Trust badge gap:       12px
```

### Most Used Fonts
```
Product title:   Space Grotesk Bold 700, -0.03em tracking
Price:           Space Grotesk Regular 400
Body copy:       Inter Regular 400, 1.65 line-height
Labels/Tags:     Inter Bold 700, uppercase, 0.2em tracking
CTA buttons:     Space Grotesk Bold 700, uppercase, 0.15em tracking
```

### Most Used Transitions
```
Selection state:  150ms ease
Card hover:       250ms ease
Gallery image:    200ms ease (opacity)
Product zoom:     600ms ease (scale)
Scroll reveal:    600ms ease
```

---

## 🚫 Don't Use

- ❌ Arbitrary spacing (17px, 22px, 37px)
- ❌ Purple/pink gradients — wrong brand register
- ❌ Colored CTAs — brand is always black/white
- ❌ Rounded corners on gallery images or size chips — must be sharp
- ❌ More than 2 font families
- ❌ Cheap drop shadows — use flat or very subtle only
- ❌ Snap/bounce animations without easing
- ❌ Missing `prefers-reduced-motion` guard
- ❌ Discount-speak copy: "SALE", "LIMITED TIME ONLY"

---

## ✅ Always Use

- ✅ 4px spacing grid only
- ✅ Sharp corners on interactive product UI (size chips, gallery, CTA)
- ✅ Space Grotesk for all headings, prices, and buttons
- ✅ Inter for body, labels, trust text
- ✅ `object-fit: cover` on all product images with fixed aspect ratio containers
- ✅ `onerror` fallback on every `<img>`
- ✅ `cursor: pointer` on every clickable element
- ✅ Alt text on every product image: `{brand} {product} — {variant}`
- ✅ Mobile bottom action bar on PDP (fixed, backdrop-blur)
- ✅ Semantic HTML throughout

---

**Design System Owner:** OTLY 869 / Arira (Fiverr)  
**Version:** 1.0.0  
**Last Updated:** April 17, 2026  
**Applies To:** PDP mockup · Woodmart CSS overrides · Future page builds
