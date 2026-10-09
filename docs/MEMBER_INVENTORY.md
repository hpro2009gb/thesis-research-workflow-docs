# Thesis Workflow — Candidate Member and Dependency Inventory

[Overview](../README.md) · [Feature reference](FEATURES.md) · [Release status](RELEASE_STATUS.md)

**Scope:** THESIS_RESEARCH_WRITING_VNEXT. RC6 has ten ZIP member trees that match the installed Skill copies file-for-file in the audited environment. Baseline equality is not proof of redistribution safety or independent run-time success.

## Core and specialist Skills known in the current environment

| Entry point | Role in workflow | Packaging / compatibility caveat |
|---|---|---|
| `thesis-lifecycle-orchestrator` | Human-governed whole-thesis parent, Research Rounds, Knowledge Delta | Exact references, domain/profile and handoff contracts require closure audit |
| `thesis-task-execution-controller` | One bounded task with checkpoint and evidence return | Depends on specialist routing, scientific-debug rules, contract validation and runtime evidence |
| `thesis-suite-contract-v2` | Cross-stage typed packet and legacy pack validation | Schema scripts, versions, examples and regression tests need complete local packaging |
| `thesis-context-bootstrap-v2` | Convert author materials into canonical Context Pack | Public examples must be entirely fictional |
| `thesis-literature-search-p5-json-perplex-split` | Chapter-profile search and source candidate assembly | Provider access optional/external; no included paid subscriptions |
| `thesis-source-audit-v1` | Check scholarly source metadata/strength, audit handoff | Source access is not an automatic redistribution grant |
| `thesis-reference-library-manager` | Stable work IDs, source/version records and claim bindings | Must not independently judge scientific support or promote claims |
| `thesis-batch-writer-digest-system-writing-v1` | Source freeze, scoped drafting and consistency | Needs audited sources; no real thesis chapters in release examples |
| `ai-math-word-export` | Mathematical review, semantic lock, multilingual export | Profile-driven; prior Vietnamese/Russian profile is not generic default |
| `evidence-first-differential-debugger` | Read-only diagnostic investigation | Cross-use with non-thesis workflows requires explicit profile boundary |

## External / shared infrastructure, not automatically included

- `repo-local-memory-gate`, `repo-session-memory`: generic repo continuity and read-only recall. Installed on one account does not guarantee availability on another.
- `skill-creator`: used to build/validate portable individual Skill packages; not part of thesis runtime logic.
- Optional public-web/GitHub/research providers, code runners, simulation tools and institutional bibliographic access.
- Domain-specific research or language/export specialists selected by an approved Context/Profile; never auto-bundle unverified local variants.

## Dependency and authority edges (intent)

```text
Author + validated Context/Profile
              |
              v
thesis-lifecycle-orchestrator (only Round / Knowledge parent)
              |
              +--> thesis-task-execution-controller
              |            |-- literature-search / source-audit
              |            |-- reference-library-manager
              |            |-- batch-writer / math-export
              |            |-- evidence-first-differential-debugger (READ_ONLY)
              |
              +--> thesis-suite-contract-v2 (contracts/authority)
              |
              +--> canonical thesis evidence + continuation state
                              |
                         repo memory (navigation, not scientific truth)
```

**Strict constraints:** a completed child task cannot close a Research Round; an audit record cannot grant scientific claim strength without the owning decision; a read-only diagnosis cannot silently become repair; Human Round Review is necessary for Knowledge Delta promotion.

## Candidate validation state

- **Structural package closure:** RC6 source identity and ten ZIPs captured; sanitized public package still pending.
- **Semantic preservation:** installed members equal RC6; no sanitized-candidate regression or fresh-account canary yet.
- **Dependency / trigger / handoff compatibility:** GAP pending exact source/reference closure.
- **Fresh-chat canary:** NOT_RUN.
- **Rollback target:** internal RC6 embeds RC4 rollback; no verified public-release rollback artifact exists yet.
- **Release disposition:** `BLOCKED` for the **standalone Skill suite**.
- **Local installed status:** the entrypoints listed above are available in the authoring environment. This is not the same as public distribution.

This is a **read-only inventory**: no existing Skill has been replaced, activated, deprecated or published. Before packaging, pin immutable baselines and check ownership/licence of each member.

## Preliminary source-tree inventory (2026-10-09)

Read-only Skill-root listings show **203 declared files across the ten principal installed members** (including entrypoints, reference files, schemas, scripts, fixtures, metadata and icon assets), plus **12 declared files** in the two shared repository-memory members. These counts are path inventory, not proof of safe/public content or archive integrity.

One generic-core portability risk is already explicit: `ai-math-word-export/references/[subject-specific-profile].md` binds a real-domain compatibility profile. A standalone generic public package must **exclude or replace this instance-bound profile only after dependency and semantic impact review**. The Thesis Contract member also carries many test fixtures that require line-by-line confidentiality and copyright classification before redistribution.

No member-level licence files were listed in this inventory. Licence/ownership decisions, full-tree privacy review, cryptographic digests, complete handoff closure and recipient canary remain OPEN. Do **not** publish these installed trees as a suite from this path inventory alone.
