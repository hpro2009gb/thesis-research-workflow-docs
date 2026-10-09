# Thesis Research Workflow — Full Feature Reference

[Home](../README.md) · [User guide (Vietnamese)](USER_GUIDE.vi.md) · [Privacy and portability](PORTABILITY.md)

**Basis:** inspected Skill entrypoints and the RC6 baseline. Ten member ZIP trees exactly match the ten installed Skills in the audited environment. This proves identity, not standalone installability, runtime correctness, or safe redistribution.

## Scope and roles

| Subsystem / owning Skill | Expected inputs | Designed actions and explicit boundary | Core outputs |
|---|---|---|---|
| **Context Bootstrap** — `thesis-context-bootstrap-v2` | Author materials, outline, proposal, publications, methods, data policy | Organize canonical context; separate evidence vs plans vs administrative context; report gaps. Does not search or write thesis prose | Five canonical context files plus `05-CONTEXT-GAP-ASSESSMENT.md`; optional `thesis-context-profile/1.0` |
| **Parent Lifecycle** — `thesis-lifecycle-orchestrator` | Validated Context/Profile, canonical continuation, intake/returns, Human decisions | Own whole-thesis direction, Research Round creation/closure, approved Knowledge Delta, global impact and next action. Cannot delegate parent authority | `research-intake/1.0`, `research-round-charter/1.0`, `research-round-synthesis/1.0`, `knowledge-delta/1.0`, `thesis-continuation-state/1.0` |
| **Task Controller** — `thesis-task-execution-controller` | Exact one-task contract, scope, artifact refs and evidence ceiling | Execute/delegate one bounded task and return verifiable evidence; cannot alter approved questions or close Round | `thesis-task-return/1.0`, evidence/gap refs, checkpoints, recommended next parent action |
| **Literature Search** — `thesis-literature-search-p5-json-perplex-split` | Five-file context, chapter scope, source search mode | Chapter-profile-driven taxonomy and query packs, structured provider handoff and source-candidate assembly; discovery is not verification | P1 taxonomy, P2 query bank, provider handoff, chapter Pass 1 source/map/gap artifacts |
| **Source Audit** — `thesis-source-audit-v1` | Chapter Pass 1 pack, URL/DOI metadata, Human review | Check source identity/access/strength and preserve per-chapter P4/P5/gap continuity; no scientific truth promotion | Audit patches, unresolved queue, Human review register, Round 2 ready candidate |
| **Reference Library** — `thesis-reference-library-manager` | Accepted audited source versions and claim refs | Stable work IDs `B0001`…, source version and claim binding persistence, chapter slices, derived index and structural reference audit; not evidence-support judge | Canonical source JSON, version/binding records, audit receipts, bibliography/chapter projections |
| **Writing / consistency** — `thesis-batch-writer-digest-system-writing-v1` | Approved context + audited sources + chapter freeze | Freeze source/binding/gap/claim constraints, lock cross-chapter terms/formulas and draft bounded prose. Must not fabricate claims or turn digests into bibliography truth | Chapter `Context_Freeze_Pack`, guards, ledgers, batch drafts, consistency findings |
| **Mathematical translation/export** — `ai-math-word-export` | Language Profile, approved semantic source, equations/notation | Review and lock meaning before multilingual adaptation, notation consistency and Word-ready material. No hard-coded universal language pair | Review/lock artifacts, notation comparison and export-ready Markdown/LaTeX |
| **Scientific Debug** — `evidence-first-differential-debugger` via controller | Golden baseline + failing model/results + exact context | Read-only diagnosis, differential evidence and falsification; never patch accepted model during diagnosis | Diagnostic evidence, root-cause state or bounded separate repair request |
| **Contract Validation** — `thesis-suite-contract-v2` | Legacy or VNext packets/schemas | Validate structure, version, authority, hash/path and cross-file integrity; **not** judge whether physics/science is true | PASS/FAIL diagnostics and integrity findings |
| **Repo memory continuity** — `repo-local-memory-gate` / `repo-session-memory` | Canonical repository locator and valid memory contract | Resume/recall evidence and checkpoints; never become scientific source of truth or grant approval | Memory readiness, bounded refs and next legal action anchors |

Specialist availability depends on the eventual public package composition and the receiving user's permissions. A status of `COMPLETE` for one specialist is never equivalent to completing or accepting the whole thesis.

## Canonical context files

The Context Bootstrap convention uses:

```text
00-THESIS-INTAKE-MASTER.md
01-TOC-MAP.md
02-CONTRIBUTION-AND-EVIDENCE.md
03-MODEL-METHOD-DATA-PACK.md
04-WRITING-POLICY.md
05-CONTEXT-GAP-ASSESSMENT.md
```

The first five are the canonical context basis; the sixth identifies missing/ambiguous content. A portable Context/Profile binding resolves thesis identity, language and domain scope. Do **not** copy another author's instance IDs, private content or a previous thesis's language settings.

## Research Round life cycle

1. **Intake:** classify one pain, question, hypothesis, result anomaly, source/evidence gap or contradiction. Compare with active work and avoid duplicates.
2. **Charter:** choose a bounded scope and record what would support, weaken, falsify or leave the question unresolved. Record tasks and stop conditions.
3. **Execute:** delegate exactly one valid task contract at a time by default; record evidence and checkpoint on meaningful transitions.
4. **Consume:** verify task identity, return status and provenance, then merge only into **candidate** Round evidence.
5. **Synthesize:** parent contrasts promised and actual results, contradictions, scientific gaps, and cross-chapter impact.
6. **Human Round Review:** author chooses APPROVE, PATCH, CONTINUE or REJECT for the exact synthesis and Knowledge Delta.
7. **Promote:** only accepted changes update the canonical thesis-wide claim/evidence state; impacted chapters, references, formulas or exports become STALE or RECHECK_REQUIRED.

This is intentionally **not** “ask AI to write a complete dissertation from a topic.” Human review and source ceilings are first-class parts of the workflow.

## Evidence and reference governance

- Assign stable B-IDs to works, not every URL or PDF mirror. Track accepted/published/preprint versions under the same work when identity permits.
- Keep a binding from one exact claim revision to an exact source version, locator and audit decision.
- A relevant paper is **not** necessarily supporting evidence. It may be contradictory, lower strength, inaccessible or ambiguous.
- DOI/title equality does not by itself prove identical evidence content across versions.
- SQLite/FTS or retrieval caches are derived and can be rebuilt from canonical records. They do not promote scientific truth.
- A writing freeze must specify allowed sources/versions and evidence strength; redacted or retracted evidence cannot be silently reused.

## Scientific debug and quantitative claims

A suspect result requires a golden identity where possible (code/model hash, solver/runtime version, parameter set, raw output ref and prior acceptance metrics). Diagnose with read-only comparisons, one-variable probes and negative evidence. Only a confirmed `ROOT_CAUSE_LOCKED` finding together with an independently authorized bounded repair scope can permit a **separate** repair task.

Numerical-model evidence does not automatically count as experimental validation. A simulation's “completed” status does not establish correct physics, identification, calibration, or academic novelty.

## Authority & limitations

| Actor | May do | Must not do |
|---|---|---|
| Author/Human | Approve context, change research direction, review synthesis, authorize knowledge promotion and releases | Delegate own scholarly responsibility away implicitly |
| Lifecycle parent | Control Round state, task routing and global staleness | Treat agent success as automatic scientific promotion |
| Bounded task/specialist | Gather evidence, audit, draft, check or translate inside approved limits | Close Round or widen research question independently |
| Reference library manager | Persist identity/version/bindings and bibliography data | Raise evidence ceiling or author a scientific claim |
| Memory/indexing tools | Find files, recover checkpoints and source pointers | Become canonical experiment/source truth |
| Exporters | Produce presentation/Word-ready artifacts from approved state | Infer PRINT_READY from layout alone |

## What is still not publicly verified

- Standalone installable ZIP(s) for this family, complete closure/dependencies and licence approval.
- Actual round-trip canary using a separate ChatGPT account and non-sensitive synthetic thesis.
- Safe integration with external providers, reference databases, PDF/OCR or local simulation.
- Any claims of academic success, reduced review time, publication acceptance or established scientific accuracy.

Treat this file as a product-specification-level **public-release candidate inventory**, not a production certification.
