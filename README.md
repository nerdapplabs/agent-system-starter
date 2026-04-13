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

1. Copy `.agent/` into your repo

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
.agent/
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

Don’t use everything.

Start with:

* behavior
* rules
* one workflow

Add more only when needed.

-- 
## Why this exists

Most AI workflows rely heavily on prompts, which leads to inconsistent behavior.

This repo shows a simple way to separate:
- intent (prompts)
- behavior (system structure)

If you want a deeper explanation, We’ve written it here:

📖 Full blog:
https://medium.com/@nerdapplabs/the-agent-pattern-a-simple-anatomy-for-ai-systems-76a4d30a9a9b