# Game Development Pipeline

Track your progress by checking off items as you complete them.

---

## Phase 1 — Pre-production

- [ ] Fill out `.claude/rules/gdd.md` — concept, pillars, mechanics, art/audio direction
- [ ] Fill out `.claude/rules/game-design.md` — terminology and spatial/mechanical constraints
- [ ] **Systems Design** — list every system, its single responsibility, and dependencies
- [ ] **System Build Order** — group systems into tiers:
  - [ ] **Tier 1 (Foundation)** — systems everything else depends on *(e.g. GameManager, SceneLoader, input)*
  - [ ] **Tier 2 (Core Loop)** — minimum systems for an ugly-but-playable game *(e.g. player, basic enemy, win/lose)*
  - [ ] **Tier 3 (Supporting)** — systems that enrich the core loop *(e.g. scoring, progression, UI)*
  - [ ] **Tier 4 (Polish)** — juice, VFX, audio, difficulty tuning *(handled in Beta)*
- [ ] Fill out `.claude/rules/architecture.md` — finalize script table using the tiers above
- [ ] **Milestone 0** — GDD complete, all systems listed and tiered, architecture finalized

---

## Phase 2 — Production

> Build tier-by-tier. Per feature: implement → `check_compile_errors` → `play_game` test → `save_scene` → architecture review if needed.

### Tier 1 — Foundation
- [ ] *(list your Tier 1 systems here once defined)*

### Tier 2 — Core Loop
- [ ] *(list your Tier 2 systems here once defined)*

**Milestone 1** — Tier 1 + Tier 2 complete; core loop playable end-to-end
- [ ] Milestone 1 reached

### Tier 3 — Supporting Systems
- [ ] *(list your Tier 3 systems here once defined)*

**Milestone 2** — All features in, content complete, no placeholder mechanics
- [ ] Milestone 2 reached

---

## Phase 3 — Beta

- [ ] **Juice pass** — screen shake, particles, hit-stop, SFX, music, UI animations
- [ ] **Feel tuning** — tweak values via ScriptableObjects/Inspector (no code changes)
- [ ] **Difficulty tuning** — curve, pacing, escalation
- [ ] **Bug pass** — all known issues fixed
- [ ] **Performance pass** — GC allocs within budget, target frame rate stable
- [ ] **Ship** — final build, smoke test, release
