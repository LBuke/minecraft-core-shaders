# Minecraft 1.21.11 — core shaders

| | |
|---|---|
| **Minecraft version** | `1.21.11` |
| **Protocol version** | `774` |
| **Shader files** | 93 |
| **Folders** | `core/` (75), `include/` (8), `post/` (10) |

## Changes since 1.21.10

`+8 added` · `-0 removed` · `~10 modified`

- **Terrain splits into `core/block`.** Block rendering gets its own `block.vsh`/`block.fsh` alongside `terrain`, sharing the new `include/chunksection.glsl`.
- **Sprite animation moves to the GPU.** `animate_sprite.vsh`, `animate_sprite_blit.fsh` and `animate_sprite_interpolate.fsh` arrive with `include/animation_sprite.glsl`.
- Adds `core/debug_point.vsh`; `LineWidth` moves out of `DynamicTransforms` into the globals block, and debug line colours become fully opaque.
- Nearest-neighbour sampling becomes texel-size aware, using `dFdx`/`dFdy` derivatives to pick the sample.

**Added (8)**

- `core/animate_sprite.vsh`
- `core/animate_sprite_blit.fsh`
- `core/animate_sprite_interpolate.fsh`
- `core/block.fsh`
- `core/block.vsh`
- `core/debug_point.vsh`
- `include/animation_sprite.glsl`
- `include/chunksection.glsl`

**Modified (10)**

- `core/gui.fsh`
- `core/gui.vsh`
- `core/position_tex_color.fsh`
- `core/position_tex_color.vsh`
- `core/rendertype_clouds.vsh`
- `core/rendertype_lines.vsh`
- `core/terrain.fsh`
- `core/terrain.vsh`
- `include/dynamictransforms.glsl`
- `include/globals.glsl`

---

◀ [1.21.10](../1.21.10/README.md) · [All versions](../README.md) · [26.1](../26.1/README.md) ▶
