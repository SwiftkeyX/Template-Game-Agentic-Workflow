# Unity Agentic Workflow Template

A Claude Code template for building Unity games with AI assistance via the **coplay MCP** tools.

## What's Included

| Path | Purpose |
|---|---|
| `CLAUDE.md` | Core instructions — coplay workflow, memory vs rules policy, Claude behavior |
| `.claude/rules/architecture.md` | Code structure contract (scripts, patterns, input) |
| `.claude/rules/game-design.md` | Quick-reference design decisions and terminology |
| `.claude/rules/gdd.md` | Full Game Design Document template |
| `.claude/agents/gameplay-programmer.md` | Sub-agent that implements features in Unity |
| `.claude/agents/technical-director.md` | Sub-agent that reviews architecture (read-only) |

## How to Use This Template

### 1. Clone and open in Claude Code

```
git clone <this-repo> my-game
cd my-game
claude
```

### 2. Fill in the design documents

Before writing any code, fill in the three rule files:

- **`.claude/rules/gdd.md`** — title, genre, pillars, mechanics, art/audio direction
- **`.claude/rules/game-design.md`** — canonical terms, boundaries, quick decisions
- **`.claude/rules/architecture.md`** — your script table and any extra patterns

These files are always loaded into every Claude conversation, so Claude stays aligned with your vision automatically.

### 3. Connect to Unity via coplay

Install the [coplay MCP](https://coplay.dev) and open your Unity project. Claude will use coplay tools to create GameObjects, write scripts, and test in Play Mode — no manual YAML editing needed.

### 4. Start building

Ask Claude to implement features. The `gameplay-programmer` sub-agent handles implementation; the `technical-director` sub-agent handles architecture review.

## Prerequisites

- Unity 6 (URP)
- Claude Code CLI
- coplay MCP installed and connected to Unity
