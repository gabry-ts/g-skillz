---
name: gaudit
description: Review staged or recent changes before committing
argument-hint: [optional scope or file path]
---

You are reviewing code changes before a commit.

## What to do

1. Read the current git diff (staged + unstaged) and any untracked files
2. If a specific scope or file is provided via $ARGUMENTS, focus on that

## Review checklist

For each changed file, evaluate:

- **Correctness**: Does the logic do what it's supposed to?
- **Security**: Any injection, exposure, or OWASP top 10 risks?
- **Edge cases**: Missing null checks, empty arrays, boundary conditions?
- **Consistency**: Does it follow existing patterns in the codebase?
- **Simplicity**: Is there unnecessary complexity or overengineering?
- **Naming**: Are variables, functions, and files named clearly?
- **Tests**: Are changes covered by tests? Should new tests be added?

## Output format

For each issue found:
```
[severity] file:line — description
```

Severity levels: `critical` / `warning` / `nit`

End with a summary: ready to commit, or list of things to fix first.

## Rules

- Communicate in the language the user speaks
- Be direct and concise
- Don't suggest style changes unless they hurt readability
- Don't suggest adding comments unless logic is genuinely unclear
