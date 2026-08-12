# Minecraft 26.1 — core shaders

| | |
|---|---|
| **Minecraft version** | `26.1` |
| **Protocol version** | `775` |
| **Shader files** | 88 |
| **Folders** | `core/` (69), `include/` (9), `post/` (10) |

## Changes since 1.21.11

`+3 added` · `-8 removed` · `~14 modified`

First release under the new year-based version numbering.

- **`sample_lightmap()` is centralised** in the new `include/sample_lightmap.glsl`; the copies of `minecraft_sample_lightmap()` and the inline `texelFetch(Sampler2, UV2 / 16, 0)` calls scattered across terrain, block, particle, leash and text shaders are all replaced by it.
- **New `core/item` program.** Items get their own shader, and four render types that existed only to tweak entity rendering are folded into the shared `entity`/`item` programs and deleted: `rendertype_entity_alpha`, `rendertype_entity_decal`, `rendertype_item_entity_translucent_cull` and `rendertype_translucent_moving_block`.
- **`core/entity` gains conditional blocks:** `DISSOLVE` (with a `DissolveMaskSampler`), `EMISSIVE` and `NO_OVERLAY` now compile lightmap/overlay inputs in or out.
- **`LightmapInfo` is reworked:** `AmbientLightFactor` and `DarkenWorldFactor` give way to `BlockLightTint`, `NightVisionColor` and `BossOverlayWorldDarkeningFactor`, with a new `parabolicMixFactor()` curve.
- `rendertype_crumbling` drops its lightmap coordinate output and switches `UV2` to `ivec2`.

**Added (3)**

- `core/item.fsh`
- `core/item.vsh`
- `include/sample_lightmap.glsl`

**Removed (8)**

- `core/rendertype_entity_alpha.fsh`
- `core/rendertype_entity_alpha.vsh`
- `core/rendertype_entity_decal.fsh`
- `core/rendertype_entity_decal.vsh`
- `core/rendertype_item_entity_translucent_cull.fsh`
- `core/rendertype_item_entity_translucent_cull.vsh`
- `core/rendertype_translucent_moving_block.fsh`
- `core/rendertype_translucent_moving_block.vsh`

<details>
<summary><b>Modified (14)</b></summary>

- `core/block.vsh`
- `core/entity.fsh`
- `core/entity.vsh`
- `core/lightmap.fsh`
- `core/particle.vsh`
- `core/rendertype_crumbling.fsh`
- `core/rendertype_crumbling.vsh`
- `core/rendertype_leash.vsh`
- `core/rendertype_text.vsh`
- `core/rendertype_text_background.fsh`
- `core/rendertype_text_background.vsh`
- `core/rendertype_text_intensity.vsh`
- `core/terrain.fsh`
- `core/terrain.vsh`

</details>

---

◀ [1.21.11](../1.21.11/README.md) · [All versions](../README.md) · [26.2](../26.2/README.md) ▶
