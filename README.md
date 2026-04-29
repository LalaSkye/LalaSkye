# Ricky Jones

**Execution-Boundary Governance · Fail-Closed AI Systems · Runtime Control**

I build small, auditable systems that stop unsafe AI actions
before they become real.

Most AI governance explains what *should* happen.
My work asks a harder question:

> Where does the system physically stop?

---

## Start here

- [`commit-gate-core`](https://github.com/LalaSkye/commit-gate-core) — no state mutation without a valid DecisionRecord
- [`artifact-readiness-engine`](https://github.com/LalaSkye/artifact-readiness-engine) — turns messy repos into runnable, auditable project artefacts

If the gate cannot prove authority, scope, freshness, and replay
safety, the action does not run.

It holds.

---

## Repo Triage

I help founders and small teams turn messy GitHub repos into clean,
runnable, auditable projects.

Fixed-price repo triage available:

- install / build check
- README and setup review
- failure points identified
- clear fix plan before cleanup

[Get in touch →](mailto:ricky.mcjones@gmail.com)

---

## Core Thesis

**Much of the field focuses on whether an action may execute. My work also examines the earlier boundary where interpretation becomes admissible.**

Between a raw signal and an executed action, there is an interpretation step. That step introduces assumptions, collapses ambiguity, expands scope, and attributes intent. None of these operations are neutral. All of them can be tested against formal rules — *before any execution-layer question is even asked*.

Current field (Faramesh, Thinking OS, POLARIS) gates at the execution boundary. This work gates one full layer upstream: at meaning construction itself.

---

## Why follow

Small, auditable Python primitives for AI governance: commit gates, stop machines, invariant locks, policy linting, replay resistance, and fail-closed control surfaces.

---

## Architecture

```
environment
  |
signal
  |
interpretation proposal   <-- meaning construction boundary
  |
interpretation admissibility   <-- 10-rule upstream gate [interpretation-boundary-lab]
  |
pressure monitoring   <-- 5 sources, 3 signal quality axes
  |
C-sector rotation   <-- pressure-activated defensive geometry
  |
state mutation gate   <-- downstream admissibility [dual-boundary-admissibility-lab]
  |
authority gate   <-- commit boundary [constraint-workshop]
  |
execution boundary   <-- [execution-boundary-lab]
  |
action
  |
audit / evidence   <-- [csgr-lab]
```

Every layer is fail-closed: if a gate cannot determine admissibility, execution does not proceed.

---

## Repository Architecture

### The Corridor

| Repo | Layer | Tests | What It Does |
|---|---|---|---|
| [interpretation-boundary-lab](https://github.com/LalaSkye/interpretation-boundary-lab) | Upstream boundary | 81 | 10-rule admissibility gate for interpretation proposals |
| [dual-boundary-admissibility-lab](https://github.com/LalaSkye/dual-boundary-admissibility-lab) | Full corridor | 261 | Dual-boundary model with pressure monitoring and C-sector rotation |
| [execution-boundary-lab](https://github.com/LalaSkye/execution-boundary-lab) | Execution boundary | - | Demonstrates cascading failures without upstream governance |

### Control Primitives

| Repo | Layer | What It Does |
|---|---|---|
| [stop-machine](https://github.com/LalaSkye/stop-machine) | Halt primitive | Deterministic three-state stop controller. Once RED, nothing runs. |
| [constraint-workshop](https://github.com/LalaSkye/constraint-workshop) | Primitive composition | Authority gate, invariant litmus, stop machine — composable bricks |
| [invariant-lock](https://github.com/LalaSkye/invariant-lock) | Drift prevention | Refuse execution unless invariant version increments |
| [deterministic-lexicon](https://github.com/LalaSkye/deterministic-lexicon) | Vocabulary | Fixed terms, exact matches, no inference |
| [policy-lint](https://github.com/LalaSkye/policy-lint) | Policy validation | Deterministic linter for governance statements |

### Measurement

| Repo | Layer | What It Does |
|---|---|---|
| [csgr-lab](https://github.com/LalaSkye/csgr-lab) | Audit / evidence | Contracted stability and drift measurement for LLMs |

---

## Canonical Vocabulary

| Term | Meaning |
|---|---|
| **interpretation admissibility** | Gating whether meaning construction is structurally sound before it reaches verdict |
| **commit boundary** | The point at which a decision becomes irreversible |
| **authority gate** | A check that execution has explicit, evidence-backed permission |
| **fail-closed control** | If a gate cannot decide, execution does not proceed |
| **C-sector rotation** | Pressure-activated defensive geometry — interrupt vector rotates into control path |

---

## Design Principles

- Determinism over optimisation
- Explicit authority required for execution
- Stop is a first-class primitive
- Shrink degrees of freedom before adding complexity
- Tests are mandatory
- Public artefacts do not expose private orchestration

---

## Research and Publications

LinkedIn: [linkedin.com/in/ricky-jones-1b745474](https://linkedin.com/in/ricky-jones-1b745474)

---

## Work With Me

I consult on AI governance architecture, runtime constraint design, and EU AI Act compliance tooling.

If your team is building AI systems that need deterministic governance, auditable policy enforcement, or compliant stop mechanisms — I can help.

→ **ricky.mcjones@gmail.com**
→ [LinkedIn](https://linkedin.com/in/ricky-jones-1b745474)
→ [GitHub Sponsors](https://github.com/sponsors/LalaSkye)

---

## Contribution Pattern

Small, auditable tools. Clear failure modes. Minimal claims. Running code over commentary.

---

## Authorship & Rights

All architecture, methods, and system designs across this profile and its repositories are the original work of **Ricky Dean Jones** unless otherwise stated.

No rights to use, reproduce, or implement are granted without explicit permission beyond the terms of each repository licence.

**Author:** Ricky Dean Jones
**GitHub:** [LalaSkye](mailto:ricky.mcjones@gmail.com)
**Organisation:** Os-Trilogy LMT / AlvianTech
**Status:** Active research / architecture work
