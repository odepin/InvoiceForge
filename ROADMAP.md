# InvoiceForge - development roadmap

**Status:** Planned work only. None of the boxes are marked completed. Estimates are rough.

## Product-level acceptance criterion

A clean machine can validate sample documents with reproducible, actionable errors.

## Estimated work breakdown

| Step | Milestone | Estimated hours | Observable outcome |
|---|---|---:|---|
| 1 | Specify formats and fixture schemas | 7 | Document supported document variants and create a synthetic fixture manifest |
| 2 | Implement XML adapters and parsing diagnostics | 10 | Fixture documents parse into typed, source-traceable observations |
| 3 | Build versioned schema and rule checks | 12 | Deterministic results with rule IDs and explicit version handling |
| 4 | Implement synthetic invalid-document generator | 7 | At least eight invalid fixture families with expected errors |
| 5 | Create CLI plus HTML/JSON output | 7 | A documented command produces readable and machine-readable results |
| 6 | Regression tests, CI, and user documentation | 9 | Unit/fixture tests pass, CLI works from documented setup instructions |
| | **Total estimated** | **52** | |

## Detailed milestones

### 1. Specify formats and fixture schemas (7 estimated hours)

- [ ] Deliverable: Document supported document variants and create a synthetic fixture manifest.
- [ ] Add tests or demonstrations proving the deliverable works.
- [ ] Record a genuine development commit and update documentation only after the work occurs.

### 2. Implement XML adapters and parsing diagnostics (10 estimated hours)

- [ ] Deliverable: Fixture documents parse into typed, source-traceable observations.
- [ ] Add tests or demonstrations proving the deliverable works.
- [ ] Record a genuine development commit and update documentation only after the work occurs.

### 3. Build versioned schema and rule checks (12 estimated hours)

- [ ] Deliverable: Deterministic results with rule IDs and explicit version handling.
- [ ] Add tests or demonstrations proving the deliverable works.
- [ ] Record a genuine development commit and update documentation only after the work occurs.

### 4. Implement synthetic invalid-document generator (7 estimated hours)

- [ ] Deliverable: At least eight invalid fixture families with expected errors.
- [ ] Add tests or demonstrations proving the deliverable works.
- [ ] Record a genuine development commit and update documentation only after the work occurs.

### 5. Create CLI plus HTML/JSON output (7 estimated hours)

- [ ] Deliverable: A documented command produces readable and machine-readable results.
- [ ] Add tests or demonstrations proving the deliverable works.
- [ ] Record a genuine development commit and update documentation only after the work occurs.

### 6. Regression tests, CI, and user documentation (9 estimated hours)

- [ ] Deliverable: Unit/fixture tests pass, CLI works from documented setup instructions.
- [ ] Add tests or demonstrations proving the deliverable works.
- [ ] Record a genuine development commit and update documentation only after the work occurs.

## QA and release gates

- [ ] A real runnable implementation exists, with verified setup commands in `README.md`.
- [ ] Automated tests pass in a clean environment and failures are actionable.
- [ ] Only fabricated, original, openly licensed, or otherwise authorized sample data is published.
- [ ] No passwords, API keys, secrets, customer records, or employer/client confidential artifacts appear in repository history.
- [ ] A source-linked change log and actual progress notes distinguish finished work from plans.
- [ ] The GitHub history preserves authentic work and authorship; do **not** manufacture or backdate commits.

## Parking lot and risks

- Technical: Public standard versions and national business rules must be cited and tested independently; a validator is not official certification.
- Commercial hypothesis (not validated): Premium CI integrations and curated conformance test suites.
- Beyond MVP: defer paid extensions and hosted features until the underlying product works.
