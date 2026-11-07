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

Verbal compound: wozakabu = woza 'magic' + kabu 'creation' → 'creation of magic'. The object–head order matches SOV clauses; it is used as a verb by zero-conversion (see below).

## Derivational devices

- `di-` person/agent **prefix** (attested, 9 words): dikabu 'god', didabu 'worker', disamu 'king', dima 'woman', diba 'man', dijohua 'Chinese person', diwota 'outsider', diwoza 'priest', digoga 'criminal'. Attaches to nouns and to adjectives (digoga, diwota) with the reading 'person characterized by X'. The only prefix in the language.
- Clipping: a free word is clipped to a bound morpheme for use in compounds (confirmed, 2026-11-08) — weru → we 'fluid', mama → ma 'female', baba → ba 'male'.
- ma 'female' / ba 'male' bound gender morphemes (clipped from mama / baba): dima = di + ma, diba = di + ba — kinship and gender unite with the di- person prefix. The bi/ya/ta of dibi/diya/dita have no corresponding system (roots).
- V↔N zero-conversion (attested): suse 'speak / speech', kabu 'create / creation, thing', dabu 'work / labor'.
- `-we` as second element = clipped weru 'water' (see clipping), modifier 'fluid/flow of X': hosiwe 'the air's water' = wind, zijawe 'the lightning's water' = electric current, susewe 'the speech's water' = sentence.
- `-fu` as second element (attested in susefu, kabufu, gogafu-within-mahagogafu): **fu = 'collection (of X)'** (confirmed, 2026-11-08). susefu 'collection of speech' = language, kabufu 'collection of creations' = world, gogafu 'collection of evil (things)'.
- Color terms: yoki 'yellow' is the only attested color word; no color-suffix pattern is confirmed.

## What the language lacks (attested absences; proposed as systematic)

- No number marking: nouns are number-ambiguous; pronouns cover all numbers (diya 'you (sg/pl)', dita 'he/she/it/they').
- No tense/aspect inflection attested; how time is expressed is open.
- No case affixes: core relations are carried by word order; obliques by si/so; possession by de.

## Inflection

- None attested; none proposed.

## Pending owner input

Slots for numerals, interrogatives, demonstratives, negators, connectives and the rest of the basic vocabulary are reserved in `swadesh-coverage.md` for the owner to fill manually. Nothing enters this file or `lexicon.toml` until the owner supplies it.
