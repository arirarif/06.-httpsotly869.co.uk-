# Google Stitch Brief - OTLY 869 Single Product Page (Woodmart-Compatible)

## Project context
Create a visual mockup for ONE single product page only.
This is not a full website redesign.
The real site uses WooCommerce + Woodmart, so the design must be realistic for that structure.

## Business constraints
- Budget-sensitive implementation (target low-cost changes only).
- Keep existing Woodmart ecosystem and page architecture.
- Focus on conversion improvements and gallery experience.

## Primary objective
Design a premium but practical single product page that solves:
- "Gallery feels clunky"
- "Need fuller product view like modern fashion ecommerce PDP"

## Visual direction
- Keep OTLY 869 tone: premium, calm, purposeful, not flashy.
- Dark-on-light or light-neutral base acceptable, but avoid neon or overly experimental styling.
- Product imagery must be the hero.
- Typography should prioritize readability and scan speed.

## Required page structure (top to bottom)
1. Breadcrumb row
2. Product top section (2-column desktop, stacked mobile)
   - Left: large gallery area with clear thumbnail strip
   - Right: title, price, short copy, size/color selectors, quantity, add-to-basket
3. Trust micro-block directly below add-to-basket
4. Product details tabs/accordion block
5. Related products strip/grid

## Top section detailed requirements

### Gallery (left)
- Very large primary image frame.
- Secondary thumbnails visible without tiny click targets.
- Clear active thumbnail state.
- "Click to enlarge" affordance visible.
- Must feel suitable for apparel where users need to inspect front/side/back views.

### Summary + CTA (right)
- Product title.
- Price and optional sale style.
- Short product summary (2-3 lines).
- Size options as clear chips/buttons.
- Color options as swatches.
- Quantity stepper + strong Add to Basket button.
- Secondary wishlist action.
- Meta row (SKU/category) kept subtle.

## Trust micro-block (below CTA)
Use 3 concise reassurance items with icons:
- Made to order
- Free UK shipping over GBP75
- Secure checkout

## Details block
Desktop: tabs.
Mobile: accordion.
Tabs/sections:
1. Description
2. Additional Information
3. Shipping & Returns
4. Reviews

## Related products block
- Clean card grid with image, name, price, and compact CTA.
- Keep this section visually secondary to main PDP conversion actions.

## Mobile rules
- Preserve image prominence on first screen.
- Keep variant selectors easy to tap.
- Ensure Add to Basket remains easy to reach.
- Avoid long walls of text before key CTA.

## Copy tone examples
- Title area tone: straightforward and premium.
- Description tone: concise first, story second.
- CTA text: "Add to Basket".
- Microcopy: "Made to order to reduce overproduction."

## Component realism constraints
Design only components that Woodmart/WooCommerce can reasonably support without custom app rebuild:
- Product gallery
- Variations (size/color)
- Quantity + add to cart
- Wishlist
- Tabs/accordion
- Related products

## Deliverables expected from Stitch
- One desktop PDP mockup
- One mobile PDP mockup
- Clear component hierarchy suitable for implementation in Woodmart layout builder

## Source references used
- Client site: https://otly869.co.uk/
- Client PDP examples:
  - https://otly869.co.uk/product/otly-869-disco-tee/
  - https://otly869.co.uk/product/short-sleeve-unisex-t-shirt/
  - https://otly869.co.uk/product/dad-hat/
- Woodmart docs:
  - https://xtemos.com/docs-topic/single-product-page-builder/
- Woodmart demo PDP references:
  - https://woodmart.xtemos.com/shop/furniture/eames-lounge-chair/
  - https://woodmart.xtemos.com/shop/furniture/reflect-chest-of-drawers/
  - https://woodmart.xtemos.com/shop/accessories/iphone-dock/demo/architecture-studio/

## Notes
Client screenshot URLs were provided but automated scrape was blocked by redirect. Keep these as manual visual references:
- https://prnt.sc/I7DJswXUPBiL
- https://prnt.sc/2iZDUkb48c3n
- https://prnt.sc/OsnTSpxR9qJO
- https://prnt.sc/ClHIO1DjkDhJ