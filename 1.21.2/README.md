# Minecraft 1.21.2 — core shaders

| | |
|---|---|
| **Minecraft version** | `1.21.2` |
| **Protocol version** | `768` |
| **Shader files** | 149 |
| **Folders** | `core/` (121), `include/` (4), `post/` (24) |

## Changes since 1.21.1

`+31 added` · `-82 removed` · `~87 modified`

A major consolidation: instead of one shader pair per render type, a handful of **shared programs** are specialised through preprocessor defines.

- **New shared programs:** `core/entity`, `core/terrain`, `core/glint`, `core/gui` and `core/lightmap`. The 57 per-render-type `.vsh`/`.fsh` files they replace are deleted; the remaining JSONs simply point at a shared program and set `"defines"` / `"flags"` (for example `"ALPHA_CUTOUT": "0.1"`).
- **`program/` is renamed to `post/`.** Post-processing programs now sit next to the effect chains that reference them.
- **Imports are namespaced:** `#moj_import <fog.glsl>` becomes `#moj_import <minecraft:fog.glsl>`.
- A `ModelOffset` uniform is added for entity/terrain offsetting.

<details>
<summary><b>Added (31)</b></summary>

- `core/entity.fsh`
- `core/entity.vsh`
- `core/glint.fsh`
- `core/glint.vsh`
- `core/gui.fsh`
- `core/gui.vsh`
- `core/lightmap.fsh`
- `core/lightmap.json`
- `core/rendertype_armor_translucent.json`
- `core/terrain.fsh`
- `core/terrain.vsh`
- `post/bits.fsh`
- `post/bits.json`
- `post/blit.fsh`
- `post/blit.json`
- `post/blit.vsh`
- `post/blur.vsh`
- `post/box_blur.fsh`
- `post/box_blur.json`
- `post/color_convolve.fsh`
- `post/color_convolve.json`
- `post/entity_outline_box_blur.fsh`
- `post/entity_outline_box_blur.json`
- `post/entity_sobel.fsh`
- `post/invert.fsh`
- `post/invert.vsh`
- `post/rotscale.vsh`
- `post/screenquad.vsh`
- `post/sobel.vsh`
- `post/spiderclip.fsh`
- `post/transparency.fsh`

</details>

<details>
<summary><b>Removed (82)</b></summary>

- `core/rendertype_armor_cutout_no_cull.fsh`
- `core/rendertype_armor_cutout_no_cull.vsh`
- `core/rendertype_armor_entity_glint.fsh`
- `core/rendertype_armor_entity_glint.vsh`
- `core/rendertype_breeze_wind.fsh`
- `core/rendertype_breeze_wind.vsh`
- `core/rendertype_cutout.fsh`
- `core/rendertype_cutout.vsh`
- `core/rendertype_cutout_mipped.fsh`
- `core/rendertype_cutout_mipped.vsh`
- `core/rendertype_energy_swirl.fsh`
- `core/rendertype_energy_swirl.vsh`
- `core/rendertype_entity_cutout.fsh`
- `core/rendertype_entity_cutout.vsh`
- `core/rendertype_entity_cutout_no_cull.fsh`
- `core/rendertype_entity_cutout_no_cull.vsh`
- `core/rendertype_entity_cutout_no_cull_z_offset.fsh`
- `core/rendertype_entity_cutout_no_cull_z_offset.vsh`
- `core/rendertype_entity_glint.fsh`
- `core/rendertype_entity_glint.vsh`
- `core/rendertype_entity_glint_direct.fsh`
- `core/rendertype_entity_glint_direct.json`
- `core/rendertype_entity_glint_direct.vsh`
- `core/rendertype_entity_no_outline.fsh`
- `core/rendertype_entity_no_outline.vsh`
- `core/rendertype_entity_smooth_cutout.fsh`
- `core/rendertype_entity_smooth_cutout.vsh`
- `core/rendertype_entity_solid.fsh`
- `core/rendertype_entity_solid.vsh`
- `core/rendertype_entity_translucent.fsh`
- `core/rendertype_entity_translucent.vsh`
- `core/rendertype_entity_translucent_cull.fsh`
- `core/rendertype_entity_translucent_cull.json`
- `core/rendertype_entity_translucent_cull.vsh`
- `core/rendertype_entity_translucent_emissive.fsh`
- `core/rendertype_entity_translucent_emissive.vsh`
- `core/rendertype_eyes.fsh`
- `core/rendertype_eyes.vsh`
- `core/rendertype_glint.fsh`
- `core/rendertype_glint.vsh`
- `core/rendertype_glint_translucent.fsh`
- `core/rendertype_glint_translucent.vsh`
- `core/rendertype_gui.fsh`
- `core/rendertype_gui.vsh`
- `core/rendertype_gui_ghost_recipe_overlay.fsh`
- `core/rendertype_gui_ghost_recipe_overlay.vsh`
- `core/rendertype_gui_overlay.fsh`
- `core/rendertype_gui_overlay.vsh`
- `core/rendertype_gui_text_highlight.fsh`
- `core/rendertype_gui_text_highlight.vsh`
- `core/rendertype_solid.fsh`
- `core/rendertype_solid.vsh`
- `core/rendertype_translucent.fsh`
- `core/rendertype_translucent.vsh`
- `core/rendertype_tripwire.fsh`
- `core/rendertype_tripwire.vsh`
- `post/blur.json`
- `post/creeper.json`
- `program/bits.fsh`
- `program/bits.json`
- `program/blit.fsh`
- `program/blit.json`
- `program/blit.vsh`
- `program/blur.vsh`
- `program/box_blur.fsh`
- `program/box_blur.json`
- `program/color_convolve.fsh`
- `program/color_convolve.json`
- `program/entity_outline.json`
- `program/entity_outline_box_blur.fsh`
- `program/entity_outline_box_blur.json`
- `program/entity_sobel.fsh`
- `program/invert.fsh`
- `program/invert.json`
- `program/invert.vsh`
- `program/rotscale.vsh`
- `program/screenquad.vsh`
- `program/sobel.vsh`
- `program/spider.json`
- `program/spiderclip.fsh`
- `program/transparency.fsh`
- `program/transparency.json`

</details>

<details>
<summary><b>Modified (87)</b></summary>

- `core/blit_screen.fsh`
- `core/blit_screen.json`
- `core/particle.fsh`
- `core/particle.json`
- `core/particle.vsh`
- `core/position.fsh`
- `core/position.json`
- `core/position.vsh`
- `core/position_color.json`
- `core/position_color_lightmap.json`
- `core/position_color_tex_lightmap.json`
- `core/position_tex.json`
- `core/position_tex_color.fsh`
- `core/position_tex_color.json`
- `core/rendertype_armor_cutout_no_cull.json`
- `core/rendertype_armor_entity_glint.json`
- `core/rendertype_beacon_beam.fsh`
- `core/rendertype_beacon_beam.json`
- `core/rendertype_breeze_wind.json`
- `core/rendertype_clouds.fsh`
- `core/rendertype_clouds.json`
- `core/rendertype_clouds.vsh`
- `core/rendertype_crumbling.json`
- `core/rendertype_cutout.json`
- `core/rendertype_cutout_mipped.json`
- `core/rendertype_end_gateway.json`
- `core/rendertype_end_portal.fsh`
- `core/rendertype_end_portal.json`
- `core/rendertype_end_portal.vsh`
- `core/rendertype_energy_swirl.json`
- `core/rendertype_entity_alpha.json`
- `core/rendertype_entity_cutout.json`
- `core/rendertype_entity_cutout_no_cull.json`
- `core/rendertype_entity_cutout_no_cull_z_offset.json`
- `core/rendertype_entity_decal.fsh`
- `core/rendertype_entity_decal.json`
- `core/rendertype_entity_decal.vsh`
- `core/rendertype_entity_glint.json`
- `core/rendertype_entity_no_outline.json`
- `core/rendertype_entity_shadow.fsh`
- `core/rendertype_entity_shadow.json`
- `core/rendertype_entity_shadow.vsh`
- `core/rendertype_entity_smooth_cutout.json`
- `core/rendertype_entity_solid.json`
- `core/rendertype_entity_translucent.json`
- `core/rendertype_entity_translucent_emissive.json`
- `core/rendertype_eyes.json`
- `core/rendertype_glint.json`
- `core/rendertype_glint_translucent.json`
- `core/rendertype_gui.json`
- `core/rendertype_gui_ghost_recipe_overlay.json`
- `core/rendertype_gui_overlay.json`
- `core/rendertype_gui_text_highlight.json`
- `core/rendertype_item_entity_translucent_cull.fsh`
- `core/rendertype_item_entity_translucent_cull.json`
- `core/rendertype_item_entity_translucent_cull.vsh`
- `core/rendertype_leash.fsh`
- `core/rendertype_leash.json`
- `core/rendertype_leash.vsh`
- `core/rendertype_lightning.fsh`
- `core/rendertype_lightning.json`
- `core/rendertype_lightning.vsh`
- `core/rendertype_lines.fsh`
- `core/rendertype_lines.json`
- `core/rendertype_lines.vsh`
- `core/rendertype_outline.json`
- `core/rendertype_solid.json`
- `core/rendertype_text.fsh`
- `core/rendertype_text.json`
- `core/rendertype_text.vsh`
- `core/rendertype_text_background.fsh`
- `core/rendertype_text_background.json`
- `core/rendertype_text_background.vsh`
- `core/rendertype_text_background_see_through.json`
- `core/rendertype_text_intensity.fsh`
- `core/rendertype_text_intensity.json`
- `core/rendertype_text_intensity.vsh`
- `core/rendertype_text_intensity_see_through.json`
- `core/rendertype_text_see_through.json`
- `core/rendertype_translucent.json`
- `core/rendertype_translucent_moving_block.json`
- `core/rendertype_tripwire.json`
- `core/rendertype_water_mask.json`
- `post/entity_outline.json`
- `post/invert.json`
- `post/spider.json`
- `post/transparency.json`

</details>

---

◀ [1.21.1](../1.21.1/README.md) · [All versions](../README.md) · [1.21.3](../1.21.3/README.md) ▶
