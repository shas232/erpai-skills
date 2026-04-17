# ERP AI Skills

A collection of Claude Code skills for working with ERPAI apps.

## Skills

| Skill | Purpose |
|---|---|
| [test-erpai-app](./test-erpai-app/SKILL.md) | **Testing agent** — end-to-end smoke test for any ERPAI app. Discovers schema, infers data-load order from refs, seeds realistic multi-record data covering every column + branch, verifies rollups/formulas/lookups, ensures every dashboard lights up with real data, checks reports + roles + workflows, then outputs a pass/fail report. |

## Install

Drop any skill folder into your `~/.claude/skills/` directory:

```bash
git clone https://github.com/shas232/erpai-skills.git ~/.claude/skills-erpai
# Symlink or copy individual skills into ~/.claude/skills/
ln -s ~/.claude/skills-erpai/test-erpai-app ~/.claude/skills/test-erpai-app
```

Or clone directly into `~/.claude/skills/`:

```bash
cd ~/.claude/skills/
git clone https://github.com/shas232/erpai-skills.git
# Each sub-folder becomes a discoverable skill
```

## Invoking

Claude Code auto-loads all skills in `~/.claude/skills/`. After install, Claude will trigger `test-erpai-app` when you say things like:

- "Test the app"
- "QA the app end-to-end"
- "Run a full smoke test"
- "Verify data flow"
- "Is the app working?"

## Contributing

Each skill is a single folder with a `SKILL.md` at its root. The frontmatter declares the name, description, and allowed tools. See [test-erpai-app/SKILL.md](./test-erpai-app/SKILL.md) for the reference format.
