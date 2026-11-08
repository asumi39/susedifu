# AGENTS.md

This repository is the database of susedifu, a constructed language. It holds documents and fonts only, no code: no build, test, lint, or CI. After changes, run the consistency checks below.

## Language essentials

- susedifu means 'language of the people': suse ('speech') + difu ('person')
- Agglutinative morphology; new words derive from root compounding: `hosiwe` = hosi ('air') + we; `di-` marks person (dikabu 'god', didabu 'worker')
- Word forms are lowercase Latin letters without spaces; fictional-world vocabulary (woza 'magic', mahasamu 'capital') must keep a consistent setting style

## Files

- `lexicon.toml` — the lexicon (68 entries: 64 from the original table + 4 bound morphemes), grouped into semantic sections with root families kept adjacent; the single source of truth for words and etymology; one `[[word]]` block per entry, field reference in the header comment
- `grammar/` — phonology / morphology / syntax / examples; examples is the regression corpus of probe sentences
- `swadesh-coverage.md` — Swadesh 207-item coverage map; the ⬜ slots are reserved for the owner to fill manually — the agent must not invent words into them
- `alphabet.md` — the alphabet: owner-confirmed letter order (2026-11-08), letterform chart, script facts; the script's open points (letter names, writing direction, the reserved symbol x) are recorded there
- `fonts/susedifu.svg` — the hand-drawn Inkscape design source; **the authority for letterforms**
- `fonts/susedifu.ttf` — the official font; its outlines must stay point-identical to the SVG (container spec and verification record in `fonts/SPEC.md`)
- `fonts/alphabet.png` — rendered letterform chart
- `fonts/archive/` — provenance copies and rejected experiments (READMEs inside); nothing there is official
- `LICENSE` (CC-BY 4.0, applies to all content) and `LICENSE-FONT` (SIL OFL 1.1, applies to fonts/)

## Font discipline (hard rule)

- The letterforms are the owner's hand-drawn design. Never redraw, regenerate, or "fix" them — not even to repair container defects. A parametric rebuild was attempted on 2026-11-08 and rejected; it survives only as `fonts/archive/v2-parametric-2026-11-08/`.
- Container-level changes (metrics, name table, table set) are allowed only on explicit owner request.
- Protocol for any font action: build in a temp directory → verify outline point-identity against the current official font → show per-glyph proof comparisons → get owner approval in chat → only then touch repo files and record the change in `fonts/SPEC.md`.

## Claim discipline

- `grammar/` and `alphabet.md` tag every claim: **confirmed** (owner decision) / **(attested)** (generalizable from `lexicon.toml` or the font) / **(proposed)** (new, needs owner confirmation) / **open** (undecided).
- Undecided points stay marked **open** — the owner decides them in chat. Never fill an open point by invention, in any file.

## Consistency checks (run after every change)

No tooling or CI exists for these — they are grep-and-read checks.

1. Every word cited in `grammar/` exists in `lexicon.toml`.
2. No duplicate word forms in `lexicon.toml`, except attested homonyms (sa, entries 19/20).
3. Every `etym` decomposition matches an attested derivational pattern in `grammar/morphology.md`; new patterns need owner approval.
4. Word forms are lowercase Latin without spaces and use only attested phonemes (vowels a e i o u; consonants b d f g h k m r s t w y z; j only in the johua family, i.e. the loanword and its derivatives).
5. Words enter `lexicon.toml` only from the owner — the ⬜ slots in `swadesh-coverage.md` are theirs to fill; grammar docs never duplicate the root inventory.
6. After any grammar change, re-check every sentence in `grammar/examples.md` against the new rules.

## Conventions

- All repository content — this file included — is written in English; terminology and gloss abbreviations follow the Leipzig Glossing Rules. The `zh` fields/columns keep the original Chinese glosses as reference data. Conversation with the owner stays Traditional Chinese.
- Commit directly to `main` and push; no PR process.
