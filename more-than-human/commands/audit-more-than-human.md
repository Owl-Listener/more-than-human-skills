---
description: Run the full four-lens audit on a product or feature and output a findings report with a tradeoff ledger and named acceptors.
argument-hint: "[product or feature — e.g., 'the AI photo generator in our seller app' or a link to a spec]"
---
# /audit-more-than-human
Assess whether a product serves living things beyond its human users. Runs the complete arc: who is affected, what it costs, whether a non-human is a user, and what conflicts need deciding. Produces a report ending in decisions with names attached, not a score.
## Steps
1. **Map the stakeholders** — Trace all six impact pathways and name every affected population specifically, marking pathways found empty and why, using `nonhuman-stakeholder-map` skill.
2. **Scan the downstream** — Identify what the product makes cheaper or easier, follow that to physical consequence, and find the design lever on each chain, using `downstream-consequence-scan` skill.
3. **Estimate the footprint** — Produce per-session energy and carbon ranges with assumptions and boundary stated, using `ai-energy-footprint` skill. Add water and land against the actual basin and site using `water-and-land-impact` skill, and embodied hardware cost including client-device pressure using `hardware-and-minerals` skill.
4. **Check for non-human users** — If any living thing interacts with the system directly, assess the welfare floor, ergonomics, and end-of-life plan using `animal-computer-interaction` skill; verify a working refusal path using `nonhuman-consent-and-agency` skill. If nothing interacts directly, record the dimension as not applicable and move on.
5. **Test the red lines** — Check the proposal against the team's standing refusal conditions, escalating any that trigger, using `biosphere-red-lines` skill.
6. **Build the ledger** — For every harm that survives to shipping, record benefit, harm, reversibility, real alternatives, committed mitigation, residual harm, and a named acceptor, using `harm-tradeoff-ledger` skill.
7. **Identify the reductions** — List the design changes that would cut the footprint, ordered by leverage, each with its quality cost stated, using `model-choice-tradeoffs` skill.
## Output
A report in five parts:
- **Stakeholder map** — table of named populations by pathway, with confidence and what would settle each.
- **Footprint** — energy, water, and hardware estimates as ranges, each with its boundary and grid or basin stated.
- **Non-human users** — welfare and refusal assessment, or an explicit "not applicable" with reasoning.
- **Tradeoff ledger** — one row per conflict, residual harm visible after mitigation, a named individual per row.
- **Decision list** — changes to make this cycle, ordered by leverage, each with estimated reduction and quality cost.
Close with the single most consequential unexamined question, and any red line that triggered.
