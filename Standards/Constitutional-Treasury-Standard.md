# Constitutional Treasury Standard
## Deterministic, WAD‑Scaled Treasury Evaluation Framework

The Constitutional Treasury Standard defines how treasury, liquidity, funding,
and capital constraints are expressed as **constitutional predicates** and
**WAD‑scaled thresholds**. It ensures that all treasury evaluations are
deterministic, auditable, and anchored to statutory regulatory text.

Normative Reference:  
Russell, “Constitutional Mathematics for Treasury Systems” (SSRN‑6609638, 2026)

---

## 1. Purpose

This standard replaces heuristic treasury models with:

- deterministic predicate evaluation  
- fixed‑point WAD arithmetic  
- explicit regulatory anchors  
- reproducible findings and remedies  

It defines the **constitutional layer**, not the implementation layer.

---

## 2. Treasury Predicate Classes

Treasury constraints fall into four constitutional predicate classes:

### 2.1 Liquidity Predicates
Examples:
- `LCR.MinFloor` — Liquidity Coverage Ratio ≥ statutory minimum  
- `HQLA.Structure` — Level 1 + Level 2A + Level 2B composition rules  
- `InflowCap` — inflows ≤ 75% of outflows  

### 2.2 Funding Stability Predicates
Examples:
- `NSFR.MinFloor` — ASF / RSF ≥ 100%  
- `ASF.Classification` — liability stability factors  
- `RSF.AssetFactors` — asset liquidity risk factors  

### 2.3 Capital Adequacy Predicates
Examples:
- `CET1.Min` — CET1 ≥ base + buffers  
- `Tier1.Min` — Tier 1 ≥ statutory minimum  
- `Leverage.Min` — leverage ratio ≥ jurisdictional floor  

### 2.4 Hard‑Breach Predicates
These represent constitutional “red lines”:
- CET1 < base minimum  
- LCR < critical floor  
- NSFR < hard breach threshold  

Hard breaches always trigger immediate remedies.

---

## 3. WAD‑Scaled Thresholds

All thresholds are expressed as WAD constants:

- 100% → `1e18`  
- 80% → `0.8e18`  
- 2.5% buffer → `0.025e18`  
- 250 bps → `250 * 1e14`  

This ensures:

- exactness  
- cross‑implementation reproducibility  
- formal verifiability  

---

## 4. Constitutional Evaluation Tuple

Given input state \(x\), the evaluation function produces:

\[
E(x) \rightarrow (s, c, h, F, R)
\]

Where:

- **s** — WAD‑scaled score  
- **c** — compliant / non‑compliant  
- **h** — hard breach flag  
- **F** — finding (plain language)  
- **R** — remedy (statute‑anchored)  

This tuple is:

- deterministic  
- stateless  
- auditable  

---

## 5. Regulatory Anchors

Each predicate is mapped to a regulatory anchor:

- Basel III / Basel IV  
- Dodd‑Frank 165  
- 12 CFR 249 (LCR)  
- 12 CFR 249 Subpart P (NSFR)  
- 12 CFR 3 / 217 / 324 (Capital)  

Anchors include:

- citation  
- paragraph reference  
- threshold source  
- remedy text  

---

## 6. Findings and Remedies

### Findings
Plain‑language explanations of predicate outcomes.

Example:
- “LCR below statutory minimum.”

### Remedies
Explicit instructions tied to regulatory text.

Example:
- “Notify primary regulator within 24 hours (12 CFR 249.30).”

---

## 7. Implementation Independence

This standard does **not** prescribe a programming language.

Any implementation must preserve:

- predicate truth conditions  
- WAD arithmetic semantics  
- invariant behavior  
- deterministic evaluation  
- regulatory anchor integrity  

The constitutional layer is implementation‑agnostic.
