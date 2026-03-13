# 🧱 Ricky Jones
**Constraint-First Systems Architect**  
London, UK  

I design deterministic control primitives for AI systems.

My work focuses on **pre-execution governance**: explicit authority, halt-first design, and minimising degrees of freedom before optimisation is introduced.

This profile contains small, auditable public primitives.  
Composition and orchestration logic remain private by design.

---

## Core Thesis

**Governance begins before execution.**

Most AI systems optimise first and constrain later.  
I design systems where:

- Constraints are explicit  
- Execution requires authority  
- Halt is a structural capability  
- Behaviour is deterministic  
- Failure modes are defined in advance  

No narrative compliance.  
No hidden autonomy.  
No optimisation-first architecture.

---

## Architecture

```
environment
       ↓
 signal
       ↓
 interpretation proposal    ← meaning construction boundary
       ↓
 interpretation admissibility   ← pre-verdict gate
       ↓
 admissibility gate         ← pre-execution boundary
       ↓
 authority gate             ← commit boundary
       ↓
 execution boundary
       ↓
 action
       ↓
 audit / evidence
```

Every layer is fail-closed: if a gate cannot determine admissibility, execution does not proceed.

---

## Repository Architecture

The repositories below form a coherent control layer stack.

---

### 🔬 [interpretation-boundary-lab](https://github.com/LalaSkye/interpretation-boundary-lab)
Deterministic admissibility layer for interpretation proposals. 10 named rules, closed graph topology, pressure-activated sector rotation, meaning drift replay.

**Layer:** Interpretation admissibility — gates meaning construction before verdict and execution. Evaluates whether the interpretation that produced a candidate action is itself admissible.

---

### 🛑 [stop-machine](https://github.com/LalaSkye/stop-machine)
Finite-state stop controller (GREEN → AMBER → RED).  
RED is absorbing. Deterministic transitions. Fully tested.

**Layer:** Halt primitive — fail-closed control at the execution boundary.

---

### 🔒 [invariant-lock](https://github.com/LalaSkye/invariant-lock)
Hash-based invariant locking for configuration and execution boundaries.

**Layer:** Drift prevention — fail-closed enforcement at the commit boundary.

---

### 🧪 [constraint-workshop](https://github.com/LalaSkye/constraint-workshop)
Public workbench of deterministic control primitives: stop machines, authority gates, commit gates, and invariant classifiers.

**Layer:** Primitive composition — authority gate, commit boundary, and admissibility logic.

---

### ⚙️ [execution-boundary-lab](https://github.com/LalaSkye/execution-boundary-lab)
Demonstrates how information pre-positioning causes cascading execution failures. Publishes the phenomenon and conformance tests. Gate implementation is private.

**Layer:** Pre-execution admissibility — fail-closed gating before the commit boundary.

---

### 📚 [deterministic-lexicon](https://github.com/LalaSkye/deterministic-lexicon)
Typed, versioned language primitives for reducing ambiguity in AI governance contexts.

**Layer:** Vocabulary control — exact terms, no inference, no drift.

---

### 🧹 [policy-lint](https://github.com/LalaSkye/policy-lint)
Static analysis for detecting ambiguity, missing halt semantics, and weak constraint definitions in policy text.

**Layer:** Admissibility surface — makes governance claims mechanically inspectable.

---

### 📊 [csgr-lab](https://github.com/LalaSkye/csgr-lab)
Contracted Stability & Drift Measurement for LLMs. Deterministic scoring, auditable evidence, reproducible runs.

**Layer:** Audit and evidence — tamper-evident hash chains for contract conformance.

---

## Canonical Vocabulary

These terms are used consistently across all repositories:

| Term | Meaning |
|---|---|
| **commit boundary** | The point at which a decision becomes irreversible |
| **authority gate** | A check that execution has explicit, evidence-backed permission |
| **pre-execution admissibility** | Filtering inputs before they reach the execution boundary |
| **interpretation admissibility** | Gating whether meaning construction is structurally sound before it reaches verdict |
| **fail-closed control** | If a gate cannot decide, execution does not proceed |

---

## Design Principles

- Determinism over optimisation  
- Explicit authority required for execution  
- Stop is a first-class primitive  
- Shrink degrees of freedom before adding complexity  
- Tests are mandatory  
- Public artefacts do not expose private orchestration  

---

## Research & Publications

📄 Zenodo:  
[https://zenodo.org/search?q=ricky%20dean%20jones](https://zenodo.org/search?q=ricky%20dean%20jones)

🔗 LinkedIn:  
[https://linkedin.com/in/ricky-jones-1b745474](https://linkedin.com/in/ricky-jones-1b745474)

---

## Current Focus

- Interpretation admissibility layers  
- Pre-execution admissibility layers  
- Halt-first AI architecture  
- Deterministic control in large model environments  
- Structural governance beyond narrative compliance  

---

## Contribution Pattern

Small, auditable tools.  
Clear failure modes.  
Minimal claims.  
Running code over commentary.
