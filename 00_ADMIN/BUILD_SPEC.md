# BUILD_SPEC

**Authority:** This file is the executable build specification for v1.

## 1. Product Scope & Niche Lock
- Build only nursery printable wall kits in v1.
- Keep delivery digital-only in v1 (no default physical fulfillment).
- Do not expand niche scope until:
  - at least 10 SKUs are live, and
  - at least one offer path shows repeatable conversion.

## 2. Offer Architecture (Single vs Trio)
- Launch offer types:
  - Single (Starter): 1 print.
  - Trio Kit (Most Popular / Best Value): 3 coordinated prints + layout suggestion.
- Keep Weekend Kit (6-9 prints) as post-validation placeholder only.
- Required deliverables per SKU:
  - 1 ZIP package
  - 5 ratio files per print asset
  - `PRINT_ME_FIRST.pdf`

## 3. Pricing & Value Framing
- Lock launch prices in AUD:
  - Single = $12
  - Trio = $29
  - Weekend Kit = $49 (placeholder)
- Required Trio anchor line:
  - "Save $7 vs buying singles."
- Tier labels:
  - Single = Starter
  - Trio = Most Popular / Best Value
  - Weekend = Complete the Wall
- Prohibit perpetual discount styling and aggressive crossed-out pricing patterns.

## 4. PDP Structure (section-by-section, ordered)
1. Title + format clarity
2. Micro-badges (Instant Download, 300 DPI, 5 Ratios, Beginner-Friendly)
3. Hook (calm outcome + confidence)
4. Price + digital-only microcopy
5. Choose-your-set block (Single vs Trio)
6. Primary CTA + instant delivery line
7. Mini what-you-get bullets
8. CTA trust cluster (`PRINT_ME_FIRST`, support SLA, support-first line)
9. How it works (`Download -> Print -> Frame`)
10. Full what’s-included manifest
11. Print confidence section (`PRINT_ME_FIRST` + print path guidance)
12. Size/ratio chart
13. Trio value module (layout suggestion + cohesion)
14. FAQ (digital-anxiety questions first)
15. License summary
16. Support-first guarantee summary + policy link
17. Optional non-intrusive cross-sell block

## 5. Product Gallery Rules (Singles + Trio)
### Singles (7-8 images, fixed order)
1. Nursery hero mockup
2. Detail crop (quality proof)
3. What’s included graphic
4. `Download -> Print -> Frame` panel
5. Size/ratio chart
6. `PRINT_ME_FIRST` preview
7. Secondary lifestyle angle
8. Optional support/license strip

### Trio (8-10 images, fixed order)
1. Trio hero in-room
2. Trio grid overview
3. Layout suggestion
4. Detail crop
5. File breakdown
6. `Download -> Print -> Frame` panel
7. Size/ratio chart
8. Secondary lifestyle angle
9. Optional Trio vs Singles value strip
10. Optional support/license strip

## 6. Copy Blocks (templates, not prose)
- Product title templates:
  - Single: `{Style} Nursery Print — {Subject} (Printable Wall Art)`
  - Trio: `{Style} Nursery Trio Kit — {Collection} (3 Coordinated Prints)`
- Canonical digital-delivery line:
  - "Digital download only. No physical item is shipped."
- Core process line:
  - `Download -> Print -> Frame`
- Trio value line:
  - `Curated set + layout included`
- Anchor line:
  - `Save $7 vs buying singles`
- Trust cluster near CTA must include:
  - canonical digital-only line
  - `PRINT_ME_FIRST` included
  - support SLA
  - support-first fix path

## 7. Trust & Legitimacy Rules
- Apply trust stack in this order:
  1) Process proof
  2) Visual proof
  3) Language proof
  4) Policy proof
  5) Support proof
- Keep trust language specific, calm, and non-hype.
- Show digital-only + instant-delivery clarity before or adjacent to first CTA.
- Prohibit countdown urgency, exaggerated claims, and inconsistent funnel wording.

## 8. Policy Rules (Digital, License, Support, Refund)
- Policy pages must start with 2-3 line human summary, then legal detail.
- Digital policy must repeat canonical digital-delivery line exactly.
- License policy at launch is Personal Use Only.
  - Allowed: home use (and gifting only if explicitly enabled).
  - Not allowed: resale, redistribution, file sharing.
- Support-first guarantee path must be explicit:
  - troubleshoot -> resolve -> refund if unresolved (within defined window).
- Place policy summaries near CTA and in FAQ; keep full policy text on policy pages.

## 9. Ad Creative Constraints (for future assets)
- Base ad format: 9:16 MP4, approximately 14 seconds.
- First-second rule: show finished-wall outcome immediately.
- Allowed launch angles only:
  - Transformation
  - Print-confidence
  - Instant gift convenience
- Launch batch rule: 4 creatives total (2 transformation, 1 confidence, 1 gift).
- Readability rule: hooks 3-5 words; critical text must stay in safe zones.
- Show digital-only disclosure in first 2-3 seconds.

## 10. Testing & Iteration Rules (what changes, what stays fixed)
- Use two-gate model:
  - Gate 1 = CTR/CPC
  - Gate 2 = CVR/CPA
- Sprint operating rules:
  - 4-day cycles
  - ABO/ad-group parity
  - minimum 2 creatives per angle
- CPA anchors (P = Trio price):
  - tCPA = 0.7P
  - maxCPA = 1.0P
  - stop if >1.3P after minimum data
- Minimum data before evaluation:
  - Gate 1: >=1,500 impressions OR >=$10 spend per creative
  - Gate 2: >=50 LPVs AND >=1.0P spend per angle
- Change order (single variable per sprint):
  1) Hook / first 2 seconds
  2) Page clarity / trust modules
  3) Offer-price framing
  4) Audience/scale

## 11. Explicit Non-Goals (what we will NOT build yet)
- No physical-first or broad POD rollout in v1.
- No commercial-use licensing in launch offer.
- No niche expansion beyond nursery kits.
- No mega-bundle quantity strategy.
- No heavy CRO multivariate testing beyond 3 launch A/B tests.
- No aggressive urgency/discounter UI patterns.
- No AI-generated room backgrounds in v1 mockups.

## AMBIGUITIES
- **Ambiguity:** Product architecture for Single vs Trio on Shopify (variant model vs separate products).
  - **Option A:** Single PDP with variants (`Single`, `Trio Kit`) using choose-your-set variant selector.
  - **Option B:** Separate product records for Singles and Trio with cross-sell links between them.
  - **Recommendation:** Start with **Option B** for launch scaffolding (clear SKU-level asset/package ownership and simpler product operations), while keeping section logic compatible with Option A later.
