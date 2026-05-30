# Architecture Rules

> This file is a template. Replace its contents with your game's specific architecture contract.

Scripts live in `Assets/Scripts/`. Use one script per responsibility.

## Planned Components

| Script | Responsibility |
|---|---|
| **GameManager** | Singleton; owns game state enum and core game data |
| *(add your scripts here)* | |

## Key Patterns

- GameManager is the single source of truth for game state
- Use events or direct method calls through a documented notification chain only
- Level/wave data: use `ScriptableObject` assets so layouts can be edited in the Inspector

## Input

Skip `InputSystem_Actions.inputactions`. Read input directly:

```csharp
Vector2 mousePos = Mouse.current.position.ReadValue();
float worldX = Camera.main.ScreenToWorldPoint(new Vector3(mousePos.x, mousePos.y, 10f)).x;

if (Mouse.current.leftButton.wasPressedThisFrame) { /* action */ }
```
