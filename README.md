# susedifu

susedifu is a constructed language, the 'language of the people' (suse 'speech' + difu 'person'), with a custom script font.

## Language highlights

- **Agglutinative morphology** — new words derive from basic roots by compounding:
  - `hosi` (air) + `we` → `hosiwe` (wind)
  - `suse` (speech) + `difu` (person) → `susedifu` (the language's own name)
  - `di-` marks person: `dikabu` (creator / god), `didabu` (worker), `dijohua` (Chinese person)
- **A fictional world** — the vocabulary carries the Difu people's world setting: magic (woza), the magic-storing organ (dukawoza), the king (yikasamu), the capital Mahasamu (mahasamu), and more

## Repository layout

| Path | Description |
| --- | --- |
| `lexicon.toml` | The lexicon — 64 base entries; the single source of truth for words and etymology |
| `grammar/` | Grammar docs: phonology, morphology, syntax, and a regression corpus of example sentences |
| `swadesh-drafts.md` | Swadesh 207-item comparison with new-word drafts |
| `fonts/` | The custom script font (TTF + SVG) |

## License

- Language data and documentation: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — susedifu © 2026 asumi39 (`LICENSE`)
- The Susedifu font: [SIL Open Font License 1.1](https://openfontlicense.org/) with Reserved Font Name "Susedifu" (`LICENSE-FONT`)
