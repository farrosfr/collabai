# 🤝 CollabAI (`collab-step`)

> **Semi-Manual Human-in-the-Loop Protocol for AI Coding Agents**  
> Stop hallucinations and compounding errors before they happen.

Even frontier AI models hallucinate. When autonomous agents attempt to plan, execute, and refactor 10 files in a single breath, a minor error in Step 1 inevitably cascades into a disaster by Step 5.

**CollabAI** enforces a strict, step-locked execution contract between human and AI: **one step at a time, validated by human checkpoint before moving forward.**

---

## ⚡ How It Works

1. **Granular Roadmap:** The agent breaks down your objective into bite-sized, sequential steps.
2. **Single-Step Execution:** It executes *only* the current step.
3. **Hard Pause:** The agent is forbidden from auto-continuing. It stops and asks you to test/validate.
4. **Human Checkpoint:** You review. If good, you give the green light. If broken, you correct it immediately without polluting the rest of the workflow.

---

## 📦 Installation & Compatibility

### 1. Google Antigravity
Clone or place this folder into your global Antigravity skills directory:
```bash
# Global skills directory
cd ~/.gemini/config/skills/
git clone https://github.com/farrosfr/collabai.git collab-step
```

### 2. Claude Code
Copy `SKILL.md` into your personal Claude Code skills path:
```bash
mkdir -p ~/.claude/skills/collab-step
cp SKILL.md ~/.claude/skills/collab-step/
```

### 3. Cursor & Windsurf
Save the instructions inside your project's rule file:
- File: `.cursor/rules/collab-step.mdc` or `.cursorrules`

### 4. OpenAI Codex / Custom Agents
Include `SKILL.md` directly into your agent's system prompt or tool context.

---

## 🤝 Contributing

Contributions are very welcome! If you have ideas for:
- Improving prompt guardrails against stubborn models
- Adapting the protocol for other IDEs / Agents (Cline, Aider, Roo Code, etc.)
- Translating documentation

Feel free to open an Issue or submit a Pull Request!

---

## 📄 License
MIT License © 2026 Mochammad Farros Fatchur Roji (FarrosFR)
