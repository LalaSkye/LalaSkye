# Ricky Jones — execution-boundary engineer

I build bounded, inspectable controls at the point of authorisation for
AI-supported systems. The objects named below are reference demonstrations,
not production enforcement.

## Core question

> **Where does the system physically stop?**

The work focuses on execution-boundary control, admissibility, refusal, authority, receipts, and replay.

## Public inspection standard

```text
claim → evidence object → inspection path → claim limit
```

Public GitHub is an inspection surface, not full architecture disclosure.

## Three public inspection objects

These three names are the admitted public inspection class. They are the
objects this profile asks a reader to inspect.

- [stop-machine](https://github.com/LalaSkye/stop-machine) — current public halt primitive and canonical starting link
- [commit-gate-core](https://github.com/LalaSkye/commit-gate-core) — authorize-only kernel: binds exact payload bytes to a DecisionRecord and returns authorisation or refusal; it does not apply the payload
- [obligation-bound-policy-admission-lab](https://github.com/LalaSkye/obligation-bound-policy-admission-lab) — single-engine reference harness: historical admission ≠ current standing ≠ observed active state; not a gate

These are separate objects. Do not inherit proofs across them.

Historical, superseded inspection artefact: [start-here](https://github.com/LalaSkye/start-here) — earlier entry demo retained for inspection only; superseded as the public halt primitive by stop-machine. Its demonstrated path claim stays bounded to start-here and does not transfer to stop-machine.

Routing index (not a fourth object): [inspection-surface](https://lalaskye.github.io/inspection-surface/)

## Other public repositories

The account also contains other public repositories — labs, scaffolds, indexes,
and earlier experiments. A public name is not admission to the inspection class
above. Those repositories do not inherit proofs from the three objects, and the
three objects do not inherit proofs from them.

The Repositories tab is GitHub's inventory. It is not the inspection class.

## What this work proves

Each of the three inspection objects supports one local claim with an inspectable
evidence object and an explicit stopping point.

## What this work does not prove

Unless explicitly stated, these artefacts do not prove:

- production readiness
- compliance or certification
- enterprise deployment
- adoption or standardisation
- path-universal governance
- full architecture disclosure

## Evidence and authorship boundary

Repository-level authorship and contribution statements are recorded in each
object. GitHub timestamps establish public possession at the recorded dates;
they do not by themselves establish novelty, category priority or copying.

## Contact

LinkedIn: [linkedin.com/in/ricky-jones-trinityos](https://www.linkedin.com/in/ricky-jones-trinityos)

**Status:** active research and engineering work.
