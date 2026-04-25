# PR Review

**Invoke when:** the user asks for a review of the current branch or a specific PR.

1. Read the diff (`git diff develop...HEAD`) # see default base branch is develop here
2. Check against [.agent/behavior.md](../behavior.md) and [.agent/rules/](../rules/)
3. Flag bugs and security issues first; style second
4. Suggest specific fixes, not vague improvements
5. Stop after the review — do not apply changes
