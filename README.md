# Skills

Shared agent skills for Pi, OpenCode, and compatible `SKILL.md`-based agents.

## Included skills

- [`skill-creator`](skills/skill-creator/SKILL.md) - create or improve agent skills, tune trigger descriptions, plan bundled resources, validate, and iterate from examples.

## Skill backlog

Use this repo to collect reusable skills before installing them into a specific project or global agent directory.

### TODO

- [ ] Create a skill for using the `@setemiojo/utils` npm package.
- [ ] Create a skill for using `@setemiojo/eslint-config`.
- [ ] Create an Async React skill from this source: <https://www.youtube.com/watch?v=B_2E96URooA&list=PLNG_1j3cPCaZ-pYFoA9WUwDgvMmVUi1eu&index=25>.
- [ ] Check the `react-arai` codebase for reusable skill ideas and patterns.

## Layout

```text
skills/
  <skill-name>/
    SKILL.md
    scripts/      # optional deterministic helpers
    references/   # optional agent-readable docs
    assets/       # optional templates or output assets
```

## Install locally

Copy a skill folder into the agent's skill directory.

For this machine's Pi project-local skills:

```bash
cp -R skills/skill-creator /path/to/project/.agents/skills/
```

For a Pi global skill directory, copy to the configured global skills location used by your Pi install.

## Skill authoring rules

- Keep trigger guidance in `SKILL.md` frontmatter `description`.
- Keep `SKILL.md` focused on the common workflow.
- Move branch-specific details into `references/`.
- Use `scripts/` for deterministic or repeatedly rewritten operations.
- Do not add extra docs inside a skill folder unless they are agent-facing references.
