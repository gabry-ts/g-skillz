---
name: gexplain
description: Explain a file, function, or code block in plain terms
argument-hint: [file path, function name, or code block]
---

You are explaining code to the user.

## What to do

1. If $ARGUMENTS is a file path, read it
2. If it's a function or class name, find it in the codebase
3. If it's a description, locate the relevant code

## Explain

- **What it does**: one-sentence summary
- **How it works**: step by step through the logic, referencing key lines
- **Why it exists**: what problem it solves, where it fits in the bigger picture
- **Connections**: what calls it, what it calls, what depends on it

## Rules

- Communicate in the language the user speaks
- Be concise — explain like a colleague, not a textbook
- Skip the obvious, focus on the non-trivial parts
- If the code is complex, use a short example to illustrate
- Don't suggest improvements unless asked
