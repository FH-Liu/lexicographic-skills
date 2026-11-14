---
name: lexicographic-families-and-loans
description: Search a lexical corpus jointly for word families, entry consolidation and inflections, then detect loans. Record family membership, formal-variant merges or inflected-form merges centrally with scoped evidence and confidence. Use for lexical identity, family and borrowing analysis, not raw dictionary transcription or surname genealogy.
---

# Search families, variants and inflections, then loans

Finish one unified search for word families, formal variants and inflected forms across the whole authorized corpus, resolve entry consolidation and family membership, then freeze the resulting lexeme inventory and grouping before loan screening. Keep all work centrally offline; upload only after the whole corpus's requested analysis is complete. If a loan finding exposes an identity or family problem, revise the affected decisions and dependent proposals explicitly rather than silently changing membership during propagation.

For long tasks or goals, ask the user to allow parallel processing with three subagents unless already authorized. Give each a concise handout with its scope, expected findings and pointers to essential current skills and applicable instruction sheets. The main agent reconciles their findings and records decisions, evidence and coverage in the central register. With or without subagents, use substantial coherent batches: avoid tiny batches that inflate per-item bookkeeping cost, while preserving complete review and required checks.

The confirmed stopping rule is to complete the declared search routes across all entries, resolve their candidates, then review remaining singletons once and resolve any candidates arising from that review. Declare the applicable form, pronunciation, pattern, meaning and reference routes; record unavailable routes and limitations. This establishes completion of the agreed search coverage, not exhaustive discovery. Further full recall passes require a later instruction or material new evidence.

For new executable-register runs, declare the requested phases once and record compact lexical effects on the existing decisions. The register derives surviving lexemes/singletons, handles phase handoffs and retains unaffected coverage on reopening; do not maintain parallel inventories or handoff reports. Use the contract in `workflows/OFFLINE_WORK.md`; legacy runs retain their documented checks until explicitly migrated.

Consult references as needed: [analysis](references/analysis-workflow.md), [areal comparisons](references/areal-comparisons.md), [publication](references/lexicon-editor.md), [offline storage](references/offline-workspace.md), and [policy history](references/evidence.md).

## Scope and evidence

A family is a common lexical-root hypothesis among distinct lexemes. The root need not be a listed word; members need not derive directly from one another. The same search also identifies formal variants and inflections of one lexeme for consolidation. Read selected forms, pronunciations, POS and source-attributed meanings together. A shared affix, substring, spelling, topic, translation or imaginable metaphor is insufficient alone. Conversely, semantic distance or POS difference alone does not disprove a supported common root.

Within-variety family detection, cross-variety inherited cognacy, lexical identity, equivalence and borrowing remain distinct judgments within the workflow. Merge entries only on supported identity and within the authorized scope, never to improve apparent recall. Do not merge varieties. Preserve the corpus's inclusion policy; do not silently expand the inventory to productive phrases or sentences.

Retain actual entry/form/sense IDs and source pairings. Search normalization is not a stored-form rewrite. Use available evidence in imperfect records without manufacturing meanings or a source-repair holding queue. For an unambiguous 同 reference, use the target's semantics with the original attribution and scope. Ambiguous targets reduce confidence; do not select whichever supports the preferred hypothesis.

## First pass: one search, three recording options

Include verified nested source groups through the shared [local source-structure route](references/analysis-workflow.md#local-analysis-of-nested-source-groups), which may start during import. Reuse its decisions and coverage in the corpus-wide search. Printed parentage supplies candidates, not proof of identity or kinship; example occurrences need scoped attestation/analysis links without becoming extra lexemes. Local completion does not replace other declared searches or trigger singleton review or loans.

Resume unfinished frozen work before generating another bounded queue. Retrieve through exact forms/variants, pronunciation, inflectional paradigms and grammatical features, derivational morphology, induced patterns, meanings and references. Use one queue for consolidation and family discovery. Prioritize unassigned entries without omitting identity/inflection comparisons among existing family members. Deduplicate unordered pairs at actual form scope while retaining direction for base/inflected-form and retained/merged-entry decisions. Retrieval rank never determines the outcome.

Record an accepted comparison as **word family membership**, **merge entry formal variant**, or **merge entry inflected form**. Family membership retains distinct lexemes sharing a root; a formal-variant merge unites forms of one lexeme without an inflectional distinction; an inflected-form merge retains a grammatical realization under its base lexeme. Distinguish inflection from derivation and lexicalization using meaning and grammatical function, not suffix resemblance alone. Record the base, supported features and any stem alternation; do not invent a missing lemma or segmentation. Reject unsupported comparisons explicitly. A rejection of identity does not reject a separately supported family relationship.

Reuse the established merge scope and identity policy; clarify only consequential unresolved scope. A supported family hypothesis need not justify a merge. Preserve all source forms, meanings, locators and stable mappings when merging, and rebind affected references and memberships explicitly. Resolve conflicting assertions rather than silently coalescing them; preserve unaffected confidence. An inflectional translation belongs with the inflected form unless there is independent evidence for a lexical sense.

Inspect every affected family before accepting an addition or merger. Prevent weak bridges from uniting unrelated roots; shared membership does not authorize transitive closure. Use explicit compound-origin evidence where informative without requiring complete constituent analysis. Preserve unaffected confidence during mergers and reassess memberships whose hypothesis changes. These two instructions supersede the historical ignore-compounds and reset-all-confidence rules.

Every adjudicated comparison ends in acceptance or rejection. Register warranted uncertain memberships with qualitative confidence; reject unsupported or excessively uncertain comparisons without requiring proof of unrelatedness. Unexamined work can remain unprocessed, but an uncertain completed judgment is not an unexamined item or a hold. A rejection records the current assessment at exact scope, not proof that no relationship could ever exist.

Assign confidence to each membership: `certain`, `probable`, `possible`, `unlikely`, `unspecified`. Use `certain` for convincing linguistic evidence without requiring documentary proof. `Unspecified` means unassessed legacy/source confidence, not another uncertainty grade. Use no numerical scores or acceptance quotas. Preserve compact reasons for changed decisions and enough evidence to support review.

Maintain local variation and morphological-construction patterns separately, with variety, conditions, function, exact examples, independent-root support and counterexamples. A pattern-derived acceptance is not independent confirmation of that pattern. The Dorji five-root robustness convention is local; robust patterns do not automatically make a membership certain.

## Second pass: loans

Freeze the consolidated lexeme inventory and family revision, and derive singletons from the surviving lexemes. Merged source entries remain covered through their mappings; do not count them again as singletons or independent roots. Inspect each family as one unit and every member before propagating a loan. Start with its own source meaning and pronunciation. Generate plausible donors from whole lexical shape and meaning, considering historical/regional synonyms, recipient morphology, competing languages and intermediaries. A Chinese translation is not automatically the donor.

Keep borrowing likelihood, donor-language/form identification, direction and direct/mediated route distinct. An unexplained segment, missing donor spelling or unresolved route need not block a warranted `possible`/`probable` proposal. Convincing matches may be `certain`; they do not thereby establish direct transmission, chronology or independent review. Do not invent a donor to fill a field.

For the current platform, materialize the borrowed-base claim on every applicable member, retaining form/component/sense restrictions and full member-specific models. This says that a member continues or contains the borrowed base, not that every derivative was borrowed independently. Do not propagate a full compound donor to siblings sharing only one component. Multiple constituent-family loans can coexist.

For Dagur, keep Engkebatu's existing loan assertions and source provenance active in the eventual live dictionary. Express analyst disagreement or scope/confidence qualifications as concise attributed comments, without replacement or duplicate assertions. Correct OCR/digitisation errors without live notes; reserve a short correction note for errors present in the printed source itself. Preserve attribution/history and resolve legacy ownership from the linguistic recipient, including reversed edges. The [loan adapter](references/lexicon-editor.md#engkebatu-source-loans) specifies this source-preservation policy; it supersedes earlier retirement/replacement plans.

When a concrete family inconsistency would make propagation false, settle the affected grouping/scope first using normal confidence decisions and preserve the candidate locally. Continue all unaffected analysis. Keep source-data corrections separate from analytical judgments; do not alter source forms/meanings to improve a proposed etymology.

## Record, check and deliver

Keep current memberships, formal-variant and inflected-form merge decisions, rejections, loan proposals, evidence, patterns and resume state in one central store. Store hypotheses immediately, including weak warranted ones; keep elaborate research and supersessions offline. Live comments retain only specific sound/semantic insight, material alternatives or necessary scope. Leave them empty when structured fields suffice.

Reuse saved source passages and scoped judgments before retrieving them again; batch related lookups. Investigate uncertainties that could change the decision, and record unresolved route or ultimate origin when further research would not change the warranted judgment. Reuse of a root analysis still requires checking each recipient's form, sense and component scope.

For executable Dagur work, use the maintained inspection, evidence lookup and finalization commands in [OFFLINE_WORK.md](https://github.com/FH-Liu/lexicon-editor/blob/d7b7c84d49afd9c36cadbacc5d16f2f84bd05777/workflows/OFFLINE_WORK.md#efficient-dagur-batches). Inspect related groups in one read snapshot, retrieving saved passages before external research. Use a local source index with exact page/hash locators and explicit extraction aliases; aliases are retrieval aids, never source corrections. If equivalent text searches fail, inspect the relevant source page or record the bounded limitation instead of repeating spelling probes. A failed lookup is not absence evidence.

Prefer finalizing 20–30 fully reviewed groups together when complexity permits; use smaller coherent batches for difficult material. This is an administrative preference, not a review quota or permission to omit members. Use a data packet and the maintained finalizer rather than regenerating save/audit/close scripts. Keep continuation compact and refer to earlier obligations by record key. Required new-evidence reassessments and all source-preservation rules still apply.

Validate fields before saving. Recheck changed records and affected dependencies; reuse verification only while its inputs, sources and rules match. A new session alone does not require a full audit. Keep historical checks as dated snapshots and derive current totals once. At corpus completion, check all dispositions, coverage, mappings and loan scopes, then run the publication gates. “No proposal” does not establish native origin or exhaustive discovery.

At the end, reconcile against the fresh live revision, prepare one final delta, run the required platform gates and publish only within authorization. Keep a receipt and one read-back reconciliation. Report distinct roots/families, memberships, group loan proposals and materialized relations separately; repeated derivatives are not independent borrowing events or sound-correspondence attestations.

When uploading materials, update the platform's source description and other relevant source information in the same guarded publication. Infer the appropriate content and format from existing source descriptions: bibliographic identity and scope, separate source-item and reconciled-entry counts, an illustrative source page with its locator, how source information is represented, and what agents or inference algorithms added, with attribution. Derive counts from the reconciled register and describe actual published coverage and enrichment.

## Close each session

Save decisions and coverage centrally with a compact continuation: exact next action, changed record keys and unresolved limitations. Reference existing evidence instead of repeating findings or status dumps. Remove this session's disposable artifacts after verification; preserve originals, unique evidence, referenced snapshots, drafts and required receipts. Verify a retained identical copy and references before deleting a duplicate. See [guarded cleanup](references/offline-workspace.md#end-of-session-cleanup).
