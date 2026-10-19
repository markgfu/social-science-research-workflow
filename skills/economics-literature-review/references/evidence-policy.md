# Evidence Policy

## Evidence hierarchy

| Level | Meaning | Allowed use |
| --- | --- | --- |
| A | Verified full text with page, section, table, figure, appendix, or equation anchor | Core argument, model comparison, synthesis, draft |
| B | Verified formal abstract | Relevance screening and provisional description only |
| C | Metadata, search result, citation graph, repository page, or secondary mention | Discovery only |

An open PDF is not automatically level A. Level A requires that the relevant passage has actually been checked and anchored.

## Claim classes

- `SOURCE CLAIM`: explicitly stated by the paper.
- `CODEX INTERPRETATION`: a transparent reading of the paper's structure or mechanism.
- `CROSS-PAPER SYNTHESIS`: a comparison supported by multiple accepted notes.
- `OUR INFERENCE`: a project-level judgment, conjecture, or candidate extension.

Keep the label visible in notes or the Evidence Ledger whenever ambiguity is possible.

## Claims requiring full-text anchors

Models, assumptions, equations, propositions, mechanisms, theoretical contributions, datasets, parameters, empirical results, welfare conclusions, and limitations normally require level A evidence.

If the location cannot be supplied, write `needs-verification`. If the possible absence of literature has not been demonstrated by a documented search, write `needs-search` rather than calling it a gap.

## Acceptance gate

A paper can be `accepted` only when:

1. the canonical citekey and core metadata are present;
2. relevant full text has been checked;
3. model and result claims have page/section anchors;
4. inference labels are not mixed with author claims;
5. unresolved markers do not affect the proposed core use;
6. a human has reviewed the Literature Note.

The only automatic core-synthesis predicate is:

```text
status == accepted AND source_level == A
```

## Safe failure behavior

- Preserve uncertainty rather than guessing.
- Keep excluded records with an exclusion reason.
- Keep superseded records linked to the canonical record.
- Do not let citation counts substitute for relevance or evidence quality.
- Do not turn a missing search result into a novelty claim.
