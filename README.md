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
