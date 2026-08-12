# Minecraft 1.20 — core shaders

| | |
|---|---|
| **Minecraft version** | `1.20` |
| **Protocol version** | `763` |
| **Shader files** | 276 |
| **Folders** | `core/` (181), `include/` (4), `post/` (26), `program/` (65) |

## Changes since 1.19.4

`+12 added` · `-6 removed` · `~0 modified`

- Adds four GUI render types — `rendertype_gui`, `rendertype_gui_overlay`, `rendertype_gui_ghost_recipe_overlay` and `rendertype_gui_text_highlight` — as the GUI moves onto the same core shader system as the world.
- Removes `core/block` and `core/new_entity`, two leftover shaders that were never used by the game.

**Added (12)**

- `core/rendertype_gui.fsh`
- `core/rendertype_gui.json`
- `core/rendertype_gui.vsh`
- `core/rendertype_gui_ghost_recipe_overlay.fsh`
- `core/rendertype_gui_ghost_recipe_overlay.json`
- `core/rendertype_gui_ghost_recipe_overlay.vsh`
- `core/rendertype_gui_overlay.fsh`
- `core/rendertype_gui_overlay.json`
- `core/rendertype_gui_overlay.vsh`
- `core/rendertype_gui_text_highlight.fsh`
- `core/rendertype_gui_text_highlight.json`
- `core/rendertype_gui_text_highlight.vsh`

**Removed (6)**

- `core/block.fsh`
- `core/block.json`
- `core/block.vsh`
- `core/new_entity.fsh`
- `core/new_entity.json`
- `core/new_entity.vsh`

---

◀ [1.19.4](../1.19.4/README.md) · [All versions](../README.md) · [1.20.1](../1.20.1/README.md) ▶
