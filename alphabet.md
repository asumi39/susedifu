# Alphabet

> Letterforms come from the Susedifu font (`fonts/susedifu.ttf`); Latin letters are the romanization used throughout the repository, and the mapping is one-to-one.
> Claim tags: **confirmed** (owner decision) / **(attested)** = read directly from the font or the lexicon / **open** = undecided — the owner decides.

## Letter order (confirmed, 2026-11-08)

- Vowels: **a i u e o**
- Consonants, seven pairs arranged by place of articulation, front to back:
  - Labial: **m b · w f**
  - Coronal: **t d · s z**
  - Guttural: **k g · h y**
  - Sonorant: **r j**

Within each place group, the pair with more closure comes first (m b → w f, t d → s z, k g → h y). The full order: `a i u e o m b w f t d s z k g h y r j` — 19 letters.

## Letterform chart

![The susedifu alphabet](fonts/alphabet.png)

## Attested facts

- One-to-one mapping: each Latin letter has exactly one letterform; the font has no uppercase.
- Within each consonant pair the two letterforms share a base shape — the second member adds a small circle (b = m + ◦, d = t + ◦, and likewise in all seven pairs). The circle marks the stronger member of the pair (confirmed, 2026-11-08 — see Pair semantics).
- The seven pairs coincide exactly with the font's base+circle families — the script itself asserts these pairings.
- All 19 letters occur in `lexicon.toml`; j is restricted to the johua family (see phonology.md).
- Punctuation glyphs in the font: space, comma `,`, period `.`, slash `/`, question mark `?`.
- The Latin letters c l n p q v have no glyphs — they correspond to sounds absent from the phoneme inventory.
- The font includes **x**, a reserved **symbol** (not an alphabet letter) with a deliberately smaller body (owner decision, 2026-11-08); its intended use: open. The old design source also held a **p** layer, never exported and now retired to git history.
- Repository documents are written in Latin letters; the font renders them as the custom letterforms.

## Pair semantics (confirmed, 2026-11-08)

Within each pair, the first member is the weaker consonant and the second the stronger — the circle marks the strong member.

Natural correlates (h, j, r and the five vowels confirmed; other consonant values open): the weak member is the voiceless one in t–d, k–g, s–z, h–y; the hum before the burst in m–b; the smooth glide before the turbulent fricative in w–f; and the tap [ɾ] r before the fricative [ʐ] in r–j. Strength is thus acoustic substance — voicing, turbulence, burst — rather than any single feature.

## Open points

- Letter names — names are words, and words enter the language only from the owner (see AGENTS.md).
- Writing direction and text layout.
- The intended use of the reserved symbol **x**.

## Files

- `fonts/susedifu.ttf` — the compiled font, v2.0 (normalized parametric rebuild; 26 glyphs: 19 alphabet letters + x + 4 punctuation + space)
- `fonts/susedifu.svg` — the stroke-based design source: one layer per glyph, metric guides, directly editable
- `fonts/SPEC.md` — the font specification: global grid, stroke weights, height classes, skeleton summary
