# Reliability Gate (Axiom XI)
## Constitutional Minimum‑Reliability Requirement for Safety‑Critical Systems

The Reliability Gate is the eleventh constitutional axiom and the third gate in
the Safety‑Critical Systems Framework. It enforces the requirement that a
system’s reliability — the probability of correct operation under all expected
conditions — must remain **above the constitutional minimum reliability
threshold**.

This gate parallels the  
**[Reproducibility Gate (Axiom VIII)](ca://s?q=Open_Reproducibility_Gate)**  
in the pharma domain.

Normative Reference:  
Russell, “Constitutional Safety Mathematics” (SSRN‑6900021, 2026)

---

## 1. Axiom XI — Reliability Condition

A safety‑critical system \(S\) is constitutionally admissible only if:

\[
\text{Reliability}(S) \geq \theta_{\text{reliability}}
\]

Where:

- \(\text{Reliability}(S)\) is a WAD‑scaled reliability metric  
- \(\theta_{\text{reliability}}\) is the constitutional minimum reliability threshold  
- Both expressed in \(10^{18}\) fixed‑point (WAD)

If this predicate fails, the system is **non‑admissible**, regardless of
exposure or integrity.

---

## 2. Threshold Definition (WAD)

The constitutional reliability threshold is defined as:

\[
\theta_{\text{reliability}} = \gamma \times 10^{18}
\]

Where \(\gamma\) is the minimum acceptable reliability fraction.

Examples:

- 97% reliability → \(0.97 \times 10^{18}\)  
- 99% reliability → \(0.99 \times 10^{18}\)

Thresholds are:

- explicit  
- immutable  
- domain‑anchored  

---

## 3. Predicate Definition

The Reliability Gate predicate is:

\[
P_{\text{ReliabilityGate}}(S) =
\left( \text{Reliability}(S) \geq \theta_{\text{reliability}} \right)
\]

This predicate is:

- deterministic  
- stateless  
- WAD‑scaled  
- constitutionally binding  

---

## 4. Hard Breach Classification

A violation of Axiom XI is a **hard breach**.

Consequences:

- system cannot enter Safety F2  
- system cannot be considered for Safety F3  
- system must be shut down, isolated, or rejected  
- no remediation is possible  

This is a constitutional red line.

---

## 5. Finding (F)

Example finding:

- “Reliability below constitutional minimum (Axiom XI).”

Findings must be:

- deterministic  
- human‑readable  
- anchored to the axiom  

---

## 6. Remedy (R)

The remedy for violating Axiom XI is:

- “System must be shut down or isolated per Axiom XI — reliability below constitutional limit.”

Remedies are:

- explicit  
- non‑negotiable  
- anchored to the axiom  

---

## 7. Implementation Independence

This document defines the **constitutional layer** only.

Any implementation (avionics, robotics, medical devices, autonomous systems,
Solidity, Rust, hardware, etc.) must:

- preserve the reliability predicate  
- preserve the WAD threshold  
- preserve deterministic evaluation  
- preserve hard breach semantics  

The Reliability Gate is implementation‑agnostic.
