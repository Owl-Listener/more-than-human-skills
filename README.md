# More-Than-Human Skills

Agentic skills and commands for checking whether what we build serves all living things — not just humans.

**14 skills and 3 commands across 1 plugin.**

## Why this exists

Design has a boundary baked into its vocabulary. A *user* is a human. A *stakeholder* is a human with budget. Everything else — the animals in the supply chain a recommender optimises, the watershed a datacentre draws from, the species whose habitat a mapping tool makes legible for clearing — is an externality by construction.

It isn't that teams decide against non-human life. It's that no step in the process asks. There is no slot in a design review, a PRD, or a launch checklist where a river or a barn owl could come up, so it doesn't.

This repo is an attempt at that slot.

It draws on work that already exists and is rarely applied in product teams: **more-than-human design** (Wakkary, Forlano), **animal-computer interaction** (Mancini), multispecies ethnography, and the environmental-computing literature on the energy, water, and material cost of machine learning.

## What stops it being decoration

This genre collapses into virtue signalling in about a page. Three commitments hold it open:

**Name specific beings, not "nature."** "Migratory birds along the Atlantic flyway" is auditable. "The environment" isn't. Every stakeholder entry has to be specific enough that someone could go and check it.

**Quantify with honest proxies.** kWh, litres, hectares — stated as ranges, with the measurement boundary attached, and with uncertainty admitted rather than smoothed. Not a five-point vibes score.

**Force a decision.** Every finding ends in a change to the product, or it gets logged as accepted harm with a named individual attached. There is no third option and no composite score, because a score is how a decision gets made without anyone making it.

## The four lenses

| Lens | Question | Skills |
| --- | --- | --- |
| Who is affected | Which living things does this touch, and by what route? | `nonhuman-stakeholder-map`, `more-than-human-personas`, `downstream-consequence-scan` |
| What it costs | What does running it take from the world? | `ai-energy-footprint`, `water-and-land-impact`, `hardware-and-minerals`, `model-choice-tradeoffs` |
| When the user isn't human | An animal is using this. Now what? | `animal-computer-interaction`, `nonhuman-consent-and-agency`, `sensory-fit-design`, `conservation-tech-ethics` |
| What we're trading | What harm are we accepting, and who signed? | `harm-tradeoff-ledger`, `biosphere-red-lines`, `more-than-human-critique` |

A few things these lenses turn up that standard impact assessment misses:

- **The behavioural pathway.** The largest impact of most software is what human behaviour it changes, not what its servers draw. It's omitted from nearly every assessment because the harm happens through a user's free choice, and so feels like someone else's.
- **The epistemic pathway.** Making something visible changes what can be done to it. Satellite analysis that maps intact forest also maps it for the logger.
- **Rebound.** Efficiency lowers cost of use, which raises volume, which can exceed the saving. Reporting efficiency per unit as though it were the total is the standard error.
- **Water isn't fungible.** Carbon averages meaningfully across the globe; a litre does not. A global average water figure is the one number in this domain guaranteed to be locally wrong.
- **Refusal instead of consent.** An animal can't give informed consent — but it can refuse, behaviourally. The design question is never "can it consent?" It's "can it refuse, will we notice, and will we stop?"

## Install

```
/plugin marketplace add Owl-Listener/more-than-human-skills
/plugin install more-than-human@more-than-human-skills
```

Works in Claude Code. The `.gemini/extensions/` directory ships the same skills as a Gemini CLI extension.

## Plugin

| Plugin | Skills | Commands | Description |
| --- | --- | --- | --- |
| more-than-human | 14 | 3 | Non-human stakeholder mapping, AI footprint estimation, animal-computer interaction, and a harm tradeoff ledger with named acceptors. |

### All commands

| Command | Plugin | Description |
| --- | --- | --- |
| `/more-than-human:audit-more-than-human` | more-than-human | Run the full four-lens audit on a product or feature and output a findings report with a tradeoff ledger and named acceptors. |
| `/more-than-human:design-for-nonhuman-users` | more-than-human | Specify a system whose user is an animal — welfare requirements, sensory fit, refusal path, and behavioural success measures. |
| `/more-than-human:estimate-ai-footprint` | more-than-human | Produce a defensible per-session footprint estimate for an AI feature and a ranked list of reductions with their quality costs. |

## Where to start

- **Assessing something already built** — `/audit-more-than-human`, or `more-than-human-critique` for a review without the full pipeline.
- **You need a number for a roadmap argument** — `/estimate-ai-footprint`.
- **An animal will actually use the thing** — `/design-for-nonhuman-users`.
- **Setting policy before the hard case arrives** — `biosphere-red-lines`. This one is worth doing early; a line drawn with a signed offer on the table is a negotiation, not a line.

## On the numbers

Figures in this space move fast and vendor methodologies differ in what they include. The skills teach an estimation *method* and give order-of-magnitude anchors — they deliberately avoid hardcoding constants that will be wrong within a year. Every skill that produces a number instructs the agent to verify against current sources and to state the boundary of whatever figure it used.

## Status

Version 0.1. The framework is complete across all four lenses and the skills lint clean, but none of it has been run against a real product assessment yet. Expect the estimation skills in particular to need calibration once they meet a live case. Issues and corrections welcome — especially from people working in conservation technology, ACI, or environmental computing, where I am reading the literature rather than practising in it.

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md). Skills are nouns, commands are verbs, and every description says when to use it and how it differs from its nearest neighbour.

## Related

Built alongside [designer-skills](https://github.com/Owl-Listener/designer-skills) — the same conventions, linter, and generators.

## License

MIT — see [LICENSE](./LICENSE).
