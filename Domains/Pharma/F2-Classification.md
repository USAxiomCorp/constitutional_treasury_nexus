# F2 Classification Standard
## Constitutional Membership Criteria for Pharmaceutical Entities

F2 Classification is the constitutional determination of whether a
pharmaceutical entity qualifies for membership in the **F2 Fixed‑Point Class**.
Only entities that pass all upstream constitutional gates (Purity, Stability,
Reproducibility) may be evaluated for F2 membership.

Normative Reference:  
Russell, “Constitutional Mathematics for Pharma” (SSRN‑6816078, 2026)

---

## 1. Definition of F2

F2 is the **Constitutional Fixed‑Point Class** for pharmaceutical entities that
satisfy:

1. **Axiom VI — Purity Gate**  
2. **Axiom VII — Stability Gate**  
3. **Axiom VIII — Reproducibility Gate**

Only entities that satisfy all three axioms are eligible for F2 evaluation.

---

## 2. F2 Membership Predicate

A pharmaceutical entity \(Y\) is a member of F2 if and only if:

\[
P_{\text{PurityGate}}(Y) = \text{true}
\]
\[
P_{\text{StabilityGate}}(Y) = \text{true}
\]
\[
P_{\text{ReproGate}}(Y) = \text{true}
\]

Thus:

\[
P_{\text{F2}}(Y) =
\left(
P_{\text{PurityGate}}(Y)
\land
P_{\text{StabilityGate}}(Y)
\land
P_{\text{ReproGate}}(Y)
\right)
\]

This predicate is:

- deterministic  
- stateless  
- WAD‑scaled  
- constitutionally binding  

---

## 3. F2 Score (s)

The F2 score is a WAD‑scaled value in \([0,1]\) representing the **quality of
constitutional compliance** across all three gates.

Example scoring model (normative):

\[
s = \frac{
\text{PurityScore} +
\text{StabilityScore} +
\text{ReproScore}
}{3}
\]

Where each component is a WAD‑scaled score in \([0,1]\).

---

## 4. Compliance Flag (c)

The F2 compliance flag is:

- **true** — all three gates satisfied  
- **false** — at least one gate failed  

This is the constitutional admissibility decision for F2 membership.

---

## 5. Hard Breach Flag (h)

If any upstream gate registers a **hard breach**, then:

\[
h = \text{true}
\]

Consequences:

- entity cannot enter F2  
- entity must be rejected  
- no remediation is possible  

Hard breaches override all other considerations.

---

## 6. Finding (F)

Example findings:

- “Entity admitted to F2 — all constitutional gates satisfied.”  
- “Entity rejected — failed Axiom VII (Stability Gate).”  
- “Entity rejected — impurity exceeds constitutional threshold (Axiom VI).”  

Findings must be:

- deterministic  
- human‑readable  
- anchored to predicate outcomes  

---

## 7. Remedy (R)

Remedies depend on the failing gate.

Examples:

- Axiom VI failure → “Batch must be destroyed per Axiom VI.”  
- Axiom VII failure → “Batch must be rejected per Axiom VII.”  
- Axiom VIII failure → “Batch must be rejected per Axiom VIII.”  

If all gates pass:

- “Entity admitted to F2 — no remedy required.”

---

## 8. Implementation Independence

This document defines the **constitutional layer** only.

Any implementation (LIMS, lab systems, Solidity, Rust, hardware, etc.) must:

- preserve the F2 predicate  
- preserve WAD arithmetic semantics  
- preserve deterministic evaluation  
- preserve hard breach semantics  

F2 Classification is implementation‑agnostic.
