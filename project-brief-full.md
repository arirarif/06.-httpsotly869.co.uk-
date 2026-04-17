# OTLY 869 — Full Project Brief & Requirements

**Client:** Zionw (UK)  
**Site:** https://otly869.co.uk  
**Budget:** £200 strict cap (Fiverr order)  
**Platform:** WooCommerce + WoodMart v6.4.1 + Printful (POD)  
**Date:** April 17, 2026

---

## 1. What the Client Asked For (Original Job Post)

> "I'm looking for a WooCommerce UX/UI expert who can review and improve my existing store, primarily to enhance conversions."

### Scope of Work (from listing)
- Review and optimize **product detail pages (PDP)** for better conversion rates
- Enhance **product visibility and checkout process** to reduce drop-off
- Provide advice on **integrating Prodigi** for greeting card sales
- Focus on **low-cost improvements without a full rebuild**
- Review current connection with **Printful** and ensure optimization

### Budget & Constraints
- **£200 strict** — cannot be exceeded
- No full redesign — improvements only
- Assumes it can be done using suitable plugins
- Client expects to see a **mockup** before implementation
- Must be **responsive during UK daytime hours** with regular updates
- Client is UX-focused — "I need someone who is UX-focused, not just a developer who will churn out a page"
- Previous Fiverr experience wasn't great — client will be honest if unhappy

---

## 2. What the Client Specifically Wants (From Chat Messages)

### Priority 1 — Better Gallery / Product Page UX
> "I like Zalando's product page as it gives me a full view of the product, in comparison to mine, which is clunky."

- Current PDP: https://otly869.co.uk/product/otly-869-rb-heritage-tee/
- **Main complaint:** Gallery feels clunky, doesn't give full product view confidence
- **Inspiration:** Zalando-style PDP with large clear images and easy browsing
- Screenshots provided:
  - https://prnt.sc/I7DJswXUPBiL (Zalando reference)
  - https://prnt.sc/2iZDUkb48c3n (Zalando reference)

### Priority 2 — Greeting Card Product Page
- Wants to add **static greeting cards** (not customizable initially)
- Cards will use **Prodigi** integration (not Printful)
- Mockup screenshots:
  - https://prnt.sc/OsnTSpxR9qJO
  - https://prnt.sc/ClHIO1DjkDhJ
- "They will be static — what the customer sees, they buy. Customisation is too complex, but I won't rule out that option."

### Priority 3 — Prodigi Integration
- Currently set up with Printful for apparel
- Wants Prodigi added for greeting cards
- Needs site setup recommendations for this

### Client's Exact Words
- "I have a domain and hosting, I just want a better gallery view and potentially a product page for my greeting cards"
- "I want improvements made to my existing page, plus potentially an additional page for greeting cards"
- "I would love to see a mockup of the product page"

---

## 3. Brand Context

### Brand Identity
- **Name:** OTLY 869
- **Tagline:** "Wear Your Resolve."
- **Positioning:** Affirmation-led apparel inspired by Caribbean heritage, resilience, identity, and music culture
- **Name origin:** 869 = St Kitts country dial code, tied to founder's heritage
- **Story:** Brand born from a difficult personal period — founder reconnected with roots and created purposeful streetwear
- **Tone:** Reflective, purposeful, emotional but grounded, premium not flashy

### Products Currently Sold
| Product | Category | Price |
|---|---|---|
| R&B Heritage Tee | T-Shirts | £29.00 |
| Disco Tee | T-Shirts | £29.99 |
| "Buried in Doubt" Graphic Tee | T-Shirts | £29.99–£31.99 |
| Heritage 869 T-shirt | T-Shirts | varies |
| Dad Hat | Accessories | £20.00 |
| Snapback Hat | Accessories | £17.00 |

- All apparel is **variable products** (size + color variants)
- Fulfilled via **Printful** (print-on-demand)
- Each product has **multi-angle images** per color variant

### Trust Signals on Site
- "Made to order" (waste reduction messaging)
- "Premium quality"
- "Secure checkout"
- "Free UK shipping over £75" (header banner)

### Contact Info
- Phone: 07909 667 085
- Email: customer@otly869.co.uk

---

## 4. Current Site Problems (Why Client Is Unhappy)

1. **Gallery is "clunky"** — doesn't give full product view confidence like Zalando
2. **PDP visual experience** doesn't match the premium storytelling on the homepage
3. **Variant selection UX** (size/color) isn't clear enough for confident purchase
4. **No trust reassurance near the CTA** — shipping, returns, secure checkout info is scattered
5. **Mobile PDP** likely has scrolling fatigue before reaching Add to Basket
6. **Green primary color + 3D button style** feels cheap — doesn't match premium brand intent
7. **Fonts (Lato/Poppins)** are generic — need editorial fashion typefaces

---

## 5. What Needs to Be Delivered

### Deliverable A — Single Product Page Mockup ✅ (Done)
- Desktop + mobile HTML mockup showing redesigned PDP
- Built as self-contained HTML with Tailwind CSS
- Files: `index.html`, `code/single-product-mockup.html`, `code/single-product.md`
- Design system: `design-system.md`

### Deliverable B — Woodmart Implementation Guide ✅ (Done)
- Step-by-step settings changes for Woodmart admin panel
- Custom CSS overrides for the design system
- File: `web/woodmart-settings-guide.md`

### Deliverable C — Apply Changes to Live Site (Pending)
Using Woodmart's existing tools (no custom theme rebuild):

1. **Typography swap** — Lato/Poppins → Inter/Space Grotesk
2. **Color swap** — Green primary → Black (#000000)
3. **Button style** — 3D → Flat, square, black
4. **Page background** — White → Warm off-white (#fbf9f2)
5. **Gallery layout** — Switch to extended/vertical thumbnail strip (Zalando-style)
6. **Sticky summary column** — Enable on desktop so CTA stays visible
7. **Variation swatches** — Color circles + square size chips with clear active states
8. **Trust chips block** — Add 3 trust items below Add to Basket (Made to order / Free shipping / Secure checkout)
9. **Tab cleanup** — Description, Additional Info, Shipping & Returns, Reviews
10. **Custom CSS** — Full override block from design system
11. **Mobile optimization** — Ensure gallery swipe, tappable selectors, CTA reachable without scroll fatigue

### Deliverable D — Greeting Card Page (Optional/Phase 2)
- New product category for static greeting cards
- Simpler variant structure (no size/color matrix — just buy as-is)
- Visual-first card preview with finish/size details
- Prodigi integration setup

### Deliverable E — Prodigi Integration (Optional/Phase 2)
- Connect Prodigi to WooCommerce for greeting card fulfillment
- Printful stays for apparel
- Site setup recommendations for dual-POD workflow

---

## 6. PDP Layout Blueprint (What the Redesign Looks Like)

### Desktop (≥1024px) — Two Column
```
Left Column (58%)                Right Column (42%) — sticky
├── Vertical thumbnail strip     ├── Product title (Space Grotesk 48px)
│   88px wide, 12px gap          ├── Price (Space Grotesk 24px)
├── Main hero image              ├── Short description (2-3 lines)
│   flex:1, aspect 3:4           ├── Color swatches (circle)
│   cursor: zoom-in              ├── Size chips (square, 48×48px)
                                 ├── Qty stepper + ADD TO BASKET
                                 ├── Save to Wishlist link
                                 ├── Trust chips (3 items)
                                 │   • Made to order
                                 │   • Free UK shipping over £75
                                 │   • Secure checkout
                                 └── SKU / Category meta (subtle)
```

### Below the Fold
```
├── Tabs (desktop) / Accordion (mobile)
│   1. Description
│   2. Additional Information
│   3. Shipping & Returns
│   4. Reviews
├── Related Products (4-col grid)
└── Footer
```

### Mobile (<1024px)
```
├── Full-width hero image (4:5)
├── Horizontal thumbnail strip (scroll)
├── Product title (36px)
├── Price
├── Color swatches
├── Size chips (flex-wrap)
├── Trust chips (condensed)
├── Accordion (Description / Shipping / Returns)
├── Related products (horizontal scroll)
└── Fixed bottom bar: price + "ADD TO BASKET" (backdrop-blur)
```

---

## 7. Design System Summary

| Token | Value | Usage |
|---|---|---|
| Primary | `#000000` | CTAs, headings, nav |
| Surface | `#fbf9f2` | Page background |
| Surface-3 | `#f6f4ec` | Section bg, thumbnail bg |
| Text | `#1b1c18` | Headings |
| Text-2 | `#5f5e5e` | Body text |
| Outline | `#cfc4c5` | Borders |
| Heading font | Space Grotesk 700 | Titles, prices, buttons |
| Body font | Inter 400 | Copy, labels, UI |
| Label style | Inter 700, uppercase, 0.2em tracking | Tags, breadcrumbs |
| Button | Flat, square (0px radius), black bg, white text |
| Spacing | 4px grid only: 4/8/12/16/24/32/48/64/96/128 |
| Radius | 0px on gallery, CTAs, size chips; pill on badges |
| Image ratio | 3:4 portrait (all products) |

---

## 8. Woodmart Settings Changes (Quick Reference)

| Setting | Before | After |
|---|---|---|
| Primary color | Green | `#000000` |
| Secondary color | Yellow | `#424242` |
| Body font | Lato 400 | Inter 400 |
| Heading font | Poppins 600 | Space Grotesk 700 |
| Accent button style | 3D | Flat |
| Accent button bg | Green | `#000000` |
| Page background | White | `#fbf9f2` |
| Gallery type | Default | Extended, vertical thumbs |
| Sticky summary | Off | On (desktop) |
| Sticky add-to-cart | Off | On |

Full settings guide: `web/woodmart-settings-guide.md`

---

## 9. Implementation Priority Order

| # | Task | Effort | Impact |
|---|---|---|---|
| 1 | Gallery layout → vertical thumbs + large hero | Medium | **Highest** (client's #1 complaint) |
| 2 | Typography swap (Inter + Space Grotesk) | Low | High (premium feel) |
| 3 | Color + button style changes | Low | High (removes cheap green 3D look) |
| 4 | Custom CSS overrides (full block) | Low | High (applies design system) |
| 5 | Variation swatches (color circles + size squares) | Medium | High (purchase confidence) |
| 6 | Trust chips below CTA | Low | Medium (reduces checkout anxiety) |
| 7 | Sticky summary + mobile bottom bar | Low | Medium (keeps CTA visible) |
| 8 | Tab/accordion cleanup | Low | Low-Medium |
| 9 | Related products styling | Low | Low |
| 10 | Greeting card page + Prodigi (Phase 2) | High | Future revenue |

---

## 10. Files in This Project

| File | Purpose |
|---|---|
| `details.md` | Raw client conversation + job post |
| `design-system.md` | Complete design tokens and component patterns |
| `index.html` | Main PDP mockup (desktop + mobile, Tailwind) |
| `code/single-product-mockup.html` | Same mockup (alternate build) |
| `code/single-product.md` | Full HTML source of both mockup variants |
| `web/woodmart-settings-guide.md` | Step-by-step Woodmart admin settings + CSS |
| `research/brand.md` | Brand identity, tone, audience |
| `research/hero.md` | Above-the-fold and hero analysis |
| `research/products.md` | Product catalog and pricing |
| `research/about.md` | Brand story and CRO implications |
| `research/sections.md` | Homepage section map |
| `research/images.md` | Image URLs and media patterns |
| `research/single-product-stitch-brief.md` | Google Stitch mockup brief |
| `research/implementation-notes-single-product.md` | Implementation sequence |
| `research/woodmart-single-product-blueprint.md` | Woodmart-native layout plan |
| `filter-everything-pro/` | Filter plugin (separate task — custom CSS for shop filters) |
| `project-brief-full.md` | **This file** — complete project summary |

---

## 11. Success Criteria

- [ ] Client can see full product views without gallery feeling "clunky"
- [ ] Gallery mimics Zalando-style: large images, clear thumbs, easy browsing
- [ ] Size and color selection is obvious and tappable (mobile)
- [ ] Add to Basket is always visible/reachable (sticky summary + mobile bar)
- [ ] Trust cues (shipping, returns, secure checkout) are near the CTA
- [ ] Brand feels premium and editorial (not generic WooCommerce)
- [ ] All changes done within Woodmart settings + CSS (no custom theme rebuild)
- [ ] Total cost stays within £200 budget
- [ ] Mobile PDP works smoothly at 375px, 768px, 1024px

---

**Owner:** Arira (Fiverr)  
**Version:** 1.0  
**Date:** April 17, 2026
