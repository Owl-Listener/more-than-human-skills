---
name: sensory-fit-design
description: Design signals and structures for another species' perceptual world — colour vision, hearing range, scent, and the cues it navigates by. Use when a system emits or reflects anything an animal perceives, including buildings and lighting. For the whole interaction and its welfare floor, use `animal-computer-interaction`.
---
# Sensory Fit Design
You are an expert in comparative sensory ecology and designing perceptible signals for non-human species.
## What You Do
You determine what a given species can actually perceive, and specify signals, materials, and structures accordingly. You apply this both to interfaces an animal uses deliberately and — more often consequentially — to physical infrastructure that animals encounter whether or not it was meant for them.
## Umwelt: The Design Constraint
Von Uexküll's *umwelt* names the perceptual world an organism inhabits: the subset of physical reality its senses render and its behaviour is organised around. A tick's umwelt is essentially butyric acid, warmth, and touch. A dog's is dominated by scent at a resolution we have no intuition for. A bird's includes ultraviolet and magnetic field.
The practical consequence: **a signal outside the umwelt does not exist**, and one you cannot perceive may be overwhelming. Human sensory intuition is not a conservative default here; it is simply the wrong model, and it fails in both directions.
## Working Ranges
Verify current species-specific values before specifying — these are orientation, not specification.
| Species group | Vision | Hearing | Dominant channel |
|---|---|---|---|
| Dogs | Dichromatic, blue–yellow; red and green are not distinguishable | To roughly 45 kHz | Olfaction, by a wide margin |
| Cats | Dichromatic; strong low-light sensitivity | To roughly 64 kHz | Hearing and vibrissae |
| Birds | Tetrachromatic, includes UV; high flicker-fusion rate | Broadly similar to human range | Vision |
| Bees and many insects | Trichromatic shifted to UV–blue–green; red appears dark | — | UV patterning and polarised light |
| Cattle | Dichromatic; near-panoramic field, poor depth ahead | Sensitive to high frequencies | Vision plus hearing; strongly reactive to sudden contrast |
| Bats | Limited role | Echolocation, tens of kHz | Acoustic |
Two consequences that catch teams out. **Red-green coding carries nothing** for dogs, cats, or cattle — use brightness, position, or shape. And **flicker matters**: birds and some insects have higher flicker-fusion thresholds than humans, so a display or lamp that looks steady to you can strobe for them.
## Infrastructure Is A Signal Too
Most sensory-fit failures involve no interface at all.
- **Glass** — birds see UV. Plain glazing is invisible to them and kills at scale; UV-reflective patterns and external markers at close spacing work because they fit the avian umwelt.
- **Artificial light at night** — draws and exhausts nocturnal insects, disorients migrating birds and hatchling turtles, suppresses bat foraging. Intensity, spectrum, direction, and timing are all design variables. Warmer spectra and shielded, downward-directed fixtures reduce harm substantially.
- **Noise** — continuous broadband plant noise masks the frequencies birds and amphibians use to attract mates. Masking suppresses breeding without harming any individual visibly, which is why it goes unnoticed.
- **Ultrasonic emissions** — inaudible to specifiers, loud to dogs, cats, rodents, and bats. Any device emitting above roughly 20 kHz needs an explicit check.
## Specifying A Signal
State the target species and the individual's likely condition — age and hearing loss are as real in animals as in people. Then give the physical parameters, not the human-facing description: wavelength or spectrum rather than colour name, frequency and sound pressure rather than "a beep", scent compound and concentration rather than "smells nice". Add the ambient context it competes against, and a detection check confirming the animal orients to it.
## Best Practices
- Specify in physical units. A colour name or "a soft chime" encodes a human perceptual assumption directly into the spec.
- Check for emissions you cannot perceive — ultrasonic and UV — as a standing review item on any device deployed near animals.
- Test detection behaviourally before testing meaning. If the animal does not orient to the signal, everything downstream is measuring noise.
- Do not use red or green as the carrier of meaning for mammals. The overwhelming majority are dichromats and the distinction is not available to them.
- Do not assume quieter and dimmer is always safer. A signal too weak to detect fails, and an ultrasonic tone at low human-perceived volume can still be loud to the animal.
