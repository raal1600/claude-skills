# Claude skills

Skills for [Claude Code](https://claude.com/claude-code).

| Skill | What it does |
|---|---|
| [build-patterns](build-patterns/SKILL.md) | How to design, build and ship software with an owner so the first version is the right one: one vocabulary, derived status, a record for every run, safe data changes, app-level defaults, and a way of working that shows one real screen first, verifies by measurement and an independent reviewer, and asks before publishing. |
| [apple-interfaces](apple-interfaces/SKILL.md) | How to lay out, build and check an interface the way Apple's own apps work: the app shell (sidebar, account area, toolbar), summary, list and detail levels, split view and navigation stack, lists before tables, inspectors, popovers and sheets, a current item that drives every page, visible runs, the right control for each choice, and a measured check. Companion to build-patterns. |
| [helper-sessions](helper-sessions/SKILL.md) | How to split work across helper sessions or agents and bring it back together without rework: visible helpers, contracts frozen first, one owner per file, briefs that settle questions up front, trial merges, corrections routed to the builder, work sized to the allowance. |
| [stay-in-scope](stay-in-scope/SKILL.md) | Keeps agents' web reads, searches and outside calls to what the task needs: no unrequested policy research, re-checks or exploration; stop at real blocks. |

## Install

Copy a skill folder into `~/.claude/skills/` (for all your projects) or `.claude/skills/` in one project:

```bash
git clone https://github.com/raal1600/claude-skills.git
cp -r claude-skills/build-patterns ~/.claude/skills/
```
