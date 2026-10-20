# Repository Hardening

The private delivery repository contains production source and authorized private input material. The public companion uses a deliberately different security model.

## Private repository controls

The confidential repository enforces:

- real environment files and secret material excluded from Git;
- generated databases and delivery archives excluded;
- approved private data paths only;
- source compilation checks;
- deterministic regression tests;
- documented production baseline, backup and rollback procedures;
- explicit public/private disclosure rules.

## Public repository controls

This public showcase:

- has independent Git history;
- contains no private source tree;
- contains no financial statements, spreadsheets, PDFs or client datasets;
- contains no credentials or production configuration;
- contains no private screenshots or conversations;
- contains no proprietary ranking/valuation implementation;
- validates its disclosure boundary through GitHub Actions.

## Why independent history matters

A clean public history prevents accidental disclosure through deleted files, old commits, private filenames or earlier credentials.

The public repository is therefore authored from sanitized documentation, not converted from the private source repository.
