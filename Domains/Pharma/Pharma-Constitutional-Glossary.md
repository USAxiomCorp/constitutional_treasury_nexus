# Pharma Constitutional Glossary
## Canonical Definitions for Constitutional Pharmaceutical Evaluation

The Pharma Constitutional Glossary provides the **authoritative definitions**
for all terms used across the Constitutional Pharma Framework. These terms are
normative and binding across:

- **[Pharma Metric Definitions](ca://s?q=Open_Pharma_Metric_Definitions)**
- **[Constitutional Pharma Mathematics](ca://s?q=Open_Constitutional_Pharma_Mathematics)**
- **[Purity, Stability, Reproducibility Gates](ca://s?q=Open_Axiom_Index)**
- **[F2 Classification](ca://s?q=Open_F2_Classification)**
- **[F3 Advanced Classification](ca://s?q=Open_F3_Advanced_Classification)**
- **[Deterministic Evaluation Standard](ca://s?q=Open_Deterministic_Evaluation_Standard)**

Normative Reference:  
Russell, “Constitutional Mathematics for Pharma” (SSRN‑6816078, 2026)

---

## 1. Admissibility
Whether a pharmaceutical entity is eligible for constitutional evaluation.
Determined by:

- **[Pharma Validation Envelope](ca://s?q=Open_Pharma_Validation_Envelope)**
- constitutional gate predicates

---

## 2. Axiom
A constitutional rule governing admissibility.  
Pharma uses:

- **Axiom VI — Purity Gate**
- **Axiom VII — Stability Gate**
- **Axiom VIII — Reproducibility Gate**

Indexed in the  
**[Axiom Index](ca://s?q=Open_Axiom_Index)**.

---

## 3. Batch
A manufacturing unit of pharmaceutical production.  
Used for:

- reproducibility analysis  
- cross‑batch evaluation  
- F2/F3 classification  

---

## 4. Constitutional Gate
A deterministic predicate that enforces a constitutional requirement:

- **[Purity Gate](ca://s?q=Open_Purity_Gate)**
- **[Stability Gate](ca://s?q=Open_Stability_Gate)**
- **[Reproducibility Gate](ca://s?q=Open_Reproducibility_Gate)**

All must pass before F2 evaluation.

---

## 5. Constitutional Threshold
A WAD‑scaled constant defining the minimum or maximum allowable value for a
metric. Examples:

- \(\theta_{\text{impurity}}\)
- \(\theta_{\text{stability}}\)
- \(\theta_{\text{repro}}\)

Defined in  
**[Constitutional Pharma Mathematics](ca://s?q=Open_Constitutional_Pharma_Mathematics)**.

---

## 6. Excellence Margin
A WAD‑scaled margin above constitutional minima used for F3 classification:

- \(\delta_{\text{impurity}}\)
- \(\delta_{\text{stability}}\)
- \(\delta_{\text{repro}}\)

Defined in  
**[F3 Advanced Classification](ca://s?q=Open_F3_Advanced_Classification)**.

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

- impurity > threshold  
- stability < threshold  
- reproducibility < threshold  

Hard breaches require rejection or destruction.

---

## 9. Impurity
A WAD‑scaled metric representing contamination fraction.  
Defined in  
**[Pharma Metric Definitions](ca://s?q=Open_Pharma_Metric_Definitions)**.

---

## 10. Reproducibility
A WAD‑scaled metric representing cross‑batch consistency.  
Defined in  
**[Pharma Metric Definitions](ca://s?q=Open_Pharma_Metric_Definitions)**.

---

## 11. Stability
A WAD‑scaled metric representing structural or chemical integrity.  
Defined in  
**[Pharma Metric Definitions](ca://s?q=Open_Pharma_Metric_Definitions)**.

---

## 12. Validation Envelope
The admissible domain for all metrics:

- impurity ∈ \([0, 1e18]\)
- stability ∈ \([0, 1e18]\)
- reproducibility ∈ \([0, 1e18]\)

Defined in  
**[Pharma Validation Envelope](ca://s?q=Open_Pharma_Validation_Envelope)**.

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

- **[F2 Classification](ca://s?q=Open_F2_Classification)**
- **[F3 Advanced Classification](ca://s?q=Open_F3_Advanced_Classification)**

---

## 15. Entity
A pharmaceutical item under evaluation.  
Schema defined in the  
**[Pharma Data Model](ca://s?q=Open_Pharma_Data_Model)**.

---

## 16. Error Condition
A deterministic failure state that prevents evaluation.  
Defined in  
**[Pharma Error Conditions](ca://s?q=Open_Pharma_Error_Conditions)**.

---

## 17. Predicate
A boolean function determining compliance with a constitutional rule.  
Examples:

- \(P_{\text{PurityGate}}\)
- \(P_{\text{StabilityGate}}\)
- \(P_{\text{ReproGate}}\)

---

## 18. Score
A WAD‑scaled value in \([0,1]\) representing quality of compliance.

---

## 19. Remedy
A deterministic instruction tied to a constitutional or regulatory anchor.

---

## 20. Finding
A human‑readable explanation of evaluation outcome.

---

## 21. Implementation Independence
The requirement that all constitutional behavior must be preserved across:

- LIMS  
- lab systems  
- computational pipelines  
- Solidity, Rust, TypeScript, hardware  

---

This glossary is the canonical reference for all constitutional pharma terms.
