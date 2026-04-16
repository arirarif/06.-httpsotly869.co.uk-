# Woodmart Theme Settings — OTLY 869 Configuration Guide

**Site:** otly869.co.uk &nbsp;|&nbsp; **Theme:** WoodMart v6.4.1 &nbsp;|&nbsp; **Date:** April 17, 2026

> ⚠️ **Before saving:** PHP Max Input Vars is currently set to **1000** — increase to **2000** in cPanel → PHP Settings first, otherwise large settings pages may silently drop data.

---

## 1. Styles and Colors → Colors

| Setting | Current | Change To |
|---|---|---|
| Primary color | 🟢 Green | `#000000` — Pure Black |
| Secondary color | 🟡 Yellow/Amber | `#424242` — Charcoal |
| Mobile browser top bar color | *(empty)* | `#fbf9f2` — Warm Off-White |

---

## 2. Typography → Basic

**Path:** WoodMart → Theme Settings → Typography → Basic

### Current state (from screenshot)
| Setting | Current Font | Weight | Size | Notes |
|---|---|---|---|---|
| Text font (body) | Lato | Normal 400 | 15px | Used for all general content |
| Title font (h1–h6) | Poppins | Semi-Bold 600 | — | Used for all headings |
| Entities names font | Poppins | Medium 500 | — | Product/post/category names |
| Secondary font | Lato | Normal 400 | — | Page builder secondary elements |
| Widget titles font | Poppins | Semi-Bold 600, Uppercase | 16px | Sidebar/widget headings |
| Header font | Lato | Bold 700, Uppercase | 13px | Navigation/header elements |

### ✅ Change to
| Setting | New Font | Weight | Size | Color | Notes |
|---|---|---|---|---|---|
| Text font (body) | **Inter** | Normal 400 | **15px** | `#5f5e5e` | Keep size, swap font only |
| Title font (h1–h6) | **Space Grotesk** | **Bold 700** | — | `#1b1c18` | Letter-spacing: -0.03em via Custom CSS |
| Entities names font | **Space Grotesk** | **Medium 500** | — | `#1b1c18` | Product titles, category names |
| Secondary font | **Inter** | Normal 400 | — | — | Page builder fallback |
| Widget titles font | **Space Grotesk** | **Semi-Bold 600**, Uppercase | **14px** | `#000000` | Reduce size slightly |
| Header font | **Space Grotesk** | **Bold 700**, Uppercase | **13px** | `#000000` | Keep size, swap font |

**Important:** After changing fonts in Typography, also go to **Typography → Advanced** and add a custom rule to apply `-0.03em` letter-spacing to `h1, h2, h3` — Woodmart's basic tab doesn't have a letter-spacing field.

---

## 3. Styles and Colors → Buttons

**Path:** WoodMart → Theme Settings → Styles and Colors → Buttons

### Current state (from screenshot)
| Setting | Current Value | Notes |
|---|---|---|
| Default buttons style | **FLAT** ✅ | Correct — keep |
| Default buttons background | Empty/transparent | Needs updating |
| Default buttons hover background | Light gray | Needs updating |
| Default buttons text color scheme | **Dark** | Correct — keep |
| Default buttons hover text color scheme | **Dark** | Correct — keep |
| Accent buttons style | **3D BUTTON** ❌ | Wrong — must change to FLAT |
| Accent buttons background | 🟢 Green | Wrong — must change |
| Accent buttons hover background | 🟢 Green | Wrong — must change |
| Accent buttons text color scheme | **Light** ✅ | Correct — keep (white text on black) |
| Accent hover buttons text color scheme | **Light** ✅ | Correct — keep |

### ✅ Change to
| Setting | New Value | Notes |
|---|---|---|
| Default buttons style | **FLAT** | No change needed |
| Default buttons background | `#f0eee7` | Surface taupe — ghost/secondary buttons |
| Default buttons hover background | `#e4e2dc` | Slightly darker surface |
| Default buttons text color scheme | **Dark** | No change needed |
| Accent buttons style | **FLAT** | ← **Critical change** — removes fake 3D shadow |
| Accent buttons background | `#000000` | Pure black |
| Accent buttons hover background | `#1b1b1b` | Near-black — subtle darkening effect |
| Accent buttons text color scheme | **Light** | White text on black — no change needed |
| Accent hover buttons text color scheme | **Light** | No change needed |

**Why 3D → FLAT matters:** The 3D button style adds a bottom shadow that looks cheap on editorial/fashion brands. FLAT is required for the clean, square CTA aesthetic in the OTLY mockup.

---

## 4. Styles and Colors → Page Background

**Path:** WoodMart → Theme Settings → Styles and Colors → Page Background

### ✅ Set to
| Setting | Value |
|---|---|
| Page background color | `#fbf9f2` (Warm Off-White) |
| Background pattern | None |

---

## 5. Styles and Colors → Links

**Path:** WoodMart → Theme Settings → Styles and Colors → Links

### ✅ Set to
| Setting | Value |
|---|---|
| Link color | `#000000` |
| Link hover color | `#5f5e5e` |
| Link decoration | None (underline only on explicit text links via CSS) |

---

## 6. Shop → Product Archive

**Path:** WoodMart → Theme Settings → Shop → Product Archive

### ✅ Recommended settings
| Setting | Value | Notes |
|---|---|---|
| Products per row (desktop) | 4 | Standard fashion grid |
| Products per row (tablet) | 2 | |
| Products per row (mobile) | 2 | Allows visual browsing |
| Image size | Crop to 3:4 ratio | Portrait product images |
| Product card hover | Second image | Shows back/alt view on hover |
| Add to cart button | Show on hover | Keeps grid clean |
| Product title font | Space Grotesk Bold | Applied via Typography above |
| Sale badge style | Flat / Pill | Match brand |

---

## 7. Single Product

**Path:** WoodMart → Theme Settings → Single Product

### ✅ Recommended settings
| Setting | Value | Notes |
|---|---|---|
| Product layout | Default (or use Single Product Builder for PDP rebuild) | |
| Gallery type | **Extended** or **Default** | Enables multiple images + thumb strip |
| Gallery position | Left thumbnails (vertical strip) | Matches Zalando/OTLY mockup layout |
| Gallery thumbnails direction | **Vertical** | Left strip, scrolls down |
| Main image click action | **Zoom** or **Lightbox** | Enables full-product view |
| Sticky add-to-cart | **Enabled** | Keeps buy button visible on scroll |
| Sticky summary column | **Enabled** (desktop only) | Right column stays visible while scrolling gallery |
| Variation swatches | **Enabled via WooCommerce Variation Swatches** | Color circles + text for size |

---

## 8. Custom CSS

**Path:** WoodMart → Theme Settings → Custom CSS

Paste the following CSS block after configuring all settings above. This applies the OTLY 869 design system details that Woodmart's settings panels cannot control:

```css
/* ================================================
   OTLY 869 — Custom CSS Overrides
   Applied on top of Woodmart Theme Settings
   ================================================ */

/* ── Google Fonts Load ── */
@import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&family=Inter:wght@300;400;500;600;700&display=swap');

/* ── Heading letter-spacing (Woodmart has no field for this) ── */
h1, h2, h3, h4, h5, h6,
.product_title,
.woodmart-title {
  font-family: 'Space Grotesk', sans-serif;
  letter-spacing: -0.03em;
  line-height: 1.05;
}

/* ── Body text ── */
body,
p,
.woocommerce-product-details__short-description {
  font-family: 'Inter', sans-serif;
  color: #5f5e5e;
  line-height: 1.65;
}

/* ── Product price ── */
.price,
.woocommerce-Price-amount {
  font-family: 'Space Grotesk', sans-serif;
  font-weight: 400;
  color: #4c4546;
}

/* ── Size/variation labels — uppercase tracking ── */
.variations label,
.single_variation_wrap label,
.woodmart-variation-title {
  font-family: 'Inter', sans-serif;
  font-size: 9px;
  font-weight: 700;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: #000000;
}

/* ── Size selector chips — square, not rounded ── */
.variations select,
.woodmart-size-guide-btn,
.wc-pao-addon-field {
  border-radius: 0 !important;
}

/* ── CTA button — square, all-caps, no 3D shadow ── */
.single_add_to_cart_button,
.button.alt,
button[type="submit"] {
  font-family: 'Space Grotesk', sans-serif !important;
  font-weight: 700 !important;
  letter-spacing: 0.15em !important;
  text-transform: uppercase !important;
  border-radius: 0 !important;
  box-shadow: none !important;
  background: #000000 !important;
  color: #ffffff !important;
  padding: 18px 32px !important;
  transition: opacity 0.2s ease !important;
}
.single_add_to_cart_button:hover,
.button.alt:hover {
  opacity: 0.88 !important;
  background: #000000 !important;
  box-shadow: none !important;
  transform: none !important;
}

/* ── Breadcrumb ── */
.woocommerce-breadcrumb,
.breadcrumb-nav {
  font-family: 'Inter', sans-serif;
  font-size: 9px;
  font-weight: 400;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: #5f5e5e;
}
.woocommerce-breadcrumb a {
  color: #5f5e5e;
}
.woocommerce-breadcrumb a:hover {
  color: #000000;
}

/* ── Gallery thumbnails — clean border, no shadow ── */
.woocommerce-product-gallery__image,
.flex-viewport,
.woodmart-product-gallery__wrapper img {
  border-radius: 0 !important;
}
.woocommerce-product-gallery .flex-control-thumbs li img {
  border-radius: 0 !important;
  border: 2px solid transparent !important;
  transition: border-color 0.15s ease !important;
}
.woocommerce-product-gallery .flex-control-thumbs li img.flex-active,
.woocommerce-product-gallery .flex-control-thumbs li img:hover {
  border-color: #000000 !important;
}

/* ── Tab navigation — minimal underline style ── */
.woocommerce-tabs ul.tabs li a {
  font-family: 'Inter', sans-serif;
  font-size: 9px;
  font-weight: 700;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: #5f5e5e;
  background: transparent !important;
  border: none !important;
  border-bottom: 2px solid transparent !important;
  padding: 16px 24px !important;
}
.woocommerce-tabs ul.tabs li.active a {
  color: #000000 !important;
  border-bottom-color: #000000 !important;
}

/* ── Related products heading ── */
.related h2,
.upsells h2 {
  font-family: 'Space Grotesk', sans-serif;
  font-size: clamp(24px, 3vw, 32px);
  font-weight: 700;
  letter-spacing: -0.03em;
  color: #000000;
}

/* ── Announcement bar (if using Woodmart's top bar) ── */
.woodmart-top-bar,
.wd-header-bar {
  background: #000000 !important;
  color: #ffffff !important;
  font-family: 'Inter', sans-serif !important;
  font-size: 9px !important;
  letter-spacing: 0.2em !important;
  text-transform: uppercase !important;
}

/* ── Reduced motion guard ── */
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
  }
}
```

---

## 9. WooCommerce → Variation Swatches

If using a swatches plugin (recommended: **WooCommerce Variation Swatches by Iconic** — free tier works):

| Setting | Value |
|---|---|
| Colour swatch shape | Circle |
| Size swatch shape | Square (no radius) |
| Out-of-stock display | Show crossed out |
| Selected state | Black outline ring |

---

## 10. Save Order

Follow this exact save sequence to avoid conflicts:

1. **Typography** → Save
2. **Styles and Colors → Colors** → Save  
3. **Styles and Colors → Buttons** → Save  
4. **Styles and Colors → Page Background** → Save  
5. **Custom CSS** → paste block above → Save  
6. Clear LiteSpeed Cache (visible in WP sidebar) after all saves

---

## Quick Diff Summary

| What | Before | After |
|---|---|---|
| Primary color | 🟢 Green | ⚫ `#000000` |
| Secondary color | 🟡 Yellow | ⬛ `#424242` |
| Body font | Lato | **Inter** |
| Heading font | Poppins | **Space Grotesk** |
| Accent button style | 3D Button | **Flat** |
| Accent button bg | Green | **`#000000`** |
| Page bg | Default white | **`#fbf9f2`** |
| Button radius | Rounded | **0px (square)** |

---

**File Owner:** Arira (Fiverr delivery for OTLY 869)  
**Version:** 1.0  
**Date:** April 17, 2026
