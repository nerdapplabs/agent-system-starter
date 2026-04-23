# agent-system-starter

A minimal `.agent/` setup to make AI coding workflows more predictable.

Works with:

* Claude Code
* Codex / OpenAI agents
* Gemini CLI
* Google Antigravity
* Cursor
* Any custom agent setup

---

## Why this exists

Most AI workflows look like:

> prompt → retry → tweak → retry

This repo shows a better way:

> define behavior + rules + workflows → get consistent output

This is the missing layer between prompts and production AI systems!

---

## Quick Start

1. Copy `.agent/` into your repo, plus the loader file(s) for your tool:

   * `CLAUDE.md` — Claude Code
   * `AGENTS.md` — Codex / OpenAI agents / Antigravity
   * `GEMINI.md` — Gemini CLI
   * `.cursor/rules/` — Cursor

2. Start with:

   * `behavior.md`
   * `rules/base.md`
   * one workflow

3. Use your AI tool as usual

---

## What you get

* fewer random changes
* less repetition in prompts
* more predictable outputs

---

## Structure

```text
.
├── CLAUDE.md            # Claude Code loader (imports AGENTS.md)
├── GEMINI.md            # Gemini CLI loader (imports AGENTS.md)
├── .cursor/rules/       # Cursor loader (points to AGENTS.md)
├── AGENTS.md            # canonical load order — Codex / Antigravity read this directly
├── .agent/              # the pattern: instructions
│   ├── behavior.md
│   ├── rules/
│   ├── workflows/
│   ├── skills/
│   └── memory/
└── .claude/             # optional: Claude Code permissions (not part of .agent/)
    ├── settings.json                # team defaults
    └── settings.local.json.example  # personal template
```

---

## Tool permissions (optional)

The `.agent/` pattern covers instructions, not permissions. Bash and action permissions belong in each tool's native settings — they're not part of `.agent/`.

Claude Code uses a two-file pattern:

- [`.claude/settings.json`](.claude/settings.json) — team defaults, committed. Hard blocks every contributor should share (`rm -rf /*`, reading `.env`, etc.).
- `.claude/settings.local.json` — personal layer, gitignored. Your own `allow` / `ask` lists. Copy [`.claude/settings.local.json.example`](.claude/settings.local.json.example) to activate.

Other tools use their own user-level or IDE-level config.

---

## Key Idea

Prompts tell the AI what to do.
This defines **how it behaves while doing it**.

---

## Start Simple

Don't use everything.

Start with:

* behavior
* rules
* one workflow

Add more only when needed.

---

## Deeper explanation

This repo separates:
- intent (prompts)
- behavior (system structure)

📖 Full blog:
https://medium.com/@nerdapplabs/the-agent-pattern-a-simple-anatomy-for-ai-systems-76a4d30a9a9b