# Claude skills

Skills for [Claude Code](https://claude.com/claude-code).

| Skill | What it does |
|---|---|
| [build-patterns](build-patterns/SKILL.md) | Principles for designing and changing software: one vocabulary, derived statuses, staged automation with handoffs, a minimal data model, calm Apple-style interfaces, end-to-end verification. |
| [apple-interfaces](apple-interfaces/SKILL.md) | How to lay out and check an interface the way Apple's own apps work: summary, list and detail levels; split view on wide screens, navigation stack on a phone; lists before tables; inspectors, popovers and sheets; screens that follow the selection. Companion to build-patterns. |
| [stay-in-scope](stay-in-scope/SKILL.md) | Keeps agents' web reads, searches and outside calls to what the task needs: no unrequested policy research, re-checks or exploration; stop at real blocks. |

## Install

Copy a skill folder into `~/.claude/skills/` (for all your projects) or `.claude/skills/` in one project:

```bash
git clone https://github.com/raal1600/claude-skills.git
cp -r claude-skills/build-patterns ~/.claude/skills/
```
