# WAD Arithmetic Standard
## 1e18 Fixed‑Point Constitutional Numeric System

WAD Arithmetic is the fixed‑point numeric system used by Constitutional
Mathematics. All ratios and thresholds are represented as integers scaled by
\(10^{18}\), ensuring deterministic, cross‑platform reproducibility.

Normative Reference:  
Russell, “Constitutional Mathematics for Treasury and Pharma” (SSRN‑6609638, 2026)

---

## 1. Scaling Constants

- **ONE**  
  \[
  \text{ONE} = 10^{18}
  \]  
  Represents 1.0 or 100%.

- **PRCNT**  
  \[
  \text{PRCNT} = 10^{16}
  \]  
  Represents 1%.

- **BIPS**  
  \[
  \text{BIPS} = 10^{14}
  \]  
  Represents 0.01% (1 basis point).

---

## 2. Ratios

\[
\text{ratio}(a, b) =
\left\lfloor \frac{a \cdot \text{ONE}}{b} \right\rfloor
\quad (b > 0)
\]

Examples:

- \(a = b \Rightarrow \text{ratio} = \text{ONE}\)  
- \(2/5 = 0.4 \times \text{ONE}\)

---

## 3. Multiplication

\[
\text{mul}(x, y) = \left\lfloor \frac{x \cdot y}{\text{ONE}} \right\rfloor
\]

Preserves WAD scaling.

---

## 4. Division

\[
\text{div}(x, y) = \left\lfloor \frac{x \cdot \text{ONE}}{y} \right\rfloor
\quad (y > 0)
\]

---

## 5. Basis Points to WAD

\[
\text{bps\_to\_wad}(bps) = bps \cdot \text{BIPS}
\]

Examples:

- 100 bps = 1%  
- 250 bps = 2.5%

---

## 6. Invariants

Any conforming implementation must:

- Use non‑negative integers  
- Guard overflow  
- Define explicit division‑by‑zero behavior  
- Preserve determinism  
- Avoid floating‑point math  

---

## 7. Purpose

WAD Arithmetic ensures:

- Exact thresholds  
- Reproducible ratios  
- Cross‑implementation agreement  
- Formal verifiability
