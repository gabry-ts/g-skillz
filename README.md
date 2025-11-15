# g-skillz

A collection of practical Claude Code skills for a structured, no-nonsense development workflow.

## Skills

| Skill | Description |
|-------|-------------|
| `/gdraft` | Iterative questioning until full understanding, then a structured implementation plan |
| `/gaudit` | Review staged or recent changes before committing (severity: critical/warning/nit) |
| `/gexplore` | Explore and map the structure of a codebase |
| `/gfix` | Investigate a bug or error, find the root cause, propose a fix |
| `/gexplain` | Explain a file, function, or code block in plain terms |
| `/gcommit` | Generate a commit message from the current diff and commit |

## Installation

### All skills

```bash
git clone https://github.com/gabry-ts/g-skillz.git ~/.claude/skills
```

### Single skill

Copy the desired skill folder into your `~/.claude/skills/` directory:

```bash
mkdir -p ~/.claude/skills
cp -r gdraft ~/.claude/skills/
```

### As a submodule (for dotfiles repos)

```bash
git submodule add https://github.com/gabry-ts/g-skillz.git skills
```

## Usage

Once installed, use any skill by typing its name in Claude Code:

```
/gdraft build a REST API for user management
/gaudit
/gexplore ./src
/gfix TypeError: Cannot read property 'id' of undefined
/gexplain src/auth/jwt.service.ts
/gcommit
```

## Philosophy

- Ask before doing — never assume
- Plans before code — understand first, build second
- Keep it simple — no overengineering
- Communicate in Italian — code in English

## License

MIT — see [LICENSE](LICENSE) for details.
