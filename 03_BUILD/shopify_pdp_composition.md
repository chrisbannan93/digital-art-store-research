# Shopify PDP Composition Notes (Implementation Order)

## Required section order in Shopify theme editor
1. `pdp-hero-offer`
2. `pdp-gallery`
3. `pdp-how-it-works`
4. `pdp-whats-included`
5. `pdp-print-confidence`
6. `pdp-size-ratio-chart`
7. `pdp-trio-value`
8. `pdp-faq`
9. `pdp-license`
10. `pdp-support-guarantee` (lower PDP placement)

## Required vs optional
- **Required for all SKUs**
  - `pdp-hero-offer`
  - `pdp-gallery`
  - `pdp-how-it-works`
  - `pdp-whats-included`
  - `pdp-print-confidence`
  - `pdp-size-ratio-chart`
  - `pdp-faq`
  - `pdp-license`
  - `pdp-support-guarantee`
- **Optional**
  - `pdp-trio-value` (show only when Trio is available)

## Trio-only section
- `pdp-trio-value` is Trio-only.
- In `pdp-hero-offer`, set `offer_mode` to `both` when a page supports Single and Trio selector logic.

## Mobile ordering considerations
- Keep identical section order as desktop.
- Keep hero trust cluster expanded on mobile (do not collapse digital-only, support SLA, support-first line).
- Keep micro-badges and mini “what you get” lines above fold where possible.

## Sticky CTA usage notes
- Use theme-level sticky mobile CTA with:
  - `{{PRICE}}`
  - selected set (`Single` or `Trio`)
  - primary CTA button
- Keep `Digital download only. No physical item is shipped.` visible near hero price and trust cluster (not hidden in accordion).
- Place support-first content in two places:
  - Near CTA in `pdp-hero-offer` trust cluster
  - Lower PDP in `pdp-support-guarantee`
