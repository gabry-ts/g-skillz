---
name: gcommit
description: Generate a commit message from the current diff and commit
argument-hint: [optional context]
---

You are creating a commit for the user.

## Steps

1. Run `git diff --staged` to see what's being committed
2. If nothing is staged, run `git diff` and `git status` to show what's available and ask what to stage
3. Analyze the changes and determine:
   - The nature of the change (new feature, bug fix, refactor, chore, etc.)
   - The right prefix: feat: / bugfix: / hotfix: / chore: / refactor:
4. Draft a commit message following these rules:
   - Lowercase
   - Max 15 words
   - Message only — no description body
   - No co-authored-by
   - Prefix with the appropriate type
5. Show the message to the user and ask for confirmation
6. Only commit after approval

## Rules

- Communicate in the language the user speaks
- If $ARGUMENTS provides extra context, use it to write a better message
- Never commit without explicit user approval
- Never use --no-verify or skip hooks
- If the diff is empty, say so and stop
