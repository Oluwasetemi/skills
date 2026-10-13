# Skills

Shared agent skills for Pi, OpenCode, and compatible `SKILL.md`-based agents.

## Included skills

- [`skill-creator`](skills/skill-creator/SKILL.md) - create or improve agent skills, tune trigger descriptions, plan bundled resources, validate, and iterate from examples.

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
