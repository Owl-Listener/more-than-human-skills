# more-than-human

Check whether what you build serves all living things, not just humans.

Four lenses: who is affected and by what route, what the system costs ecologically, what changes when the user is not human, and what harm is being accepted without anyone writing it down.

## Skills (14)
- **ai-energy-footprint** — Estimate the energy and carbon cost of an AI feature to a defensible order of magnitude, using per-session rather than per-call units, with uncertainty stated. Use when you need a number for a design decision. For reducing the number once you have it, use `model-choice-tradeoffs`.
- **animal-computer-interaction** — Design and evaluate systems whose user is an animal — welfare-first requirements, ergonomics for non-human bodies, and success measures the animal defines. Use when an animal directly interacts with the system. For animals affected without interacting, use `nonhuman-stakeholder-map`.
- **biosphere-red-lines** — Define the small set of ecological harms a team refuses regardless of benefit, written as testable conditions and committed to before a specific deal is on the table. Use when setting policy or when a tradeoff involves irreversible loss. For harms that are genuinely tradeable, use `harm-tradeoff-ledger`.
- **conservation-tech-ethics** — Assess wildlife monitoring and conservation technology for data hazards, dual use, and community data sovereignty — including when location data endangers the species it documents. Use when building anything that observes or records wild populations. For the animal's direct experience of the device, use `animal-computer-interaction`.
- **downstream-consequence-scan** — Trace what a product accelerates in the world — rebound effects, induced demand, and the ecological cost of behaviour it makes easier. Use when a system's direct footprint looks small but its purpose is to increase throughput of something. For the direct footprint itself, use `ai-energy-footprint`.
- **hardware-and-minerals** — Account for the embodied cost of the hardware a product depends on — extraction sites, manufacturing, device replacement pressure, and e-waste. Use when a feature raises hardware requirements or shortens device life. For the electricity that hardware then draws, use `ai-energy-footprint`.
- **harm-tradeoff-ledger** — Make a conflict between human benefit and non-human harm explicit, comparable, and owned — with reversibility weighted and a named person accepting each residual harm. Use when an assessment has found harm and the product is shipping anyway. For harms that should not be traded at all, use `biosphere-red-lines`.
- **model-choice-tradeoffs** — Cut an AI feature's footprint through design decisions — right-sizing the model, trigger points, output length, caching, and defaults — with the quality cost of each stated. Use when you have an estimate and need to reduce it. For producing the estimate first, use `ai-energy-footprint`.
- **more-than-human-critique** — Review an existing product against all four lenses at once and return findings with severity, evidence, and a required change for each. Use when assessing something already built or specified. For building the stakeholder inventory from scratch, use `nonhuman-stakeholder-map`.
- **more-than-human-personas** — Build a rigorous representation of a non-human stakeholder — biological requirements, thresholds, evidence, and who speaks for it — without anthropomorphising. Use when one stakeholder needs to be present in design decisions. For finding which stakeholders exist, use `nonhuman-stakeholder-map`.
- **nonhuman-consent-and-agency** — Build refusal into a system an animal cannot consent to — behavioural opt-out, non-coercive incentives, and a proxy who can withdraw participation. Use when an animal is enrolled in or subjected to a system. For the interaction design and welfare floor, use `animal-computer-interaction`.
- **nonhuman-stakeholder-map** — Enumerate the non-human living things a product touches, traced along six impact pathways, each named specifically enough to be checked later. Use when starting any assessment of a system's effect beyond its human users. For turning one identified stakeholder into a usable representation, use `more-than-human-personas`.
- **sensory-fit-design** — Design signals and structures for another species' perceptual world — colour vision, hearing range, scent, and the cues it navigates by. Use when a system emits or reflects anything an animal perceives, including buildings and lighting. For the whole interaction and its welfare floor, use `animal-computer-interaction`.
- **water-and-land-impact** — Assess the water withdrawal and land consequence of the infrastructure a product runs on, weighted by local scarcity and the ecology of the actual site. Use when siting, choosing a region, or accounting beyond carbon. For energy and carbon specifically, use `ai-energy-footprint`.

## Commands (3)
- `/audit-more-than-human` — Run the full four-lens audit on a product or feature and output a findings report with a tradeoff ledger and named acceptors.
- `/design-for-nonhuman-users` — Specify a system whose user is an animal — welfare requirements, sensory fit, refusal path, and behavioural success measures.
- `/estimate-ai-footprint` — Produce a defensible per-session footprint estimate for an AI feature and a ranked list of reductions with their quality costs.

## Install

```
/plugin marketplace add Owl-Listener/more-than-human-skills
/plugin install more-than-human@more-than-human-skills
```

## License

MIT
