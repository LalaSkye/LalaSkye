# Ricky Jones

**Constraint-First Systems Architect** | London, UK

I design deterministic control primitives for AI systems.

My work focuses on **pre-execution governance**: explicit authority, halt-first design, and minimising degrees of freedom before optimisation is introduced. The core claim is that governance belongs *upstream* of action — at the interpretation layer — not downstream of execution.

This profile contains small, auditable public primitives.
Composition and orchestration logic remain private by design.

---

## Core Thesis

**Everyone else governs whether an action may execute. This work governs whether an interpretation may exist.**

Between a raw signal and an executed action, there is an interpretation step. That step introduces assumptions, collapses ambiguity, expands scope, and attributes intent. None of these operations are neutral. All of them can be tested against formal rules — *before any execution-layer question is even asked*.

Current field (Faramesh, Thinking OS, POLARIS) gates at the execution boundary. This work gates one full layer upstream: at meaning construction itself.

---

## Architecture

```
environment
       |
signal
       |
interpretation proposal    <-- meaning construction boundary
       |
interpretation admissibility   <-- 10-rule upstream gate [interpretation-boundary-lab]
       |
  pressure monitoring          <-- 5 sources, 3 signal quality axes
       |
  C-sector rotation            <-- pressure-activated defensive geometry
       |
  state mutation gate          <-- downstream admissibility [dual-boundary-admissibility-lab]
       |
authority gate                 <-- commit boundary [constraint-workshop]
       |
execution boundary             <-- [execution-boundary-lab]
       |
action
       |
audit / evidence               <-- [csgr-lab]
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

Papers: [Zenodo](https://zenodo.org/search?q=ricky%20dean%20jones)
LinkedIn: [linkedin.com/in/ricky-jones-1b745474](https://linkedin.com/in/ricky-jones-1b745474)

---

## Contribution Pattern

Small, auditable tools.
Clear failure modes.
Minimal claims.
Running code over commentary.
