# Contributing

More-Than-Human Skills is maintained by MC Dean. Contributions are welcome — corrections especially. Much of this repo draws on conservation technology, animal-computer interaction, and environmental computing, fields I read rather than practise in. If something here is wrong, please say so.

## How to Contribute

- **Bugs, corrections, and small fixes** — open a PR directly.
- **New skills, commands, or larger changes** — open an issue first so we can discuss the approach.

## Guidelines

- Keep PRs focused — one change per PR.
- **Skills are nouns** (domain knowledge), **commands are verbs** (workflows).
- Every skill needs frontmatter with `name` and `description`.
- Every command needs `description` and `argument-hint`.
- Skill name must match its directory name.
- Every skill description must say **when to use it** and, where a near-neighbour exists, **where the boundary is**.
- No cross-plugin references in commands.

## Writing descriptions

The description is the only thing an agent reads when deciding which skill to fire:

```
<What it produces>. Use when <situation>. <Boundary against the nearest neighbour>.
```

Rules the linter enforces:

- **A "Use when ..." sentence is required.**
- **A boundary clause whenever a near-neighbour exists.** Name it and say what separates them.
- **Reference other skills in backticks** — `` `skill-name` `` in the same plugin, `` `skill-name` (plugin-name) `` elsewhere. The linter rejects references that don't resolve.
- **Under 400 characters.**

## Quality bar for this repo specifically

Beyond the shared bar, a skill here is ready when:

1. **It names beings, not categories.** If an example could be satisfied by writing "the environment", it is not concrete enough.
2. **Numbers come with a boundary and a range.** Any skill producing a figure must say what the figure includes and instruct the agent to verify against current sources. Do not hardcode constants that will be wrong in a year.
3. **It ends in a decision.** A skill that produces awareness without producing a change to the product, or a recorded acceptance, is decoration.
4. **It states its own limits.** Where the evidence is weak, say so. Overclaiming in this domain is how the whole framework gets dismissed.
5. **Best Practices includes at least one "do not"** — usually the highest-value line in the file.

## Verifying your work

Run these before every commit — CI runs the same set:

```
python3 scripts/lint-frontmatter.py
python3 scripts/check-runtimes.py
python3 scripts/generate-readmes.py
python3 scripts/generate-index.py
bash   scripts/build-gemini.sh
python3 scripts/check-marketplace.py
```

`lint-frontmatter.py` needs PyYAML (`pip install pyyaml`). It parses frontmatter the way the runtimes do, so **quote any value containing brackets, a colon, or a bare `yes`/`no`** — an unquoted `argument-hint: [like this]` is a YAML *list*, not a string.

Everything between the `BEGIN GENERATED INDEX` and `END GENERATED INDEX` markers in `INDEX.md` is rebuilt from skill descriptions. Don't edit it by hand. The two sections above the markers are hand-written and worth extending.

Commit whatever the generators change.

## License

By contributing, you agree that your contributions will be licensed under the MIT License.
