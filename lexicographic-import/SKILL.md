---
name: lexicographic-import
description: Prepare and import scanned or digital dictionaries through central offline staging, faithful transcription and a unified search for families, formal variants and inflections. Includes Oroqen, Ewenki/Solon and Dagur guidance. Use for dictionary ingestion or import planning; use lexicographic-families-and-loans for standalone lexical analysis.
---

# Import a dictionary through central offline staging

Complete the whole dictionary or agreed corpus offline before any upload. Pilots and processing batches are local work units, not publication checkpoints. If only a section is authorized, finish it offline; do not treat that as permission to publish an unfinished dictionary. A later explicit user instruction can change this boundary. Preparing an import does not itself authorize publication.

Produce a source inventory, source-to-platform mapping, reviewed records, stable reconciliation/coverage ledger and final publication package. Preserve information without filling fields merely because the interface offers them.

For long tasks or goals, ask the user to allow parallel processing with three subagents unless already authorized. Give each a concise handout with its scope, expected findings and pointers to essential current skills and applicable instruction sheets. The main agent reconciles their findings and records decisions, evidence and coverage in the central register. With or without subagents, use substantial coherent batches: avoid tiny batches that inflate per-item bookkeeping cost, while preserving complete review and required checks.

For new executable-register runs, declare the requested import/family/loan `plan` once. The register advances through those phases and gates final export; keep mappings, decisions and batch source-review receipts there, without separate handoff reports. See the offline-workspace reference and `workflows/OFFLINE_WORK.md` for the compact contract; preserve legacy active runs unless explicitly migrated.

Read [offline workspace](references/offline-workspace.md) when establishing the register, [platform adapter](references/lexicon-editor.md) for this editor, and the relevant [source profile](references/areal-source-profiles.md) for Hu, Engkebatu, Dular, Delkir or Dorji. Other platforms and varieties need their own mappings. [Evidence and policy lineage](references/evidence.md) identifies the sources and superseded practices.

For Oroqen, Ewenki/Solon and Dagur transcription, read [phonetic symbols](references/phonetic-symbols.md). For future imports, expand affricate ligatures `ʧ → tʃ`, `ʤ → dʒ`, and `ʦ → ts`, and normalize `γ → ɣ` as general transcription rules across sources, retaining the literal source reading offline. These current rules supersede older instructions to preserve those input symbols; it does not request a rewrite of completed imports.

## Establish source and data-model fit

Inventory editions, native text/spreadsheets, scans and supplements; hash retained sources once. Distinguish printed pages, PDF pages, page series and assigned extraction keys. Preserve gaps and exclusions. Prefer trustworthy digital text to unnecessary OCR, checking encoding and layout losses. Inspect front matter and representative difficult entries before bulk processing.

Map entries, homonyms, senses, forms, phonetic transcriptions, examples, subsidiaries, labels and references to supported fields. Specify variety/dialect scope, source locators, enrichment and merge policy. Test a detached pilot containing difficult structures and Unicode symbols. Where the model cannot express a distinction, propose a typed field or lossless sidecar and disclose publication loss. Do not flatten subentries, put examples in definitions or use lexical notes as a catch-all.

A printed parent is not proof of derivation; whitespace is not a universal POS test; a Chinese gloss is not a donor assertion. Identical spelling and different meanings do not independently settle lexical identity. Ask about consequential unresolved choices, such as cross-source merging or an incompatible sense model, using concrete examples. Continue unaffected preparation.

## Digitise non-body material to Markdown

As part of dictionary preparation, inventory and transcribe the non-body sections to Markdown, including title/publication pages, contents, prefaces, usage instructions, abbreviation and symbol lists, phonological or grammatical descriptions, appendices, indexes and bibliographies. Honour explicit source-scope exclusions and record missing pages. Track eligibility for lexical import separately from documentary transcription coverage, so an appendix excluded from entry import can still be retained as source documentation.

Keep a canonical Markdown transcription with the retained source materials and reference it from the central register. Reuse an existing verified transcription where available. Preserve the full source content, section order, headings, lists, notes, examples and table relationships, with source/edition identity and printed-page and PDF-page locators. Retain source notation and distinguish any approved conversions or editorial annotations. For layouts or figures that Markdown cannot express faithfully, retain linked source images with locators and transcribe their readable text. Use trustworthy native text when available and check extraction for encoding, omissions and layout loss.

For scanned material, including PDFs with an OCR text layer, check the entire transcription against the original page images, then perform a separate source-to-Markdown proofreading pass before marking it verified. Check omissions and duplicated passages as well as OCR substitutions, especially phonetic symbols, diacritics, length marks, superscripts, grammatical notation, example numbering and table alignment. Apply the scan-batch correction and review-receipt rules below to these sections too. Mark unresolved readings explicitly with exact locators and retain supporting images. Record section/page coverage, corrections, outstanding uncertainties and both review passes centrally, and cite verified passages when using their conventions or grammar descriptions in later analysis.

## Extract once and enrich explicitly

- Preserve literal source records alongside reviewed readings. Stable source keys survive corrections; one source record can map to several forms or senses.
- Record independently listed productive phrases and full sentences as standalone examples with their own source locators. Lexicalized expressions and conventional formulas qualify as entries.
- For scans, stage OCR or visual-transcription drafts, then check every candidate against the original image before accepting its entry/form records or using its spelling for segmentation, matching, families or loans. Check diacritics, vowel quality/length, spacing, superscripts, numbering, POS, meanings and reference targets. Raw drafts and unresolved alternatives may be retained centrally as evidence; mark them pending and keep form-dependent conclusions provisional. OCR confidence, model agreement and structural validation are not visual verification.
- Close each scan batch with a separate source-to-register proofreading pass and a receipt stating the pages/items and error classes actually checked. Inspect the source images as well as retrieved suspect strings, so omitted or misrecognised glyphs can be found. If a recurring error is discovered, audit its plausible earlier scope once, preserving explicit coverage and corrections; do not claim a whole-page audit from a few targeted checks or repeatedly reread unchanged, adequately audited pages. Correct affected mappings and analyses before relying on the forms downstream; preserve stable keys, earlier readings and unaffected linguistic confidence.
- For digital sources, check encoding, displayed versus stored values where relevant, row uniqueness, multivalue delimiters and numbering. Sample against originals and expand checking when systematic errors appear. Do not claim scan review that did not occur.
- Keep search/comparison normalization separate from stored forms. Apply only approved preparation conversions and preserve their raw inputs and authority. Never populate pronunciation from an orthography diagnostic or strip endings without a source-specific rule.
- Attribute printed content to its source, translations to translator/LLM, algorithms to inference, and editorial corrections to their actual author. Supporting evidence is not intellectual authorship. Do not invent dates, human checks or references.
- Keep optional content absent unless enrichment is authorized. Missing English should not block a faithfully transcribed entry; preserve user-directed blanks. Separate transcription uncertainty, translation uncertainty and analytical confidence.

If a glyph or identity cannot be determined, retain alternatives/image evidence offline, complete usable fields and report the exact gap. Use provisional readings only where they can be represented honestly. Otherwise omit only the unrepresentable assertion from publication. Confidence levels for linguistic analyses do not authorize guessing source text.

## Search once for families, variants and inflections

Unify entry consolidation, word-family detection and inflection detection in one search. As each complete nested source group is verified, run the [local source-structure search](../lexicographic-families-and-loans/references/analysis-workflow.md#local-analysis-of-nested-source-groups) over its head, subentries and relevant example occurrences. Preserve printed organization independently of the inferred relations. Record decisions and coverage once in the central register. After checking the whole source, continue corpus-wide retrieval over verified forms, pronunciations, meanings, grammatical behavior and references, including separately staged heads; reuse unchanged local decisions rather than repeating their adjudication.

Reuse the user's established merge scope. If it is undecided, clarify whether to retain source entry boundaries, consolidate within the incoming dictionary, or include specified existing entries of the same highest-level variety. Continue independent extraction and retrieval while awaiting that scope; do not infer cross-source merge authority from an earlier import. Compare each variety separately.

Accepted comparisons have three recording options:

| Recording option | Decision and representation |
|---|---|
| **word family membership** | Distinct lexemes share a supported lexical root; retain separate entries and record scoped membership with its own confidence. |
| **merge entry formal variant** | Forms represent the same lexeme without an inflectional distinction; consolidate under the retained entry, preserving forms, senses and source evidence. |
| **merge entry inflected form** | A form realizes a grammatical inflection of the same lexeme; retain it as an inflected form of the base entry, with supported grammatical analysis and its source meaning. |

Reject unsupported comparisons explicitly; rejection is a decision status, not a fourth recording option. A common root alone does not establish lexical identity, and an apparent ending alone does not establish inflection. Keep derivatives and homonyms distinct. If only family relatedness is warranted, record that assessment without forcing a merge. Do not invent an unattested base or turn an inflected translation into a new lexical sense automatically.

Retain provenance and exact source locators on each form, sense and example. Keep stable source keys mapped to retained entry/form/sense identities after consolidation, and update affected references, family memberships and analyses. Assert explicit form–sense links only where the platform represents them. Complete declared search routes and resolve candidates, then review the remaining singleton lexemes once. When loans are in scope, screen the resulting families and singletons afterward.

## Reconcile centrally

Account for every source item as represented, explicitly excluded, unresolved source content, or already represented by a stable mapping. Track prepared coverage separately from published coverage. Complete page-crossing entries together and resolve forward references after corpus assembly.

Resolve references to exact targets and intended homonyms/senses. Formal variants, translation-equivalent entries and see-references are different outcomes. Do not attach a merely similar target or emit dangling relations. Log an unresolved reference once and revisit when its target is available.

Keep routine extraction/conversion/import explanations in source-level documentation or the offline log. Dictionary remarks should add a specific lexical fact, correction, ambiguity or necessary restriction. Omit repeated field values, certainty labels, “imported from dictionary” and “matches in form and meaning.”

## Validate and publish at the end

During preparation, check changed records and affected dependencies: types, IDs, Unicode distinctions, source coverage, duplicate keys, cycles, attribution and approved field scope. Maintain one resume cursor. Avoid full-project candidates and browser round trips per page batch.

After the whole source scope is complete, obtain the current platform revision, reconcile the offline delta with intervening edits, bind destination IDs and build the final candidate. Run required structural, preservation, provenance, interchange and protected-save checks. Inspect a representative read-only UI sample for display problems; this supplements source checking.

When uploading materials, update the platform's source description and other relevant source information in the same guarded publication. Infer the appropriate content and format from existing source descriptions: bibliographic identity and scope, separate source-item and reconciled-entry counts, an illustrative source page with its locator, how source information is represented, and what agents or inference algorithms added, with attribution. Derive counts from the reconciled register and describe actual published coverage and enrichment.

Publish through the existing protected route with the exact baseline and backup, then perform one read-back reconciliation and retain the receipt. A conflict requires rebasing and rebuilding; never put a new revision into old verification. If payload limits require chunks, prepare them only after the full corpus is complete; retain dependencies, each required save gate and resumable receipts. Do not resend successful chunks after a partial failure.

Report coverage, entries/senses, exclusions, unresolved content, enrichment and publication status. Source rows, entries and assertions are different counts. Successful validation does not establish independently verified linguistic truth.

## Close each session

Save durable records, decisions, coverage and one precise resume cursor centrally. Then delete session-created temporary or redundant materials and logs whose useful contents are retained: scratch candidates, regenerable previews, successful-test output and duplicate progress narratives. Preserve originals, unique evidence, referenced snapshots, unsaved drafts, deliverables and necessary recovery/publication receipts. Verify an identical retained canonical copy and its references before deleting a duplicate; never treat age or a filename as proof. Keep only concise actionable failure evidence until resolved. See the offline-workspace reference for guarded cleanup.
