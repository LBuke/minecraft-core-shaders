# Minecraft 26.2 — core shaders

| | |
|---|---|
| **Minecraft version** | `26.2` |
| **Protocol version** | `776` |
| **Shader files** | 80 |
| **Folders** | `core/` (61), `include/` (9), `post/` (10) |

## Changes since 26.1

`+4 added` · `-12 removed` · `~6 modified`

- **Text shaders are consolidated.** The six `rendertype_text*` programs (plain, intensity, background and their see-through variants) are replaced by two shared programs, `core/text` and `core/text_background`, with the variants selected by defines.
- **Items get lighting and overlay back.** `core/item` now passes `lightMapColor` and `overlayColor` through to the fragment stage and applies the damage/hurt overlay, instead of folding the lightmap into `vertexColor`.
- `rendertype_beacon_beam` computes fragment distance as `1.0 / gl_FragCoord.w` instead of reconstructing it from the projection matrix.
- **Bug fix in `post/transparency.fsh`:** the depth-layer insertion sort comparison is flipped (`>` becomes `<`), correcting the ordering of translucent layers.
- `core/entity` only imports `light.glsl` when it is actually needed, and `rendertype_crumbling` drops its unused `Normal` attribute.

**Added (4)**

- `core/text.fsh`
- `core/text.vsh`
- `core/text_background.fsh`
- `core/text_background.vsh`

**Removed (12)**

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

**Modified (6)**

- `core/entity.vsh`
- `core/item.fsh`
- `core/item.vsh`
- `core/rendertype_beacon_beam.fsh`
- `core/rendertype_crumbling.vsh`
- `post/transparency.fsh`

---

◀ [26.1](../26.1/README.md) · [All versions](../README.md) · _latest version_ ▶
