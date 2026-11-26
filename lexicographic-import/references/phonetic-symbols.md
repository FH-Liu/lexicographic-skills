# Special-symbol catalogue for Tungusic and Mongolic dictionaries

This is a reusable recognition and treatment guide induced from existing import workflows, not a universal phoneme inventory. Establish the source's actual alphabet and distinguish orthography, source transcription and independently printed pronunciation. Keep detailed source conventions, exceptional readings and their locators in that source's central register.

For a new import, ask about the symbols actually present before choosing their stored encoding. Show a literal sample and the proposed output. For example, “This dictionary prints ʦ. Should the form display ʦ or ts? Should the same convention apply to ʧ/tʃ and ʤ/dʒ?” Record the agreed scope. Preserve the literal evidence whichever convention is chosen. For an ongoing import, reuse the user’s recorded choice unless they change it.

## Common distinctions and encoding options

| Symbols or notation | Treatment |
|---|---|
| `ʧ`, `ʤ`, `ʦ`; `tʃ`, `dʒ`, `ts` | The split convention uses `ʧ → tʃ`, `ʤ → dʒ` and `ʦ → ts`. A literal convention retains the ligatures. Show both choices, especially where a source also prints adjacent stop and fricative letters. Preserve any source contrast in the mapping. |
| `tɕ`, `tʂ`, `dʐ`; `s ʃ ɕ ʂ` | Distinguish the actual series and inspect whether a separate stop component is printed. An encoding choice for one series applies only within its agreed scope. Preserve other notation unless its treatment is established for the source. |
| `n ŋ ȵ ɲ`; possible lookalikes `ɳ η`, sequences `nj/ng` | Inspect hooks, loops and descenders; preserve distinctions rather than treating nasal-looking characters or digraphs as equivalent. A source inventory guides inspection but does not justify correcting a clearly printed exception. |
| `e ə`, `a ʌ`, `o ɔ ɵ`, `u ʊ ʉ`, `i ɪ`, `æ y ɿ` | Preserve vowel quality. Check missing bars, open versus closed shapes and small-cap forms. `ɵ/θ` and `ʊ/ⱱ` are known visual confusions, not automatic replacement pairs. Do not infer a vowel from a translation, pronunciation aid or expected harmony. |
| `γ/ɣ`, `g`, `ḡ/ḡ` | One transcription convention maps Greek `γ → ɣ` (Latin gamma). Confirm its use for this source and field. Preserve the printed reading. This does not convert plain or marked orthographic g, or authorize generating pronunciation from orthography. |
| `ʲ`, `ʷ`, baseline `j/w`, aspiration `h` | Preserve secondary-articulation marks and their attachment to the preceding consonant. Raised marks, full segments and punctuation are different. Do not flatten superscripts or discard h. |
| `ː` (U+02D0), transcription `:`, doubled vowels/consonants | When the user chooses IPA length notation, encode transcription `:` as `ː` where the source uses it for length. Retain the literal input. Preserve doubled letters as printed rather than converting them to `ː`. Leave punctuation colons, labels and identifiers untouched. Keep length and gemination in stored forms and identity comparisons. |
| Macron and other diacritics; case; hyphens; spaces; optional segments | Preserve these distinctions. A macron need not mean length. Do not remove stem-final hyphens, flatten alternatives or split every slash/parenthesis mechanically. Canonical Unicode equivalence does not license transliteration, case folding or diacritic stripping. Avoid NFKC on stored transcription because it can flatten modifier letters. |

## Reading and recording

Compare difficult glyphs with clear instances in the same print/font, inspect code points and use a display font that distinguishes the candidates. Morphology, alphabetical order, OCR agreement and an expected sound system help find suspect readings; they do not substitute for checking the source. Record raw text, verified reading and any approved conversion separately, with its scope and authority. Attribute a source-reading correction separately from the source's own spelling or a proposed printing error.

Use the main skill's source-to-register proofreading pass to check complete symbol sequences, including ordinary-looking OCR where a bar, hook, repeated letter or superscript may have disappeared. Keep unresolved alternatives and dependent judgments explicit offline. A change of transcription policy requires remapping affected search keys and dependencies; it does not authorize rewriting previously published data.
