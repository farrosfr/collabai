# CollabAI (collab-step)

A human-in-the-loop (HITL) step-locked protocol for AI coding agents.

## Problem

Frontier LLMs frequently hallucinate and compound errors when executing multi-step tasks autonomously. An undetected error in step 1 cascades across subsequent files and tool calls, requiring tedious manual rollbacks.

## Solution

CollabAI enforces a strict execution contract:
1. Break down the task into an explicit, sequential roadmap.
2. Execute exactly one step per turn.
3. Halt execution and wait for human validation before proceeding to the next step.

## Installation

### Google Antigravity
Clone into your global skills directory:
```bash
cd ~/.gemini/config/skills/
git clone https://github.com/farrosfr/collabai.git collab-step
```

### Claude Code
Copy `SKILL.md` to your Claude skills directory:
```bash
mkdir -p ~/.claude/skills/collab-step
cp SKILL.md ~/.claude/skills/collab-step/
```

### Cursor & Windsurf
Add the contents of `SKILL.md` to your project rules:
- `.cursor/rules/collab-step.mdc` or `.cursorrules`

### OpenAI Codex / Other Agents
Include `SKILL.md` directly into the system instructions or agent context.

## Contributing

Pull requests and issues are welcome for:
- Improving prompt guardrails against autonomous chaining
- Compatibility guides for other agents (Aider, Cline, Roo Code)
- Documentation improvements

## License

MIT License (c) 2026 Mochammad Farros Fatchur Roji (FarrosFR)
