# agent-system-starter

A minimal `.agent/` setup to make AI coding workflows more predictable.

Works with:

* Claude Code
* OpenAI / Codex-style agents
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
   * `AGENTS.md` — Codex / OpenAI agents
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
├── AGENTS.md            # canonical load order — Codex / OpenAI agents
├── GEMINI.md            # Gemini CLI loader (imports AGENTS.md)
├── .cursor/rules/       # Cursor loader (points to AGENTS.md)
└── .agent/
    ├── behavior.md
    ├── coding-guidelines.md
    ├── rules/
    ├── workflows/
    ├── skills/
    ├── memory/
    └── permissions.json
```

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