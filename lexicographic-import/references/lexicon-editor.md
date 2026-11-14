# Adapter: FH-Liu/lexicon-editor

Updated for the local implementation on 27 October 2026; source policies were gathered on 26 October. Locate the checkout and read current `schema/PROVENANCE.md`, `schema/dictionary-v2.schema.json`, `ARCHITECTURE.md` and `workflows/shared/instructions/PROVENANCE_IMPORTS.md` before preparing executable staging. The former `CacinieP/lexicon-editor` remote resolves to private `FH-Liu/lexicon-editor`. This is a browser editor with a local Python persistence server and whole-project saves; do not assume a public hosted API.

## Representation

- Schema 2 has explicit source/editor registries and stable assertion/value identities. Entries contain senses/examples; `parentEntryId` organizes subentries. Preserve IDs and avoid unsupported live fields.
- Repeatable forms/definitions have value-level attribution. A formal endpoint's `formId` is an owner-local lexical/variant row ID, not its metadata `valueId`, citation or pronunciation ID.
- With `dialectScopeVersion: 1`, the entry has only its top-level variety. Lower dialect labels belong on supported forms, senses or examples. Do not emit `entry.dialects`; retain qualified Dular paths.
- Current Oroqen taxonomy (user, 8–9 November 2026). Heilongjiang contains Birarqen and Kumarqen. Inner Mongolia contains Toqen, Dobkorqen, Nanmu 楠木, and Gaanqen. Gaanqen contains Chaoyang and Gankui 甘奎. Use `domain.js` for current paths and stable node values. Preserve existing Gaanqen/Chaoyang identities and provenance. Assign Gankui and Nanmu only where source evidence supports the respective dialect. The central `mapping:oroqen-taxonomy-current` records this revision. Historical source snapshots do not override it; rebuild affected publication candidates and rerun protected verification under the current rules.
- Import execution generates no citations, POS, pronunciation, RTR, translations, donors or domains. Stage exact intended strings and explicitly approved preparation inferences. Contextual NFC equality does not authorize transliteration or merging owners.
- Families and inherited cognates use `relationSets`; each membership has separate provenance and certainty. Loans, equivalence and see-relations are pairwise. Equivalence binds actual senses. Do not revive pairwise family edges.
- Review, attribution and linguistic certainty are separate. Agent processing is not an LF check. Changed evidence may invalidate prior review coverage without erasing its history.
- The unified search's three recording options map to word-family membership, same-lexeme formal variants, or `variants` with `variantType: inflected`. Inflected forms retain source meaning in `usageNotes`; supported grammatical analysis uses the independently attributed `form-analysis` operation. Analysis target/base references are global native value IDs, distinct from owner-local family endpoint row IDs. Read the [analytical adapter](../../lexicographic-families-and-loans/references/lexicon-editor.md) before materializing these decisions. A merge must preserve source mappings and rebind affected references and analyses explicitly.

## Final staging and save

Use a new version-2 staging ID, current `baseRevision`, actor/source IDs, truthful preparation timestamp and ordered operations. Supported operations include `entry`, `sense`, `example`, `value`, `slot`, `evidence`, `relation`, `relation-set`, `set-member` and guarded `correct-assertion`; staging keys can reference previously declared objects. Container operations are not arbitrary repeatable-value inserts. Register sources explicitly.

Dictionary contributions need real locators, normally compact `locator.freeText`. LLM translations use `llm` with the dictionary as supporting evidence. LLM analyses may legitimately have blank locator/commentary. Do not fabricate a bibliography or local artifact citation to satisfy an importer.

Corrections/merges require supported capabilities, exact target guards and a signed explanation. A routine `slot` does not overwrite populated content. Preserve source history and unrelated content through the provenance API; do not rewrite metadata directly or replay saved batches.

At final publication, from the checkout root, use a new prefix:

```sh
python3 workflows/shared/scripts/run_provenance_batch.py prepare <new-prefix> --staging <final-staging.json>
python3 workflows/shared/scripts/run_provenance_batch.py verify <new-prefix>
python3 workflows/shared/scripts/run_provenance_batch.py save <new-prefix>
```

These are conditional final-publication commands, not instructions to execute while merely planning. `prepare --project <copy.json>` supports an isolated baseline. Verification currently reconstructs deterministically, checks schema/references, exact JSON/browser LIFT round trips and the official LIFT schema, then binds artifacts and rules. Save requires current verification, unchanged baseline, backup and read-back. Retain required tool dependencies for that final gate.

The generic runner now supports attributed family sets, members, scoped loans and expected-value-guarded assertion corrections. `scripts/preview_provenance_batch.cjs BASELINE STAGING` gives an in-memory conflict preview before final preparation. Read `workflows/OFFLINE_WORK.md` for the register and staging contracts. Inspect support for any additional custom operation; historical relation tools used detached candidates and the provenance API. Inspect any reused script for hard-coded paths and side effects. Do not execute old scripts against current data merely because they once worked.

File import replaces the project: combine preserved baseline content with the reconciled delta. Browser drafts can contain unsaved work beyond saved JSON; reconcile that state at publication. Revision conflict requires a fresh baseline and regenerated candidate.

## Practical limits

Keep real source/contributor/producer attribution and bibliographic references live. OCR receipts, hashes, local paths, reconciliation history and routine ingestion narratives belong offline. The latest comment cleanup supersedes older routine-method commentary requirements. Honor mechanically required API fields without injecting user-facing boilerplate.

Estimate whole-corpus size from representative records and test detached loading/export early. Inspect actual payload size and current server configuration; historical page counts or size limits do not prove usability. Splitting final operations into chunks does not solve a limit on the complete saved project: this editor still saves whole-project candidates. If the completed project exceeds capacity, resolve configuration/storage fit before publication rather than truncating content or bypassing safeguards.

LIFT self-round-trip success establishes preservation within this editor, not interchange with every external tool. For another target, test representative target import/export or state the limitation.
