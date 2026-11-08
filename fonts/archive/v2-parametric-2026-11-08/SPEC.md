# Susedifu Font Specification (v2.0)

> Normalized rebuild of the hand-drawn original (2026-11-08). The letterform
> designs are the owner's; this document records the normalized execution grid.
> Editable design source: `fonts/susedifu.svg` (stroke-based). Compiled font:
> `fonts/susedifu.ttf`. Historical hand-drawn version: git history.

## Global grid

| Property | Value |
|---|---|
| Units per em | 1024 |
| Baseline | 0 (glyph bottoms sit on it) |
| Stroke width, letters | 100, round caps and joins |
| Stroke width, `,` `/` `?` | 40 |
| Dot rings (strong-member mark) | centerline radius 65, stroke 22 |
| Advance width | 648, monospaced (owner decision); glyphs centered |
| Ascender class (b d e f h i j m r s t w y z) | stroke centers at 555 (top edge ≈ 605) |
| Mid class (a g k o u) | stroke centers at 455 (top edge ≈ 505) |
| `x` (reserved symbol, not a letter) | deliberately smaller: body ≈ 300 tall |
| Period `.` | filled circle, radius 115 |

## Glyph skeleton summary

Letters are built from these skeletons (centerline coordinates, x from glyph left,
y from baseline):

- **m** (base of **b**): top bar, bottom bar, X cross (hourglass); b adds the ring at (505, 330)-ish
- **t** (base of **d**): И — two stems, top bar, diagonal; d adds the ring above the bar's right end
- **w** (base of **f**): top bar, right descender, check swoosh; f adds the ring in the notch
- **k** (base of **g**): Z + small wedge at bottom-left; g adds the ring right of the diagonal
- **h** (base of **y**): stem + full-width bar + V converging at the stem foot; y adds the ring top-right
- **r** (base of **j**): stem + full-width bar + curved swoosh to the stem foot; j adds the ring top-right
- **s** (base of **z**): 4-shape — stem, left bar, diagonal, crossbar; z adds the ring top-right
- **a**: script-2 — top-left hook, left descend, bottom sweep, right rise
- **i**: ring head (centerline circle r 55) + straight stem on its right
- **u**: descend, bottom sweep, big loop crossing back under the descend
- **e**: ram horns (two arcs) meeting a center stem
- **o**: S-spiral with inner curl
- **x**: small ring + tail hook (reserved symbol)
- `,` `/` `?`: thin-stroke curls / zigzag / ring-with-arches; `.`: filled circle

## Verified facts

- Glyph↔character mapping is 1:1; lowercase only.
- The strong-member mark is a thin ring (not a filled dot), matching the hand-drawn original.
- Line metrics: hhea and OS/2 both ascent 819 / descent −205 (aligned; the original conflicted).
- The `x` glyph is a reserved symbol with a deliberately smaller body (owner decision, 2026-11-08).
