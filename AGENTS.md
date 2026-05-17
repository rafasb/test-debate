# AGENTS.md

## Core Workflow

Run the structured 5-round AI debate:
```
/debate
```
This invokes the debate command which orchestrates Agente A (pro-IA) and Agente B (anti-IA) through 5 rounds and generates a consensus document.

## Agent Definitions

- **Agente A** (Defensor IA): `.opencode/agents/agente-a.md`
- **Agente B** (Crítico IA): `.opencode/agents/agente-b.md`

## Generated Files

During debate execution:
- Individual responses: `agente-a-ronda-[N].md` and `agente-b-ronda-[N].md` (N=1-5)
- Final consensus: `consenso-final.md` (created after round 5)

> **Rule**: All generated files (`agente-a-ronda-[N].md`, `agente-b-ronda-[N].md`, `consenso-final.md`) **must** be saved inside the debate's own directory (`DEBATE-[NN]/`). No debate files may be written to the workspace root.

## Key Commands

- Start debate: `/debate`
- View agent instructions: Read files in `.opencode/agents/`
- Check debate protocol: `.opencode/commands/debate.md`

## Output Format

Each round follows:
```
---
## Ronda [N]

### Agente A (Defensor)
[response]

### Agente B (Crítico)
[response]
---
```

Consensus document must include:
1. Points of agreement
2. Points of disagreement  
3. Concrete solutions both positions could accept