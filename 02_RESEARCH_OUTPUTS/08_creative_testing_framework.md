# 08_creative_testing_framework

## Summary (5 bullets max)
- Run a 2-gate testing model: Gate 1 (CTR/CPC) to qualify attention, then Gate 2 (CVR/CPA) to qualify commerce efficiency.
- Use ABO-style equalized ad-set/ad-group budgets so each angle gets fair spend and clean comparative signal.
- Enforce minimum-data decision rules (impressions/clicks/spend/LPV) to prevent early false negatives and late false positives.
- Define validation as repeatability: an angle must generate purchases with acceptable CPA and thresholded CTR/CVR, not one-off wins.
- Iterate one variable at a time: first hook/first-2-seconds, then page clarity, then offer/price structure, then audience/scale.

## Deep insights (detailed)
### Core testing problem
Early budgets create sparse conversion data. If you judge only on CPA too early, you kill potential winners; if you judge only on CTR, you promote clickbait losers. The two-gate model solves this.

### Metric definitions (standardize)
- **CTR (Meta):** Outbound CTR
- **CTR (TikTok):** Destination CTR
- **CPC:** cost per outbound/destination click
- **CVR:** Purchases / Landing page views
- **CPA:** Spend / Purchases (AUD)

### Tracking requirements
Use mandatory creative-level UTMs:
- `utm_source=meta|tiktok`
- `utm_campaign=ANGLE_A|ANGLE_B|ANGLE_C`
- `utm_content=HOOK_01|HOOK_02|CREATIVE_01`

### Why this structure gives clean signal
- ABO equal spend isolates angle quality.
- Two creatives per angle reduces one-execution luck.
- Constant format + constant LP in Sprint 1 isolates the tested variable.
- Minimum data gates enforce disciplined, non-emotional decisions.

### Immediate decisions to set
- Trio price `P` remains anchor for CPA rules.
- Set target CPA model:
  - `tCPA = 0.7 × P`
  - `maxCPA = 1.0 × P`
- Confirm event tracking: ViewContent, AddToCart, InitiateCheckout, Purchase on both platforms.

### Sprint 1 structure (exact)
#### Global constants
- Format: 9:16 before/after slideshow
- Landing page: one shared cold-traffic URL
- Attribution: 1-day click
- Optimization: Purchase

#### Meta
- 1 Sales campaign, ABO
- 2–3 ad sets (one per angle)
- 2 creatives per ad set
- Budget:
  - 3-angle test: $12/day per ad set
  - 2-angle test: $18/day per ad set
- Duration: 4 days

#### TikTok
- 1 Website Conversions campaign
- 2–3 ad groups (one per angle)
- 2 ads per ad group
- Match Meta budgets
- Duration: 4 days

### Thresholds (decision numbers)
#### CTR
- **Meta Outbound CTR:**
  - too weak < 0.8%
  - promising 0.8–1.2%
  - good ≥ 1.2%
- **TikTok Destination CTR:**
  - too weak < 1.0%
  - promising 1.0–1.5%
  - good ≥ 1.5%

#### CPC
- **Meta:**
  - too weak > $2.20
  - promising $1.20–$2.20
  - good ≤ $1.20
- **TikTok:**
  - too weak > $1.80
  - promising $0.90–$1.80
  - good ≤ $0.90

#### CVR
- too weak < 0.9%
- promising 0.9–1.7%
- good ≥ 1.7%

#### CPA (with P = Trio price)
- too weak > 1.0P
- promising 0.7P–1.0P
- good ≤ 0.7P
- hard learning ceiling: if CPA > 1.3P after minimum data, stop.

### Kill rules (non-negotiable)
#### Minimum data before judging
- Gate 1: do not judge until creative has ≥ 1,500 impressions or ≥ $10 spend.
- Gate 2: do not judge until angle has ≥ 50 LP views and ≥ 1.0P spend.

#### Creative-level kill
Kill if minimums met and:
- Meta outbound CTR < 0.8%, or
- TikTok destination CTR < 1.0%.

Also kill if:
- Meta: CTR < 0.8% and CPC > $2.20
- TikTok: CTR < 1.0% and CPC > $1.80

#### Angle-level stop/park
Stop angle if:
- spend ≥ 2.0P and purchases = 0, or
- spend ≥ 1.0P and CVR < 0.9% despite good Gate 1 signal.

Kill vs Park:
- Kill = fails Gate 1 across both creatives.
- Park = passes Gate 1 but fails Gate 2 (usually page/offer issue).

### Iteration logic
- **If CTR low:** change only first 2s hook/overlay framing.
- **If CTR good but CVR poor:** fix page/offer clarity first (what’s included, kit preview, trust/risk module, checkout friction).
- **If sales exist but CPA high:** lift AOV (bundle prompts/order bump), then CVR, then CPC.

### Budget protection rules
- Don’t judge below minimum gates.
- Don’t scale from one purchase.
- Scale only when:
  - ≥ 2 purchases,
  - CPA ≤ 0.8P,
  - CTR at least good-threshold.
- Don’t change budgets by >20% per day.
- Don’t launch retargeting until ~1,000+ visitors.

### Validation definitions
#### Validated creative angle
Within a 4-day sprint on at least one platform:
- ≥ 2 purchases,
- CPA ≤ 0.8P,
- CTR at/above good threshold,
- at least one purchase from each of the 2 creatives.

#### Validated offer
Using validated angle:
- ≥ 4 purchases total,
- CVR ≥ 1.7%,
- average CPA ≤ 0.7P,
- Trio Kit is majority purchase path or can be profitably steered.

#### Failed test
- both creatives fail Gate 1 after minimums, or
- after 2.0P spend: purchases = 0 and CVR < 0.9% with sufficient LPVs.

## Decisions I should make now
- [ ] Confirm Trio price `P` is the CPA anchor for all tests.
- [ ] Lock Sprint 1 to 2 or 3 angles based on budget capacity.
- [ ] Confirm required conversion events are firing correctly on both platforms.
- [ ] Set `tCPA = 0.7P` and `maxCPA = 1.0P` in reporting sheet.
- [ ] Freeze one variable per sprint rule.

## What to put into CONTEXT_PACK (10 bullets max)
- Trio Kit price `P` (AUD) and AOV expectation.
- CPA rule: `tCPA = 0.7P`, `maxCPA = 1.0P`.
- Locked test angles as ANGLE_A/B/C.
- Hook IDs HOOK_01..HOOK_15.
- Shared Sprint 1 landing page URL.
- Meta + TikTok Purchase event confirmation.
- Delivery/refund stance for ads + LP consistency.
- Bundle/file-format clarity statement.
- Audience geo constraints.
- Daily budget range for Sprint 1.

## Open questions / risks
- Tracking quality risk can invalidate CPA/CVR decisions.
- If P is too low, acceptable CPA bands become too restrictive.
- Small budgets can create platform volatility despite gating rules.
- Nursery intent may create save/share-heavy behavior before purchase.

## Next actions (checklist)
- [ ] Build Sprint 1 matrix (2–3 angles × 2 creatives each).
- [ ] Apply consistent UTMs and verify events before spend.
- [ ] Launch 4-day ABO tests on Meta and TikTok.
- [ ] Evaluate by gate thresholds only after minimum data is met.
- [ ] Kill/park/continue by rule, not intuition.
- [ ] Run next sprint with one-variable iteration.

## Sources / Examples (optional)
- Prior DR-07 angle/hook framework and launch creative standards.
- Platform-level conversion testing best practices for low-volume accounts.
