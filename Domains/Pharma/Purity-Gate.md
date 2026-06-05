# Purity Gate (Axiom VI)
## Constitutional Impurity Threshold for Pharmaceutical Entities

The Purity Gate is the sixth constitutional axiom governing pharmaceutical
reproducibility. It establishes the **maximum admissible impurity threshold**
for any pharmaceutical entity before it can be classified, evaluated, or
considered for fixed‑point membership in F2.

Normative Reference:  
Russell, “Constitutional Mathematics for Pharma” (SSRN‑6816078, 2026)

---

## 1. Axiom VI — Impurity Threshold

A pharmaceutical entity \(Y\) is constitutionally admissible only if:

\[
\text{Impurity}(Y) \leq \theta_{\text{impurity}}
\]

Where:

- \(\text{Impurity}(Y)\) is a WAD‑scaled impurity ratio  
- \(\theta_{\text{impurity}}\) is the constitutional impurity threshold  
- Both values are expressed in \(10^{18}\) fixed‑point (WAD)  

If this predicate fails, the entity is **non‑admissible**, regardless of any
other properties.

---

## 2. Threshold Definition (WAD)

The constitutional impurity threshold is defined as:

\[
\theta_{\text{impurity}} = \alpha \times 10^{18}
\]

Where \(\alpha\) is the maximum allowable impurity fraction.

Examples:

- 0.1% impurity → \(0.001 \times 10^{18}\)  
- 0.01% impurity → \(0.0001 \times 10^{18}\)  

Thresholds are:

- explicit  
- immutable  
- domain‑anchored  

---

## 3. Predicate Definition

The Purity Gate predicate is:

\[
P_{\text{PurityGate}}(Y) =
\left( \text{Impurity}(Y) \leq \theta_{\text{impurity}} \right)
\]

This predicate is:

- deterministic  
- stateless  
- WAD‑scaled  
- constitutionally binding  

---

## 4. Hard Breach Classification

A violation of Axiom VI is a **hard breach**.

Hard breach consequences:

- entity cannot enter F2  
- entity cannot be evaluated by downstream gates  
- entity must be rejected or destroyed  
- no remediation is possible  

This is a constitutional red line.

---

## 5. Finding (F)

Example finding:

- “Impurity exceeds constitutional threshold (Axiom VI).”

Findings must be:

- deterministic  
- human‑readable  
- anchored to the axiom  

---

## 6. Remedy (R)

The remedy for violating Axiom VI is:

- “Batch must be destroyed per Axiom VI — impurity exceeds constitutional limit.”

Remedies are:

- explicit  
- non‑negotiable  
- anchored to the axiom  

---

## 7. Implementation Independence

This document defines the **constitutional layer** only.

Any implementation (lab system, LIMS, Solidity, Rust, hardware, etc.) must:

- preserve the impurity predicate  
- preserve the WAD threshold  
- preserve deterministic evaluation  
- preserve hard breach semantics  

The Purity Gate is implementation‑agnostic.
