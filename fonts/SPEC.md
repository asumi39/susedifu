# Susedifu Font Container Specification

> Scope: this document records the **technical container** of
> `fonts/susedifu.ttf` — metrics, tables, glyph inventory, and the verification
> record of the 2026-11-08 rebuild. It deliberately says nothing about glyph
> design: the letterforms belong to the owner, and their authority is the
> hand-drawn design source `fonts/susedifu.svg`.

## Design grid (owner's guides in the SVG source)

The SVG carries Inkscape font guides (y-up units, `em` = 1024):

| Guide | Label | y (absolute) | relative to baseline |
|---|---|---|---|
| Ascender | 上伸線 | 950 | +750 |
| Caps | 大寫線 | 800 | +600 |
| x-height | x 字高 | 600 | +400 |
| **Baseline** | **基線** | **200** | **0** |
| Descender | 下伸線 | 0 | −200 |

These are the owner's drawn references; the hand-drawn glyphs sit on the 200
line with natural jitter (letter bottoms 191–202, ±9 around the guide).

## The 2026-11-08 container rebuild

Motivation: the FontForge-exported container had inconsistent metrics and a
floating baseline. The rebuild changed **only the container** — every glyph
outline is point-identical to the original (verified op-by-op, point-by-point,
flag-preserving), translated by exactly (0, −200) so the baseline sits at 0.
Structure (curve segmentation, explicit/implied points) is preserved as-is.

| Property | Before | After |
|---|---|---|
| Baseline | ink floated at y ≈ 196–202 | baseline 0 (uniform −200 shift) |
| hhea ascent / descent / lineGap | 1024 / 0 / 92 | 750 / −200 / 0 (design grid) |
| OS/2 typo | 819 / −205 / 92 | 750 / −200 / 0 (matches hhea) |
| OS/2 win | 1024 / 0 | 750 / 200 (matches hhea) |
| OS/2 fsType | 8 (restricted embedding) | 0 (installable; SIL OFL 1.1) |
| OS/2 version | 1 | 4 (sxHeight = 287, sCapHeight = 600) |
| head unitsPerEm | 1024 | 1024 (unchanged) |
| head fontRevision | 1.0 | 1.1 |
| Advance widths | 648 monospace, space 0 | 648 monospace incl. space (owner decision); .null 0 |
| hhea numberOfHMetrics | 5 | 28 (one full pair per glyph) |
| post | format 2.0, underline 0/0, fixed 0 | format 2.0, underline −100/50, isFixedPitch 1 |
| vhea / vmtx | present (half-configured) | removed (horizontal-only font) |
| FFTM / GDEF | FontForge extras | removed |
| gasp | {65535: grayscale} | unchanged |
| Glyph names | glyph00003…glyph00027 | space, comma, period, slash, question, a–z (from cmap); .notdef / .null / nonmarkingreturn kept |
| name table | family "susedifu", full name "font1", no license records | family "susedifu" (unchanged), full name "susedifu Regular", PS "Susedifu-Regular", version 1.1, copyright + SIL OFL 1.1 records added |

## Glyph inventory

28 glyphs: `.notdef`, `.null`, `nonmarkingreturn`, plus 24 mapped characters —
the 19 alphabet letters (a i u e o m b w f t d s z k g h y r j), the reserved
symbol **x** (not a letter; deliberately smaller body), and punctuation
`, . / ?`. The strong-member mark is a thin ring drawn into each glyph outline
(b d f g j y z); there are no mark anchors, no GPOS/GSUB, no hinting.

## Verification record

- Outline identity: all 24 mapped glyphs re-verified after rebuild — pen
  records exactly equal to the originals modulo (0, −200); glyph bboxes equal
  to the original (exact curve-extreme) bboxes shifted by −200.
- Geometry render check: even-odd polygon fill of flattened outlines,
  old (lowered 200) vs new: **0 differing pixels across all 24 glyphs**.
- Renderer note: FreeType's auto-hinter grid-fits differently when glyphs move
  relative to the baseline; residual rasterization differences under hinting
  are renderer-side and not outline changes.

## The 2026-11-08 stroke-width normalization (v1.2)

Letterform-level change, owner-requested in chat and owner-approved on proof
comparisons before anything touched the repository.

Motivation: measured typical stroke width varied 32–70 units across the 19
letters (i/e lightest, k/g ≈ +50% heavier). The owner chose full
normalization toward a 40u target.

Method: structure-preserving point offset. Every non-ring outline point moves
along its local normal (neighbor-tangent estimate); point counts, curve
segmentation, and flags are unchanged — the outlines are moved, never redrawn.
Deltas are per pair (both members of a letter pair share the value, keeping
pair base identity). Three passes: pass 1 = approved table
(a +1, i +4, u +1, e +4, o +1, m/b −2.5, w/f +1, t/d +0.5, s/z +1.5,
k/g −7.5, h/y −1, r/j +1 — units, em = 1024); passes 2–3 measurement-driven
refinement (d = (40 − measured)/gain, learned per letter). The same pass
sequence was replayed on the SVG's own cubic points, so the design source and
the font moved together.

Ring exemption: the strong-member ring dot (31/15 + 22/10 + 21/10 point
signatures) is byte-exact untouched. Note: the d ring inner contour is 21/10 —
the first experiment run missed it (1.3u shift); the released artifact was
regenerated with the corrected signature before approval/installation.

Verification (all pass on the released artifact):

- Structure identity vs v1.1: point counts, flags, contour ends identical for
  all 19 letters.
- Ring points byte-identical in all seven strong letters.
- No stroke breakage: connected-component counts unchanged.
- Convergence: typical stroke width 38–42u (was 32–70u).
- Max single-point displacement 13u (k; ≤7u for most letters) — same order as
  the hand-drawn baseline jitter (±9u).
- Metrics invariants unchanged: em 1024, hhea/OS-2 750/−200, fsType 0,
  advances 648, gasp, glyph inventory 28. hmtx lsb and hhea bearing fields
  reconciled to the moved outlines. Version 1.2.
- SVG sync: 24 path elements rewritten (19 letters; e/w/z/j/h exist as two
  identical full-size sets, both synced). Per-letter rasterized ink changes
  match the recorded pass sequence. Word-sample layers did not match font
  geometry and were left untouched (historical drawings at other scales).
- `fonts/alphabet.png` regenerated from v1.2.

## Files

- `fonts/susedifu.ttf` — the official font, container v1.2 (2026-11-08)
- `fonts/susedifu.svg` — the design source (stroke-normalized in lockstep with the font; authority for letterforms)
- `fonts/archive/original-container-2026-11-08/` — the pre-rebuild binary, kept for provenance
- `fonts/archive/v2-parametric-2026-11-08/` — rejected 2026 letterform-rebuild experiment (NOT the official font)
