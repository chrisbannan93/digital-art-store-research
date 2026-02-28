# Digital Art Store Research OS

A structured workspace to run a 15-topic research chain in ChatGPT for a **digital-first printable wall art store on Shopify** (with optional future print-on-demand expansion).

## Quickstart (do this first)
1. Open `00_ADMIN/CONTEXT_PACK.md` and fill obvious known assumptions.
2. Run `01_RESEARCH_PROMPTS/01_audience_psychology.md` in ChatGPT.
3. Save the response in `02_RESEARCH_OUTPUTS/01_audience_psychology.md` using the output template sections.
4. Update `00_ADMIN/CONTEXT_PACK.md` with validated learnings.
5. Log any major decision in `00_ADMIN/DECISIONS.md`.
6. Check off Topic 01 in `00_ADMIN/STATUS.md` and move to Topic 02.

## How to Run the Research Chain
1. Work topics in order from `01` to `15` inside `01_RESEARCH_PROMPTS/`.
2. For each topic prompt:
   - Paste the full prompt into ChatGPT.
   - Ensure response follows required structure.
   - Save structured output into matching file in `02_RESEARCH_OUTPUTS/`.
3. After each topic:
   - Extract key truth updates into `00_ADMIN/CONTEXT_PACK.md`.
   - Capture meaningful commitments in `00_ADMIN/DECISIONS.md`.
   - Update completion status in `00_ADMIN/STATUS.md`.
4. Keep outputs concise but decision-oriented; avoid generic notes that do not drive action.

## How to Update Context Pack
1. Only update with information supported by topic outputs, tests, or strong evidence.
2. Keep entries short and specific (especially Niche, Buyer, Promise, hooks, and testing rules).
3. Replace weak assumptions instead of adding conflicting versions.
4. If uncertain, mark as hypothesis and define what evidence will confirm/refute it.
5. Use context updates to sharpen the next topic prompt run.

## How to Log Decisions
1. Add a date-stamped entry in `00_ADMIN/DECISIONS.md` whenever you choose a direction that affects product, ads, pricing, legal policy, or operations.
2. Include: Decision, Why, Evidence, Tradeoffs, and Revisit trigger.
3. Keep decisions reversible where possible.
4. Revisit decisions when trigger conditions are met (not based on emotion or one bad day).

## Stop Conditions
Pause or reset the research chain if any of these happen:
- Three consecutive topics do not produce actionable decisions.
- Context pack quality does not improve after two consecutive topics.
- Economics remain unworkable based on current CPA, AOV, and margin assumptions.
- Legal/licensing constraints invalidate the current delivery model.
- Execution bandwidth is too low to complete next actions consistently.

## How This Feeds into Building the Store + Ads
- **Store build:** Use Context Pack + topic outputs to define collections, PDP structure, policy language, and licensing clarity.
- **Creative production:** Convert hooks, angles, and visual rules into weekly ad briefs and asset batches.
- **Testing system:** Apply metrics and testing frameworks to run disciplined experiments instead of random campaigns.
- **Scaling decisions:** Use decision log + status tracker to know when to scale winning niches/offers or pivot.

## Folder Guide
- `00_ADMIN/` — Operating docs: status tracking, decisions, context truth pack, glossary.
- `01_RESEARCH_PROMPTS/` — 15 reusable ChatGPT prompts.
- `02_RESEARCH_OUTPUTS/` — Topic-by-topic structured outputs.
- `03_ASSETS/` — Swipe files, mockup examples, and notes/screenshots.
- `04_TEMPLATES/` — Reusable templates for outputs, context pack, and decision log.
