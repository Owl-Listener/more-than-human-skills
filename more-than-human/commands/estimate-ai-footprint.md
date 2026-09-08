---
description: Produce a defensible per-session footprint estimate for an AI feature and a ranked list of reductions with their quality costs.
argument-hint: "[AI feature and its scale — e.g., 'chat assistant, 40k sessions/month, hosted frontier model']"
---
# /estimate-ai-footprint
Get a number you can defend in a roadmap meeting, then the shortest path to lowering it. Use when the footprint question is live but the broader stakeholder work is not yet warranted.
## Steps
1. **Estimate energy and carbon** — Compute per-session energy from per-call cost, calls per session, and retry rate; convert using the grid intensity of the region inference actually runs in; report as a range with the boundary stated, using `ai-energy-footprint` skill.
2. **Add water and land** — Convert facility energy to on-site and off-site water, weight by the stress of the specific basin, and note the seasonal peak, using `water-and-land-impact` skill.
3. **Add embodied cost** — Account for server hardware amortised across real utilisation, and for any device-requirement or on-device change that shortens client hardware life, using `hardware-and-minerals` skill.
4. **Rank the reductions** — Identify changes ordered by leverage — model right-sizing, trigger point, retry rate, output defaults, caching, feature defaults, scheduling — each with its quality cost and confidence, using `model-choice-tradeoffs` skill.
5. **Check the rebound** — Test whether the efficiency gain will be consumed by volume growth, and name the cap, default, or pricing unit that would hold it, using `downstream-consequence-scan` skill.
## Output
- **Headline estimate** — annual energy, carbon, and water as ranges, with the assumption the estimate is most fragile to.
- **Assumption table** — model and size class, calls per session, retry rate, source and its boundary, grid region, basin, projected sessions.
- **Anchors** — the figures restated against something physical, so the number is arguable.
- **Reduction list** — Change · Estimated reduction · Quality cost · Confidence · Effort.
- **Rebound note** — whether the saving survives volume growth, and what would hold it.
