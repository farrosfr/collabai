# CollabAI (collab-step)

A human-in-the-loop (HITL) step-locked protocol for AI coding agents.

## Problem

Frontier LLMs frequently hallucinate and compound errors when executing multi-step tasks autonomously. Furthermore, agents often waste tokens and time generating lengthy 5-step roadmap outlines before writing a single line of actionable code.

## Solution

CollabAI enforces a strict, laser-focused execution contract:
1. **Zero upfront outline bloat:** The agent never dumps a speculative roadmap. It begins directly with Step 1.
2. **Execute only the active step:** Every response is short, focused, and immediately actionable.
3. **Hard pause for human checkpoint:** The agent halts execution after each step, waiting for your test results before moving to the next step.

## Token & Speed Efficiency

CollabAI makes agent interactions significantly faster and cheaper:
- **Instant responses:** Eliminates the 30-60 second thinking delay spent generating speculative outlines.
- **Eliminates self-correction spirals:** Catching mistakes immediately prevents 20,000+ token repair loops.
- **Minimizes expensive output tokens:** Emits concise 100-250 token instructions per step rather than speculative multi-file dumps.
- **Optimized for prompt caching:** Turn-by-turn context reads utilize modern prompt caching (80-90% cheaper input rates).

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
