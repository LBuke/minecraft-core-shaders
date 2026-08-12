# Minecraft 1.19.4 — core shaders

| | |
|---|---|
| **Minecraft version** | `1.19.4` |
| **Protocol version** | `762` |
| **Shader files** | 270 |
| **Folders** | `core/` (175), `include/` (4), `post/` (26), `program/` (65) |

## Changes since 1.19.3

`+6 added` · `-0 removed` · `~14 modified`

- **Enchantment glint strength becomes controllable.** A `GlintAlpha` uniform is added to all seven glint shaders and their JSONs, and multiplied into the fog fade: `linear_fog_fade(...) * GlintAlpha`. This is what backs the *Glint Strength* video setting.
- Adds `rendertype_text_background` and `rendertype_text_background_see_through` for the text background/shadow rendering introduced with the new chat and sign text.

**Added (6)**

- `core/rendertype_text_background.fsh`
- `core/rendertype_text_background.json`
- `core/rendertype_text_background.vsh`
- `core/rendertype_text_background_see_through.fsh`
- `core/rendertype_text_background_see_through.json`
- `core/rendertype_text_background_see_through.vsh`

<details>
<summary><b>Modified (14)</b></summary>

- `core/rendertype_armor_entity_glint.fsh`
- `core/rendertype_armor_entity_glint.json`
- `core/rendertype_armor_glint.fsh`
- `core/rendertype_armor_glint.json`
- `core/rendertype_entity_glint.fsh`
- `core/rendertype_entity_glint.json`
- `core/rendertype_entity_glint_direct.fsh`
- `core/rendertype_entity_glint_direct.json`
- `core/rendertype_glint.fsh`
- `core/rendertype_glint.json`
- `core/rendertype_glint_direct.fsh`
- `core/rendertype_glint_direct.json`
- `core/rendertype_glint_translucent.fsh`
- `core/rendertype_glint_translucent.json`

</details>

---

◀ [1.19.3](../1.19.3/README.md) · [All versions](../README.md) · [1.20](../1.20/README.md) ▶
