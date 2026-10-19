---
name: economics-literature-review
description: Run auditable economics literature reviews centered on model lineages, benchmark assumptions, mechanisms, and marginal theoretical extensions. Use for economics-paper discovery, screening, PDF-grounded extraction, Zotero/Obsidian synthesis, literature-review drafting, or claim-evidence auditing. For prose-only polishing after the evidence set is fixed, use research-paper-writing instead.
---

# Economics Literature Review

Build a review whose claims can be traced from the draft back to accepted full-text evidence. Organize theory papers by model lineage and changed assumptions, not as a chronological citation list.

## Non-negotiables

- Zotero items and verified PDFs are the factual source of truth; never edit `zotero.sqlite`.
- Browser snippets and search metadata discover papers but do not establish models, assumptions, propositions, mechanisms, or results.
- Distinguish `SOURCE CLAIM`, `CODEX INTERPRETATION`, `CROSS-PAPER SYNTHESIS`, and `OUR INFERENCE`.
- Mark unsupported details `needs-verification`; do not fill them from memory or another paper's description.
- Do not delete or overwrite human notes without an explicit request.
- Only notes with `status: accepted` and `source_level: A` may support the core synthesis or draft.
- Preserve the sequence `source -> literature note -> human review -> lineage -> synthesis -> draft`.

Read [references/evidence-policy.md](references/evidence-policy.md) whenever classifying evidence, accepting a paper, or drafting a substantive claim.

## Stage routing

1. Scope: lock the working question, inclusion criteria, taxonomy, databases, languages, and date bounds.
2. Discovery: record exact queries and export metadata as evidence level C.
3. Screening: record inclusion/exclusion decisions and reasons; do not silently discard records.
4. Acquisition: use open access, an authorized institutional browser session, or user-provided files; log the route.
5. Extraction: create one canonical Literature Note per citekey with page/section anchors.
6. Human review: wait for human acceptance before promoting evidence.
7. Lineage: map predecessor, baseline, changed assumption, new variable, mechanism, and result.
8. Synthesis: compare lineages and separate a verified gap from `needs-search`.
9. Draft and audit: draft by argument, then verify every major claim against accepted evidence.

For stages 1-7, read [references/workflow.md](references/workflow.md). For stages 8-9, read [references/writing.md](references/writing.md).

## Durable artifacts

Prefer small, recoverable files over chat-only state:

- exact search runs and candidate exports;
- a canonical source manifest;
- one Literature Note per citekey;
- lineage and synthesis tables;
- review status and claim-evidence ledgers;
- audit reports that report problems but never auto-repair academic content.

Process small batches: normally 3-5 short papers or 1-2 long papers. A completed AI pass moves work to `waiting-review`, not `accepted`.

## Shared author standard

For literature synthesis, drafting, and revision, first read the companion workflow's [author-judgment and evidence standard](../social-science-research-workflow/references/author-judgment-writing.md). Preserve it during the writing handoff; it takes precedence over generic paragraph templates in the references.

## Writing handoff

Use [research-paper-writing](../research-paper-writing/SKILL.md) only after the evidence gate is satisfied. Retain its useful constraints—one message per paragraph, a clear main point placed where the argument needs it, reverse outlining, skeptical self-review, and claim-evidence mapping—but replace ML-specific framing with economics concepts such as assumptions, equilibrium, welfare, comparative statics, and institutional setting.

## Completion contract

Report:

1. artifacts created or updated;
2. papers and claims processed;
3. evidence levels and unresolved verification markers;
4. gate status (`pass`, `waiting-review`, or `blocked`);
5. the smallest safe next step.
