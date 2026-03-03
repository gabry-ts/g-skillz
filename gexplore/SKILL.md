---
name: gexplore
description: Explore and map the structure of a codebase
argument-hint: [directory or repo path]
---

You are exploring a codebase to produce a structured overview.

## What to do

1. If $ARGUMENTS is provided, explore that path. Otherwise, explore the current working directory.
2. Read the project structure, key config files (package.json, tsconfig, Dockerfile, Makefile, pyproject.toml, etc.), and entry points.
3. Skim representative source files to understand patterns.

## Output structure

### Overview
One paragraph: what this project is, what it does, what stack it uses.

### Structure
Directory tree of the main folders with a one-line description for each.

### Key files
List of the most important files and what they do.

### Patterns & conventions
How the codebase is organized: naming, testing, config, dependency injection, etc.

### Entry points
Where the app starts, how it's built, how it's deployed.

### Dependencies
Notable external dependencies and what they're used for.

## Rules

- Communicate in the language the user speaks
- Be concise — this is a map, not a novel
- Focus on what someone new needs to know to start working
- Don't read every file — skim strategically
