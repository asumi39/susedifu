# Archived: original hand-drawn font container (pre-rebuild)

`susedifu-handdrawn.ttf` is the compiled font as exported from FontForge on
2024-05-01 from the hand-drawn design, copied here on 2026-11-08 just before
the font-container rebuild replaced `fonts/susedifu.ttf`.

The rebuild changed only the container: every glyph outline is point-identical
to this binary's outlines (verified point-for-point), shifted down by exactly
200 units so the baseline sits at 0 (the design baseline of the SVG guides).
This copy is kept for provenance; the letterform authority remains
`fonts/susedifu.svg`. See `fonts/SPEC.md` for the full record.

Also kept here: `Susedifu-installed-2026-02-12.ttf` — the variant that was
installed in `~/Library/Fonts` until 2026-11-08 (same outlines, separate
FontForge export with a capitalized family name). The system copy was
replaced with the rebuilt container on 2026-11-08.
