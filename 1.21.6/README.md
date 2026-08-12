# Minecraft 1.21.6 — core shaders

| | |
|---|---|
| **Minecraft version** | `1.21.6` |
| **Protocol version** | `771` |
| **Shader files** | 94 |
| **Folders** | `core/` (73), `include/` (6), `post/` (15) |

## Changes since 1.21.5

`+8 added` · `-0 removed` · `~79 modified`

The uniform system is rebuilt around **std140 uniform blocks**, and the sky gets real shaders.

- **New includes:** `include/dynamictransforms.glsl` (ModelViewMat, ColorModulator, ModelOffset, TextureMat, LineWidth) and `include/globals.glsl` (screen/game-wide values). Loose `uniform mat4 ModelViewMat;` / `uniform mat4 ProjMat;` / `uniform vec4 ColorModulator;` declarations disappear from ~40 shaders in favour of `#moj_import <minecraft:dynamictransforms.glsl>` and `#moj_import <minecraft:projection.glsl>`.
- **New core shaders:** `core/sky`, `core/stars` and `core/panorama`.
- **Fog is split in two.** `vertexDistance` becomes `sphericalVertexDistance` + `cylindricalVertexDistance`, and shaders call `apply_fog(color, spherical, cylindrical, FogEnvironmentalStart/End, FogRenderDistanceStart/End, FogColor)` — environmental fog and render-distance fog are now separate contributions.

**Added (8)**

- `core/panorama.fsh`
- `core/panorama.vsh`
- `core/sky.fsh`
- `core/sky.vsh`
- `core/stars.fsh`
- `core/stars.vsh`
- `include/dynamictransforms.glsl`
- `include/globals.glsl`

<details>
<summary><b>Modified (79)</b></summary>

- `core/entity.fsh`
- `core/entity.vsh`
- `core/glint.fsh`
- `core/glint.vsh`
- `core/gui.fsh`
- `core/gui.vsh`
- `core/lightmap.fsh`
- `core/particle.fsh`
- `core/particle.vsh`
- `core/position.fsh`
- `core/position.vsh`
- `core/position_color.fsh`
- `core/position_color.vsh`
- `core/position_color_lightmap.fsh`
- `core/position_color_lightmap.vsh`
- `core/position_color_tex_lightmap.fsh`
- `core/position_color_tex_lightmap.vsh`
- `core/position_tex.fsh`
- `core/position_tex.vsh`
- `core/position_tex_color.fsh`
- `core/position_tex_color.vsh`
- `core/rendertype_beacon_beam.fsh`
- `core/rendertype_beacon_beam.vsh`
- `core/rendertype_clouds.fsh`
- `core/rendertype_clouds.vsh`
- `core/rendertype_crumbling.fsh`
- `core/rendertype_crumbling.vsh`
- `core/rendertype_end_portal.fsh`
- `core/rendertype_end_portal.vsh`
- `core/rendertype_entity_alpha.vsh`
- `core/rendertype_entity_decal.fsh`
- `core/rendertype_entity_decal.vsh`
- `core/rendertype_entity_shadow.fsh`
- `core/rendertype_entity_shadow.vsh`
- `core/rendertype_item_entity_translucent_cull.fsh`
- `core/rendertype_item_entity_translucent_cull.vsh`
- `core/rendertype_leash.fsh`
- `core/rendertype_leash.vsh`
- `core/rendertype_lightning.fsh`
- `core/rendertype_lightning.vsh`
- `core/rendertype_lines.fsh`
- `core/rendertype_lines.vsh`
- `core/rendertype_outline.fsh`
- `core/rendertype_outline.vsh`
- `core/rendertype_text.fsh`
- `core/rendertype_text.vsh`
- `core/rendertype_text_background.fsh`
- `core/rendertype_text_background.vsh`
- `core/rendertype_text_background_see_through.fsh`
- `core/rendertype_text_background_see_through.vsh`
- `core/rendertype_text_intensity.fsh`
- `core/rendertype_text_intensity.vsh`
- `core/rendertype_text_intensity_see_through.fsh`
- `core/rendertype_text_intensity_see_through.vsh`
- `core/rendertype_text_see_through.fsh`
- `core/rendertype_text_see_through.vsh`
- `core/rendertype_translucent_moving_block.fsh`
- `core/rendertype_translucent_moving_block.vsh`
- `core/rendertype_water_mask.fsh`
- `core/rendertype_water_mask.vsh`
- `core/rendertype_world_border.fsh`
- `core/rendertype_world_border.vsh`
- `core/terrain.fsh`
- `core/terrain.vsh`
- `include/fog.glsl`
- `include/light.glsl`
- `include/projection.glsl`
- `post/bits.fsh`
- `post/blit.fsh`
- `post/blit.vsh`
- `post/blur.vsh`
- `post/box_blur.fsh`
- `post/color_convolve.fsh`
- `post/invert.fsh`
- `post/invert.vsh`
- `post/rotscale.vsh`
- `post/screenquad.vsh`
- `post/sobel.vsh`
- `post/spiderclip.fsh`

</details>

---

◀ [1.21.5](../1.21.5/README.md) · [All versions](../README.md) · [1.21.7](../1.21.7/README.md) ▶
