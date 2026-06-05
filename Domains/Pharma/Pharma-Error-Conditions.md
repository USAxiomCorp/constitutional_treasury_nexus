# Pharma Error Conditions
## Constitutional Error States for Pharmaceutical Evaluation

Pharma Error Conditions define the **deterministic error states** that may occur
before, during, or after constitutional pharmaceutical evaluation. These errors
are distinct from constitutional hard breaches and ensure that invalid,
malformed, or non‑admissible data never enters the constitutional pipeline.

This document integrates with:
- **[Pharma Validation Envelope](ca://s?q=Open_Pharma_Validation_Envelope)**  
- **[Pharma Data Model](ca://s?q=Open_Pharma_Data_Model)**  
- **[Pharma Metric Definitions](ca://s?q=Open_Pharma_Metric_Definitions)**  
- **[Constitutional Pharma Mathematics](ca://s?q=Open_Constitutional_Pharma_Mathematics)**  
- **[Deterministic Evaluation Standard](ca://s?q=Open_Deterministic_Evaluation_Standard)**  

Normative Reference:  
Russell, “Constitutional Mathematics for Pharma” (SSRN‑6816078, 2026)

---

## 1. Purpose of Error Conditions

Error conditions ensure:

- invalid data is rejected deterministically  
- malformed entities cannot enter constitutional evaluation  
- WAD‑scaling violations are caught early  
- schema integrity is preserved  
- reproducibility across labs and implementations  

Errors are **not** constitutional breaches; they are **pre‑constitutional
failures**.

---

## 2. Error Condition Categories

Pharma error conditions fall into four categories:

### 2.1 Structural Errors
Entity does not match the  
**[Pharma Data Model](ca://s?q=Open_Pharma_Data_Model)**.

Examples:
- missing fields  
- incorrect types  
- malformed metadata  
- non‑WAD numeric values  

### 2.2 Range Errors
Metrics fall outside the  
**[Pharma Validation Envelope](ca://s?q=Open_Pharma_Validation_Envelope)**.

Examples:
- impurity < 0  
- stability > 1e18  
- reproducibility = undefined  

### 2.3 Threshold Errors
Thresholds are missing or malformed.

Examples:
- missing \(\theta_{\text{impurity}}\)  
- negative stability threshold  
- reproducibility threshold > 1e18  

### 2.4 Evaluation Errors
Errors that occur during constitutional evaluation.

Examples:
- division by zero in scoring  
- undefined predicate state  
- missing excellence margins for F3  

---

## 3. Error Condition Schema

All error conditions must be represented as:
Error { code: string message: string field: string fatal: bool }
### Properties

- **code** — deterministic error identifier  
- **message** — human‑readable explanation  
- **field** — the field that caused the error  
- **fatal** — whether evaluation must halt  

---

## 4. Canonical Error Codes

### 4.1 Structural Errors
- `ERR_STRUCT_MISSING_FIELD`  
- `ERR_STRUCT_INVALID_TYPE`  
- `ERR_STRUCT_NON_WAD_VALUE`  

### 4.2 Range Errors
- `ERR_RANGE_IMPURITY`  
- `ERR_RANGE_STABILITY`  
- `ERR_RANGE_REPRO`  

### 4.3 Threshold Errors
- `ERR_THRESH_IMPURITY`  
- `ERR_THRESH_STABILITY`  
- `ERR_THRESH_REPRO`  

### 4.4 Evaluation Errors
- `ERR_EVAL_UNDEFINED`  
- `ERR_EVAL_DIV_ZERO`  
- `ERR_EVAL_MISSING_MARGIN`  

---

## 5. Error vs. Hard Breach

Error conditions are **not** constitutional hard breaches.

| Condition Type | Meaning | Outcome |
|----------------|---------|---------|
| Error | Invalid or malformed input | Evaluation cannot proceed |
| Hard Breach | Violates constitutional axiom | Entity must be rejected/destroyed |

Hard breaches are defined in:
- **[Purity Gate](ca://s?q=Open_Purity_Gate)**  
- **[Stability Gate](ca://s?q=Open_Stability_Gate)**  
- **[Reproducibility Gate](ca://s?q=Open_Reproducibility_Gate)**  

---

## 6. Error Handling Rules

### 6.1 Deterministic Behavior
Errors must be:

- deterministic  
- reproducible  
- implementation‑independent  

### 6.2 No Partial Evaluation
If any error occurs:

- evaluation halts  
- no score is produced  
- no predicate is evaluated  

### 6.3 No Silent Failures
All errors must produce a canonical error object.

---

## 7. Relationship to Constitutional Evaluation

Errors occur **before** the constitutional evaluation tuple:

\[
E(Y) \rightarrow (s, c, h, F, R)
\]

If an error occurs, **E(Y) is never invoked**.

---

## 8. Implementation Independence

Error conditions apply universally across:

- LIMS  
- lab instrumentation  
- computational pipelines  
- Solidity, Rust, TypeScript, hardware  

Any implementation must preserve:

- error codes  
- error semantics  
- deterministic behavior  

Pharma error conditions are universal and implementation‑agnostic.
