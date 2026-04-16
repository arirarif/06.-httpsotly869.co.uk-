# Woodmart Single Product Blueprint (OTLY 869)

## Goal
Create a high-converting single product layout using existing Woodmart/WooCommerce structure only (no full redesign), with major focus on gallery UX and variant clarity.

## Confirmed Woodmart capabilities (from docs + demos)
- Native single product layout builder with condition rules.
- Product gallery block with multiple images and enlarge behavior.
- Product title, price, rating, breadcrumbs, short description, meta.
- Variable product add-to-cart form.
- Wishlist/compare buttons.
- Size guide support.
- Product tabs (description, additional info, reviews, custom tab).
- Frequently bought together support.
- Related/upsell products blocks.
- Brand/social/product navigation elements.

## Current OTLY PDP elements observed
- Product title + price + variation selectors.
- Qty + add to basket.
- Wishlist and share links.
- Long product description + details.
- Additional information and reviews tabs.
- Related products.
- Multi-image product set already present.

## Key UX gap to solve first
- Client perceives gallery as clunky and not giving enough full-product confidence.
- Must move toward "full view of product" feel (client mentioned Zalando style reference).

## Recommended Woodmart-native single product layout

### Above the fold
- Left: large media area (dominant visual priority).
- Right: sticky summary column on desktop.
- Include:
  - Product title
  - Price and sale indicator (if applicable)
  - Optional rating count
  - Short description (2-3 lines)
  - Size selector (button-style)
  - Color swatches
  - Qty + Add to basket primary CTA
  - Wishlist secondary action
  - 3 trust chips below CTA

### Trust chips under CTA
- Made to order
- Free UK shipping over GBP75
- Secure checkout

### Mid-page
- Tabs as accordion on mobile, tabs on desktop.
- Tab order:
  1) Description
  2) Product details / additional info
  3) Shipping and returns (custom tab)
  4) Reviews

### Bottom
- Related products in a clean grid (4 desktop, 2 tablet, 1-2 mobile).
- Optional: Frequently Bought Together (for accessories/cards later).

## Layout/behavior settings to implement in Woodmart (practical)
- Use Single Product Layout Builder and apply condition to apparel products first.
- Set gallery mode to maximize image visibility (large main image + clear thumbs).
- Keep sticky summary enabled on desktop to prevent add-to-cart loss.
- Keep variation selection above add-to-cart.
- Ensure mobile gallery swipe and thumb targeting is easy.
- Add custom trust microcopy block under CTA.

## Mobile-critical behavior
- Sticky bottom add-to-cart bar (if available in current stack) or maintain CTA in first viewport after media.
- Size and color selectors must be tappable with clear active state.
- Description starts concise, with progressive disclosure.

## Low-cost implementation approach (aligned with GBP200 cap)
- No custom theme rebuild.
- Prefer Woodmart built-ins + minimal CSS adjustments.
- Add only essential plugin support if a must-have interaction is missing.

## Prioritized backlog (single product only)
1. Rebuild PDP structure with Woodmart layout builder.
2. Improve gallery visual hierarchy and thumbnail clarity.
3. Improve variant selector UX (size/color readability).
4. Add trust chips and shipping/returns reassurance near CTA.
5. Refine tabs/accordion information architecture.
6. Tune related products for cleaner scan.

## Success criteria
- Faster image understanding (desktop and mobile).
- Fewer interactions needed to select variant and add to basket.
- Increased confidence before checkout due to visible trust cues.
- Better parity with modern PDP expectations without replacing theme.