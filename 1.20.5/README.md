# Minecraft 1.20.5 — core shaders

| | |
|---|---|
| **Minecraft version** | `1.20.5` |
| **Protocol version** | `766` |
| **Shader files** | 209 |
| **Folders** | `core/` (175), `include/` (4), `post/` (6), `program/` (24) |

## Changes since 1.20.4

`+8 added` · `-75 removed` · `~121 modified`

A large cleanup of both the post-processing pack and the core shader JSONs.

- **75 files removed.** Most of the legacy "Super Secret Settings" post effects are deleted (`art`, `pencil`, `green`, `notch`, `bumpy`, `blobs`, `blobs2`, `sobel`, `wobble`, `ntsc`, `fxaa`, `phosphor`, `deconverge`, `scan_pincushion`, `antialias`, `flip`, `outline` and friends), leaving only the effects the game actually uses. Three unused core shaders go too (`position_color_normal`, `position_tex_color_normal`, `position_tex_lightmap_color`).
- **8 files added.** `rendertype_clouds`, plus a new `box_blur` / `entity_outline_box_blur` pair (and `blur.vsh`) that replaces the old blur chain for the glowing entity outline.
- **121 files modified.** The `"attributes"` array is removed from every shader JSON — the vertex format is now supplied by the game rather than declared in the pack. Alongside that, the `IViewRotMat` uniform and the `normal` varying are dropped, and fog distance simplifies to `fog_distance(Position, FogShape)`.

**Added (8)**

- `core/rendertype_clouds.fsh`
- `core/rendertype_clouds.json`
- `core/rendertype_clouds.vsh`
- `program/blur.vsh`
- `program/box_blur.fsh`
- `program/box_blur.json`
- `program/entity_outline_box_blur.fsh`
- `program/entity_outline_box_blur.json`

<details>
<summary><b>Removed (75)</b></summary>

- `core/position_color_normal.fsh`
- `core/position_color_normal.json`
- `core/position_color_normal.vsh`
- `core/position_tex_color_normal.fsh`
- `core/position_tex_color_normal.json`
- `core/position_tex_color_normal.vsh`
- `core/position_tex_lightmap_color.fsh`
- `core/position_tex_lightmap_color.json`
- `core/position_tex_lightmap_color.vsh`
- `post/antialias.json`
- `post/art.json`
- `post/bits.json`
- `post/blobs.json`
- `post/blobs2.json`
- `post/bumpy.json`
- `post/color_convolve.json`
- `post/deconverge.json`
- `post/desaturate.json`
- `post/flip.json`
- `post/fxaa.json`
- `post/green.json`
- `post/notch.json`
- `post/ntsc.json`
- `post/outline.json`
- `post/pencil.json`
- `post/phosphor.json`
- `post/scan_pincushion.json`
- `post/sobel.json`
- `post/wobble.json`
- `program/antialias.fsh`
- `program/antialias.json`
- `program/blobs.fsh`
- `program/blobs.json`
- `program/blobs.vsh`
- `program/blobs2.fsh`
- `program/blobs2.json`
- `program/blur.fsh`
- `program/blur.json`
- `program/bumpy.fsh`
- `program/bumpy.json`
- `program/bumpy.vsh`
- `program/deconverge.fsh`
- `program/deconverge.json`
- `program/downscale.fsh`
- `program/downscale.json`
- `program/downscale.vsh`
- `program/flip.json`
- `program/flip.vsh`
- `program/fxaa.fsh`
- `program/fxaa.json`
- `program/fxaa.vsh`
- `program/notch.fsh`
- `program/notch.json`
- `program/ntsc_decode.fsh`
- `program/ntsc_decode.json`
- `program/ntsc_encode.fsh`
- `program/ntsc_encode.json`
- `program/outline.fsh`
- `program/outline.json`
- `program/outline_combine.fsh`
- `program/outline_combine.json`
- `program/outline_soft.fsh`
- `program/outline_soft.json`
- `program/outline_watercolor.fsh`
- `program/outline_watercolor.json`
- `program/overlay.fsh`
- `program/overlay.json`
- `program/phosphor.fsh`
- `program/phosphor.json`
- `program/scan_pincushion.fsh`
- `program/scan_pincushion.json`
- `program/sobel.fsh`
- `program/sobel.json`
- `program/wobble.fsh`
- `program/wobble.json`

</details>

<details>
<summary><b>Modified (121)</b></summary>

- `core/blit_screen.json`
- `core/particle.json`
- `core/particle.vsh`
- `core/position.json`
- `core/position.vsh`
- `core/position_color.json`
- `core/position_color_lightmap.json`
- `core/position_color_tex_lightmap.json`
- `core/position_tex.json`
- `core/position_tex_color.json`
- `core/rendertype_armor_cutout_no_cull.fsh`
- `core/rendertype_armor_cutout_no_cull.json`
- `core/rendertype_armor_cutout_no_cull.vsh`
- `core/rendertype_armor_entity_glint.json`
- `core/rendertype_armor_entity_glint.vsh`
- `core/rendertype_armor_glint.json`
- `core/rendertype_armor_glint.vsh`
- `core/rendertype_beacon_beam.json`
- `core/rendertype_breeze_wind.json`
- `core/rendertype_breeze_wind.vsh`
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
- `core/rendertype_end_portal.json`
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
- `core/rendertype_entity_glint.json`
- `core/rendertype_entity_glint.vsh`
- `core/rendertype_entity_glint_direct.json`
- `core/rendertype_entity_glint_direct.vsh`
- `core/rendertype_entity_no_outline.fsh`
- `core/rendertype_entity_no_outline.json`
- `core/rendertype_entity_no_outline.vsh`
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
- `core/rendertype_entity_translucent_emissive.fsh`
- `core/rendertype_entity_translucent_emissive.json`
- `core/rendertype_entity_translucent_emissive.vsh`
- `core/rendertype_eyes.json`
- `core/rendertype_eyes.vsh`
- `core/rendertype_glint.json`
- `core/rendertype_glint.vsh`
- `core/rendertype_glint_direct.json`
- `core/rendertype_glint_direct.vsh`
- `core/rendertype_glint_translucent.json`
- `core/rendertype_glint_translucent.vsh`
- `core/rendertype_gui.json`
- `core/rendertype_gui_ghost_recipe_overlay.json`
- `core/rendertype_gui_overlay.json`
- `core/rendertype_gui_text_highlight.json`
- `core/rendertype_item_entity_translucent_cull.fsh`
- `core/rendertype_item_entity_translucent_cull.json`
- `core/rendertype_item_entity_translucent_cull.vsh`
- `core/rendertype_leash.json`
- `core/rendertype_leash.vsh`
- `core/rendertype_lightning.json`
- `core/rendertype_lightning.vsh`
- `core/rendertype_lines.json`
- `core/rendertype_lines.vsh`
- `core/rendertype_outline.json`
- `core/rendertype_solid.fsh`
- `core/rendertype_solid.json`
- `core/rendertype_solid.vsh`
- `core/rendertype_text.json`
- `core/rendertype_text.vsh`
- `core/rendertype_text_background.json`
- `core/rendertype_text_background.vsh`
- `core/rendertype_text_background_see_through.json`
- `core/rendertype_text_intensity.json`
- `core/rendertype_text_intensity.vsh`
- `core/rendertype_text_intensity_see_through.json`
- `core/rendertype_text_see_through.json`
- `core/rendertype_translucent.fsh`
- `core/rendertype_translucent.json`
- `core/rendertype_translucent.vsh`
- `core/rendertype_translucent_moving_block.fsh`
- `core/rendertype_translucent_moving_block.json`
- `core/rendertype_translucent_moving_block.vsh`
- `core/rendertype_tripwire.fsh`
- `core/rendertype_tripwire.json`
- `core/rendertype_tripwire.vsh`
- `core/rendertype_water_mask.json`
- `include/fog.glsl`
- `include/light.glsl`
- `post/blur.json`
- `post/entity_outline.json`
- `post/spider.json`

</details>

---

◀ [1.20.4](../1.20.4/README.md) · [All versions](../README.md) · [1.20.6](../1.20.6/README.md) ▶
