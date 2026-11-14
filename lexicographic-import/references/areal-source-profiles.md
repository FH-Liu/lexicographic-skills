# Oroqen–Solon–Dagur import profiles

These are source-specific editorial mappings, not universal descriptions of the languages. Current schema and user decisions supersede obsolete transport fields in old sheets. Apply an old linguistic transformation only when still authorized for the source/task; import execution itself performs no inference.

The shared [phonetic-symbol treatment](phonetic-symbols.md) governs future imports, including `ʧ → tʃ`, `ʤ → dʒ`, `ʦ → ts`, and `γ → ɣ` across sources. Do not extend this profile collection with isolated reading corrections or narrowly scoped conventions; keep those in the relevant workflow's central register.

## Hu (2001): Oroqen, Chaoyang

- Preserve original workbook row identity; references such as `Sheet1:r1273` are workbook positions, not printed entry numbers. Variety is Oroqen, language tag `orh`; Chaoyang belongs at the supported lower scope in the current schema.
- The historical authorized verb preparation treats a terminal consonant + vowel + n: if that consonant is m/n/ŋ/ȵ, remove final vowel+n and append `-`; otherwise remove consonant+vowel+n and append `-`. Apply only to confirmed verbs, each actual alternative separately. If the pattern is unclear or leaves no stem, retain the source form. Preserve the supplied wordlist citation independently; never regenerate it from a guessed stem.
- Examples in the sheet: `ʊdɪnan → ʊdɪn-`, `itʃərən → itʃə-`, `jabʊran → jabʊ-`. These are Hu conventions, not a Solon/Dagur stemmer. Any newly authorized conversion needs inference provenance, not dictionary authorship for the derived stem.
- Preserve specified POS; historical Hu classifier-as-noun and other category decisions are source policies, not defaults for new dictionaries. Missing POS must not silently become `n`. Apply any intended inference in a declared preparation pass.
- Preserve concise translations and fuller definitions without inventing encyclopedic content. Earlier blanket bilingual enrichment, `style`, `needsCheck`, phrase overrides and prohibition on provenance were superseded by schema 2. Preserve deliberately blank values.

## Engkebatu (1984): Dagur, Tengke

- Use the clearer `workflows/engkebatu/source/dagur dictionary.pdf` when present. Its known body-page examples have PDF offset +17; verify actual page labels, not a universal offset. Printed p338 was unavailable in both historical scans. Record the gap rather than fabricate coverage. Old scans remain evidence.
- Distinguish palatalization `ʲ`, labialization `ʷ`, baseline w, length and vowel quality. Approved preparation conversions include `ʧ→tʃ`, `ʤ→dʒ`, `γ→ɣ`, transcription `:→ː`; preserve original readings. A label such as `满:` is not vowel-length notation. Do not apply NFKC, case folding or diacritic stripping to stored forms.
- Engkebatu transcription is not automatically an IPA pronunciation. Preserve lexical verb stems. Historical `-→bəj` citation generation is a source-specific inference requiring present authorization and separate attribution; never run it merely on import. Do not use Hu stem conversion.
- Variety Dagur, language `dta`. Store `Tengke` on the relevant forms and senses. The platform derives its Buteha ancestry from the [current Dagur mapping](https://github.com/FH-Liu/lexicon-editor/blob/d7b7c84d49afd9c36cadbacc5d16f2f84bd05777/workflows/shared/instructions/PROVENANCE_IMPORTS.md#dialect-scope-8-october-2026).
- Circled numbers divide senses; punctuation between equivalents does not automatically divide senses. Subsidiaries are entries with their actual parent, not senses of the parent. Keep homonyms separate.
- Resolve 同 to its exact normalized target. A credible formal variant can attach; non-phonological equivalence needs a separate entry and sense equivalence. The historical homonym-wide ll~ld, nn~nd and C₁C₂~rC₂ attachments are specific authorized conventions, not a general license to attach every reference to every homonym. Source sense restrictions still govern.
- Preserve printed POS. The historical 情→adv mapping is source-specific. The old rule replacing every phrase's POS with `phrasal` is superseded. Dagur classifiers must not inherit Hu's classifier-as-noun rule. If authorized RTR classification encounters `ɿ`, retain `unsure` under this project's rule.
- A clear source reading with uncertain English may be imported with English blank. Do not invent botanical species, anatomical specificity or cultural explanations to fill a field. Retain user-confirmed unusual Chinese text unless an explicit correction is made.
- The historical task excluded Mongolian and Khitan comparisons while retaining relevant Chinese, Manchu and Ewenki comparisons. Preserve that task's exclusion record; do not silently generalize it to every future Dagur import. Distinguish a printed comparison from an analyst's expanded donor and a modern lexical gloss.

## Dular (2019) and Delkir (2021): Nonni Solon

- Within merged entries, retain each Dular or Delkir form, sense and example with its own source locator. Follow the skill's consolidation rule for explicit form–sense mappings. Preserve Dular's qualified dialect paths and assign Delkir only where supported.
- Delkir's digital wordlist has 4,310 historical records. `DLK-W…` is the unique staging key; `source_entry_id` alone is not unique. Printed locator is page + printed entry number: `2-14`, not a page-reset `2-1`. Read BOM-bearing UTF-8 correctly.
- Preserve source spelling, diacritics and actual slash-separated alternatives. Do not normalize Delkir to Dular orthography, strip verbal endings or generate pronunciation/citation duplicates.
- The approved Delkir–Dular identity plan treated `same_lexeme` and `probable_same_lexeme` as merges, including groups with several existing Dular entries. This is a historical authorized editorial plan, not a universal rule that probable identity implies destructive unification. Preserve every source form, meaning and exact locator when applying an authorized merge.
- Related lexemes remain distinct with family membership under the current set model. Translation equivalence joins corresponding senses only. Semantic similarity alone emits no relation. Selected compound indexing gives child→parent, at most one parent, with no cycle; this does not capture all compound constituents.
- Chinese strings are definitions; new English definitions have LLM provenance. Do not invent additional short glosses. Preserve raw source categories offline and map to the current controlled vocabulary with attribution; older instructions demanding exact source domain labels and entry-level dialects need reconciliation with the later canonical domain/scope policies.
- Mixed POS sections such as 虚词 or 数量词和方向方位词 cannot be mapped uniformly to particles/numerals. Any individual classification is an attributed preparation judgment, not an import default.

## Dorji (1998): Hailar Solon and explicitly marked varieties

- Registered source `dorji-1998`: 杜·道尔基, *Ewengki Nihang bilehu biteḡ 鄂汉词典*. Unmarked material maps to Hailar Solon; 〈卡〉 to Khamnigan Ewenki; 〈使〉 to Aoluguya Ewenki, using `evn`. Do not invent subdialects or relabel these as Nonni Solon.
- Main body pp1–772; appendices from p773 were excluded. Main-body PDF page is normally printed page +23, checked at boundaries; preliminary numbering is separate. The import is already complete in the inspected workspace: any future correction/import needs new scope, not replay of completed batches.
- Do not reconcile pre-existing Hailar records during ordinary Dorji import. Use Dorji's coverage ledger to avoid duplicates, including scattered pilot items; a pilot page was not necessarily imported in full.
- Preserve orthographic `Ē ē Ɵ ɵ`, Ḡ/ḡ (NFC Ḡ/ḡ), doubled vowels/consonants and case. Macron ē marks vowel quality, not automatically length.
- Store printed IPA independently. The diagnostic mapping `e→ə, ē→e, ɵ→ɔ, o→ʊ, v→ɵ, c→ts, j→dʒ, q→tʃ, x→ʃ, y→j, z→dz, ng→ŋ, ḡ/ḡ→ɣ` is an OCR comparison aid only. Multigraphs precede single letters; h is not universally predictable. Never populate IPA from this mapping or generate absent phrase pronunciations.
- Distinguish 一/二 homonyms, Roman POS/homonym divisions and circled senses by context. Bold subsidiary groups are entries; illustrations are sense examples. Parent linkage does not infer POS. Missing printed POS remains missing. RTR `phrasal` is not POS `phrasal`.
- Preserve grammatical qualifications in sense-level `custom.grammatical_note`, with Chinese source and separately attributed English. Domain labels are separate values. Use the existing Chinese–English mapping; distinguish zoology from animals, anatomy from physiology, and broader categories from narrower ones. No domain inference for unlabelled senses.
- An unknown printed domain abbreviation may receive its best supported interpretation with LLM provenance and retained literal evidence; it does not hold the whole entry. Record uncertainty once in the mapping.
- Authorized RTR preparation: phrases first → `phrasal`; single-word orthography `{a,ɵ,o,ē}` positive, `{e,ə,u,v}` negative, both → `mixed`, no diagnostic vowel → `unsure`. Attribute algorithm `dorji-rtr-v2`; do not overwrite independent source-attributed RTR. This is not a general Tungusic vowel classifier.

## Transfer to another variety

Create a new profile from its own alphabet, phonology, lexical structure, reference conventions, source hierarchy and editorial purpose. Reuse the separation of raw text, interpretation and publication—not another variety's substitutions, stemmer, POS defaults, vowel classes or donor assumptions. Trial known difficult forms and references before bulk extraction.
