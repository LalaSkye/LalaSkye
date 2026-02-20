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

## Repository Architecture

The repositories below form a coherent control layer stack.

---

### 🛑 stop-machine  
Finite-state stop controller (GREEN → AMBER → RED).  
RED is absorbing. Deterministic transitions. Fully tested.

**Purpose:** Make "halt" a mechanical property of the system rather than a policy suggestion.

---

### 🔒 invariant-lock  
Hash-based invariant locking for configuration and execution boundaries.

**Purpose:** Prevent silent drift in systems that must remain stable over time.

---

### 🧪 constraint-workshop  
Public workbench of small deterministic control primitives.

**Purpose:** Publish the bricks, not the aircraft blueprint.

---

### 📚 deterministic-lexicon  
Typed, versioned language primitives for reducing ambiguity in AI governance contexts.

**Purpose:** Reduce interpretive drift by constraining vocabulary.

---

### 🧹 policy-lint  
Static analysis for detecting ambiguity, missing halt semantics, and weak constraint definitions in policy text.

**Purpose:** Make policy mechanically inspectable.

---

### ⚙ execution-boundary-lab  
Experimental boundary-testing primitives exploring admissibility and explicit authority gates.

**Purpose:** Stress-test execution assumptions before deployment.

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
