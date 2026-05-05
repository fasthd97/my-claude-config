#my-claude-config
This repo stores my personal CLAUDE.md — a set of behavioral rules that shape how Claude behaves when I'm working with it. It covers how to plan before coding, keep things simple, document decisions, and debug before deleting.
The rules are based on Andrej Karpathy's observations about common LLM coding mistakes, with two additional rules added for documentation and debugging discipline.
Storing it here means one place to update the rules, and one command to deploy to any machine.
Install
Windows (PowerShell)
powershellInvoke-WebRequest -Uri "https://raw.githubusercontent.com/fasthd97/my-claude-config/main/CLAUDE.md" -OutFile "$env:APPDATA\Claude\CLAUDE.md"
Mac / Kali Linux (Terminal)
bashmkdir -p ~/.claude && curl -o ~/.claude/CLAUDE.md https://raw.githubusercontent.com/fasthd97/my-claude-config/main/CLAUDE.md
Updating the rules
Edit CLAUDE.md in this repo, then re-run the install command on any machine that needs the update.
