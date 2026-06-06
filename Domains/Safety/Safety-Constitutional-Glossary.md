# Safety Constitutional Glossary
## Canonical Definitions for Constitutional Safety‑Critical Evaluation

The Safety Constitutional Glossary provides the **authoritative definitions**
for all terms used across the Constitutional Safety Framework. These terms are
normative and binding across:

- **[Safety Metric Definitions](ca://s?q=Open_Safety_Metric_Definitions)**
- **[Safety‑Critical Systems Overview](ca://s?q=Open_Safety_Critical_Systems_Overview)**
- **[Exposure, Integrity, Reliability Gates](ca://s?q=Open_Axiom_Index)**
- **[Safety F2 Classification](ca://s?q=Open_Safety_F2_Classification)**
- **[Safety F3 Classification](ca://s?q=Open_Safety_F3_Classification)**
- **[Deterministic Evaluation Standard](ca://s?q=Open_Deterministic_Evaluation_Standard)**

Normative Reference:  
Russell, “Constitutional Safety Mathematics” (SSRN‑6900021, 2026)

---

## 1. Admissibility
Whether a safety‑critical system is eligible for constitutional evaluation.
Determined by:

- **[Safety Validation Envelope](ca://s?q=Open_Safety_Validation_Envelope)**
- constitutional safety gate predicates

---

## 2. Axiom
A constitutional rule governing admissibility.  
Safety uses:

- **Axiom IX — Exposure Gate**
- **Axiom X — Integrity Gate**
- **Axiom XI — Reliability Gate**

Indexed in the  
**[Axiom Index](ca://s?q=Open_Axiom_Index)**.

---

## 3. System
A safety‑critical entity under evaluation.  
Schema defined in the  
**[Safety Data Model](ca://s?q=Open_Safety_Data_Model)**.

---

## 4. Constitutional Gate
A deterministic predicate enforcing a constitutional requirement:

- **[Exposure Gate](ca://s?q=Open_Exposure_Gate)**
- **[Integrity Gate](ca://s?q=Open_Integrity_Gate)**
- **[Reliability Gate](ca://s?q=Open_Reliability_Gate)**

All must pass before F2 evaluation.

---

## 5. Constitutional Threshold
A WAD‑scaled constant defining the minimum or maximum allowable value for a
safety metric. Examples:

- \(\theta_{\text{exposure}}\)
- \(\theta_{\text{integrity}}\)
- \(\theta_{\text{reliability}}\)

Defined in the safety axioms.

---

## 6. Excellence Margin
A WAD‑scaled margin above constitutional minima used for F3 classification:

- \(\delta_{\text{exposure}}\)
- \(\delta_{\text{integrity}}\)
- \(\delta_{\text{reliability}}\)

Defined in  
**[Safety F3 Classification](ca://s?q=Open_Safety_F3_Classification)**.

---

## 7. Evaluation Tuple
The deterministic output of constitutional evaluation:

\[
(s, c, h, F, R)
\]

Defined in the  
**[Deterministic Evaluation Standard](ca://s?q=Open_Deterministic_Evaluation_Standard)**.

---

## 8. Hard Breach
Violation of a constitutional red line.  
Occurs when:

- exposure > threshold  
- integrity < threshold  
- reliability < threshold  

Hard breaches require shutdown, isolation, or rejection.

---

## 9. Exposure
A WAD‑scaled metric representing hazard, load, or risk fraction.  
Defined in  
**[Safety Metric Definitions](ca://s?q=Open_Safety_Metric_Definitions)**.

---

## 10. Integrity
A WAD‑scaled metric representing structural, mechanical, logical, or cryptographic integrity.  
Defined in  
**[Safety Metric Definitions](ca://s?q=Open_Safety_Metric_Definitions)**.

---

## 11. Reliability
A WAD‑scaled metric representing probability of correct operation.  
Defined in  
**[Safety Metric Definitions](ca://s?q=Open_Safety_Metric_Definitions)**.

---

## 12. Validation Envelope
The admissible domain for all safety metrics:

- exposure ∈ \([0, 1e18]\)
- integrity ∈ \([0, 1e18]\)
- reliability ∈ \([0, 1e18]\)

Defined in  
**[Safety Validation Envelope](ca://s?q=Open_Safety_Validation_Envelope)**.

---

## 13. WAD (1e18 Fixed‑Point)
The universal scaling system for all constitutional metrics.  
Defined in  
**[Pharma WAD Scaling](ca://s?q=Open_Pharma_WAD_Scaling)**.

---

## 14. F‑Classes
Fixed‑point constitutional classes:

- F0 — non‑admissible  
- F1 — diagnostic  
- F2 — constitutionally admissible  
- F3 — exceeds constitutional minima  

Defined in:

- **[Safety F2 Classification](ca://s?q=Open_Safety_F2_Classification)**
- **[Safety F3 Classification](ca://s?q=Open_Safety_F3_Classification)**

---

## 15. Error Condition
A deterministic failure state that prevents evaluation.  
Defined in  
**[Safety Error Conditions](ca://s?q=Open_Safety_Error_Conditions)**.

---

## 16. Predicate
A boolean function determining compliance with a constitutional rule.  
Examples:

- \(P_{\text{ExposureGate}}\)
- \(P_{\text{IntegrityGate}}\)
- \(P_{\text{ReliabilityGate}}\)

---

## 17. Score
A WAD‑scaled value in \([0,1]\) representing quality of compliance.

---

## 18. Remedy
A deterministic instruction tied to a constitutional or regulatory anchor.

---

## 19. Finding
A human‑readable explanation of evaluation outcome.

---

## 20. Implementation Independence
The requirement that all constitutional behavior must be preserved across:

- avionics  
- autonomous vehicles  
- medical devices  
- industrial robotics  
- nuclear systems  
- embedded controllers  
- Rust, Solidity, TypeScript, hardware  

---

This glossary is the canonical reference for all constitutional safety terms.
