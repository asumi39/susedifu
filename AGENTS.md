# AGENTS.md

This repository is the database of susedifu, a constructed language. It holds documents and fonts only, no code: no build, test, or lint. After changes, rely on content-consistency checks.

## Language essentials

- susedifu means 'language of the people': suse ('speech') + difu ('person')
- Agglutinative morphology; new words derive from root compounding: `hosiwe` = hosi ('air') + we; `di-` marks person (dikabu 'god', didabu 'worker')
- Word forms are lowercase Latin letters without spaces; fictional-world vocabulary (woza 'magic', mahasamu 'capital') must keep a consistent setting style

## Files

- `Documents/words.toml` — the lexicon (64 entries), the single source of truth for etymology; one `[[word]]` block per entry, field reference in the header comment
- `Documents/swadesh-drafts.md` — Swadesh 207-item comparison and new-word drafts (drafts are tentative and may be edited or rejected; adopt into words.toml only after approval)
- `Documents/grammar/` — grammar docs: phonology / morphology / syntax / examples; examples is the regression anchor for grammar changes
- `Fonts/susedifu.ttf`, `Fonts/susedifu.svg` — the custom script font; do not modify unless necessary

## Conventions

- All repository content — this file included — is written in English; terminology and gloss abbreviations follow the Leipzig Glossing Rules. The `zh` fields/columns keep the original Chinese glosses as reference data. Conversation with the owner stays Traditional Chinese.
- Commit directly to `main` and push; no PR process.
