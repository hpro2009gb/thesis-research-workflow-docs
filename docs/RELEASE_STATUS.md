# Thesis Research Workflow — Public Release Status

**PUBLIC_DOCS_PREVIEW** — documentation and fictional examples. **SKILL_SUITE_BLOCKED** — no installable public ZIP.

This repository documents a founder-led research workflow. It does not assert scientific validity, publication success, or that a new user can install the full Skill family today.

## Included

- English and Vietnamese overviews, feature reference and user guides.
- Twelve prompts and a wholly fictional six-file research Context Pack.
- Source verification, member inventory and safety/portability policy.

## Audited internal baseline (not distributed)

- Suite: `thesis-research-writing-suite-v1.0.0-rc.6.zip`.
- SHA-256: `6063d0f3d242a26dff1a55bbac57d490405de95b3e9e245d3c926f40c4cb2774`.
- Ten child Skill ZIP files passed ZIP reading/integrity checks; all ten match installed source trees in the audited environment.
- Two external memory dependencies match their pinned RC16 references, and are NOT bundled in RC6.
- Original RC6 reports `CANARY_REQUIRED`; its fresh-account canary was `NOT_RUN`. RC5 was quarantined for shared-Skill replacement risk, and RC4 is the rollback archive for the internal lineage.
- Some member fixtures/references include case-specific text; no public Skill redistribution rights have been verified.

## Remaining public Skill release requirements

| Requirement | Status |
|---|---|
| Member identity and existing RC6 dependency pins | BASELINE CAPTURED |
| Source ownership and redistribution licences | OPEN |
| Sanitized standalone member trees and dependency closure | NOT BUILT |
| Per-Skill package validation + deterministic delivery manifest | NOT RUN |
| Independent synthetic-context canary and negative authority tests | NOT RUN |
| Privacy/secret scan on exact proposed public ZIP | NOT RUN |
| Review and authorize the exact public binary artifact | PENDING |

## Disclosure boundary

This documentation-only repo contains no original RC6 ZIP, unpublished research, laboratory data, supervisor correspondence, third-party copyrighted PDFs, credentials, local Aki memory or private research history. It is not a license to share or claim that the original suite has passed production readiness.

Read [source verification](SOURCE_VALIDATION.md), [safe portability](PORTABILITY.md), and the [fictional context example](../examples/synthetic-context/README.md).

Last reviewed 2026-10-09.