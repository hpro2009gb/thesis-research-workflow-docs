# Thesis Research Workflow — Portability, Privacy and Redistribution

[Overview](../README.md) · [Capabilities](FEATURES.md) · [Usage](USER_GUIDE.vi.md) · [Release gate](RELEASE_STATUS.md)

## Public-distribution objective

A receiving researcher should be able to download and install each declared Skill without relying on the original author's thesis repository, old ChatGPT conversations, local OneDrive paths, internal Aki services, school/lab records, or private AI Brain state. A Skill's workflows and templates should work on **another researcher’s own Context Pack**. Actual cloud tools, university access and software versions remain environment-dependent.

## Data that must not ship

- Unpublished dissertation text, advisor emails, academic/reviewer correspondence and institutional administrative records.
- Raw or processed laboratory signals, equipment calibration, private experimental logs, simulation results and scientific model parameters tied to a live research program.
- Copyright-restricted PDF papers, textbooks, paywalled sources, unpublished datasets, paper drafts and coauthor materials without explicit redistribution rights.
- Research-instance-specific question/claim IDs, approved Knowledge Delta text, unredacted project decisions, real thesis Continuation State and personal language profile.
- Credentials, Git remotes of private repositories, personal paths, proxy/CLI/Aki/Run leases, SSH keys, cookies, tokens, internal chat archives and memory files.
- Hidden demo instructions that pretend synthetic work is actual scholarly validation.

## Potentially portable once validated

- Generic Skill behavior boundaries, workflow contracts and source-independent schemas.
- Synthetic bibliography, research question, evidence/claim bindings, model output and discrepancy examples.
- Source-agnostic safety/verification scripts and clearly licensed templates.
- Demonstrations that exercise Gate/authority constraints, Research Round review, source versioning, contradiction retention and read-only Scientific Debug.

## Exact export procedure

1. Inventory the family and all declared references/scripts/assets.
2. Bind each member to an immutable source digest and published licence decision.
3. Create a fresh export worktree using an **explicit allowlist**; never copy a private project's `.git` history.
4. Replace instance-specific names, paths, science data and provider/account settings with entirely synthetic fixtures.
5. Validate YAML frontmatter and skill metadata, exact references, JSON Schemas and runnable scripts.
6. Build and re-open one ZIP per Skill, record its SHA-256, and verify all declared members in one versioned manifest.
7. Run package-level tests, behavioral/authority-negative cases, and independent synthetic-context canary on an eligible fresh account.
8. Review privacy findings, permissions and licence obligations for the exact export candidate, then obtain explicit Human release approval.
9. Only then push a history-clean public release. Keep prior binaries/hashes available for rollback.

## Safety and evidence rules

Canonical scientific data and Human-approved knowledge are stronger authority than ChatGPT memory or tool summaries. A fresh account must **not** infer approval, treat a task return as Round completion or use simulation evidence as experimental proof. The Scientific Debug lane defaults to read-only. Invalid or incomplete references block evidence promotion.

Public source does not guarantee **local-only AI inference**. When end users connect cloud models, pasted research data may be transmitted to those services. Users must review data handling, contracts and institutional requirements separately.

## Licensing

Open GitHub visibility does not by itself grant redistribution permission. Audit source ownership and third-party dependencies individually before adding an open-source licence or packaging third-party files.

## Honest current status

**Public documentation preview only.** The internal RC6 ZIP remains private; no sanitized installable package or independent recipient-account canary has been released. See SOURCE_VALIDATION.md and RELEASE_STATUS.md.
