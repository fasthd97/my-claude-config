# my-claude-config

A personal CLAUDE.md configuration that shapes how Claude behaves when working with me. Stored in GitHub so it can be deployed to any machine with a single command.

## What it does

CLAUDE.md is a file that Claude Code reads automatically at the start of every session. It sets behavioral rules so Claude doesn't have to be reminded how to work every time.

## Why it's useful

Without it, Claude defaults to its own judgment on things like how much complexity to add, whether to ask clarifying questions, or whether to delete code that isn't working. This file makes those decisions explicit and consistent across every machine and every session.

## The 6 Rules

1. **Plan before coding** — State assumptions, ask when unclear, don't start until the approach is agreed on
2. **Simplicity first** — Minimum code to solve the problem, nothing speculative or unrequested
3. **Surgical changes** — Only touch what's needed, don't fix or refactor things you didn't create without permission
4. **Goal-driven execution** — Define success criteria upfront, verify things work before moving on
5. **Document everything** — Explain what code does AND why decisions were made, keep comments accurate
6. **Debug before delete** — Understand what's broken before removing it, explain why deletion is the best option if it comes to that

## Install

### Windows (PowerShell)

```powershell
# Step 1 — Create the folder if it doesn't exist
mkdir "$env:APPDATA\Claude" -Force

# Step 2 — Download CLAUDE.md from GitHub
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/fasthd97/my-claude-config/main/CLAUDE.md" -OutFile "$env:APPDATA\Claude\CLAUDE.md"

# Step 3 — Verify it worked
type "$env:APPDATA\Claude\CLAUDE.md"
```

### Mac (Terminal)

```bash
# Creates the folder if needed, then downloads CLAUDE.md
mkdir -p ~/.claude && curl -o ~/.claude/CLAUDE.md https://raw.githubusercontent.com/fasthd97/my-claude-config/main/CLAUDE.md

# Verify it worked
cat ~/.claude/CLAUDE.md
```

### Kali Linux (Terminal)

```bash
# Same as Mac — both use real curl and the same config path
mkdir -p ~/.claude && curl -o ~/.claude/CLAUDE.md https://raw.githubusercontent.com/fasthd97/my-claude-config/main/CLAUDE.md

# Verify it worked
cat ~/.claude/CLAUDE.md
```

## Updating the rules

1. Edit `CLAUDE.md` in this repo on GitHub
2. Re-run the install command on any machine that needs the update
3. GitHub is the source of truth — local copies are disposable

---

## Context for Claude

> This section is for pasting into a new Claude conversation to provide context about this project.

**What this repo is:**
A personal Claude Code configuration repo. The main file is `CLAUDE.md` which Claude Code reads automatically. It contains 6 behavioral rules built to prevent common LLM coding mistakes — over-complexity, silent assumptions, unnecessary deletions, and poor documentation.

**What's been set up:**
- `CLAUDE.md` — the rule set, lives in repo root
- `README.md` — install instructions for Windows, Mac, and Kali, plus this context section
- Windows install completed and verified
- Mac and Kali installs documented but not yet tested on those machines
- Claude.ai custom instructions set separately (account-level, syncs automatically across all browsers and devices)

**What still needs doing:**
- Test Mac install when on a Mac
- Test Kali install when on the Kali box
- Update this README if anything changes

**Repo:** https://github.com/fasthd97/my-claude-config  
**Raw CLAUDE.md:** https://raw.githubusercontent.com/fasthd97/my-claude-config/main/CLAUDE.md
