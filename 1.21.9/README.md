# Minecraft 1.21.9 — core shaders

| | |
|---|---|
| **Minecraft version** | `1.21.9` |
| **Protocol version** | `773` |
| **Shader files** | 85 |
| **Folders** | `core/` (69), `include/` (6), `post/` (10) |

## Changes since 1.21.8

`+1 added` · `-10 removed` · `~84 modified`

- **GLSL is bumped from `#version 150` to `#version 330`** across all 84 shaders.
- **Per-face lighting.** `core/entity` and `core/terrain` gain a `PER_FACE_LIGHTING` path with front/back vertex colours (`vertexPerFaceColorFront` / `Back`), replacing the old `NO_CARDINAL_LIGHTING` define.
- **Screen-space vertex shaders are merged.** `post/blit.vsh`, `post/blur.vsh`, `post/invert.vsh`, `post/sobel.vsh`, `post/screenquad.vsh` and `core/blit_screen.vsh` collapse into a single `core/screenquad.vsh`; `oneTexel` / `sampleStep` are now computed in the fragment stage from a `SamplerInfo` uniform block.
- `lightmap.fsh` is reworked (the `UseBrightLightmap` path is dropped, `AmbientLightFactor` is blended in), and `position_color_lightmap` / `position_color_tex_lightmap` are removed.

**Added (1)**

- `core/screenquad.vsh`

**Removed (10)**

- `core/blit_screen.vsh`
- `core/position_color_lightmap.fsh`
- `core/position_color_lightmap.vsh`
- `core/position_color_tex_lightmap.fsh`
- `core/position_color_tex_lightmap.vsh`
- `post/blit.vsh`
- `post/blur.vsh`
- `post/invert.vsh`
- `post/screenquad.vsh`
- `post/sobel.vsh`

<details>
<summary><b>Modified (84)</b></summary>

- `core/blit_screen.fsh`
- `core/entity.fsh`
- `core/entity.vsh`
- `core/glint.fsh`
- `core/glint.vsh`
- `core/gui.fsh`
- `core/gui.vsh`
- `core/lightmap.fsh`
- `core/panorama.fsh`
- `core/panorama.vsh`
- `core/particle.fsh`
- `core/particle.vsh`
- `core/position.fsh`
- `core/position.vsh`
- `core/position_color.fsh`
- `core/position_color.vsh`
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
- `core/rendertype_entity_alpha.fsh`
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
- `core/sky.fsh`
- `core/sky.vsh`
- `core/stars.fsh`
- `core/stars.vsh`
- `core/terrain.fsh`
- `core/terrain.vsh`
- `include/dynamictransforms.glsl`
- `include/fog.glsl`
- `include/globals.glsl`
- `include/light.glsl`
- `include/matrix.glsl`
- `include/projection.glsl`
- `post/bits.fsh`
- `post/blit.fsh`
- `post/box_blur.fsh`
- `post/color_convolve.fsh`
- `post/entity_outline_box_blur.fsh`
- `post/entity_sobel.fsh`
- `post/invert.fsh`
- `post/rotscale.vsh`
- `post/spiderclip.fsh`
- `post/transparency.fsh`

</details>

---

◀ [1.21.8](../1.21.8/README.md) · [All versions](../README.md) · [1.21.10](../1.21.10/README.md) ▶
