# Unified lexical search, followed by loan analysis

## Central analytical records

Use the existing canonical store when available. A new store can have immutable lexical inputs, current families, scoped rejections, loans, patterns and compact coverage/progress tables. Store semantic decisions once; reports and viewers are projections. Suggested analytical fields are an **offline contract**, not accepted live API fields:

| Record | Minimum useful content |
|---|---|
| Corpus manifest | Input hashes/revision, inclusion rules, varieties, source IDs, count units, family-policy version |
| Family | Stable family ID, root hypothesis, exact entry/form memberships, per-membership confidence, evidence/scope |
| Unified candidate/decision | Stable exact endpoints, retrieval routes, accepted recording option or rejection, evidence/confidence, scope and input revisions; retained/merged entry IDs or base/inflected form IDs as applicable |
| Consolidation mapping | Every source occurrence and former entry/form/sense ID → retained identity; formal-variant versus inflected-form role, preserved meanings/locators, affected references and explicit supersessions |
| Rejection | Unordered exact endpoints, current decision, concise material reason, evidence revision and reopening trigger where useful |
| Loan proposal | Stable proposal/group IDs, family revision, recipient scope, donor language/form if known, likelihood, direction assessment, route qualification, actual author/evidence |
| Pattern | Stable ID, variation or construction type, variety/context/function, operation, examples, independent-root support, limitations/counterexamples |
| Progress | Stage, frozen queue ID/hash, completed/remaining exact scopes, next action; local preparation and publication separately |

Use stable family IDs instead of array positions or labels such as F52. Preserve exact form anchors. Entry-wide judgments and selected-form judgments differ; do not narrow an old entry-wide decision to evade a conflict. A single-form entry may resolve to its one form; multiple alternatives require inspection. If senses delimit a formal hypothesis, retain that restriction even when the platform's endpoint is formal.

## Local analysis of nested source groups

After verifying a complete source group, including continuations across pages, use its structure as an early route in the same unified search:

1. Preserve source parentage, order and sense attachment separately from analysis. Distinguish independent lexemes, forms of a lexeme, lexicalized expressions and usage examples using the source's conventions and the actual content.
2. Compare relevant parent/child, sibling and ancestor forms, explicit reference targets and supported compound constituents for identity, inflection and common-root membership together. Nesting is candidate evidence, not a linguistic conclusion; avoid an indiscriminate Cartesian product.
3. Anchor example occurrences to their exact token/span and relevant form/sense. Keep the whole example and translation; an unchanged occurrence needs an attestation link, and a grammatical realization may need inflectional analysis. Neither requires inventing an entry for the sentence, a duplicate variant, an unattested base or unsupported segmentation. Sense attachment and attestation are not forced into the three lexical-comparison outcomes.
4. Save warranted decisions, scoped rejections and dependencies under their existing stable keys, then cover the `source-structure` route for the group. Missing external targets remain ordinary pending candidates until available; retain usable local judgments. Reuse unchanged decisions globally, repeat only affected work when inputs change, and still complete all other declared routes. Perform singleton review and loan screening only at the corpus-wide boundaries.

The planned register permits early `phase: family` records during import after checking their source dependencies. It expands group dependencies and coverage automatically from source-parent links; use the contract in `workflows/OFFLINE_WORK.md`, without separate local inventories, reports or completion receipts.

## Unified retrieval and adjudication

1. Index current forms, source meanings, pronunciations, grammatical features, identity mappings, family membership and scoped rejections. Resume interrupted frozen queues. Consolidation, family discovery and inflection detection share one queue and evidence review. Skip unchanged decided scopes; reopen only for new evidence or an explicit reassessment. A prior family-only decision does not certify that identity and inflection were examined.
2. Prioritize entries absent from families without excluding variant/inflection candidates already in families. Retrieve exact/variant matches, inflectional paradigms, derivational extensions, sound/spelling patterns, semantic leads and references. Include supported stem alternation, not only suffix stripping. Search internal roots as well as prefixes. Apply regex to parsed form strings, never raw JSON. Escape literal material. Keep case/NFC keys distinct from stored spellings; retain length, gemination and quality contrasts.
3. Freeze a manageable candidate queue with stable endpoints and retrieval routes. The old Dorji soft limit of 20,000 entry pairs was a session workload convention, not a quality target; size new queues to realistic completion capacity. Do not pad them or restart alphabetically after every session. Local queue boundaries do not permit intermediate uploads.
4. Review full evidence and all affected entries/families once. Choose **word family membership**, **merge entry formal variant**, or **merge entry inflected form** for an accepted comparison, or reject unsupported hypotheses. Establish lexical identity and grammatical function before choosing a merge. Common-root evidence supports family membership without necessarily supporting identity. An inflection expresses a grammatical distinction of the same lexeme; derivation or lexicalization can warrant a separate lexeme. Use semantic plausibility to evaluate the proposed analysis, not to invent a story explaining any shared string. Missing data can lower confidence; it is not automatically acceptance or rejection.
5. Register every actual rejection at its proper scope, including those made during group review. Do not generate a Cartesian product of supposed rejections between two groups without adjudicating those comparisons. One accepted form pair does not close other form pairs automatically.
6. Inspect the prospective family as a whole for homonyms, incompatible roots and active conflicting rejections. Resolve actual conflicts explicitly. Overlapping families can represent separate compound components or disjoint analyses; overlap is not an instruction to union them.
7. Save decisions atomically or transactionally, validate changed dependencies and keep one recovery path. For merges retain every original source key, surviving entry/form/sense mapping, exact forms, locators and grammatical/source meanings. Record supported inflection features and base evidence separately from lexical senses. Rebind affected family memberships, references and pending endpoints; resolve conflicts and retain unaffected confidence. Do not silently treat a retired endpoint as a new comparison. Refresh unassigned priority without dropping still-undecided queue scopes. Derive yield/coverage from current decisions, not scratch counts.

The three recording options classify accepted lexical comparisons; rejection and unprocessed are statuses. Retain which hypothesis a rejection addresses: rejecting a merge must not suppress a supported family membership. A consolidated lexeme may separately belong to a family with other lexemes, but do not create duplicate memberships merely to record its internal inflection. Keep proposed merges outside authorized scope explicit offline, without applying them. If a base is unattested or identity unresolved, retain the supported analysis without fabricating an entry or forcing consolidation.

Use explicit compound information as evidence when available, preserving the whole source word. Do not demand a fully attested free base or completed segmentation. Never infer that two words are relatives merely because they share one grammatical affix.

## Confidence calibration

| Level | Membership interpretation | Loan interpretation |
|---|---|---|
| certain | Common root is clear and strongly supported | Proposed lexical-source relationship is convincing |
| probable | Persuasive analysis with a material uncertainty | Good loan identification with a material form, meaning or source-language qualification |
| possible | Credible hypothesis with substantial uncertainty | Plausible proposal with important unresolved correspondence/donor identification |
| unlikely | Weak but still warranted retained hypothesis | Recorded comparison assessed negatively when useful to preserve |
| unspecified | No assessment supplied, often legacy | Source/legacy assertion supplies no assessment |

These are qualitative linguistic judgments, not probabilities, human-review statuses or evidence types. Documentary proof is not required for `certain`. Assign both memberships in a new family; a new member can differ from existing members. Preserve unaffected assessments in a merger; reassess any membership whose hypothesized root or scope changes. Do not reset all memberships to `unspecified` or invent certainty for legacy records.

Reject mere conceivable resemblance rather than retaining it as `unlikely`. Do not create held/provisional-admission categories for completed judgments. Keep unprocessed work distinct from rejected comparisons. Reopening a rejection should be an evidenced change, not repeated indecision.

## Pattern induction without circular reinforcement

Record variation separately from affix/construction hypotheses. Spelling variation does not automatically establish phonetic variation; inspect actually linked pronunciations. Store conditions and source evidence rather than global substitutions.

The recovered Dorji convention calls a pattern `limited` below five independent root paradigms and `robust` at five, recording “at least five”; exhaustive counting is unnecessary. Count a root once despite derivatives, senses, alternate spellings and repeated sources. Separate unassigned entries are not automatically separate roots. A construction needs evidence for its function, not just repeated suffix letters.

Limited patterns can retrieve candidates and inform judgments. Reduce confidence when materially dependent on weak evidence, without a mechanical downgrade. A robust parent pattern cannot confer robustness on a weak branch. Preserve counterexamples and revise support after family changes. Do not count a candidate accepted solely through the pattern as fresh independent proof of that pattern.

For another corpus, choose an appropriate robustness convention and document it; do not confuse this local five-root bookkeeping threshold with a universal linguistic law.

## Loans after the family pass

Screen all accepted families and the singleton complement of the consolidated lexeme inventory. Source rows absorbed into formal variants or inflected forms retain coverage through their identity mappings; they are not additional singleton lexemes or independent-root evidence. A group representative is a retrieval aid; inspect all members of a proposed loan family. Start with recipient form–meaning pairs from their own source, identifying fallback sources explicitly.

Consider whole sound shape, meaning, plausible adaptation, recipient morphology, contact history and competing source languages. Contact plausibility cannot replace a lexical match. Search regional/older donor vocabulary rather than only translating the gloss back. Separate uncertain morphology provisionally; do not cut off lexical consonants solely to improve a match.

Record three distinguishable claims: borrowing in general, a proposed lexical source/donor, and route/direction. For example, a European-looking internationalism can be clearly borrowed while a Russian-specific attribution remains only probable. A donor dictionary corroborates spelling/meaning, not the historical borrowing event. A recognized remote lexical model does not establish the immediate donor language.

When the actual donor is unknown, leave its form blank and assess what can be supported. In the current editor, `Undetermined` is a documented placeholder, not a real language. Do not repeat its definition in each comment. Ordinary source-language competition affects that language-specific claim even if borrowing itself is obvious.

For family propagation, retain `appliesToEntryIds`, component restrictions, member-specific full donor models and excluded senses offline. Verify every applicable member and represent exceptions explicitly. A shared borrowed component does not imply that it entered as a free word. A loan to one alternative is not a loan to every alternative in the entry. Do not multiply independent-root evidence by materialized member relation counts.

If the loan analysis reveals an incoherent family, create a concrete family correction, settle the affected analysis, then regenerate only dependent loans. This is an internal return to the first pass, not a new indefinite hold queue. Preserve unchanged decisions. Record source-reading problems separately without withholding all usable analysis or silently correcting source data.

## Completion and useful reporting

The user-confirmed stopping rule is coverage of all inventory entries through the declared applicable search routes, resolution of their generated candidates and one final review of remaining singleton lexemes after consolidation. Include formal-variant and inflection routes in that same search. Resolve candidates arising from the singleton review and update the resulting inventory, then close the first pass. Record the routes, input/pattern revisions, unavailable evidence and actual outcome; repeat affected searches when material evidence changes. When the search yields reusable patterns, present the option of a second pass focused on items still lacking the relation, unless that pass has already been requested. Count distinct new supported relations and newly matched items for each comparison in every pass. If the second pass still produces substantial gains, show the yields and ask whether to continue with successive passes until returns diminish sharply. Carry out previously authorized passes directly. Freeze the cumulative results at the start of each pass, revisit unlinked items against the full comparison inventory, and test new patterns against independent examples and counterexamples. Assess the drop in yield in light of the coverage and remaining evidence routes. Record the stopping rationale alongside positive and zero-gain rounds. This establishes agreed coverage, not exhaustive discovery; a queue limit or a filled family quota does not establish corpus completion.

Every reviewed family/singleton has `registered`, `no-proposal`, or a concrete unresolved scope/source issue recorded separately. `No-proposal` is a screening outcome, not a claim of native origin or exhaustive etymological clearance. A concrete unresolved publication issue can remain disclosed without disguising it as linguistic uncertainty.

Report queued scopes resolved, actual rejections, new memberships, formal-variant merges, inflected-form merges, surviving lexemes, family mergers, pattern updates, group proposals and live relations separately. Counts of resumed work must not be repeated; aggregate yield uses aggregate numerator/denominator. No holds, high family coverage or exhaustion of one retrieval queue proves exhaustive discovery. State the retrieval routes and corpus coverage actually completed.

Keep source evidence, reusable patterns, canonical decisions, frozen queues needed for reproducibility and compact continuation. Remove disposable indexes and temporary copies after successful read-back, but do not blindly copy an old “delete every temporary file” rule when a file is the only surviving evidence or recovery record.
