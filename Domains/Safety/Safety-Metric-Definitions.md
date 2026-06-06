# Safety Metric Definitions
## WAD‑Scaled Constitutional Metrics for Safety‑Critical Systems

Safety Metric Definitions establish the **formal, WAD‑scaled metrics** used
throughout the Constitutional Safety Framework. These metrics are the atomic
inputs to the constitutional safety predicates defined in  
**[Safety‑Critical Systems Overview](ca://s?q=Open_Safety_Critical_Systems_Overview)**  
and the safety gates:

- **[Exposure Gate (Axiom IX)](ca://s?q=Open_Exposure_Gate)**
- **[Integrity Gate (Axiom X)](ca://s?q=Open_Integrity_Gate)**
- **[Reliability Gate (Axiom XI)](ca://s?q=Open_Reliability_Gate)**

Normative Reference:  
Russell, “Constitutional Safety Mathematics” (SSRN‑6900021, 2026)

---

## 1. Metric Domain

Let \(S\) be a safety‑critical system.

Each metric is a deterministic function:
\[
m_i : S \rightarrow [0, 10^{18}]
\]

All metrics use **WAD (1e18) fixed‑point scaling**, as defined in  
**[Pharma WAD Scaling](ca://s?q=Open_Pharma_WAD_Scaling)**  
(which is reused across all constitutional domains).

---

## 2. Exposure Metric

### 2.1 Definition
\[
\text{Exposure}(S) \in [0, 10^{18}]
\]

Represents the fraction of maximum allowable hazard, load, or risk the system is
subjected to.

### 2.2 Interpretation
- `0` → zero exposure  
- `1e18` → full exposure (catastrophic)  
- `5e17` → 50% of maximum allowable exposure  

### 2.3 Constitutional Use
Used by:
- **[Exposure Gate (Axiom IX)](ca://s?q=Open_Exposure_Gate)**
- **[Safety F2 Classification](ca://s?q=Open_Safety_F2_Classification)**
- **[Safety F3 Classification](ca://s?q=Open_Safety_F3_Classification)**

---

## 3. Integrity Metric

### 3.1 Definition
\[
\text{Integrity}(S) \in [0, 10^{18}]
\]

Represents structural, mechanical, logical, or cryptographic integrity.

### 3.2 Interpretation
- `1e18` → perfect integrity  
- `9.5e17` → 95% integrity  
- `8e17` → borderline integrity  

### 3.3 Constitutional Use
Used by:
- **[Integrity Gate (Axiom X)](ca://s?q=Open_Integrity_Gate)**
- **[Safety F2 Classification](ca://s?q=Open_Safety_F2_Classification)**
- **[Safety F3 Classification](ca://s?q=Open_Safety_F3_Classification)**

---

## 4. Reliability Metric

### 4.1 Definition
\[
\text{Reliability}(S) \in [0, 10^{18}]
\]

Represents the probability of correct operation under all expected conditions.

### 4.2 Interpretation
- `1e18` → perfect reliability  
- `9.9e17` → 99% reliability  
- `9.7e17` → 97% reliability  

### 4.3 Constitutional Use
Used by:
- **[Reliability Gate (Axiom XI)](ca://s?q=Open_Reliability_Gate)**
- **[Safety F2 Classification](ca://s?q=Open_Safety_F2_Classification)**
- **[Safety F3 Classification](ca://s?q=Open_Safety_F3_Classification)**

---

## 5. Derived Metrics

### 5.1 Composite Safety Metric
\[
\text{SafetyQuality}(S) =
\frac{
\text{Integrity}(S) +
\text{Reliability}(S)
}{2}
\]

Used for diagnostics only (never constitutional).

### 5.2 Distance‑to‑Threshold Metrics
\[
\Delta_{\text{exposure}} =
\theta_{\text{exposure}} - \text{Exposure}(S)
\]

\[
\Delta_{\text{integrity}} =
\text{Integrity}(S) - \theta_{\text{integrity}}
\]

\[
\Delta_{\text{reliability}} =
\text{Reliability}(S) - \theta_{\text{reliability}}
\]

Used by:
- **[Safety F3 Classification](ca://s?q=Open_Safety_F3_Classification)**

---

## 6. Implementation Independence

These metric definitions apply universally across:

- avionics  
- autonomous vehicles  
- medical devices  
- industrial robotics  
- nuclear systems  
- embedded controllers  
- Rust, Solidity, TypeScript, hardware  

Any implementation must preserve:

- WAD scaling  
- deterministic metric computation  
- constitutional threshold semantics  
- predicate compatibility  

Safety metrics are universal and implementation‑agnostic.
