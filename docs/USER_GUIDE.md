# Thesis Research Workflow — User Guide

[Overview](../README.md) · [Full features](FEATURES.md) · [Hướng dẫn tiếng Việt](USER_GUIDE.vi.md) · [Release status](RELEASE_STATUS.md)

**Current repository status:** public documentation preview, **not a publicly installable standalone Skill package**. The guide reflects current Skill instructions and the locally verified RC6 baseline; a sanitized package and fresh-account canary have not been released.

## Intended user and research boundaries

This workflow is designed for a researcher or supervisor who wants to manage dissertation context, source audits, bounded research tasks, scientific-result anomalies, draft evidence controls, Human approval and cross-session continuity. It does not autonomously write and certify a dissertation, replace academic responsibility or approve scientific truth on its own.

Use only source material you are authorized to share with your model or tools. A privately stored local file is **not** automatically protected from transmission when submitted to a cloud AI provider.

## 1. Prepare an author-controlled Context Pack

Collect a proposal, table of contents, published work, method/data specification, writing policy and approved research goals. Run the Context Bootstrap specialist to generate:

```text
00-THESIS-INTAKE-MASTER.md
01-TOC-MAP.md
02-CONTRIBUTION-AND-EVIDENCE.md
03-MODEL-METHOD-DATA-PACK.md
04-WRITING-POLICY.md
05-CONTEXT-GAP-ASSESSMENT.md
```

The first five form the canonical core; the sixth identifies gaps and blockers. Bind a thesis-specific Context/Profile so the generic workflow **does not inherit another author's subject matter, language pair, confidential results or naming**.

Example prompt:

> Organize this synthetic research proposal, toy methods and outline into a canonical Context Pack. Label assumptions and unsupported claims, list exact evidence gaps and stop. Do not conduct literature searches or write chapter prose.

## 2. Intake one research problem

Ask the Thesis Lifecycle parent to classify one bounded scientific question, contradiction or evidence gap. Avoid silently expanding the entire thesis scope or creating duplicate Research Rounds. The parent should compare to the canonical continuation state and authorize a new charter only when necessary.

Example:

> Intake the question “Does the numerical sensitivity test distinguish model A and model B?” under this synthetic Context/Profile. Create a bounded Research Round charter and identify evidence that would support, weaken or falsify the hypothesis. Do not claim a result yet.

The parent controls Round creation, scope, charter and Human review. A task executor may not change approved research questions.

## 3. Delegate bounded tasks and inspect evidence

A task contract (`thesis-task-execution/1.0`) binds thesis/round/task identities, exact input refs, allowed actions, evidence ceiling, expected output, stop conditions and return policy. The Task Controller processes **one bounded item**, checkpoints meaningful progress and returns `thesis-task-return/1.0` as COMPLETE / PARTIAL / BLOCKED / FAILED.

A return is not automatically a Round closure. Ask for raw evidence references, source or data versions, contradictory results and unresolved gaps.

## 4. Search, audit and store references

1. From the approved chapter profile and Context Pack, use the literature specialist to produce chapter-specific search taxonomy, queries and candidate source packs.
2. Keep discovery separate from audit: the Source Audit specialist verifies metadata, URLs, versions, access and material support boundaries.
3. Only after an accepted audit decision may the Reference Library Manager persist work IDs such as `B0001`, source versions and claim↔source bindings.
4. Preserve exact locator, audit receipt, claim revision and evidence limit. A paper that is relevant may still be contradictory or inadequate support.
5. Build a chapter source slice for writing; do not silently reuse superseded or unavailable evidence.

Prompts for external literature providers depend on the installed specialist version and a researcher's connected tools. This documentation does not promise the user an included Perplexity/Consensus subscription.

## 5. Handle suspicious quantitative results safely

Freeze the strongest existing model/experiment baseline: revision/hash, solver/runtime, parameter set, data identity and accepted output metrics. Diagnose with read-only comparisons and falsifiable hypotheses first.

> Compare these synthetic baseline and candidate outputs. Identify the failure layer and test one controlled difference at a time. Do not change the accepted model or promote scientific validity. Return a diagnostic evidence packet and whether a distinct repair task is justified.

**Scientific Debug and Scientific Repair are separate operations.** A successful solver run is not proof of physical validity, and a numerical comparison is not automatically experimental validation.

## 6. Synthesize and request Human Round Review

The parent evaluates task returns against the Round charter and prepares `research-round-synthesis/1.0` and, where warranted, a candidate `knowledge-delta/1.0`.

The author explicitly chooses APPROVE / PATCH / CONTINUE / REJECT for the current synthesis. Knowledge promotion without Human approval is forbidden. Approved changes may mark chapters, claims, source slices, formulas and exports stale or recheck-required.

## 7. Write only from frozen eligible evidence

Use the chapter writing specialist to construct a version-bound evidence freeze before generating prose. Lock claim strength, source versions, contradictory evidence, terminology, formula notation and unverified gaps. Treat a research digest as a reading aid, not independent bibliographic proof.

For multilingual review/export, resolve working, review and final languages from the author's **Language Profile**. Preserve approved meaning and formula conventions. Layout PASS is not scientific PASS; a file that opens correctly is not necessarily ready to submit.

## 8. Recover in a new chat

Resolve the canonical repository, require repo memory readiness and recover authoritative continuation/checkpoints. Old chat is navigation context only, not approval or scientific truth. If the required state cannot be reconstructed, stop as BLOCKED rather than invent an approval.

## 9. Troubleshooting and boundaries

| Issue | Required response |
|---|---|
| No Context/Profile | Build or validate the context first |
| Missing source DOI/version/locator | Mark insufficient evidence and request audit |
| Task complete but Round still open | Parent synthesis and Human review remain necessary |
| Research model unexpectedly fails | Diagnose read-only, then request bounded repair if justified |
| Knowledge changes across a new conversation | Rebuild from canonical approved state, not chat recollection |
| Cloud integration not connected | Do not claim access to repositories, academic databases or simulation programs |
| Public package is not available | This repo publishes documentation and fictional examples only; see RELEASE_STATUS.md |

**Privacy:** Never push private thesis chapters, actual experiments, advisor messages, paywalled full-text sources, private repos, account cookies or personal memory into a public workflow repository.

For a complete **synthetic research scenario**, see [EXAMPLES.md](EXAMPLES.md). The package still requires licence, dependency, privacy, and fresh-account validation before public release.
