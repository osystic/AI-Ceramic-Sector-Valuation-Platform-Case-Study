# Case Study

## Challenge

The engagement required a production platform that could transform heterogeneous ceramic-sector financial material into consistent analytical outputs across multiple companies, years and countries.

The core engineering problem was broader than a conventional dashboard. The system needed to ingest structured and document-based evidence, calculate comparable financial metrics, support ranking and benchmarking, answer both structured and free-text questions, generate multilingual reports, and remain reproducible enough for production maintenance.

At the same time, deterministic financial logic had to remain distinct from generative AI. Ranking behavior, metric calculations and data provenance could not depend on unconstrained language-model output.

## Solution

OSYSTIC implemented a layered analytical platform with five major boundaries:

1. **Ingestion and provenance** — controlled loading of spreadsheets, PDFs, CSV/tabular files and reference documents.
2. **Normalized analytical model** — company, country, year and metric context is converted into consistent internal contracts.
3. **Deterministic finance layer** — ratios, rankings, screening and comparison logic are computed through explicit application rules.
4. **AI-assisted analysis** — structured evidence is passed into controlled analytical channels for explanatory and forecast-oriented narrative.
5. **Delivery layer** — the platform exposes a web interface, account/access controls, administration tools and structured report exports.

## Multi-country design

Cross-country analysis introduces comparability risks because source schemas, reporting conventions and evidence availability can differ.

The platform therefore treats country context as an explicit analytical dimension rather than flattening every source into an assumed universal format. Normalized metrics are combined with country-aware metadata, validation and presentation rules.

## Deterministic and AI responsibilities

A central architectural decision was to keep financial calculation authority in deterministic code.

The AI layer is used to:

- interpret user analytical intent;
- compose evidence-grounded explanations;
- summarize comparative findings;
- generate structured narrative from validated inputs;
- support forecast-oriented analytical workflows.

The AI layer is not the authoritative source for base financial arithmetic, ranking position or source provenance.

## Document and report workflow

The private implementation includes controlled PDF/document extraction and spreadsheet processing, plus report-generation paths for multilingual outputs.

Publicly, the important engineering principle is that every extraction path requires provenance awareness and validation. A document parser can recover text or tabular signals, but those results still need to be mapped into known entities, periods, metrics and evidence scopes before they can be trusted by downstream analytics.

## Production and release governance

The private repository maintains:

- explicit production baseline documentation;
- data-update runbooks;
- backup/recovery procedures;
- release and rollback guidance;
- privacy checks for tracked files;
- secret-pattern scanning;
- Python compilation checks;
- deterministic regression tests.

This allows changes to analytical behavior to be reviewed independently of the confidential production data itself.

## Outcome

The result is a production-deployed private platform that unifies sector data ingestion, company-level financial analysis, multi-country benchmarking, AI-assisted explanation and report delivery under one governed system.

The project remains under private production maintenance. This public case study intentionally stops at the capability and architecture boundary.

## Portfolio-safe takeaway

The strongest reusable pattern from the engagement is:

**private financial evidence → normalized deterministic model → validated analytics → bounded AI explanation → controlled production delivery**

That pattern is applicable beyond ceramics to other sector-intelligence, valuation and financial-analysis systems where traceability and comparability matter.
