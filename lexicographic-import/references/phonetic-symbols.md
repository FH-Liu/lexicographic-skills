# Phonetic symbols in Oroqen, Ewenki/Solon and Dagur imports

This is a reusable recognition and treatment guide induced from existing import workflows, not a universal phoneme inventory. Establish the source's actual alphabet and distinguish orthography, source transcription and independently printed pronunciation. Keep detailed source conventions, exceptional readings and their locators in that source's central register.

## Common distinctions and treatment

| Symbols or notation | Treatment |
|---|---|
| `ʧ`, `ʤ`, `ʦ`; `tʃ`, `dʒ`, `ts` | **Future imports expand `ʧ → tʃ`, `ʤ → dʒ`, and `ʦ → ts` as general rules across sources.** Preserve the literal source glyphs offline. Apply consistently to the transcribed forms and their matching keys before reconciliation. This supersedes older source instructions retaining these ligatures. |
| `tɕ`, `tʂ`, `dʐ`; `s ʃ ɕ ʂ` | Distinguish the actual series and inspect whether a separate stop component is printed. The three approved ligature expansions do not authorize replacing other affricates or sibilants. Preserve other notation unless its treatment is established for the source. |
| `n ŋ ȵ ɲ`; possible lookalikes `ɳ η`, sequences `nj/ng` | Inspect hooks, loops and descenders; preserve distinctions rather than treating nasal-looking characters or digraphs as equivalent. A source inventory guides inspection but does not justify correcting a clearly printed exception. |
| `e ə`, `a ʌ`, `o ɔ ɵ`, `u ʊ ʉ`, `i ɪ`, `æ y ɿ` | Preserve vowel quality. Check missing bars, open versus closed shapes and small-cap forms. `ɵ/θ` and `ʊ/ⱱ` are known visual confusions, not automatic replacement pairs. Do not infer a vowel from a translation, pronunciation aid or expected harmony. |
| `γ/ɣ`, `g`, `ḡ/ḡ` | **Future imports normalize transcription `γ → ɣ` as a general rule across sources.** Preserve the literal source glyph offline and use the normalized form for matching. This does not convert plain or marked orthographic g, or authorize generating pronunciation from orthography. |
| `ʲ`, `ʷ`, baseline `j/w`, aspiration `h` | Preserve secondary-articulation marks and their attachment to the preceding consonant. Raised marks, full segments and punctuation are different. Do not flatten superscripts or discard h. |
| `ː` (U+02D0), transcription `:`, doubled vowels/consonants | Encode a colon functioning as the length mark as `ː`; retain literal source input. Preserve doubled letters as printed rather than converting them to `ː`. Leave punctuation colons, labels and identifiers untouched. Keep length and gemination in stored forms and identity comparisons. |
| Macron and other diacritics; case; hyphens; spaces; optional segments | Preserve these distinctions. A macron need not mean length. Do not remove stem-final hyphens, flatten alternatives or split every slash/parenthesis mechanically. Canonical Unicode equivalence does not license transliteration, case folding or diacritic stripping. Avoid NFKC on stored transcription because it can flatten modifier letters. |

## Reading and recording

Compare difficult glyphs with clear instances in the same print/font, inspect code points and use a display font that distinguishes the candidates. Morphology, alphabetical order, OCR agreement and an expected sound system help find suspect readings; they do not substitute for checking the source. Record raw text, verified reading and any approved conversion separately, with its scope and authority. Attribute a source-reading correction separately from the source's own spelling or a proposed printing error.

Use the main skill's source-to-register proofreading pass to check complete symbol sequences, including ordinary-looking OCR where a bar, hook, repeated letter or superscript may have disappeared. Keep unresolved alternatives and dependent judgments explicit offline. A change of transcription policy requires remapping affected search keys and dependencies; it does not authorize rewriting previously published data.

These recognition classes were distilled from the Hu and Engkebatu instructions, Dorji's orthography/IPA checks, and the Han–Meng, Nuomin–Moqi, Nanmu and comparative-wordlist workflows. They describe recurring practical risks, not frequencies or a new audit of the original scans. See [evidence](evidence.md) for the local source locations and the current user's superseding rule.
