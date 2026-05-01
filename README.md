# Ricky Jones / LalaSkye

AI Governance Systems Engineer working on execution-boundary control, admissibility, runtime authority, and fail-closed AI systems.

This GitHub contains public artefacts for a single governance question:

> **When is a system allowed to act at all?**

The work focuses on systems where AI moves beyond advice and begins participating in actions that affect money, access, legal state, infrastructure, records, workflows, or downstream commitments.

---

## Start here

### [`commit-gate-core`](https://github.com/LalaSkye/commit-gate-core)

Reference kernel for execution-boundary governance.

**Invariant:**

> No state mutation is allowed unless a signed, scoped, unexpired, unreplayed `DecisionRecord` authorises the exact commit.

If authority, scope, expiry, replay, or receipt checks fail, the action does not run.

```text
Attempt:        send external email
DecisionRecord: missing authority
Result:         HOLD
Email sent:     false
Receipt written: true
```

That is the shape of the work: unsafe consequence refused before execution, with a receipt proving why.

---

## Core themes

- Execution-boundary control
- Runtime admissibility
- Authority-before-action
- Fail-closed architecture
- Refusal and non-execution
- Commit gates
- Audit and replay evidence
- Governed human-AI workflows

---

## Repository map

### Flagship

| Repo | Purpose |
|---|---|
| [`commit-gate-core`](https://github.com/LalaSkye/commit-gate-core) | Reference kernel: no mutation without a valid `DecisionRecord` |

### Execution-boundary demos

| Repo | Purpose |
|---|---|
| [`runtime-commit-gate-demo`](https://github.com/LalaSkye/runtime-commit-gate-demo) | Demonstrates a runtime commit gate refusing unsafe consequence |
| [`execution-boundary-lab`](https://github.com/LalaSkye/execution-boundary-lab) | Shows where governance must physically stop execution |
| [`execution-gate-litmus`](https://github.com/LalaSkye/execution-gate-litmus) | Minimal litmus surface for testing whether a gate actually binds |

### Admissibility and interpretation

| Repo | Purpose |
|---|---|
| [`interpretation-boundary-lab`](https://github.com/LalaSkye/interpretation-boundary-lab) | Tests meaning construction before execution is even considered |
| [`dual-boundary-admissibility-lab`](https://github.com/LalaSkye/dual-boundary-admissibility-lab) | Models upstream interpretation plus downstream execution control |
| [`admissible-transition-lab`](https://github.com/LalaSkye/admissible-transition-lab) | Explores what makes a transition admissible rather than merely possible |
| [`transition-admissibility-gate`](https://github.com/LalaSkye/transition-admissibility-gate) | Small gate surface for transition-level admissibility |

### Control primitives

| Repo | Purpose |
|---|---|
| [`stop-machine`](https://github.com/LalaSkye/stop-machine) | Deterministic stop primitive: once RED, nothing runs |
| [`constraint-workshop`](https://github.com/LalaSkye/constraint-workshop) | Composable authority, invariant, and stop-control primitives |
| [`invariant-lock`](https://github.com/LalaSkye/invariant-lock) | Refuses execution unless invariant discipline is preserved |
| [`deterministic-lexicon`](https://github.com/LalaSkye/deterministic-lexicon) | Fixed vocabulary surface: exact terms, no inference drift |
| [`policy-lint`](https://github.com/LalaSkye/policy-lint) | Deterministic checks for governance language and policy claims |

### Readiness and evidence

| Repo | Purpose |
|---|---|
| [`artifact-readiness-engine`](https://github.com/LalaSkye/artifact-readiness-engine) | Checks whether a repo is ready to be inspected, run, and trusted |
| [`inspection-surface`](https://github.com/LalaSkye/inspection-surface) | Minimal surface for showing what can be inspected and verified |
| [`csgr-lab`](https://github.com/LalaSkye/csgr-lab) | Measurement surface for stability, drift, and audit evidence |

---

## Research surface

These repositories sit alongside published papers on admissibility, runtime governance, refusal, constraint, authority allocation, and fail-closed AI architecture.

The shared question is simple:

> **Where does the system physically stop?**

---

## Core thesis

Governance is not real because a policy says an action is forbidden.

Governance becomes real when the forbidden action cannot cross the execution boundary.

A governed AI system must be able to show:

1. what action was attempted
2. what authority was required
3. which proof was missing or invalid
4. where execution stopped
5. what receipt proves the non-execution

Without that, the system may have commentary, review, or theatre.

It does not yet have control.

---

## Design principles

- Stop is a first-class primitive.
- Authority is checked before mutation.
- Ambiguity fails closed.
- Receipts are written for refusal, not just success.
- Tests must prove bypass failure, not only happy paths.
- Public artefacts should be small enough to inspect.
- Claims should be no larger than the evidence can carry.

---

## Work with me

I help teams turn AI governance from policy language into auditable runtime control.

Useful problems include:

- AI systems that need deterministic stop mechanisms
- approval flows that must bind before action
- high-risk automation with audit requirements
- governance claims that need executable proof
- messy repositories that need to become inspectable artefacts

Email: **ricky.mcjones@gmail.com**  
LinkedIn: [linkedin.com/in/ricky-jones-1b745474](https://linkedin.com/in/ricky-jones-1b745474)  
GitHub Sponsors: [github.com/sponsors/LalaSkye](https://github.com/sponsors/LalaSkye)

---

## Authorship

All architecture, methods, and system designs across this profile and its repositories are the original work of **Ricky Dean Jones** unless otherwise stated.

Repository licences govern code use. Broader architecture, method, and authorship claims require explicit permission where not otherwise licensed.

**Status:** active research and engineering work.
