# Minecraft 1.21 — core shaders

| | |
|---|---|
| **Minecraft version** | `1.21` |
| **Protocol version** | `767` |
| **Shader files** | 200 |
| **Folders** | `core/` (166), `include/` (4), `post/` (6), `program/` (24) |

## Changes since 1.20.6

`+0 added` · `-9 removed` · `~58 modified`

- The `"blend"` block is removed from 56 shader JSONs; blend state is now set by the game's render types instead of being declared in the pack.
- `blit_screen` is rewritten to draw a fullscreen quad directly from vertex positions (`Position.xy * 2.0 - 1.0`) with no `ModelViewMat`/`ProjMat`/`ColorModulator`.
- Removes `position_color_tex`, `rendertype_armor_glint` and `rendertype_glint_direct`, which are now covered by other render types.

**Removed (9)**

- `core/position_color_tex.fsh`
- `core/position_color_tex.json`
- `core/position_color_tex.vsh`
- `core/rendertype_armor_glint.fsh`
- `core/rendertype_armor_glint.json`
- `core/rendertype_armor_glint.vsh`
- `core/rendertype_glint_direct.fsh`
- `core/rendertype_glint_direct.json`
- `core/rendertype_glint_direct.vsh`

<details>
<summary><b>Modified (58)</b></summary>

- `core/blit_screen.fsh`
- `core/blit_screen.json`
- `core/blit_screen.vsh`
- `core/particle.json`
- `core/position.json`
- `core/position_color.json`
- `core/position_color_lightmap.json`
- `core/position_color_tex_lightmap.json`
- `core/position_tex.json`
- `core/position_tex_color.json`
- `core/rendertype_armor_cutout_no_cull.json`
- `core/rendertype_armor_entity_glint.json`
- `core/rendertype_beacon_beam.json`
- `core/rendertype_breeze_wind.json`
- `core/rendertype_clouds.json`
- `core/rendertype_crumbling.json`
- `core/rendertype_cutout.json`
- `core/rendertype_cutout_mipped.json`
- `core/rendertype_end_gateway.json`
- `core/rendertype_end_portal.json`
- `core/rendertype_energy_swirl.json`
- `core/rendertype_entity_alpha.json`
- `core/rendertype_entity_cutout.json`
- `core/rendertype_entity_cutout_no_cull.json`
- `core/rendertype_entity_cutout_no_cull_z_offset.json`
- `core/rendertype_entity_decal.json`
- `core/rendertype_entity_glint.json`
- `core/rendertype_entity_glint_direct.json`
- `core/rendertype_entity_no_outline.json`
- `core/rendertype_entity_shadow.json`
- `core/rendertype_entity_smooth_cutout.json`
- `core/rendertype_entity_solid.json`
- `core/rendertype_entity_translucent.json`
- `core/rendertype_entity_translucent_cull.json`
- `core/rendertype_entity_translucent_emissive.json`
- `core/rendertype_eyes.json`
- `core/rendertype_glint.json`
- `core/rendertype_glint_translucent.json`
- `core/rendertype_gui.json`
- `core/rendertype_gui_ghost_recipe_overlay.json`
- `core/rendertype_gui_overlay.json`
- `core/rendertype_gui_text_highlight.json`
- `core/rendertype_item_entity_translucent_cull.json`
- `core/rendertype_leash.json`
- `core/rendertype_lightning.json`
- `core/rendertype_lines.json`
- `core/rendertype_outline.json`
- `core/rendertype_solid.json`
- `core/rendertype_text.json`
- `core/rendertype_text_background.json`
- `core/rendertype_text_background_see_through.json`
- `core/rendertype_text_intensity.json`
- `core/rendertype_text_intensity_see_through.json`
- `core/rendertype_text_see_through.json`
- `core/rendertype_translucent.json`
- `core/rendertype_translucent_moving_block.json`
- `core/rendertype_tripwire.json`
- `core/rendertype_water_mask.json`

</details>

---

◀ [1.20.6](../1.20.6/README.md) · [All versions](../README.md) · [1.21.1](../1.21.1/README.md) ▶
