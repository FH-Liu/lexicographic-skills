# Central offline workspace

Use one project-owned run directory, for example `workflows/offline/<corpus-id>/`. Reuse a suitable existing register. A practical layout is:

```text
manifest.json       source hashes, scope, policy/schema versions, baseline
sources/            immutable originals or references to retained originals
records.jsonl       reviewed source records; raw evidence remains recoverable
mapping.jsonl       source keys → entry/sense/form/value identities
decisions.jsonl     decisions and explicit supersessions
coverage.json       prepared, excluded, unresolved and published coverage
issues.jsonl        source/mapping issues and dependencies
evidence/          crops or locators, OCR, exceptional-reading evidence
release/           final delta, candidate, checks and publication receipt
```

The current lexicon-editor checkout provides `scripts/offline_workspace.py`, a standard-library SQLite register for indexed transactions, supersessions, dependency invalidation, coverage, resume state and deterministic final staging. Read `workflows/OFFLINE_WORK.md` in that checkout for the CLI and exact action contracts. Reuse an existing suitable central register; JSON/JSONL remains sufficient where already supported. Keep one authoritative representation and generate reports/views. Do not maintain independently editable CSV, JSON, HTML and live copies. Back up the central store; offline work must not exist only in chat memory.

## Minimum contracts

A source record needs a stable key, edition/source ID, real printed locator, precise evidence location, literal text/structure, reviewed reading, variety scope and attribution. Distinguish assigned keys from printed entry numbers. Preserve original/resolved references. Distinguish absent/unknown from unprocessed.

A decision needs a stable ID, exact endpoint/value scope, action, evidence actually used, confidence where applicable, actual author/method and decision time, and optional superseded decision ID. Derive the current projection from those records. Keep enough history to explain a change without making a full-project snapshot per micro-edit or copying superseded proposals into live remarks.

The manifest records source identities, extraction/mapping policy, scope, completion criteria and publication state. Workflow states such as `draft`, `ready`, `publishing`, `published`, `failed` are not confidence or human-review states. Record publication state by package/chunk so interrupted uploads can resume safely.

## Check frequency

| Boundary | Checks |
|---|---|
| Intake | Source/page inventory, schema capability, representative detached pilot |
| Local change | Record validity and affected identities/references |
| End of extraction/analysis | Full coverage, mappings, unresolved references, dependency consistency |
| Final candidate | Platform-required checks bound to exact baseline, candidate and rule hashes |
| Publication | Protected save, receipt and read-back reconciliation |

Bind reusable checks to input, source and rule fingerprints. Changed mappings or validation rules warrant broader checks; ordinary judgments need affected-scope checks. Preserve historical verification at its recorded revisions, with one current verification view. Do not refresh historical totals or bypass stale-input and publication guards. The executable loan helpers and their packet contracts are documented in `workflows/OFFLINE_WORK.md`.

The confirmed publication boundary is the **whole dictionary/corpus**. Local milestones are recovery checkpoints only. On interruption, save the exact next position and outstanding dependencies centrally and resume without uploading the partial corpus.

## End-of-session cleanup

After saving durable work and the resume cursor, delete temporary or redundant materials and logs from the session. Keep unique source evidence, current records and deliverables, and necessary provenance/recovery/publication receipts. Treat OCR/crops as evidence when they are the only retained support for a reading. Preserve other agents’/users’ changes and unsaved editor drafts.

The current checkout offers `offline_workspace.py RUN disposable FILE --session ID`, followed by `cleanup --session ID` (preview) and `cleanup --session ID --apply`. It deletes only registered, unchanged regular files under `RUN/.scratch/` and rejects symlinks. Required evidence must never be registered as disposable. Outside scratch, inspect exact paths, verify identical retained canonical copies, and check/update references before deleting redundancy. Do not sweep the repository or shared temporary/cache directories.

Remove successful-test artifacts and regenerable previews; retain only compact actionable failure evidence while unresolved. Keep a brief count/bytes summary if useful, not a new verbose cleanup log. The repository test runner now removes its own temporary output after success unless diagnostic retention is explicitly requested.
