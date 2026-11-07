# Morphology

> Claim tags: **(attested)** / **(proposed)** / **(draft)** — see phonology.md.

## Principles

- Word-building is done by compounding plus one prefix; there is no inflection (attested: no inflectional contrasts anywhere in the 64-word lexicon).
- The root inventory is not maintained here — `lexicon.toml` is the single source of truth (entries whose `etym` field is `(root)`).

## Compounding — head-initial (attested, 26 compounds)

**The head precedes its modifier.** Every compound in the lexicon fits this pattern; the analysis is confirmed by minimal pairs:

- wozaweru = woza 'magic' + weru 'water' → 'magic of water' = **water magic** (a spell)
- weruwoza = weru 'water' + woza 'magic' → 'water of magic' = **magic water** (a potion)

Further examples:

- hosiwe = hosi 'air' + we 'flow' → 'flow of air' = wind
- zijawe = zija 'lightning' + we → 'flow of lightning' = electric current
- susewe = suse 'speech' + we → 'flow of speech' = sentence
- susedifu = suse + difu 'people' → 'speech of the people' = the language itself
- susedikabu = suse + dikabu 'creator' → 'speech of the creator' = oracle
- susewoza = suse + woza → 'speech of magic' = incantation
- yikawoza = yika 'staff' + woza → 'staff of magic' = magic staff
- yikakada = yika + kada 'tree' → 'staff of wood' = tree branch
- yikasamu = yika + samu 'power' → 'staff of power' = scepter
- dukawoza = duka 'vessel' + woza → 'vessel of magic' = the Difu magic-storing organ
- mahasamu = maha 'place' + samu → 'place of power' = the capital
- mahagogafu = maha + [goga + fu] → 'place of the evil-domain' = the central prison (left-branching head-initial nesting)

Verbal compound: wozakabu = woza 'magic' + kabu 'creation' → 'creation of magic', used as a verb by zero-conversion (see below).

## Derivational devices

- `di-` person/agent **prefix** (attested, 7 words): dikabu 'god', didabu 'worker', disamu 'king', dijohua 'Chinese person', diwota 'outsider', diwoza 'priest', digoga 'criminal'. Attaches to nouns and to adjectives (digoga, diwota) with the reading 'person characterized by X'. The only prefix in the language.
- V↔N zero-conversion (attested): suse 'speak / speech', kabu 'create / creation, thing', dabu 'work / labor'.
- `-we` as second element is the root **we 'flow'** (draft hypothesis from swadesh-drafts.md; fits all three -we words as a following modifier, consistent with head-initial compounding).
- `-fu` as second element (attested in susefu, kabufu, gogafu-within-mahagogafu; meaning unresolved): working hypothesis **(proposed)** — fu = 'realm, domain'. susefu 'speech-domain' = language, kabufu 'creation-domain' = world, gogafu 'evil-domain'.
- Color terms: yoki 'yellow' is the only attested color word; the `-ki` color-suffix analysis is a draft (swadesh-drafts.md), unadopted.

## What the language lacks (attested absences; proposed as systematic)

- No number marking: nouns are number-ambiguous; pronouns cover all numbers (diya 'you (sg/pl)', dita 'he/she/it/they').
- No tense/aspect inflection: time comes from context or adverbial phrases (proposed).
- No case affixes: core relations are carried by word order; obliques by si/so; possession by de.

## Inflection

- None attested; none proposed.

## Draft hypotheses pending adoption

Numerals (tu ga mi su ro), interrogatives in -he, demonstratives ki/ko, negator bu, conjunction ka, minimal-pair families — live in `swadesh-drafts.md`. Adopt into this file and `lexicon.toml` only after the owner approves.
