# Technical Overview

## System layers

### 1. Ingestion and provenance

The private platform accepts multiple financial-data formats, including spreadsheets, PDF documents, CSV/tabular sources and structured reference files.

Ingestion is not treated as a simple file-read operation. Source material must be associated with the correct company, country, period and evidence scope before downstream calculations are trusted.

### 2. Normalized analytical contracts

A normalized internal model binds:

- company identity;
- country context;
- reporting period;
- metric semantics;
- source evidence;
- comparison/ranking scope.

This isolates downstream analytics from source-file layout differences.

### 3. Deterministic analytical core

Explicit code handles the authoritative financial calculations, screening, ranking and comparison behavior.

This layer is designed to remain testable without an LLM and provides the numerical grounding used by later narrative analysis.

### 4. AI-assisted channels

Generative analysis operates on validated, structured context. Typical responsibilities include intent interpretation, evidence-grounded explanation, comparison summaries and forecast-oriented narrative.

The generative layer is deliberately separated from base arithmetic and source provenance.

### 5. Delivery and operations

The private production system includes:

- web application views;
- report/export paths;
- multilingual presentation;
- controlled account/access workflows;
- administration and data-refresh paths;
- release, rollback and recovery procedures.

## Technology categories

The private implementation uses Python/FastAPI web services, HTML/Jinja presentation, spreadsheet/document parsers, OCR integration, Word document generation, OpenAI-compatible model access, payment/commercial integration and GitHub Actions.

## Public limitation

No implementation source, private company data, production configuration or proprietary business rules are included here.
