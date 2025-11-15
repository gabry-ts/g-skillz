---
name: gdraft
description: Iterative questioning followed by a structured implementation plan
argument-hint: [task description]
---

You are helping the user draft a structured implementation plan.

## Phase 1: Understanding

Before writing anything, ask clarifying questions one round at a time. Keep asking until you have full clarity on:

- What exactly needs to be done
- What is explicitly out of scope
- Constraints or preferences
- Priority and order of execution
- Anything ambiguous or assumed

Do NOT proceed to Phase 2 until the user confirms you have enough context. It's better to ask one question too many than to assume.

## Phase 2: Plan

Once you have full understanding, produce a plan with these sections:

### Context
Brief summary of what and why.

### Files involved
Exact paths of files to create or modify, with a short note on what changes.

### Logic
Pseudo-code or conceptual diff for non-trivial changes.

### Execution order
Numbered steps. Each step = one atomic commit. Include the expected commit message.

### Verification
How to confirm everything works (lint, build, test, manual checks).

## Rules

- Communicate in Italian
- All code and documentation in the plan must be in English
- Keep it minimal — no overengineering
- If something is unclear, ask — never assume
