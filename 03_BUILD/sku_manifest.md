# SKU Manifest (Launch 3)

## Scope lock
- Nursery printable wall kits only.
- Digital-only delivery.
- Offer types used in this manifest: 2 Singles + 1 Trio Kit.

## Product architecture for this scaffold
- **Scaffold choice:** separate products (2 Single products + 1 Trio product) with cross-sell links.
- **If moving to single PDP with variants later:** use variant values `Single` and `Trio Kit`.

---

## SKU 001
- **Internal SKU code:** `NUR-SGL-001`
- **Offer type:** Single (Starter)
- **Public product name:** `{{STYLE}} Nursery Print — {{SUBJECT}} (Printable Wall Art)`
- **Working style/archetype mapping:** `Calm Minimal` / `Soft Neutral Safari`
- **Hook paragraph:**
  - `Create a calm, cohesive nursery corner in minutes with {{STYLE_LOWER}} artwork designed to work beautifully in everyday family spaces. You’ll receive clear files, simple print guidance, and friendly support if you need a hand.`
- **What you get (Single template):**
  - `1 printable art design: {{SUBJECT}}`
  - `1 ZIP folder with all included files`
  - `5 print ratios: 2:3, 3:4, 4:5, 11:14, ISO (A-series)`
  - ``PRINT_ME_FIRST.pdf`` for test printing and setup confidence
  - `Digital download only. No physical item is shipped.`
- **Gallery image list (required order, placeholder filenames):**
  1. `001_01_nursery-hero-mockup.jpg`
  2. `001_02_detail-crop-quality.jpg`
  3. `001_03_whats-included-graphic.jpg`
  4. `001_04_download-print-frame-panel.jpg`
  5. `001_05_size-ratio-chart.jpg`
  6. `001_06_print-me-first-preview.jpg`
  7. `001_07_secondary-lifestyle-angle.jpg`
  8. `001_08_support-license-strip.jpg` (optional)
- **Tags:** `nursery, printable, digital-download, single, starter, 300-dpi, 5-ratios, beginner-friendly, personal-use-only`
- **Collections:** `Nursery Printable Wall Art`, `Single Prints`
- **Variant approach for this SKU:** standalone product; cross-sell to `NUR-SGL-002` and `NUR-TRI-001`.

---

## SKU 002
- **Internal SKU code:** `NUR-SGL-002`
- **Offer type:** Single (Starter)
- **Public product name:** `{{STYLE}} Nursery Print — {{SUBJECT}} (Printable Wall Art)`
- **Working style/archetype mapping:** `Whimsical Storybook` / `Pastel Animal Friends`
- **Hook paragraph:**
  - `Create a calm, cohesive nursery corner in minutes with {{STYLE_LOWER}} artwork designed to work beautifully in everyday family spaces. You’ll receive clear files, simple print guidance, and friendly support if you need a hand.`
- **What you get (Single template):**
  - `1 printable art design: {{SUBJECT}}`
  - `1 ZIP folder with all included files`
  - `5 print ratios: 2:3, 3:4, 4:5, 11:14, ISO (A-series)`
  - ``PRINT_ME_FIRST.pdf`` for test printing and setup confidence
  - `Digital download only. No physical item is shipped.`
- **Gallery image list (required order, placeholder filenames):**
  1. `002_01_nursery-hero-mockup.jpg`
  2. `002_02_detail-crop-quality.jpg`
  3. `002_03_whats-included-graphic.jpg`
  4. `002_04_download-print-frame-panel.jpg`
  5. `002_05_size-ratio-chart.jpg`
  6. `002_06_print-me-first-preview.jpg`
  7. `002_07_secondary-lifestyle-angle.jpg`
  8. `002_08_support-license-strip.jpg` (optional)
- **Tags:** `nursery, printable, digital-download, single, starter, 300-dpi, 5-ratios, beginner-friendly, personal-use-only`
- **Collections:** `Nursery Printable Wall Art`, `Single Prints`
- **Variant approach for this SKU:** standalone product; cross-sell to `NUR-SGL-001` and `NUR-TRI-001`.

---

## SKU 003
- **Internal SKU code:** `NUR-TRI-001`
- **Offer type:** Trio Kit (Most Popular / Best Value)
- **Public product name:** `{{STYLE}} Nursery Trio Kit — {{COLLECTION}} (3 Coordinated Prints)`
- **Working style/archetype mapping:** `Calm Minimal` / `Whimsical Storybook`
- **Hook paragraph:**
  - `Create a calm, cohesive nursery corner in minutes with {{STYLE_LOWER}} artwork designed to work beautifully in everyday family spaces. You’ll receive clear files, simple print guidance, and friendly support if you need a hand.`
- **What you get (Trio template):**
  - `3 coordinated printable art designs: {{COLLECTION}}`
  - `1 ZIP folder with all included files`
  - `5 print ratios for each print: 2:3, 3:4, 4:5, 11:14, ISO (A-series)`
  - `Layout suggestion guide included`
  - ``PRINT_ME_FIRST.pdf`` for test printing and setup confidence
  - `Digital download only. No physical item is shipped.`
- **Gallery image list (required order, placeholder filenames):**
  1. `003_01_trio-hero-in-room.jpg`
  2. `003_02_trio-grid-overview.jpg`
  3. `003_03_layout-suggestion.jpg`
  4. `003_04_detail-crop-quality.jpg`
  5. `003_05_file-breakdown.jpg`
  6. `003_06_download-print-frame-panel.jpg`
  7. `003_07_size-ratio-chart.jpg`
  8. `003_08_secondary-lifestyle-angle.jpg`
  9. `003_09_trio-vs-singles-value-strip.jpg` (optional)
  10. `003_10_support-license-strip.jpg` (optional)
- **Tags:** `nursery, printable, digital-download, trio-kit, most-popular, best-value, 300-dpi, 5-ratios, beginner-friendly, personal-use-only`
- **Collections:** `Nursery Printable Wall Art`, `Trio Kits`
- **Variant approach for this SKU:** standalone Trio product; cross-sell to `NUR-SGL-001` and `NUR-SGL-002`.

---

## Cross-sell relationships (for separate-products architecture)
- `NUR-SGL-001` -> recommend `NUR-TRI-001` and `NUR-SGL-002`
- `NUR-SGL-002` -> recommend `NUR-TRI-001` and `NUR-SGL-001`
- `NUR-TRI-001` -> recommend `NUR-SGL-001` and `NUR-SGL-002`

## Locked pricing reference (AUD)
- Singles: `$12`
- Trio: `$29`
- Trio anchor line: `Save $7 vs buying singles.`
