# Evidence and policy lineage

Distilled from the local lexicography workspace and its private GitHub repository, 26–27 October 2026. These skill files are reusable guidance; original sources and exact retrieval/hash manifests remain in the repository's `workflows/skill-distillation/20261026/` collection. The complete instruction sheets are evidence, not a requirement to reload all historical material for every task.

## Authority and supersession

Use the current user's task and decisions first, then applicable current source/platform contracts. Historical policy is useful for explaining existing data, not for silently overriding current instructions. Existing user edits and untracked working sheets can be newer than remote HEAD; compare content and explicit supersession statements rather than assuming Git chronology determines authority.

The user confirmed in the distillation conversation:

1. Finish the **whole dictionary or corpus offline before any upload**.
2. `Certain` retains its linguistic-confidence meaning; evidence and editorial review are separate.
3. Publish scoped member loan relations on the current platform; family-level assertions are an improvement proposal.
4. Preserve unaffected membership confidence during family mergers and reassess changed interpretations.
5. Use available compound-origin evidence without making complete segmentation a prerequisite or expanding to phrases.
6. Complete declared search routes across all entries, resolve their candidates, then review remaining singletons once. Resolve candidates from that review and close the family pass; repeated full recall until a no-additions pass is not required.

These override past per-batch upload, merger confidence reset and ignore-compound instructions. They do not authorize data changes in existing published records merely because a new skill has been written.

## Main sources

| Source | Contribution and limits |
|---|---|
| [Schema-2 provenance contract](https://github.com/FH-Liu/lexicon-editor/blob/04a57849dfdf7c935e86aa983dd93f2aba456828/schema/PROVENANCE.md) and [staging contract](https://github.com/FH-Liu/lexicon-editor/blob/04a57849dfdf7c935e86aa983dd93f2aba456828/workflows/shared/instructions/PROVENANCE_IMPORTS.md) | Explicit attribution, stable identities, scopes, sets and protected saving. Recheck actual current code before execution. |
| Local `workflows/hu2001/instructions/HU2001_INSTRUCTIONS.md` | Hu source/citation conventions and legacy practices explicitly superseded by schema 2. |
| Local `workflows/engkebatu/instructions/ENGKEBATU_IMPORT_INSTRUCTIONS.md` | Scan, Unicode, reference, homonym and source-specific decisions; historical two-page upload procedure is superseded here. |
| Local `workflows/dorji/instructions/DORJI_IMPORT_INSTRUCTIONS.md` and `workflows/dorji/reports/EHAN_IMPORT_ASSESSMENT.md` | Source/model fit, independent printed IPA, labels, domain mapping, missing POS and source-faithful extraction. The assessment is a proposal; the later instruction sheet governs actual policy. |
| [Historical Delkir instructions](https://github.com/FH-Liu/lexicon-editor/blob/171442daa328ead6050bdd3b852703827925aace/workflows/delkir/instructions/DELKIR_IMPORT_INSTRUCTIONS.md) | Digital source IDs, allowed fields, exact locators and authorized Dular reconciliation. Entry dialects and pairwise family transport are superseded. |
| [Historical family definition](https://github.com/FH-Liu/lexicon-editor/blob/4e265089/workflows/relations/dorji-families/FAMILY-DEFINITION.md) | Common morphological base, whole-family review and opposition to semantic-only splitting. Its hold policy is obsolete. |
| [Final family recovery release](https://github.com/FH-Liu/lexicon-editor/releases/tag/dorji-word-families-complete-20261026), member `workflows/relations/INSTRUCTIONS.md` | Acceptance/rejection with membership confidence, exact scope, frozen queues, induced patterns, independent-root counting and concise bookkeeping. Current user decisions amend compound handling and merger confidence. |
| Same release, `workflows/relations/dorji-families/search/patterns/README.md` | Limited/robust pattern inventory; five independent roots is a local replication convention, not a universal evidential law. |
| Local `workflows/relations/runs/held-cases-uncertainty-report.md` and `resolution-report-20261026.md` | Backlog diagnosis, direct user decisions and recorded outcomes. They do not provide a new source-page audit of every historical comparison. |
| Local `workflows/loan-detection/dorji-loan-detection-instructions.md`, Chinese/Russian pattern sheets and `dorji/loan-source-issues.md` | Latest member propagation, confidence, source pairing, competing donors, concise-comment policy and later family corrections. Some are uncommitted local developments beyond remote HEAD. |
| [Historical Nonni patterns](https://github.com/FH-Liu/lexicon-editor/blob/171442daa328ead6050bdd3b852703827925aace/workflows/nonni-loans/instructions/nonni-chinese-loan-patterns.md) | Comparative retrieval leads; later changes supersede old held lists and repetitive comment rules. |

Project etymologies cited in examples remain attributed historical analyses. Collecting their instruction sheets does not independently establish the etymologies, inspect every printed page or certify every database record.

## Deliberate new recommendations

Use one offline canonical store with stable identifiers and derived reports; perform incremental checks while working and the required full platform checks at final publication. Keep provenance structured and comments selective. Propose explicit machine-readable component/sense/route scope and family-level loan storage where useful, without claiming the current editor implements them. Keep confidence separate from review and preserve useful evidence without multiplying full snapshots or routine per-value workflow notes.

At initial distillation, the workspace layout, record contract and validation cadence were workflow recommendations. The 27 October follow-up below implements the central register and platform features. No performance benchmark is claimed, and existing final save gates remain in force.

## Implementation follow-up, 27 October 2026

The user subsequently authorized implementing the report recommendations. The checkout now contains the central SQLite register, scoped member-loan/donor-role fields, attributed relation staging and conflict preview, with usage in `workflows/OFFLINE_WORK.md`. Both skills explicitly require end-of-session disposal of temporary/redundant materials and logs after durable work is saved. Historical source snapshots remain unchanged. Family-level publication remains deferred under the confirmed member-level policy.

## Current user revision, 9 November 2026

Use one search for consolidation, word-family detection and inflection detection. Accepted recording options are **word family membership**, **merge entry formal variant**, and **merge entry inflected form**. Rejections remain statuses. Finish the combined search and singleton review before requested loan screening; preserve source mappings after consolidation.

Keep reusable symbol guidance general and detailed source conventions in their workflow registers. Future imports expand **`ʧ → tʃ`, `ʤ → dʒ`, and `ʦ → ts`**, and normalize **`γ → ɣ`** as general transcription rules across sources, superseding older source-specific preservation of those input symbols. These are prospective import rules, not authorization to rewrite completed dictionaries.
