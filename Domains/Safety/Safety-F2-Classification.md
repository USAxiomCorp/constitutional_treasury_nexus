# Safety F2 Classification
## Constitutional Admissibility Class for Safety‑Critical Systems

Safety F2 is the **constitutional admissibility class** for safety‑critical
systems. A system enters F2 only after satisfying all three safety gates:

- **[Exposure Gate (Axiom IX)](ca://s?q=Open_Exposure_Gate)**
- **[Integrity Gate (Axiom X)](ca://s?q=Open_Integrity_Gate)**
- **[Reliability Gate (Axiom XI)](ca://s?q=Open_Reliability_Gate)**

This class is the safety‑domain analogue of  
**[Pharma F2 Classification](ca://s?q=Open_F2_Classification)**.

Normative Reference:  
Russell, “Constitutional Safety Mathematics” (SSRN‑6900021, 2026)

---

## 1. Definition of Safety F2

A safety‑critical system \(S\) qualifies for F2 if:

\[
P_{\text{ExposureGate}}(S)
\land
P_{\text{IntegrityGate}}(S)
\land
P_{\text{ReliabilityGate}}(S)
\]

Where each predicate is deterministic, WAD‑scaled, and constitutionally binding.

If any predicate fails, the system is **not admissible** and cannot proceed to
F3.

---

## 2. F2 Predicate

The F2 predicate is:

\[
P_{\text{SafetyF2}}(S) =
P_{\text{ExposureGate}}(S)
\land
P_{\text{IntegrityGate}}(S)
\land
P_{\text{ReliabilityGate}}(S)
\]

This predicate is:

- boolean  
- stateless  
- deterministic  
- implementation‑independent  

---

## 3. F2 Score (s)

The F2 score is a WAD‑scaled value in \([0,1]\) representing **compliance with
constitutional minima**, not excellence.

Example scoring model:

\[
s =
\frac{
\min\left(1, \frac{\theta_{\text{exposure}}}{\text{Exposure}(S)}\right)
+
\frac{\text{Integrity}(S)}{\theta_{\text{integrity}}}
+
\frac{\text{Reliability}(S)}{\theta_{\text{reliability}}}
}{3}
\]

This score:

- is deterministic  
- is not used for F3  
- cannot override a hard breach  

---

## 4. Compliance Flag (c)

For F2:

- **true** — system satisfies all three safety gates  
- **false** — system fails at least one gate  

Compliance is binary and cannot be probabilistic.

---

## 5. Hard Breach Flag (h)

If any gate registers a hard breach:

\[
h = \text{true}
\]

Consequences:

- system cannot enter F2  
- system must be shut down or isolated  
- no remediation is possible  

Hard breaches override all other considerations.

---

## 6. Finding (F)

Example findings:

- “System admitted to Safety F2 — satisfies all constitutional safety gates.”  
- “System rejected — failed Axiom X (Integrity Gate).”  

Findings must be:

- deterministic  
- human‑readable  
- anchored to predicate outcomes  

---

## 7. Remedy (R)

If F2 criteria are met:

- “System admitted to Safety F2 — no remedy required.”

If any gate fails:

- “System must be shut down or isolated per constitutional safety axiom.”

---

## 8. Implementation Independence

This document defines the **constitutional layer**, not the implementation.

Any implementation (avionics, robotics, medical devices, autonomous systems,
Solidity, Rust, hardware, etc.) must:

- preserve F2 predicate semantics  
- preserve WAD arithmetic  
- preserve deterministic evaluation  
- preserve hard breach semantics  
- preserve fixed‑point class hierarchy  

Safety F2 is universal and implementation‑agnostic.
