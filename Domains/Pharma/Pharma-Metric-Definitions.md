# Pharma Metric Definitions
## WAD‑Scaled Constitutional Metrics for Pharmaceutical Evaluation

Pharma Metric Definitions establish the **formal, WAD‑scaled metrics** used
throughout the Constitutional Pharma Framework. These metrics are the atomic
inputs to the constitutional predicates defined in
**[Constitutional Pharma Mathematics](ca://s?q=Open_Constitutional_Pharma_Mathematics)**,
the constitutional gates, and the fixed‑point class system.

Normative Reference:  
Russell, “Constitutional Mathematics for Pharma” (SSRN‑6816078, 2026)

---

## 1. Metric Domain

Let \(Y\) be a pharmaceutical entity.

Each metric is a deterministic function:
\[
m_i : Y \rightarrow [0, 10^{18}]
\]

All metrics are expressed in **WAD (1e18) fixed‑point**, as defined in the  
**[WAD Arithmetic Standard](ca://s?q=Open_WAD_Arithmetic_Standard)**.

---

## 2. Impurity Metric

### 2.1 Definition
\[
\text{Impurity}(Y) \in [0, 10^{18}]
\]

Represents the fraction of impurity present in entity \(Y\).

### 2.2 Interpretation
- `0` → perfectly pure  
- `1e18` → 100% impurity (invalid state)  
- `1e15` → 0.1% impurity  

### 2.3 Constitutional Use
Used by:
- **[Purity Gate (Axiom VI)](ca://s?q=Open_Purity_Gate)**  
- **[F2 Classification](ca://s?q=Open_F2_Classification)**  
- **[F3 Advanced Classification](ca://s?q=Open_F3_Advanced_Classification)**  

---

## 3. Stability Metric

### 3.1 Definition
\[
\text{Stability}(Y) \in [0, 10^{18}]
\]

Represents the structural, chemical, or thermal stability of entity \(Y\).

### 3.2 Interpretation
- `1e18` → perfectly stable  
- `0.95e18` → 95% stability  
- `0.80e18` → borderline stability  

### 3.3 Constitutional Use
Used by:
- **[Stability Gate (Axiom VII)](ca://s?q=Open_Stability_Gate)**  
- **[F2 Classification](ca://s?q=Open_F2_Classification)**  
- **[F3 Advanced Classification](ca://s?q=Open_F3_Advanced_Classification)**  

---

## 4. Reproducibility Metric

### 4.1 Definition
\[
\text{Reproducibility}(Y) \in [0, 10^{18}]
\]

Represents cross‑batch consistency.

### 4.2 Interpretation
- `1e18` → perfect reproducibility  
- `0.97e18` → 97% reproducibility  
- `0.90e18` → borderline reproducibility  

### 4.3 Constitutional Use
Used by:
- **[Reproducibility Gate (Axiom VIII)](ca://s?q=Open_Reproducibility_Gate)**  
- **[F2 Classification](ca://s?q=Open_F2_Classification)**  
- **[F3 Advanced Classification](ca://s?q=Open_F3_Advanced_Classification)**  

---

## 5. Derived Metrics

### 5.1 Composite Quality Metric
\[
\text
