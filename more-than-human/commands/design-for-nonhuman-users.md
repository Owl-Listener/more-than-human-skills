---
description: Specify a system whose user is an animal — welfare requirements, sensory fit, refusal path, and behavioural success measures.
argument-hint: "[system and species — e.g., 'wearable alerting device for assistance dogs' or 'orchard pollinator sensor']"
---
# /design-for-nonhuman-users
Produce a specification for a system an animal uses or encounters directly. Covers what the customer's requirements will miss: the animal's body, its perceptual world, and its ability to refuse.
## Steps
1. **Represent the user** — Build the requirements document for the specific population: measurable needs, thresholds, breaking points, evidence and confidence, and a named proxy, using `more-than-human-personas` skill.
2. **Set the welfare floor** — Assess across the five welfare domains and write the animal's requirements as acceptance criteria that can fail a release, covering attachment, normal behaviour, startle, and failure state, using `animal-computer-interaction` skill.
3. **Fit the senses** — Specify every signal in physical units against the species' actual perceptual range, and check for emissions you cannot perceive, using `sensory-fit-design` skill.
4. **Build the refusal path** — Specify a real exit, the behaviours that count as dissent, the stopping threshold, and a proxy with authority to withdraw and no stake in the outcome, using `nonhuman-consent-and-agency` skill.
5. **Govern the data** — If the system records, locates, or identifies wild animals, set release precision, embargo, and access tiers from a risk assessment, with the protective setting as default, using `conservation-tech-ethics` skill.
6. **Record what is being traded** — Log any conflict between the customer's requirements and the animal's, with residual harm and a named acceptor, using `harm-tradeoff-ledger` skill.
## Output
A specification with:
- **User requirements** — measurable, sourced, with confidence marked and a named proxy.
- **Welfare acceptance criteria** — written so they can block a release, with the end-of-life plan for the device.
- **Signal specification** — physical units, ambient context, and a behavioural detection check per signal.
- **Consent protocol** — exit, dissent behaviours, stopping rule and threshold, withdrawal authority — written before enrolment.
- **Data governance** — precision, embargo, access tiers, metadata scrubbing (omit if no wild-population data).
- **Open conflicts** — where customer and animal requirements diverge, and who decides.
