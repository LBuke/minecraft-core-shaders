# Minecraft 1.17 — core shaders

| | |
|---|---|
| **Minecraft version** | `1.17` |
| **Protocol version** | `755` |
| **Shader files** | 261 |
| **Folders** | `core/` (166), `include/` (4), `post/` (26), `program/` (65) |

## Changes since 1.16.5

`+170 added` · `-0 removed` · `~38 modified`

The largest change in the repository's history — this is where **core shaders** are introduced.

- **`core/` (166 new files)** — the shaders that actually draw the world. Every render type (terrain, entities, particles, text, glint, lines, beacon beam, end portal, …) gets its own `.vsh`/`.fsh`/`.json` triple that resource packs can now override.
- **`include/` (4 new files)** — shared GLSL fragments pulled in with `#moj_import`: `fog.glsl`, `light.glsl`, `matrix.glsl`, `projection.glsl`.
- **All 37 post-processing programs ported from GLSL 110 to GLSL 150**: `#version 110` becomes `#version 150`, `varying` becomes `in`/`out`, `attribute` becomes `in`, `texture2D()` becomes `texture()`, and `gl_FragColor` is replaced by a declared `out vec4 fragColor`.

<details>
<summary><b>Added (170)</b></summary>

- `core/blit_screen.fsh`
- `core/blit_screen.json`
- `core/blit_screen.vsh`
- `core/block.fsh`
- `core/block.json`
- `core/block.vsh`
- `core/new_entity.fsh`
- `core/new_entity.json`
- `core/new_entity.vsh`
- `core/particle.fsh`
- `core/particle.json`
- `core/particle.vsh`
- `core/position.fsh`
- `core/position.json`
- `core/position.vsh`
- `core/position_color.fsh`
- `core/position_color.json`
- `core/position_color.vsh`
- `core/position_color_lightmap.fsh`
- `core/position_color_lightmap.json`
- `core/position_color_lightmap.vsh`
- `core/position_color_normal.fsh`
- `core/position_color_normal.json`
- `core/position_color_normal.vsh`
- `core/position_color_tex.fsh`
- `core/position_color_tex.json`
- `core/position_color_tex.vsh`
- `core/position_color_tex_lightmap.fsh`
- `core/position_color_tex_lightmap.json`
- `core/position_color_tex_lightmap.vsh`
- `core/position_tex.fsh`
- `core/position_tex.json`
- `core/position_tex.vsh`
- `core/position_tex_color.fsh`
- `core/position_tex_color.json`
- `core/position_tex_color.vsh`
- `core/position_tex_color_normal.fsh`
- `core/position_tex_color_normal.json`
- `core/position_tex_color_normal.vsh`
- `core/position_tex_lightmap_color.fsh`
- `core/position_tex_lightmap_color.json`
- `core/position_tex_lightmap_color.vsh`
- `core/rendertype_armor_cutout_no_cull.fsh`
- `core/rendertype_armor_cutout_no_cull.json`
- `core/rendertype_armor_cutout_no_cull.vsh`
- `core/rendertype_armor_entity_glint.fsh`
- `core/rendertype_armor_entity_glint.json`
- `core/rendertype_armor_entity_glint.vsh`
- `core/rendertype_armor_glint.fsh`
- `core/rendertype_armor_glint.json`
- `core/rendertype_armor_glint.vsh`
- `core/rendertype_beacon_beam.fsh`
- `core/rendertype_beacon_beam.json`
- `core/rendertype_beacon_beam.vsh`
- `core/rendertype_crumbling.fsh`
- `core/rendertype_crumbling.json`
- `core/rendertype_crumbling.vsh`
- `core/rendertype_cutout.fsh`
- `core/rendertype_cutout.json`
- `core/rendertype_cutout.vsh`
- `core/rendertype_cutout_mipped.fsh`
- `core/rendertype_cutout_mipped.json`
- `core/rendertype_cutout_mipped.vsh`
- `core/rendertype_end_gateway.json`
- `core/rendertype_end_portal.fsh`
- `core/rendertype_end_portal.json`
- `core/rendertype_end_portal.vsh`
- `core/rendertype_energy_swirl.fsh`
- `core/rendertype_energy_swirl.json`
- `core/rendertype_energy_swirl.vsh`
- `core/rendertype_entity_alpha.fsh`
- `core/rendertype_entity_alpha.json`
- `core/rendertype_entity_alpha.vsh`
- `core/rendertype_entity_cutout.fsh`
- `core/rendertype_entity_cutout.json`
- `core/rendertype_entity_cutout.vsh`
- `core/rendertype_entity_cutout_no_cull.fsh`
- `core/rendertype_entity_cutout_no_cull.json`
- `core/rendertype_entity_cutout_no_cull.vsh`
- `core/rendertype_entity_cutout_no_cull_z_offset.fsh`
- `core/rendertype_entity_cutout_no_cull_z_offset.json`
- `core/rendertype_entity_cutout_no_cull_z_offset.vsh`
- `core/rendertype_entity_decal.fsh`
- `core/rendertype_entity_decal.json`
- `core/rendertype_entity_decal.vsh`
- `core/rendertype_entity_glint.fsh`
- `core/rendertype_entity_glint.json`
- `core/rendertype_entity_glint.vsh`
- `core/rendertype_entity_glint_direct.fsh`
- `core/rendertype_entity_glint_direct.json`
- `core/rendertype_entity_glint_direct.vsh`
- `core/rendertype_entity_no_outline.fsh`
- `core/rendertype_entity_no_outline.json`
- `core/rendertype_entity_no_outline.vsh`
- `core/rendertype_entity_shadow.fsh`
- `core/rendertype_entity_shadow.json`
- `core/rendertype_entity_shadow.vsh`
- `core/rendertype_entity_smooth_cutout.fsh`
- `core/rendertype_entity_smooth_cutout.json`
- `core/rendertype_entity_smooth_cutout.vsh`
- `core/rendertype_entity_solid.fsh`
- `core/rendertype_entity_solid.json`
- `core/rendertype_entity_solid.vsh`
- `core/rendertype_entity_translucent.fsh`
- `core/rendertype_entity_translucent.json`
- `core/rendertype_entity_translucent.vsh`
- `core/rendertype_entity_translucent_cull.fsh`
- `core/rendertype_entity_translucent_cull.json`
- `core/rendertype_entity_translucent_cull.vsh`
- `core/rendertype_eyes.fsh`
- `core/rendertype_eyes.json`
- `core/rendertype_eyes.vsh`
- `core/rendertype_glint.fsh`
- `core/rendertype_glint.json`
- `core/rendertype_glint.vsh`
- `core/rendertype_glint_direct.fsh`
- `core/rendertype_glint_direct.json`
- `core/rendertype_glint_direct.vsh`
- `core/rendertype_glint_translucent.fsh`
- `core/rendertype_glint_translucent.json`
- `core/rendertype_glint_translucent.vsh`
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
- `core/rendertype_outline.fsh`
- `core/rendertype_outline.json`
- `core/rendertype_outline.vsh`
- `core/rendertype_solid.fsh`
- `core/rendertype_solid.json`
- `core/rendertype_solid.vsh`
- `core/rendertype_text.fsh`
- `core/rendertype_text.json`
- `core/rendertype_text.vsh`
- `core/rendertype_text_intensity.fsh`
- `core/rendertype_text_intensity.json`
- `core/rendertype_text_intensity.vsh`
- `core/rendertype_text_intensity_see_through.fsh`
- `core/rendertype_text_intensity_see_through.json`
- `core/rendertype_text_intensity_see_through.vsh`
- `core/rendertype_text_see_through.fsh`
- `core/rendertype_text_see_through.json`
- `core/rendertype_text_see_through.vsh`
- `core/rendertype_translucent.fsh`
- `core/rendertype_translucent.json`
- `core/rendertype_translucent.vsh`
- `core/rendertype_translucent_moving_block.fsh`
- `core/rendertype_translucent_moving_block.json`
- `core/rendertype_translucent_moving_block.vsh`
- `core/rendertype_translucent_no_crumbling.fsh`
- `core/rendertype_translucent_no_crumbling.json`
- `core/rendertype_translucent_no_crumbling.vsh`
- `core/rendertype_tripwire.fsh`
- `core/rendertype_tripwire.json`
- `core/rendertype_tripwire.vsh`
- `core/rendertype_water_mask.fsh`
- `core/rendertype_water_mask.json`
- `core/rendertype_water_mask.vsh`
- `include/fog.glsl`
- `include/light.glsl`
- `include/matrix.glsl`
- `include/projection.glsl`

</details>

<details>
<summary><b>Modified (38)</b></summary>

- `program/antialias.fsh`
- `program/bits.fsh`
- `program/bits.json`
- `program/blit.fsh`
- `program/blit.vsh`
- `program/blobs.fsh`
- `program/blobs.vsh`
- `program/blobs2.fsh`
- `program/blur.fsh`
- `program/bumpy.fsh`
- `program/bumpy.vsh`
- `program/color_convolve.fsh`
- `program/deconverge.fsh`
- `program/downscale.fsh`
- `program/downscale.vsh`
- `program/entity_sobel.fsh`
- `program/flip.vsh`
- `program/fxaa.fsh`
- `program/fxaa.vsh`
- `program/invert.fsh`
- `program/invert.vsh`
- `program/notch.fsh`
- `program/ntsc_decode.fsh`
- `program/ntsc_encode.fsh`
- `program/outline.fsh`
- `program/outline_combine.fsh`
- `program/outline_soft.fsh`
- `program/outline_watercolor.fsh`
- `program/overlay.fsh`
- `program/phosphor.fsh`
- `program/rotscale.vsh`
- `program/scan_pincushion.fsh`
- `program/screenquad.vsh`
- `program/sobel.fsh`
- `program/sobel.vsh`
- `program/spiderclip.fsh`
- `program/transparency.fsh`
- `program/wobble.fsh`

</details>

---

◀ [1.16.5](../1.16.5/README.md) · [All versions](../README.md) · [1.17.1](../1.17.1/README.md) ▶
