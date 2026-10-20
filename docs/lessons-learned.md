# Engineering Lessons Learned

## Deterministic finance must remain authoritative

Generative models are useful for explanation and intent handling, but base financial calculations, ranking positions and source provenance should remain explicit and reproducible.

## Cross-country data is not automatically comparable

Similar metric names can hide different source conventions, reporting periods or evidence quality. Country context must remain part of the data contract.

## Provenance belongs in the architecture

When spreadsheets, PDFs and document extraction all feed one analytical system, the source of a value must be recoverable. Provenance cannot be added as an afterthought.

## Report completeness is part of correctness

A result can be numerically correct but operationally wrong if a long ranking, multi-year comparison or exported report silently truncates data. Rendering/export completeness needs regression coverage.

## AI output needs scope guards

Narrative generation should be constrained by known entities, requested years, metric definitions and evidence boundaries. This reduces confident but unsupported output.

## Production data and portfolio proof must be separated

A strong public case study does not require copying private datasets or implementation source. Architecture, validation methodology and engineering decisions can demonstrate capability safely.

## Artifact recovery needs authority checks

Historical inputs or delivery artifacts should only be reintroduced when their provenance, relevance, confidentiality and supersession status are understood. Public case studies should never ingest recovered private artifacts directly.
