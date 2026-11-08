# InvoiceForge - technical plan

**Planning document, not an implementation report.**

## Product objective

Explainable, deterministic validation and reproducible synthetic regression fixtures rather than an invoicing or accounting platform.

## Intended system boundary

- **Input:** Synthetic, obviously fictitious invoice XML with invented parties and identifiers.
- **Processing stages:** Document adapter layer -> normalized field assertions; Schema/rule engine -> versioned validation packs; Fixture generator -> deterministic synthetic cases; CLI/reporters -> JSON and HTML outputs.
- **Output:** A clean machine can validate sample documents with reproducible, actionable errors.
- **Runtime / build stack (tentative):** Python 3.12+, Typer, lxml, xmlschema, pytest; optional HTML report renderer
- **Explicitly excluded:** Sending invoices, bookkeeping, customer records, bank information, connecting to live finance systems, or processing real third-party invoices.

## Functional modules

- Parse Factur-X XML payloads, UBL documents, and CII documents in separate adapters
- Apply versioned XML-schema and business-rule validation with source-located errors
- Generate fully synthetic invoices including intentionally invalid variants
- Compare validation output across rule-set revisions
- Export a CLI-friendly JSON report and human-readable HTML report

## Demonstration and acceptance cases

**Test 1:** A developer feeds a synthetic UBL document and receives precise validation failures

**Test 2:** A rule-update changes an expected result and is caught by a regression test

**Test 3:** An invalid synthetic invoice is generated for a QA automation suite

## Safety, privacy, and provenance

1. Keep example datasets fictional, self-created, or appropriately licensed.
2. Run locally for the initial prototype; do not collect data on actual third parties.
3. Document origin and versions of external specifications and dependencies.
4. Exclude production credentials; put environment variable *names* only in `.env.example` if required later.
5. Do not make certification, legal compliance, professional safety, or performance guarantees without independent validation.

## Engineering unknowns and constraints

Public standard versions and national business rules must be cited and tested independently; a validator is not official certification.

## Release definition

A first release requires a runnable prototype, verified README instructions, automated tests tied to the three demonstrations, the full LICENSE file, and an honest public GitHub development history. The roadmap estimates are hypotheses until reviewed during implementation.
