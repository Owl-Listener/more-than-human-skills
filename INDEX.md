# Index

Every skill in this repo, by the task it answers.

## Start here

**"We're shipping an AI feature and nobody has asked what it costs the world."**
Start with `nonhuman-stakeholder-map` to find who is affected, then `ai-energy-footprint` for a number you can defend.

**"Someone said our sustainability story is fine because the servers are on renewables."**
The servers are usually the smaller half. Run `downstream-consequence-scan` for what the product accelerates, and `hardware-and-minerals` for the embodied cost the energy figure omits.

**"We're building for animals and I don't know what I don't know."**
`animal-computer-interaction` for the welfare floor and ergonomics, `sensory-fit-design` for signals the animal can actually perceive, `nonhuman-consent-and-agency` for the refusal path.

**"We found a real harm and we're shipping anyway."**
`harm-tradeoff-ledger`. It won't tell you not to ship. It will make sure the residual harm survives the mitigation column and that someone's name is on accepting it.

**"I want to decide the hard cases before they arrive."**
`biosphere-red-lines`, and do it now — a line drawn with a live deal on the table is a negotiation.

## Frequently confused

| These two | The difference |
| --- | --- |
| `nonhuman-stakeholder-map` vs `more-than-human-personas` | The map finds *who* is affected across six pathways. The persona turns one of them into a usable requirements document with thresholds and a named proxy. |
| `ai-energy-footprint` vs `model-choice-tradeoffs` | The footprint produces the number. The tradeoffs skill reduces it, with the quality cost of each reduction stated. |
| `ai-energy-footprint` vs `downstream-consequence-scan` | Direct cost of running the system versus the ecological cost of the behaviour it makes easier. The second is usually larger. |
| `animal-computer-interaction` vs `nonhuman-stakeholder-map` | ACI applies when an animal *interacts* with the system. The map covers animals affected without ever touching it. |
| `animal-computer-interaction` vs `nonhuman-consent-and-agency` | ACI sets the welfare floor and the ergonomics. Consent covers whether the animal can refuse, and whether anyone will honour it. |
| `harm-tradeoff-ledger` vs `biosphere-red-lines` | The ledger is for harms that can legitimately be traded. Red lines are for harms that cannot, at any price. Reversibility usually decides which. |
| `more-than-human-critique` vs `/audit-more-than-human` | The critique reviews what exists and returns findings. The command runs the whole pipeline, including the ledger and the reduction list. |
| `water-and-land-impact` vs `hardware-and-minerals` | Where the facility sits and what it draws, versus what the hardware is made of and where that came from. |

<!-- BEGIN GENERATED INDEX -->

### Who is affected (3)

Find the living things a system touches, and by what route.

| Reach for it | Skill | Plugin |
| --- | --- | --- |
| When a system's direct footprint looks small but its purpose is to increase throughput of something | `downstream-consequence-scan` | more-than-human |
| When one stakeholder needs to be present in design decisions | `more-than-human-personas` | more-than-human |
| When starting any assessment of a system's effect beyond its human users | `nonhuman-stakeholder-map` | more-than-human |

### What it costs (4)

Estimate what running the thing takes from the world, and cut it.

| Reach for it | Skill | Plugin |
| --- | --- | --- |
| When you need a number for a design decision | `ai-energy-footprint` | more-than-human |
| When a feature raises hardware requirements or shortens device life | `hardware-and-minerals` | more-than-human |
| When you have an estimate and need to reduce it | `model-choice-tradeoffs` | more-than-human |
| When siting, choosing a region, or accounting beyond carbon | `water-and-land-impact` | more-than-human |

### When the user is not human (4)

Design for a body, a sensorium, and a being that can refuse.

| Reach for it | Skill | Plugin |
| --- | --- | --- |
| When an animal directly interacts with the system | `animal-computer-interaction` | more-than-human |
| When building anything that observes or records wild populations | `conservation-tech-ethics` | more-than-human |
| When an animal is enrolled in or subjected to a system | `nonhuman-consent-and-agency` | more-than-human |
| When a system emits or reflects anything an animal perceives, including buildings and lighting | `sensory-fit-design` | more-than-human |

### What we are trading (3)

Make the conflicts explicit, decidable, and owned by a named person.

| Reach for it | Skill | Plugin |
| --- | --- | --- |
| When setting policy or when a tradeoff involves irreversible loss | `biosphere-red-lines` | more-than-human |
| When an assessment has found harm and the product is shipping anyway | `harm-tradeoff-ledger` | more-than-human |
| When assessing something already built or specified | `more-than-human-critique` | more-than-human |

<!-- END GENERATED INDEX -->
