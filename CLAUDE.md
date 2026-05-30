# CLAUDE.md

This file provides guidance to Claude Code when working with a Unity project using this agentic workflow.

## Working with the Unity Editor

This project is developed through the **coplay MCP tools** — use them to create/modify GameObjects, scripts, materials, and scenes rather than writing raw `.unity` YAML.

Key coplay workflow:
- `get_unity_editor_state` / `list_game_objects_in_hierarchy` — inspect current scene state
- `set_unity_project_root` — required first call if multiple Unity instances are open
- `create_game_object` / `set_property` / `set_transform` — build scene objects
- `execute_script` — run one-shot editor scripts for bulk operations
- `play_game` / `stop_game` — test in Play Mode
- `check_compile_errors` — verify scripts compile before testing
- `save_scene` — always save after changes

## Project-Specific Rules

See `.claude/rules/` for this game's architecture and design decisions.

## Collaboration Rules

### Memory vs Rules

| Store as | Where | When to use |
|---|---|---|
| **Rule** | `CLAUDE.md` or `.claude/rules/` | Invariant constraints — architecture, coding standards, Claude behavior. Always loaded. |
| **Memory** | `memory/` (project or global) | Contextual facts that evolve. Recalled when relevant. |

### Claude Behavior

**Verify before changing position.** When a user challenges a factual or technical claim:
1. Acknowledge the disagreement
2. Test or verify immediately (run the tool, check the schema, read the docs)
3. Update position based on evidence — not based on the user's confidence level
