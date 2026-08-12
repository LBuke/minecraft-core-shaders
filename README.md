# minecraft-core-shaders

Vanilla core shaders of every Minecraft: Java Edition release (excluding snapshots), one folder per version.

Every version folder contains a `README.md` describing exactly what changed since the previous release —
which files were added, removed and modified, and what the change actually does.

## Versions

`+` added · `-` removed · `~` modified, relative to the version above.

| Version | Protocol | Files | Changed since previous | |
|---|---|---|---|---|
| [`1.13`](1.13/) | `393` | 87 | first entry in this repo | [notes](1.13/README.md) |
| [`1.13.1`](1.13.1/) | `401` | 87 | no changes | [notes](1.13.1/README.md) |
| [`1.13.2`](1.13.2/) | `404` | 87 | no changes | [notes](1.13.2/README.md) |
| [`1.14`](1.14/) | `477` | 87 | no changes | [notes](1.14/README.md) |
| [`1.14.1`](1.14.1/) | `480` | 87 | no changes | [notes](1.14.1/README.md) |
| [`1.14.2`](1.14.2/) | `485` | 87 | no changes | [notes](1.14.2/README.md) |
| [`1.14.3`](1.14.3/) | `490` | 87 | no changes | [notes](1.14.3/README.md) |
| [`1.14.4`](1.14.4/) | `498` | 87 | no changes | [notes](1.14.4/README.md) |
| [`1.15`](1.15/) | `573` | 87 | ~35 — GLSL 1.10 compliance pass | [notes](1.15/README.md) |
| [`1.15.1`](1.15.1/) | `575` | 87 | no changes | [notes](1.15.1/README.md) |
| [`1.16`](1.16/) | `735` | 91 | +4 — transparency post effect added | [notes](1.16/README.md) |
| [`1.16.1`](1.16.1/) | `736` | 91 | no changes | [notes](1.16.1/README.md) |
| [`1.16.2`](1.16.2/) | `751` | 91 | no changes | [notes](1.16.2/README.md) |
| [`1.16.3`](1.16.3/) | `753` | 91 | no changes | [notes](1.16.3/README.md) |
| [`1.16.4`](1.16.4/) | `754` | 91 | no changes | [notes](1.16.4/README.md) |
| [`1.16.5`](1.16.5/) | `754` | 91 | no changes | [notes](1.16.5/README.md) |
| [`1.17`](1.17/) | `755` | 261 | +170 / ~38 — core shaders introduced, post shaders ported to GLSL 150 | [notes](1.17/README.md) |
| [`1.17.1`](1.17.1/) | `756` | 261 | no changes | [notes](1.17.1/README.md) |
| [`1.18`](1.18/) | `757` | 261 | no changes | [notes](1.18/README.md) |
| [`1.18.1`](1.18.1/) | `757` | 261 | ~57 — cylindrical fog distance | [notes](1.18.1/README.md) |
| [`1.18.2`](1.18.2/) | `758` | 261 | ~71 — `FogShape` uniform | [notes](1.18.2/README.md) |
| [`1.19`](1.19/) | `759` | 264 | +3 — emissive translucent entity render type | [notes](1.19/README.md) |
| [`1.19.1`](1.19.1/) | `760` | 264 | no changes | [notes](1.19.1/README.md) |
| [`1.19.2`](1.19.2/) | `760` | 264 | no changes | [notes](1.19.2/README.md) |
| [`1.19.3`](1.19.3/) | `761` | 264 | no changes | [notes](1.19.3/README.md) |
| [`1.19.4`](1.19.4/) | `762` | 270 | +6 / ~14 — `GlintAlpha` uniform, text background render types | [notes](1.19.4/README.md) |
| [`1.20`](1.20/) | `763` | 276 | +12 / -6 — GUI render types added, unused `block`/`new_entity` removed | [notes](1.20/README.md) |
| [`1.20.1`](1.20.1/) | `763` | 276 | no changes | [notes](1.20.1/README.md) |
| [`1.20.2`](1.20.2/) | `764` | 276 | no changes | [notes](1.20.2/README.md) |
| [`1.20.3`](1.20.3/) | `765` | 276 | +3 / -3 — breeze wind render type | [notes](1.20.3/README.md) |
| [`1.20.4`](1.20.4/) | `765` | 276 | no changes | [notes](1.20.4/README.md) |
| [`1.20.5`](1.20.5/) | `766` | 209 | +8 / -75 / ~121 — legacy post effects removed, vertex attributes moved out of JSON | [notes](1.20.5/README.md) |
| [`1.20.6`](1.20.6/) | `766` | 209 | no changes | [notes](1.20.6/README.md) |
| [`1.21`](1.21/) | `767` | 200 | -9 / ~58 — blend state removed from JSON | [notes](1.21/README.md) |
| [`1.21.1`](1.21.1/) | `767` | 200 | no changes | [notes](1.21.1/README.md) |
| [`1.21.2`](1.21.2/) | `768` | 149 | +31 / -82 / ~87 — per-render-type shaders merged into shared programs, `program/` renamed to `post/` | [notes](1.21.2/README.md) |
| [`1.21.3`](1.21.3/) | `768` | 149 | no changes | [notes](1.21.3/README.md) |
| [`1.21.4`](1.21.4/) | `769` | 149 | no changes | [notes](1.21.4/README.md) |
| [`1.21.5`](1.21.5/) | `770` | 86 | +2 / -65 / ~11 — shader JSON definitions removed | [notes](1.21.5/README.md) |
| [`1.21.6`](1.21.6/) | `771` | 94 | +8 / ~79 — uniform blocks (UBOs), sky/stars/panorama shaders | [notes](1.21.6/README.md) |
| [`1.21.7`](1.21.7/) | `772` | 94 | no changes | [notes](1.21.7/README.md) |
| [`1.21.8`](1.21.8/) | `772` | 94 | no changes | [notes](1.21.8/README.md) |
| [`1.21.9`](1.21.9/) | `773` | 85 | +1 / -10 / ~84 — GLSL 330, per-face lighting | [notes](1.21.9/README.md) |
| [`1.21.10`](1.21.10/) | `773` | 85 | no changes | [notes](1.21.10/README.md) |
| [`1.21.11`](1.21.11/) | `774` | 93 | +8 / ~10 — block shaders split out, animated sprite shaders | [notes](1.21.11/README.md) |
| [`26.1`](26.1/) | `775` | 88 | +3 / -8 / ~14 — item shaders, shared `sample_lightmap()` | [notes](26.1/README.md) |
| [`26.2`](26.2/) | `776` | 80 | +4 / -12 / ~6 — text shaders consolidated | [notes](26.2/README.md) |

## Pack layout over time

| Folder | Introduced | What it holds |
|---|---|---|
| `post/` | 1.13 | Post-processing effect chains (`.json`). From 1.21.2 it also holds the post-processing GLSL that used to live in `program/`. |
| `program/` | 1.13 | The GLSL programs referenced by the `post/` chains. Renamed to `post/` in 1.21.2. |
| `core/` | 1.17 | The shaders that draw the world — terrain, entities, particles, text, GUI, sky. |
| `include/` | 1.17 | Shared GLSL pulled in with `#moj_import`, e.g. `fog.glsl`, `light.glsl`, `projection.glsl`. |

## Milestones

- **1.15** — post-processing shaders made strictly GLSL 1.10 compliant.
- **1.17** — core shaders introduced (`core/` + `include/`); post shaders ported to GLSL 150.
- **1.18.1 / 1.18.2** — fog reworked to cylindrical distance, then made per-render-type via `FogShape`.
- **1.20.5** — legacy "Super Secret Settings" post effects removed; vertex attributes moved out of the JSONs.
- **1.21** — blend state removed from the JSONs.
- **1.21.2** — per-render-type shaders merged into shared programs driven by `defines`; `program/` renamed to `post/`.
- **1.21.5** — shader JSON definitions removed entirely; the pack becomes GLSL only.
- **1.21.6** — uniforms replaced by std140 uniform blocks; fog split into spherical + cylindrical.
- **1.21.9** — GLSL raised to `#version 330`; per-face lighting.
- **26.1** — new version numbering; shared `sample_lightmap()` and a dedicated item shader.

## Notes

- Protocol numbers are the Java Edition network protocol versions. Versions sharing a protocol number
  (e.g. `1.16.4` / `1.16.5`, `1.18` / `1.18.1`, `1.20` / `1.20.1`) are network compatible with each other.
- `1.15.2` (protocol `578`) is not present in this repository.
- `.DS_Store` files are ignored when comparing versions.
