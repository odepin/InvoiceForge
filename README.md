# InvoiceForge

> Offline-first conformance testing for synthetic electronic invoices.

**Current state:** Documentation starter / proposed product. The presence of this README does **not** mean the software has been implemented, deployed, used. Update this status to reflect real work.

## What it is

InvoiceForge is a proposed specialist software tool for ERP integrators, independent accounting-software developers, and QA engineers. Invoice formats and validation rules are difficult to debug before deployment; general accounting platforms do not provide a focused developer feedback loop. The intended differentiation is: Explainable, deterministic validation and reproducible synthetic regression fixtures rather than an invoicing or accounting platform.

## Intended users and use cases

- A developer feeds a synthetic UBL document and receives precise validation failures
- A rule-update changes an expected result and is caught by a regression test
- An invalid synthetic invoice is generated for a QA automation suite

## Planned features

- Parse Factur-X XML payloads, UBL documents, and CII documents in separate adapters
- Apply versioned XML-schema and business-rule validation with source-located errors
- Generate fully synthetic invoices including intentionally invalid variants
- Compare validation output across rule-set revisions
- Export a CLI-friendly JSON report and human-readable HTML report

## Proposed technology

Python 3.12+, Typer, lxml, xmlschema, pytest; optional HTML report renderer

These technologies are *planned*, not a claim that dependencies have already been installed or code has been written. Revise this section when actual implementation decisions are made.

## Proposed architecture

- Document adapter layer -> normalized field assertions
- Schema/rule engine -> versioned validation packs
- Fixture generator -> deterministic synthetic cases
- CLI/reporters -> JSON and HTML outputs

See [TECHNICAL_PLAN.md](TECHNICAL_PLAN.md) for technical boundaries and acceptance tests.

## Running locally

**Not yet runnable.** This package contains documentation templates, not software. When a functioning implementation is available, replace this paragraph with tested prerequisites, install instructions, a verified executable command, and a reproducible example using `Synthetic, obviously fictitious invoice XML with invented parties and identifiers.`

## Data boundaries and exclusions

Sending invoices, bookkeeping, customer records, bank information, connecting to live finance systems, or processing real third-party invoices. All public examples should use Synthetic, obviously fictitious invoice XML with invented parties and identifiers.

## Known limitations / validation risks

Public standard versions and national business rules must be cited and tested independently; a validator is not official certification.

## Development roadmap

Work is broken into estimated, not-yet-completed milestones in [ROADMAP.md](ROADMAP.md). They are *planning estimates*, not an assertion that development has begun or that work will definitely be performed.

## Business direction

Potential commercial extensions: Premium CI integrations and curated conformance test suites. 

## Contributing and licensing

License: [Mozilla Public License 2.0](LICENSE) (`MPL-2.0`). The distribution contains the complete license text. Any future source files can include the SPDX identifier `MPL-2.0` and the Exhibit A notice where appropriate. Rights in contributions and project ownership must be verified before licensing.

