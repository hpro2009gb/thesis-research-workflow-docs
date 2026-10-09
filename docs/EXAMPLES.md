# Thesis Workflow — Synthetic Walkthroughs

[Overview](../README.md) · [Capabilities](FEATURES.md) · [User guide](USER_GUIDE.md)

These examples use **fictional projects, synthetic identities and invented values**. They are teaching scenarios only, **not experimental or bibliographic evidence**.

## Scenario A — One controlled Research Round

**Fictional topic:** compare two toy algorithms that estimate the mass of artificial cubes from a simulated sensor value. No real lab data or university materials are used.

| Symbol | Meaning | Synthetic fixture |
|---|---|---|
| `x` | simulated sensor output | 1.0, 2.0, 3.0 |
| `y` | synthetic target value | 1.1, 2.0, 3.2 |
| `A` | toy estimator | `yhat = x` |
| `B` | toy estimator | `yhat = 1.05 * x` |

**Step 1 — Context.** Create synthetic `00-THESIS-INTAKE-MASTER.md` to `05-CONTEXT-GAP-ASSESSMENT.md`. Explicitly label all numbers as invented and record which dataset, baseline and acceptance criteria would be necessary for a *real* claim.

**Step 2 — Intake.** Ask the Thesis Lifecycle parent to frame one question: *“Does B outperform A under a specified synthetic metric and fixed sample set?”* Do not assume the answer. Create one bounded Research Round with falsification requirements.

**Step 3 — Tasks.** A task could calculate an illustrative metric; a second could audit whether the metric supports the claim. Separate arithmetic accuracy from scientific generalizability and instrument validity.

**Step 4 — Source policy.** Do not fabricate a bibliographic citation merely to decorate the example. Mock source records must be clearly marked SYNTHETIC, without real DOI or fake journal identities.

**Step 5 — Synthesis.** Show both supporting and negative evidence, including the small sample size and inability to generalize. Human Round Review decides whether the candidate finding is acceptable *as a synthetic example only*.

**Step 6 — Promotion.** No claim of actual science may be promoted from this synthetic Round. A validated tutorial artifact may demonstrate workflow mechanics without asserting real research results.

## Scenario B — Scientific Debug should not silently repair

A toy numerical script returns a different estimate after its solver tolerance was modified. Before changing code, record (a) known-good source hash, (b) runtime and solver settings, (c) input data hash, (d) expected output, and (e) candidate changed settings.

Prompt:

> Scientific Debug, DIAGNOSE_ONLY. Compare the candidate run to the golden synthetic fixture, test tolerances while preserving canonical artifacts and identify whether the mismatch is numerical, initialization, implementation or provenance related. Report at least one hypothesis that could falsify the apparent cause. No repair patch.

A diagnostic result, even `ROOT_CAUSE_LOCKED`, is **not** authorization to change the canonical research model. Repair is a separate scoped task.

## Scenario C — Reference/version management

Create illustrative `B0001` (a fictional work without a real DOI) and claim `CL-001`. Store the work, one source version, claim revision, and an initially `UNVERIFIED` binding. The Reference Library Manager can assign stable IDs and versions, but cannot determine that the source supports the claim without an accepted audit delta.

When a fictional version changes, classify whether metadata, locator or evidence content changed; mark affected claims STALE when identity/equivalence has not been established.

## Acceptance criteria for a portable release

The same scenarios should execute on a fresh, authorized account using only generated synthetic files while keeping these invariants:

1. One parent owns thesis/Research Round state.
2. Task completion never auto-closes a Round.
3. Human review is required before Knowledge Delta promotion.
4. Unverified source records never automatically support claims.
5. Diagnostic investigation never modifies the golden baseline.
6. No confidential files or special internal connectors are needed for the generic test path.

These checks are **not yet executed** for the public candidate. See [RELEASE_STATUS.md](RELEASE_STATUS.md).
