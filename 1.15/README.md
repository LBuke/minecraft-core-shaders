# Minecraft 1.15 — core shaders

| | |
|---|---|
| **Minecraft version** | `1.15` |
| **Protocol version** | `573` |
| **Shader files** | 87 |
| **Folders** | `post/` (25), `program/` (62) |

## Changes since 1.14.4

`+0 added` · `-0 removed` · `~35 modified`

A compatibility/cleanup pass over the post-processing programs. Nothing changes visually; the shaders are made strictly GLSL 1.10-compliant so they compile on stricter drivers:

- `#version 120` lowered to `#version 110` in every program
- default initialisers dropped from uniform declarations (`uniform float Saturation = 1.5;` becomes `uniform float Saturation;`) — values now come from the JSON
- `sample`, a reserved word in later GLSL, renamed to `sampleValue` in `blur.fsh`
- implicit int/float literals fixed (`2` becomes `2.0`, `c != 0` becomes `c != 0.0`)
- an explicit `#version 110` added to `fxaa.fsh`, which previously had none

<details>
<summary><b>Modified (35)</b></summary>

- `program/antialias.fsh`
- `program/bits.fsh`
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
- `program/sobel.fsh`
- `program/sobel.vsh`
- `program/spiderclip.fsh`
- `program/wobble.fsh`

</details>

---

◀ [1.14.4](../1.14.4/README.md) · [All versions](../README.md) · [1.15.1](../1.15.1/README.md) ▶
