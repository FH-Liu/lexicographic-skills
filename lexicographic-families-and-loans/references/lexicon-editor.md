# Current lexicon-editor relation adapter

Updated for the local implementation on 27 October 2026; source policies were gathered on 26 October. Recheck the current schema, provenance API and relation tools in the actual checkout before generating an import. This adapter does not authorize executing historical import scripts or modifying the live dictionary while researching.

## Three recording options from one search

The recording option is an offline decision, not a staging operation name. **word family membership** uses the family representation below. **merge entry formal variant** preserves same-lexeme alternatives in the retained entry's forms/`variants`, without the inflected subtype. **merge entry inflected form** retains the surface form in `variants` with `variantType: inflected`; preserve form-specific meaning in `usageNotes`, and add a supported `form-analysis` separately. Do not copy an inflectional translation into a new lexical sense automatically.

Form analysis uses `type: inflection`, exact target/base text snapshots and global native `formValueId`/`baseFormValueId`, unlike the owner-local `formId` on family endpoints. Record only supported features and segmentation; grammatical analysis may be warranted without established segment boundaries. Preserve source evidence and analytical provenance separately.

Inspect the current guarded merge capability before materializing an entry merge. Reconcile forms, senses, references, existing memberships and dependent analyses explicitly; a generic entry merge is not an inflection classifier. Preserve source identities through the central mappings and retain unaffected confidence. See the [import adapter](../../lexicographic-import/references/lexicon-editor.md) and the checkout's current provenance/staging contract. Do not invent a new operation name or bypass a capability gap with direct JSON edits.

## Families

Use `relationSetsVersion: 1` and `relationSets` of type `word-family`. `cognate-by-inheritance` is a separate relation-set type. Each member has an endpoint, assertion ID, provenance and its own `certainty`. Sets have no derivational direction/root endpoint, may overlap, and are not unioned by shared membership. Do not use the derived `conceptSets` as the authoritative family register; it is a projection of eligible reviewed memberships.

For new cross-variety cognate sets use `anchorMode: family-or-singleton`. Each membership selects an existing word family by `familyId` or an unaffiliated entry by `entryId`. The entry viewer follows its word families and the family viewer exposes their cognate sets. Record variant and sense witnesses offline. A family with multiple members requires a single cognate anchor. Legacy entry/form cognate memberships retain their original scope.

For a within-variety word family, a formal endpoint is `{entryId}` or `{entryId, formId}`. `formId` is an owner-local lexical/variant row ID, not a pronunciation/citation or metadata ID. A sense endpoint has `senseId` and cannot also have `formId`. Do not invent sense endpoints for formal family membership. Where formal membership applies to only some senses, preserve the restriction in membership commentary and in structured offline scope. The current `hi` memberships use this convention for air/vital energy versus laughter.

Use normal attributed membership operations/corrections; changing certainty must not manufacture a human review or erase prior review history. An omitted old certainty means `unspecified`; do not infer that checked means certain. Current user policy preserves unaffected certainty during mergers, superseding the archived reset-all rule.

## Loans

Use pairwise `relationEdges` with `type: loan`. In the usual representation the recipient is `source` and `directionality` is `source-borrowed-from-target`; use an existing exact donor endpoint when appropriate, otherwise `externalTarget`. Do not reverse the linguistic meaning because the field is called `source`.

Current fields:

| Field | Meaning and values |
|---|---|
| `loanLikelihood` | `certain`, `probable`, `possible`, `unlikely`, `unspecified` |
| `directionCertainty` | `certain` or `uncertain`; not the five-level likelihood scale |
| `externalTarget.language` / `.form` | Language label and optional donor spelling; unknown form may remain empty |
| `recipientScope` | Optional included/excluded recipient sense IDs and exact component form/text/code-point range |
| `donorRole` / `immediateDonor` | Related endpoint is `lexical-model`, `immediate-donor` or `unspecified`; a separate immediate donor is allowed for a lexical model |
| `furtherComments` | Specific linguistic insight, alternatives, or required scope; may be empty |
| provenance `sourceId`, `locator`, `commentary` | Actual intellectual attribution and genuine source reference; inferred LLM claims can have blank locator/commentary |

Do not revive `loanStatus`, attestation/elicitation or blanket checking fields. `Undetermined` is the documented unresolved-language placeholder. The schema now distinguishes a related lexical model from an immediate donor. Omission leaves this unspecified; it does not assert a direct route. Full intermediary chains remain offline with necessary concise public qualification. Do not treat certain direction as proof of direct borrowing.

The user confirmed member-level publication for the current platform. Translate each offline family proposal into the applicable member relations, deduplicating identical scoped claims and retaining evidence. Check every member, exact form anchors and member-specific donor model. Multiple constituent loans remain separate. Use `recipientScope.senseIds`, `excludedSenseIds` and/or `component:{formId,text,start,end}`. Offsets are zero-based Unicode code points, end-exclusive; the exact text must match a recipient lexical/variant row. Included and excluded senses must be distinct recipient senses. Absent included senses means all except exclusions; absent component means the whole selected form/entry. Scope follows the proposed recipient even when direction is uncertain. The editor supplies an “Edit loan scope” action with component occurrence selection. Keep comments only for insight or restrictions the structured fields cannot express. No historical prose is automatically reinterpreted.

The offline register's `scope`, `analysis`, `evidence`, `loanScreening` and `sourceIssues` fields are **not live API fields**. Never submit the offline family extension directly to the live API. Materialize a detached schema-valid candidate through the provenance operations and established protected save route.

## Provenance, comments and publication

### Engkebatu source loans

User decision, 12 November 2026: preserve Engkebatu's original Dagur loan assertions and bibliographic provenance as source claims in the eventual live dictionary. Select them through assertion metadata and provenance events (`sourceId: engkebatu-1984`), not relation-ID spelling. Read `directionality` to identify the recipient; for `target-borrowed-from-source`, it is `target`.

Keep the existing relation and assertion identities, source endpoint restrictions, donor, confidence and direction. Record an analyst's disagreement, alternate interpretation, or narrower component assessment as a concise attributed comment on that assertion. Do not retire/supersede it, modify its substantive fields, or add another relation merely to publish the analyst's different assessment. Earlier offline dispositions saying “replace”, “reject” or “retire” remain analytical history and do not authorize those live operations. Do not manufacture a human review. Exact agreements reuse the source assertion; genuinely new borrowed-base claims on uncovered members/constituents remain eligible under the ordinary workflow after deduplication.

Distinguish digital errors from source errors by checking the printed witness. If the source is right and OCR/transcription is wrong, simply correct the digitisation to match it; add no live note about the OCR mistake. If the error is present in the printed source itself, correct the supported error with a concise note identifying the old/new reading and uncertainty where appropriate. Both use the exact-value guarded correction route, preserve bibliographic attribution and original correction history, and retain one claim rather than adding a competing relation for the corrected spelling. A spelling correction is not a new etymological rejection. Do not “repair” a substantive linguistic disagreement as an OCR error.

Before publication, verify every protected source assertion and its mapped endpoints against the fresh saved revision. Permit only the specifically recorded spelling corrections and necessary identity remappings; verify concise comments and unchanged source provenance. The existing relation, provenance, commentary and history structures suffice. Keep preparation offline until corpus completion.

Attribute new analyses to `llm` when that is their actual origin; Dorji and other books support recipient forms/meanings, not unprinted etymologies. Keep human corrections/decisions attributed truthfully. New inference does not create independent editorial review.

Retain comments such as “only the 水 component; the cement and crystal members have distinct full Chinese models” when needed. Omit comments merely restating donor, certainty, “obvious international loan,” “matches form and meaning,” a bare earlier-stratum label, or generic family-propagation disclaimers. Put the general borrowed-base semantics in project documentation once. Keep detailed method, hashes, artifact paths and superseded proposals offline; preserve real linguistic restrictions and bibliographic evidence.

After both passes over the whole corpus, compare to the fresh live revision and existing claims. Build a deterministic detached delta/candidate, validate schema/references, preserved unrelated content/provenance, exact endpoints, conflicts, scoped member coverage and required JSON/LIFT interchange. Save with the expected revision, backup and read-back. Historical receipts identify completed imports; never replay them. A stale candidate must be rebuilt, not relabelled with a new revision. This editor saves a complete project, so chunking operations does not remove whole-project memory/payload limits; assess capacity before final publication.

Implemented locally: the SQLite offline register, transactional supersessions/dependency checks, scope and donor-role fields, attributed staged sets/member updates, guarded assertion corrections and read-only conflict preview. Read `workflows/OFFLINE_WORK.md` in the checkout. These fields survive editor JSON/LIFT round trips; another LIFT consumer may ignore the archive/extension and lose scope, so test representative target interchange or use a lossless adapter/sidecar. Family-level borrowed-base assertions remain a future design; retain scoped member publication as the user requested. Do not redesign the platform during routine analysis.
