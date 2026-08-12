# Minecraft 1.21.5 — core shaders

| | |
|---|---|
| **Minecraft version** | `1.21.5` |
| **Protocol version** | `770` |
| **Shader files** | 86 |
| **Folders** | `core/` (67), `include/` (4), `post/` (15) |

## Changes since 1.21.4

`+2 added` · `-65 removed` · `~11 modified`

Shader **configuration** leaves the resource pack; only GLSL remains.

- **65 JSON files removed** — nearly every `core/*.json` and `post/*.json`. Uniforms, samplers and render targets are now declared by the game's pipeline definitions instead of the pack.
- Adds `rendertype_world_border`.
- Post-processing vertex shaders now scale by `OutSize` in the vertex stage (`ProjMat * vec4(Position.xy * OutSize, 0.0, 1.0)` with `texCoord = Position.xy`) rather than dividing in texture space.
- Values that used to be uniforms become compile-time constants: `EndPortalLayers` becomes `PORTAL_LAYERS`, and `Saturation` / colour-convolve matrices are inlined.

**Added (2)**

- `core/rendertype_world_border.fsh`
- `core/rendertype_world_border.vsh`

<details>
<summary><b>Removed (65)</b></summary>

- `core/blit_screen.json`
- `core/lightmap.json`
- `core/particle.json`
- `core/position.json`
- `core/position_color.json`
- `core/position_color_lightmap.json`
- `core/position_color_tex_lightmap.json`
- `core/position_tex.json`
- `core/position_tex_color.json`
- `core/rendertype_armor_cutout_no_cull.json`
- `core/rendertype_armor_entity_glint.json`
- `core/rendertype_armor_translucent.json`
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
- `core/rendertype_entity_no_outline.json`
- `core/rendertype_entity_shadow.json`
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
- `post/bits.json`
- `post/blit.json`
- `post/box_blur.json`
- `post/color_convolve.json`
- `post/entity_outline.json`
- `post/entity_outline_box_blur.json`
- `post/invert.json`
- `post/spider.json`
- `post/transparency.json`

</details>

**Modified (11)**

- `core/rendertype_end_portal.fsh`
- `core/rendertype_end_portal.vsh`
- `post/bits.fsh`
- `post/blit.vsh`
- `post/blur.vsh`
- `post/box_blur.fsh`
- `post/color_convolve.fsh`
- `post/invert.vsh`
- `post/rotscale.vsh`
- `post/screenquad.vsh`
- `post/sobel.vsh`

---

◀ [1.21.4](../1.21.4/README.md) · [All versions](../README.md) · [1.21.6](../1.21.6/README.md) ▶
