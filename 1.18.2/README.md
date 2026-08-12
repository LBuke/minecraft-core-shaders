# Minecraft 1.18.2 — core shaders

| | |
|---|---|
| **Minecraft version** | `1.18.2` |
| **Protocol version** | `758` |
| **Shader files** | 261 |
| **Folders** | `core/` (166), `include/` (4), `post/` (26), `program/` (65) |

## Changes since 1.18.1

`+0 added` · `-0 removed` · `~71 modified`

Fog becomes selectable per render type instead of always cylindrical.

- `cylindrical_distance()` is replaced by `fog_distance(mat4, vec3, int shape)` in `include/fog.glsl`, where shape `0` is spherical and `1` is cylindrical
- a `FogShape` int uniform is added to 35 shaders and declared in 35 JSONs
- sky and cloud render types keep spherical fog while terrain uses cylindrical fog

<details>
<summary><b>Modified (71)</b></summary>

- `core/particle.json`
- `core/particle.vsh`
- `core/position.json`
- `core/position.vsh`
- `core/position_color_normal.json`
- `core/position_color_normal.vsh`
- `core/position_tex_color_normal.json`
- `core/position_tex_color_normal.vsh`
- `core/rendertype_armor_cutout_no_cull.json`
- `core/rendertype_armor_cutout_no_cull.vsh`
- `core/rendertype_armor_entity_glint.json`
- `core/rendertype_armor_entity_glint.vsh`
- `core/rendertype_armor_glint.json`
- `core/rendertype_armor_glint.vsh`
- `core/rendertype_cutout.json`
- `core/rendertype_cutout.vsh`
- `core/rendertype_cutout_mipped.json`
- `core/rendertype_cutout_mipped.vsh`
- `core/rendertype_energy_swirl.json`
- `core/rendertype_energy_swirl.vsh`
- `core/rendertype_entity_cutout.json`
- `core/rendertype_entity_cutout.vsh`
- `core/rendertype_entity_cutout_no_cull.json`
- `core/rendertype_entity_cutout_no_cull.vsh`
- `core/rendertype_entity_cutout_no_cull_z_offset.json`
- `core/rendertype_entity_cutout_no_cull_z_offset.vsh`
- `core/rendertype_entity_decal.json`
- `core/rendertype_entity_decal.vsh`
- `core/rendertype_entity_glint.json`
- `core/rendertype_entity_glint.vsh`
- `core/rendertype_entity_glint_direct.json`
- `core/rendertype_entity_glint_direct.vsh`
- `core/rendertype_entity_no_outline.json`
- `core/rendertype_entity_no_outline.vsh`
- `core/rendertype_entity_shadow.json`
- `core/rendertype_entity_shadow.vsh`
- `core/rendertype_entity_smooth_cutout.json`
- `core/rendertype_entity_smooth_cutout.vsh`
- `core/rendertype_entity_solid.json`
- `core/rendertype_entity_solid.vsh`
- `core/rendertype_entity_translucent.json`
- `core/rendertype_entity_translucent.vsh`
- `core/rendertype_entity_translucent_cull.json`
- `core/rendertype_entity_translucent_cull.vsh`
- `core/rendertype_eyes.json`
- `core/rendertype_eyes.vsh`
- `core/rendertype_glint.json`
- `core/rendertype_glint.vsh`
- `core/rendertype_glint_direct.json`
- `core/rendertype_glint_direct.vsh`
- `core/rendertype_glint_translucent.json`
- `core/rendertype_glint_translucent.vsh`
- `core/rendertype_item_entity_translucent_cull.json`
- `core/rendertype_item_entity_translucent_cull.vsh`
- `core/rendertype_leash.json`
- `core/rendertype_leash.vsh`
- `core/rendertype_lightning.json`
- `core/rendertype_lightning.vsh`
- `core/rendertype_lines.json`
- `core/rendertype_lines.vsh`
- `core/rendertype_solid.json`
- `core/rendertype_solid.vsh`
- `core/rendertype_text.json`
- `core/rendertype_text.vsh`
- `core/rendertype_text_intensity.json`
- `core/rendertype_text_intensity.vsh`
- `core/rendertype_translucent.json`
- `core/rendertype_translucent.vsh`
- `core/rendertype_tripwire.json`
- `core/rendertype_tripwire.vsh`
- `include/fog.glsl`

</details>

---

◀ [1.18.1](../1.18.1/README.md) · [All versions](../README.md) · [1.19](../1.19/README.md) ▶
