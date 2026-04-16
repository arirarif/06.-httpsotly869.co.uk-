# Implementation Notes - Single Product First (Woodmart)

## Scope lock
This phase covers single product layout only.
No full-site redesign.

## Practical implementation sequence
1. Create new Woodmart Single Product Layout in dashboard.
2. Rebuild top section with larger media focus and cleaner summary column.
3. Ensure variation selectors (size/color) are clear and above CTA.
4. Add trust chip row below add-to-basket.
5. Configure tabs/accordion with shipping and returns content.
6. Keep related products section but reduce visual noise.
7. QA desktop/mobile and handoff screenshots to client.

## Suggested low-cost plugin/helper candidates (only if needed)
- Variation swatches plugin (if current swatches are weak).
- Product gallery/video enhancement plugin (only if Woodmart native gallery cannot meet UX target).
- Keep plugin count minimal to avoid maintenance overhead.

## QA checklist for this phase
- Gallery: user can understand product angles/colors quickly.
- Variants: size and color are obvious and tappable.
- CTA: add-to-basket visible without scrolling fatigue.
- Trust: shipping/returns/checkout reassurance is near purchase action.
- Mobile: no cramped controls, no accidental taps.
- Performance: no heavy visual scripts that degrade speed.

## Handoff checklist to client
- Before/after screenshots of current vs new PDP.
- 5-7 bullet UX wins tied to conversion friction removed.
- Clarify that structure remains Woodmart-native for budget safety.
- List optional phase-2 items (greeting card PDP + Prodigi setup).