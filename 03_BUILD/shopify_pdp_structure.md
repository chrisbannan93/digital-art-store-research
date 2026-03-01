# Shopify PDP Blueprint (v1 Nursery Printable Kits)

## Global PDP Data Placeholders
- `{{PRODUCT_TYPE}}` = `Single` or `Trio Kit`
- `{{STYLE}}`
- `{{SUBJECT}}`
- `{{COLLECTION}}`
- `{{PRICE}}`
- `{{COMPARE_PRICE_OPTIONAL}}`
- `{{DIGITAL_DELIVERY_LINE}}` = `Digital download only. No physical item is shipped.`
- `{{PROCESS_LINE}}` = `Download -> Print -> Frame`
- `{{TRIO_VALUE_LINE}}` = `Curated set + layout included`
- `{{TRIO_ANCHOR_LINE}}` = `Save $7 vs buying singles`
- `{{SUPPORT_SLA}}` (example: `Support replies within 24 hours`)
- `{{SUPPORT_CONTACT}}`
- `{{REFUND_WINDOW}}`
- `{{INCLUDED_FILES_SINGLE}}`
- `{{INCLUDED_FILES_TRIO}}`
- `{{RATIO_LIST}}` = `2:3, 3:4, 4:5, 11:14, ISO (A-series)`
- `{{PRINT_PATH_OPTIONS}}` (home printer, local print shop, online print lab)
- `{{LAYOUT_NOTE}}` (Trio-only layout suggestion summary)
- `{{POLICY_LINK_DIGITAL}}`
- `{{POLICY_LINK_LICENSE}}`
- `{{POLICY_LINK_SUPPORT}}`
- `{{POLICY_LINK_REFUND}}`
- `{{FAQ_ITEMS}}`
- `{{CROSS_SELL_ITEMS_OPTIONAL}}`

---

## Section Order (must remain fixed)

### 1) Title + format clarity
- **Purpose (anxiety resolved):** Immediate clarity on what is being bought (digital printable art, not a framed physical item).
- **Required elements:**
  - H1 title
  - Format subline (`Printable wall art` / `Digital files`)
  - Offer-type label badge (`Starter` for Single, `Most Popular / Best Value` for Trio)
- **Copy placeholders:**
  - Single title: `{{STYLE}} Nursery Print — {{SUBJECT}} (Printable Wall Art)`
  - Trio title: `{{STYLE}} Nursery Trio Kit — {{COLLECTION}} (3 Coordinated Prints)`
  - Format line includes `{{DIGITAL_DELIVERY_LINE}}`
- **Conditional logic:**
  - If `{{PRODUCT_TYPE}} = Single`, show Single title template + `Starter` label.
  - If `{{PRODUCT_TYPE}} = Trio Kit`, show Trio title template + `Most Popular / Best Value` label.
- **Shopify implementation notes:**
  - Product title from product metafields/templates.
  - Offer label as dynamic block in main product section.

### 2) Micro-badges (Instant Download, 300 DPI, 5 Ratios, Beginner-Friendly)
- **Purpose:** Fast trust scan for file quality and ease.
- **Required elements:**
  - 4 badges exactly: `Instant Download`, `300 DPI`, `5 Ratios`, `Beginner-Friendly`
- **Copy placeholders:** none required (locked terms).
- **Conditional logic:** always visible for Single and Trio.
- **Shopify implementation notes:** static icon-text blocks inside product info section.

### 3) Hook (calm outcome + confidence)
- **Purpose:** Reduces fear that room styling will feel hard or risky.
- **Required elements:**
  - One short paragraph hook under badges.
- **Copy placeholders:** `{{THEME_OUTCOME_LINE}}`, `{{CONFIDENCE_LINE}}`
- **Conditional logic:**
  - Trio hook may reference coordinated look.
  - Single hook references one focal print.
- **Shopify implementation notes:** rich text block tied to product-type template.

### 4) Price + digital-only microcopy
- **Purpose:** Price clarity and no-surprise digital format confirmation.
- **Required elements:**
  - Price shown in AUD.
  - Optional compare-at only if non-aggressive and policy-compliant.
  - Canonical line exactly: `{{DIGITAL_DELIVERY_LINE}}`
- **Copy placeholders:** `{{PRICE}}`
- **Conditional logic:**
  - Single default price = `$12 AUD`
  - Trio default price = `$29 AUD`
- **Shopify implementation notes:** native price block + locked microcopy text block directly below.

### 5) Choose-your-set block (Single vs Trio)
- **Purpose:** Prevents decision friction and clarifies value differences.
- **Required elements:**
  - Two option cards/radios: `Single (Starter)` and `Trio Kit (Most Popular / Best Value)`
  - Short descriptors:
    - Single: `1 coordinated print`
    - Trio: `3 coordinated prints + layout suggestion`
  - Trio card includes `{{TRIO_ANCHOR_LINE}}`
- **Copy placeholders:** `{{TRIO_ANCHOR_LINE}}`
- **Conditional logic:**
  - If current SKU has both Single and Trio variants, show selector and variant-switch.
  - If only Single exists, hide Trio card and selector controls.
  - If only Trio exists, hide Single card and selector controls.
- **Shopify implementation notes:** variant picker block (radio style) + metafields for descriptors and value line.

### 6) Primary CTA + instant delivery line
- **Purpose:** Confirms immediate next step with low ambiguity.
- **Required elements:**
  - Primary button (`Add to cart` / `Buy now`)
  - Instant delivery line directly adjacent to CTA.
- **Copy placeholders:** `{{INSTANT_DELIVERY_LINE}}` (example: `Files available instantly after checkout.`)
- **Conditional logic:** always visible.
- **Shopify implementation notes:** native buy buttons block; place delivery line as immediate subtext.

### 7) Mini what-you-get bullets
- **Purpose:** Quick scope clarity before scroll.
- **Required elements:**
  - 3-5 bullets.
  - Must mention ZIP package and 5 ratios.
- **Copy placeholders:**
  - Single bullets use `{{INCLUDED_FILES_SINGLE}}`
  - Trio bullets use `{{INCLUDED_FILES_TRIO}}`
- **Conditional logic:** render Single bullet set or Trio bullet set by product type.
- **Shopify implementation notes:** collapsible-free bullet list block near CTA.

### 8) CTA trust cluster (`PRINT_ME_FIRST`, support SLA, support-first line)
- **Purpose:** Resolves post-purchase anxiety (printing confidence + help availability).
- **Required elements:**
  - `PRINT_ME_FIRST.pdf included`
  - `{{SUPPORT_SLA}}`
  - Support-first line (`We help troubleshoot first, then resolve, then refund if unresolved within policy window.`)
  - Repeat canonical `{{DIGITAL_DELIVERY_LINE}}`
- **Copy placeholders:** `{{SUPPORT_SLA}}`, `{{SUPPORT_CONTACT}}`, `{{REFUND_WINDOW}}`
- **Conditional logic:** always visible; must remain adjacent to first CTA region.
- **Shopify implementation notes:** trust icon list block under CTA in product info column.

### 9) How it works (`Download -> Print -> Frame`)
- **Purpose:** Removes process uncertainty.
- **Required elements:**
  - 3 sequential steps labeled exactly with `{{PROCESS_LINE}}` flow.
- **Copy placeholders:** `{{PROCESS_LINE}}`
- **Conditional logic:** always visible.
- **Shopify implementation notes:** custom section with 3 step cards/icons.

### 10) Full what’s-included manifest
- **Purpose:** Full deliverable transparency before purchase.
- **Required elements:**
  - Explicit file manifest:
    - 1 ZIP package
    - 5 ratio files per print asset
    - `PRINT_ME_FIRST.pdf`
  - Ratio list shown.
- **Copy placeholders:** `{{RATIO_LIST}}`
- **Conditional logic:**
  - Single: quantity language for 1 print.
  - Trio: quantity language for 3 prints.
- **Shopify implementation notes:** accordion or static rich text section.

### 11) Print confidence section (`PRINT_ME_FIRST` + print path guidance)
- **Purpose:** Addresses fear of poor print results.
- **Required elements:**
  - `PRINT_ME_FIRST` explanation.
  - Print path guidance options (`{{PRINT_PATH_OPTIONS}}`).
  - Optional checklist bullets for paper/frame prep.
- **Copy placeholders:** `{{PRINT_PATH_OPTIONS}}`
- **Conditional logic:** always visible.
- **Shopify implementation notes:** dedicated section; may include expandable tips blocks.

### 12) Size/ratio chart
- **Purpose:** Prevents sizing confusion.
- **Required elements:**
  - Ratio-to-common-size mapping chart.
  - Include all 5 ratios.
- **Copy placeholders:** `{{RATIO_LIST}}`
- **Conditional logic:** always visible.
- **Shopify implementation notes:** static table block or image+table hybrid section.

### 13) Trio value module (layout suggestion + cohesion)
- **Purpose:** Justifies Trio price with planning and cohesion confidence.
- **Required elements:**
  - `{{TRIO_VALUE_LINE}}`
  - Layout suggestion callout (`{{LAYOUT_NOTE}}`)
  - `{{TRIO_ANCHOR_LINE}}`
- **Copy placeholders:** `{{TRIO_VALUE_LINE}}`, `{{LAYOUT_NOTE}}`, `{{TRIO_ANCHOR_LINE}}`
- **Conditional logic:**
  - Show only when `{{PRODUCT_TYPE}} = Trio Kit` OR Trio option exists in selector.
  - Hide for Single-only SKU.
- **Shopify implementation notes:** conditional block by template/variant metafield.

### 14) FAQ (digital-anxiety questions first)
- **Purpose:** Resolves final objections (delivery, print quality, file use, help).
- **Required elements:**
  - FAQ accordion with digital anxiety ordering:
    1. How do I receive files?
    2. What if I’m new to printing?
    3. What sizes can I print?
    4. Can I use a local/online print shop?
    5. What if I have a problem with files?
    6. What am I allowed to do with files?
- **Copy placeholders:** `{{FAQ_ITEMS}}`
- **Conditional logic:** always visible.
- **Shopify implementation notes:** FAQ section block with ordered items locked.

### 15) License summary
- **Purpose:** Prevents uncertainty about permitted use without legal overload.
- **Required elements:**
  - Plain-English summary: Personal Use Only.
  - Allowed vs not allowed bullets.
  - Link to full license policy.
- **Copy placeholders:** `{{POLICY_LINK_LICENSE}}`
- **Conditional logic:** always visible.
- **Shopify implementation notes:** policy summary block on PDP + footer policy page link.

### 16) Support-first guarantee summary + policy link
- **Purpose:** Reduces risk perception near conversion decision.
- **Required elements:**
  - Troubleshoot -> resolve -> refund if unresolved.
  - Support contact and SLA.
  - Links to support/refund policy pages.
- **Copy placeholders:** `{{SUPPORT_SLA}}`, `{{SUPPORT_CONTACT}}`, `{{REFUND_WINDOW}}`, `{{POLICY_LINK_SUPPORT}}`, `{{POLICY_LINK_REFUND}}`
- **Conditional logic:** always visible.
- **Shopify implementation notes:** static trust section; duplicate condensed form near CTA and full summary lower on page.

### 17) Optional non-intrusive cross-sell block
- **Purpose:** Offers coordinated add-ons without interruptive pressure.
- **Required elements:**
  - Low-emphasis heading (`Pair with similar nursery styles`)
  - Max 3 related products.
  - No urgency/counted timers.
- **Copy placeholders:** `{{CROSS_SELL_ITEMS_OPTIONAL}}`
- **Conditional logic:** show only if related nursery SKUs exist.
- **Shopify implementation notes:** Shopify recommendations block with subdued styling.

---

## Above-the-Fold Rules (locked)
- Must include sections 1-8 before first major scroll break on desktop where possible.
- Must include, in order above first CTA: title, badges, hook, price, set selector (if applicable), CTA, mini-what-you-get, trust cluster.
- Canonical digital-delivery line must appear at price area and trust cluster near CTA.

## Trust Placement Rules (locked)
- Apply trust stack order through PDP content:
  1. Process proof (How it works)
  2. Visual proof (gallery sequence)
  3. Language proof (specific non-hype copy)
  4. Policy proof (license/support/refund summaries)
  5. Support proof (SLA + support-first path)
- Do not add countdown timers, exaggerated claims, or aggressive discount styling.

## FAQ Placement Rules (locked)
- FAQ appears after Trio value module and before license/support policy summaries.
- Digital-anxiety questions must be listed first.

## Policy Placement Rules (locked)
- Short policy summaries appear near CTA (trust cluster) and lower PDP sections (license + support-first summary).
- Full policy text remains on dedicated policy pages linked from PDP.

## Mobile-Specific Considerations
- Use sticky mobile CTA bar containing:
  - price
  - selected set (Single/Trio)
  - primary CTA
- Ensure canonical digital-only line remains visible near primary purchase area on mobile (not hidden in collapsed content).
- Mobile order remains identical to section order above.
- Keep micro-badges and mini what-you-get above first accordion collapse.
- FAQ, license, and support sections may use accordions, but trust cluster near CTA must stay expanded.
