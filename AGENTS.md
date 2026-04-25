# Agents — Load Order

This repo uses the `.agent/` pattern. Before acting on any task, read:

1. [.agent/behavior.md](.agent/behavior.md) — how to operate and how to code
2. [.agent/rules/](.agent/rules/) — all files; hard constraints

When a task matches a workflow, follow it:

- Bug fix → [.agent/workflows/fix-bug.md](.agent/workflows/fix-bug.md)
- Docker issue → [.agent/workflows/debug-docker.md](.agent/workflows/debug-docker.md)

If no workflow matches, fall back to behavior + rules.

## Skills

Named procedures the user invokes by name (*"run the pr-review skill"*). Unlike workflows, the agent doesn't auto-select skills. Check [.agent/skills/](.agent/skills/) for the full list.

- [.agent/skills/pr-review.md](.agent/skills/pr-review.md) — review the current diff

## Precedence

rules > workflow steps > behavior

A rule always wins. If a workflow step conflicts with a rule, stop and explain.

## Memory

Check [.agent/memory/](.agent/memory/) for prior decisions and known issues before proposing changes.
