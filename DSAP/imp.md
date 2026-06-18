# DSAP (CT 704) — Past Year Question Full Analysis
**Sets analyzed: 27** (2082 Bhadra → 2066 Magh)
**Full Marks: 80 | Pass: 32 | Time: 3 hrs**

---

## Marks & Questions Per Chapter (Exam Pattern)

| Chapter | Topic | Syllabus Marks | Typical Q Nos | Typical Marks in Paper |
|---|---|---|---|---|
| 1 | Discrete Time Signals & Systems | 9 | Q1, Q2 | 4–10 |
| 2 | Z-Transform | 6 | Q3 | 6–7 |
| 3 | Analysis of LTI in Freq Domain | 10 | Q4 | 7–10 |
| 4 | Discrete Filter Structures | 10 | Q5, Q6 | 9–11 |
| 5 | FIR Filter Design | 15 | Q7, Q8 | 14–16 |
| 6 | IIR Filter Design | 15 | Q9 | 12–15 |
| 7 | DFT | 15 | Q10, Q11 | 13–15 |
| **Total** | | **80** | **~11–12 Qs** | **80** |

---

## Chapter 1 — Discrete Time Signals & Systems

**Chapter type: Both**

---

### Theory Topics

| Topic | Frequency |
|---|---|
| Fourier series coefficient calculation — explain process | 3 |
| Differentiate Fourier Series vs Fourier Transform | 2 |
| DTFT multiplication property + Drichlet conditions for Fourier series | 1 |
| Sampling — spectral relationship between CT signal and sampled DT signal | 2 |
| DT system properties — general listing and explanation (not for a specific system) | 2 |

---

### Numerical Types

```
Type 1 — Periodicity Check
Frequency: 22
Pattern:
  Given: x[n] expression (cos/sin combinations, complex exponentials)
  Find:  Is signal periodic? If yes, find fundamental period N
Method: For x[n]=cos(ω₀n), need ω₀/2π = p/q rational → N = q
        For sum of two signals, N = LCM(N₁, N₂)
⚠️ x[n]=cos(2πn/5)+sin(πn/3) in 2082 Bhadra Q1, 2079 Bhadra Q1,
   2079 Baishakh Q1 — EXACT SAME SIGNAL in 3 sets
⚠️ x[n]=cos(πn/2)·cos(πn/4) in 2078 Bhadra Q1 and 2078 Back Q1 — SAME
```

```
Type 2 — LTI Output via Convolution Sum
Frequency: 21
Pattern:
  Given: h[n] (impulse response), x[n] (input signal)
  Find:  y[n] = x[n] * h[n]
Sub-types:
  2a — Both finite sequences → tabular/graphical method
       e.g. h={1,1,1}, x={1,1,1,1} [2073 Shrawan Q2]
       e.g. h={5,4,3,2}, x={1,0,3,2} [2070 Chaitra Q2]
  2b — h[n]=aⁿ·u[n], x[n]=finite → analytical piecewise sum
       e.g. h=(1/2)ⁿu[n], x={2,1,0.5,-1} [2076 Chaitra Q3]
  2c — h[n]=aⁿ·{u[n]-u[n-M]} windowed, x=finite → analytical
       e.g. h=0.5ⁿ{u[n]-u[n-3]}, x={2,1,0.5,-1} [2082 Bhadra Q2]
  2d — h[n]=u[n]-u[n-M] rectangular, x[n]=aⁿ·u[n] → analytical
       e.g. h=u[n]-u[n-4], x=(1/2)ⁿu[n] [2078 Bhadra Q2]
  2e — x[n]=Ae^(jωn) complex exponential → eigenfunction method
       e.g. h=(1/2)ⁿu[n], x=5e^(jπn/3) [2082 Baishakh Q2]
  2f — h[n] or x[n] as sum of shifted δ[n] → impulse decomposition
       e.g. h=2δ[n+1]+2δ[n-1], x=δ[n]+2δ[n-1]-δ[n-3] [2081 Bhadra Q2]
⚠️ h=(1/2)ⁿ{u[n+2]-u[n-2]}, x={2,1,0.5,-1} in 2082 Baishakh Q2
   and 2074 Ashwin Q2 — SAME INPUT SEQUENCE
```

```
Type 3 — Energy / Power Classification of Given Signal
Frequency: 13
Pattern:
  Given: Specific x[n] expression
  Find:  Is it energy signal (E<∞) or power signal (0<P<∞)?
Method: Compute E=Σ|x[n]|², if finite → energy signal
        Else compute P=lim(1/2N+1)Σ|x[n]|², if finite → power signal
⚠️ x[n]=e^j(πn/2+4π/7) in 2082 Bhadra Q1 AND 2079 Baishakh Q1 — IDENTICAL
```

```
Type 4 — System Properties Check for Given Equation
Frequency: 12
Pattern:
  Given: Specific difference equation or system y[n]=f(x[n])
  Find:  Check any combination of: linearity, time invariance,
         causality, stability, memory, BIBO stability
e.g. y[n]=x[n]+x[-n] — check causal, time invariant [2082 Baishakh Q1]
e.g. y(n)=Σx(k) k=0 to n — check memoryless, TI, stable [2080 Bhadra Q1]
e.g. y[n]=x²[n] — linear or not [2075 Ashwin Q1]
```

```
Type 5 — Even / Odd Decomposition of Given Signal
Frequency: 7
Pattern:
  Given: x[n] defined piecewise or as an expression
  Find:  Even part xe[n] = (x[n]+x[-n])/2
         Odd part xo[n] = (x[n]-x[-n])/2, plot both
e.g. x[n]={1 for -4≤n≤0, 2 for 1≤n≤4} [2071 Chaitra Q1]
e.g. x[-2n+3] where x[n]={1,2,0,-1,-3,-4} [2076 Chaitra Q1]
```

```
Type 6 — BIBO Stability Check for Given System
Frequency: 3
Pattern:
  Given: Specific difference equation
  Find:  Is system BIBO stable? Show condition
e.g. y(n)=x(n)+eᵃy(n-1) — check BIBO [2081 Baishakh Q1]
```

```
Type 7 — Plot Given Sequence
Frequency: 4
Pattern:
  Given: x[n] defined using u[n], δ[n], combinations
  Find:  Plot x[n] on stem graph
e.g. x[n]=u[n]-u[n-3]+5δ[n-4]=nu[n-6] [2074 Chaitra Q1]
e.g. x[n]=u[n+8]-u[n-4] [2069 Bhadra Q1]
```

---

### Chapter 1 Questions by Set

| Set | Questions |
|---|---|
| 2082 Bhadra | Q1, Q2 |
| 2082 Baishakh | Q1, Q2 |
| 2081 Bhadra | Q1, Q2 |
| 2081 Baishakh | Q1, Q2 |
| 2080 Bhadra | Q1, Q2 |
| 2080 Baishakh | Q1, Q2 |
| 2079 Bhadra | Q1, Q2 |
| 2079 Baishakh | Q1, Q2 |
| 2078 Bhadra | Q1, Q2 |
| 2076 Chaitra | Q1, Q2, Q3 |
| 2076 Ashwin | Q1, Q2 |
| 2075 Chaitra | Q1, Q2 |
| 2075 Ashwin | Q1, Q2 |
| 2074 Chaitra | Q1, Q2 |
| 2074 Ashwin | Q1, Q2 |
| 2073 Shrawan | Q1, Q2 |
| 2072 Chaitra | Q1, Q2 |
| 2072 Kartik | Q1, Q2, Q4 |
| 2071 Shawan | Q1 |
| 2071 Chaitra | Q1, Q2 |
| 2070 Chaitra | Q1, Q2, Q4 |
| 2070 Ashad | Q1, Q2 |
| 2069 Bhadra | Q1, Q2, Q3, Q4 |
| 2069 Chaitra | Q1, Q2 |
| 2068 Bhadra | Q1, Q2, Q3, Q4 |
| 2067 Mangsir | Q1, Q2, Q3, Q4 |
| 2066 Magh | Q1, Q2, Q3, Q4 |

---

## Chapter 2 — Z-Transform

**Chapter type: Both**

---

### Theory Topics

| Topic | Frequency |
|---|---|
| Define ROC of Z-transform | 22 |
| Properties of ROC — list and explain | 8 |
| Convolution property of Z-transform — state and prove | 4 |
| Time-shifting property derivation | 3 |
| State and prove other Z-transform properties | 2 |

---

### Numerical Types

```
Type 1 — Inverse Z-Transform by Partial Fractions
Frequency: 24
Pattern:
  Given: X(z) as rational function + ROC specified
  Find:  x[n] using partial fraction expansion
Sub-types:
  1a — Single ROC given → one solution [most common]
  1b — Three ROC regions for same X(z) → three different x[n] [~6 sets]
       e.g. (i)|z|>1 (ii)|z|<0.5 (iii)0.5<|z|<1
⚠️ H(z)=z/(3z²-4z+1), ROC 1/3<|z|<1 in
   2082 Bhadra Q3 AND 2079 Baishakh Q3 — EXACT SAME
⚠️ X(z)=(1+2z⁻¹+z⁻²)/(1-1.5z⁻¹+0.5z⁻²), ROC|z|>1 in
   2080 Bhadra Q3, 2080 Baishakh Q3, 2076 Ashwin Q3 — 3 SETS
⚠️ X(z)=(2z⁴+2z³-3z+2)/(z²-1.5z-1), ROC|z|<0.5 in
   2079 Bhadra Q3 AND 2079 Baishakh Q3 — SAME YEAR BOTH SETS
```

```
Type 2 — Forward Z-Transform + ROC Location
Frequency: 5
Pattern:
  Given: x[n] as combination of causal/anti-causal exponential terms
  Find:  X(z) and locate ROC in z-plane
e.g. x[n]=(-1/3)ⁿu[n]-(1/3)ⁿu[-n-1] [2070 Chaitra Q3]
e.g. x[n]=(0.1)ⁿu[n]+(0.3)ⁿu[-n-1] [2075 Chaitra Q6, 2075 Ashwin Q3]
```

```
Type 3 — Zero-Input Response of Second Order System
Frequency: 3
Pattern:
  Given: y[n]-3y[n-1]-4y[n-2]=x[n] or similar second order equation
  Find:  Zero-input response (homogeneous solution from initial conditions)
⚠️ y[n]-3y[n-1]-4y[n-2]=x[n] in
   2078 Bhadra Q4 AND 2078 Back Q4 — SAME (same paper reprinted)
```

---

### Chapter 2 Questions by Set

| Set | Questions |
|---|---|
| 2082 Bhadra | Q3 |
| 2082 Baishakh | Q3 |
| 2081 Bhadra | Q3 |
| 2081 Baishakh | Q3 |
| 2080 Bhadra | Q3 |
| 2080 Baishakh | Q3 |
| 2079 Bhadra | Q3 |
| 2079 Baishakh | Q3 |
| 2078 Bhadra | Q3, Q4 |
| 2076 Chaitra | Q4 |
| 2076 Ashwin | Q3 |
| 2075 Chaitra | Q6 |
| 2075 Ashwin | Q3 |
| 2074 Chaitra | Q3 |
| 2074 Ashwin | Q3 |
| 2073 Shrawan | Q3 |
| 2072 Chaitra | Q3 |
| 2072 Kartik | Q3 |
| 2071 Shawan | Q2 |
| 2071 Chaitra | Q3 |
| 2070 Chaitra | Q3 |
| 2070 Ashad | Q3 |
| 2069 Bhadra | Q3 |
| 2069 Chaitra | Q3 |
| 2068 Bhadra | Q3 |
| 2066 Magh | Q7 |

---

## Chapter 3 — Analysis of LTI System in Frequency Domain

**Chapter type: Both**

---

### Theory Topics

| Topic | Frequency |
|---|---|
| Stability and causality of LTI in terms of impulse response and ROC | 6 |
| Linear constant coefficient difference equation + corresponding system function | 5 |
| Frequency response of LTI + compute output for sinusoidal input | 5 |
| Linear phase condition for FIR filter (symmetric h[n]) | 4 |
| Derive frequency response of symmetric linear phase FIR (M odd) | 2 |

---

### Numerical Types

```
Type 1 — Pole-Zero Plot + Magnitude Response Sketch
Frequency: 24
Pattern:
  Given: Difference equation OR poles/zeros given directly
  Find:  (a) Map poles and zeros in z-plane
         (b) Sketch magnitude response (not to scale)
Sub-type 1a — From difference equation: extract H(z), find poles/zeros [most common]
Sub-type 1b — Poles and zeros given directly, just plot + sketch
⚠️ Poles at 0.45±j1.6, zeros at 0.58±j2.06 in
   2082 Bhadra Q4, 2082 Baishakh Q4, 2080 Baishakh Q4, 2080 Back Q4
   — SAME DATA IN 4 SETS — memorize this completely
⚠️ Poles at 0.45±j1.06, zeros at 0.58±j2.06 (slight variation) in
   2076 Chaitra Q5, 2075 Ashwin Q4 — close repeat
⚠️ y[n]-0.4y[n-1]+0.25y[n-2]=x[n]-0.4x[n-1] in
   2081 Bhadra Q4, 2069 Chaitra Q4 — SAME EQUATION
```

```
Type 2 — Frequency Response + Output for Complex Exponential / Sinusoidal Input
Frequency: 6
Pattern:
  Given: Difference equation + specific input x[n] (sinusoidal or complex exp)
  Find:  H(e^jω), then compute y[n] using eigenfunction property
e.g. y[n]-(10/24)y[n-1]+(1/24)y[n-2]=x[n], x=sin(π/3 n)+sin(π/5 n) [2068 Bhadra Q5]
e.g. h=(1/3)ⁿu[n], x=5e^(jπn/2) [2070 Chaitra Q4, 2072 Kartik Q4]
```

---

### Chapter 3 Questions by Set

| Set | Questions |
|---|---|
| 2082 Bhadra | Q4 |
| 2082 Baishakh | Q4 |
| 2081 Bhadra | Q4 |
| 2081 Baishakh | Q4 |
| 2080 Bhadra | Q4 |
| 2080 Baishakh | Q4 |
| 2079 Bhadra | Q4 |
| 2079 Baishakh | Q4 |
| 2078 Bhadra | Q4, Q5 |
| 2076 Chaitra | Q5 |
| 2076 Ashwin | Q4, Q6 |
| 2075 Chaitra | Q3 |
| 2075 Ashwin | Q4 |
| 2074 Chaitra | Q4 |
| 2074 Ashwin | Q4 |
| 2073 Shrawan | Q4 |
| 2072 Chaitra | Q4, Q5 |
| 2072 Kartik | Q5 |
| 2071 Shawan | Q3 |
| 2071 Chaitra | Q4 |
| 2070 Chaitra | Q5 |
| 2070 Ashad | Q4 |
| 2069 Bhadra | Q5 |
| 2069 Chaitra | Q4 |
| 2068 Bhadra | Q5 |
| 2067 Mangsir | Q5 |
| 2066 Magh | Q7 |

---

## Chapter 4 — Discrete Filter Structures

**Chapter type: Both (numerical dominant)**

---

### Theory Topics

| Topic | Frequency |
|---|---|
| Quantization effects — truncation, rounding, error ranges | 7 |
| Limit cycle in recursive systems — definition and example | 6 |
| Differentiate FIR vs IIR system | 5 |
| Sign magnitude and 2's complement representation of binary fractions | 3 |
| Dead band definition | 2 |

---

### Numerical Types

```
Type 1 — Direct Form I and Direct Form II Realization
Frequency: 14
Pattern:
  Given: Difference equation y[n]=... or H(z)
  Find:  Draw DF-I signal flow graph + DF-II signal flow graph
⚠️ y[n]-0.75y[n-1]-0.25y[n-2]=x[n]+0.5x[n-1] in
   2082 Bhadra Q5 AND 2079 Baishakh Q6 — EXACT SAME SYSTEM
⚠️ y[n]-0.25y[n-2]+x[n]+0.4x[n-1]+0.5x[n-2] in
   2079 Bhadra Q5 AND 2079 Baishakh Q5 — close repeat
```

```
Type 2 — Cascade Form (2nd Order Sections) Realization
Frequency: 10
Pattern:
  Given: H(z) in fully factored form with complex conjugate pole/zero pairs
  Find:  Signal flow graph as cascade of 2nd order sections (biquads)
e.g. H(z)=10(1-0.25z⁻¹)(1-0.667z⁻¹)(1+2z⁻¹)/
          (1-0.75z⁻¹)(1-0.125z⁻¹){1-(0.5+j0.5)z⁻¹}{1-(0.5-j0.5)z⁻¹}
```

```
Type 3 — FIR Lattice Structure (All-Zero)
Frequency: 12
Pattern:
  Given: H(z)=1+a₁z⁻¹+a₂z⁻²+...+aₘz⁻ᴹ  OR  K₁,K₂,...Kₘ values
  Find:  Compute reflection coefficients Kₘ via backward Levinson recursion,
         draw lattice structure. Sometimes check stability.
Sub-type 3a — Given H(z), extract K coefficients, draw structure [most common]
Sub-type 3b — Given K values, find H(z) and FIR coefficients
⚠️ H(z)=1+(13/24)z⁻¹+(5/8)z⁻²+(1/3)z⁻³ in
   2078 Bhadra Q6 AND 2078 Back Q6 — SAME (same paper reprinted)
⚠️ H(z)=1+2z⁻¹-3z⁻²+4z⁻³ in 2072 Kartik Q6 AND 2069 Chaitra Q6 — SAME
⚠️ H(z)=2+1.8z⁻¹-1.6z⁻²+z⁻³ in 2073 Shrawan Q5 AND 2072 Chaitra Q5 — SAME
⚠️ K₁=1/4, K₂=1/2, K₃=1/3 in 2079 Bhadra Q6 AND 2071 Shawan Q4 — SAME
```

```
Type 4 — IIR Lattice-Ladder Structure (Mixed Pole-Zero)
Frequency: 12
Pattern:
  Given: H(z) = N(z)/D(z) rational system function
  Find:  (a) Compute denominator lattice coefficients Kₘ
         (b) Compute numerator ladder coefficients Cₘ
         (c) Draw complete lattice-ladder structure
⚠️ H(z)=(2-0.7z⁻¹+0.5z⁻²)/(1-0.3z⁻¹+0.25z⁻²) in
   2082 Bhadra Q6, 2080 Baishakh Q5, 2079 Baishakh Q5
   — SAME DATASET IN 3+ SETS — memorize this completely
⚠️ H(z)=(1+z⁻¹+z⁻²)/[(1+0.5z⁻¹)(1+0.3z⁻¹)(1+0.4z⁻¹)] in
   2081 Bhadra Q5 AND 2081 Baishakh Q5 — SAME
⚠️ H(z)=(0.5-2z⁻¹+3z⁻²)/(1-0.5z⁻¹-0.7z⁻²+0.3z⁻³) in
   2076 Chaitra Q6 AND 2076 Ashwin Q5 — SAME
```

---

### Chapter 4 Questions by Set

| Set | Questions |
|---|---|
| 2082 Bhadra | Q5, Q6 |
| 2082 Baishakh | Q5 |
| 2081 Bhadra | Q5 |
| 2081 Baishakh | Q5 |
| 2080 Bhadra | Q5 |
| 2080 Baishakh | Q5, Q6 |
| 2079 Bhadra | Q5, Q6 |
| 2079 Baishakh | Q5, Q6 |
| 2078 Bhadra | Q6 |
| 2076 Chaitra | Q6, Q7 |
| 2076 Ashwin | Q5 |
| 2075 Chaitra | Q4 |
| 2075 Ashwin | Q5 |
| 2074 Chaitra | Q5, Q6 |
| 2074 Ashwin | Q5 |
| 2073 Shrawan | Q5 |
| 2072 Chaitra | Q6, Q7 |
| 2072 Kartik | Q6, Q7 |
| 2071 Shawan | Q4, Q5 |
| 2071 Chaitra | Q5, Q6 |
| 2070 Chaitra | Q6, Q7 |
| 2070 Ashad | Q5, Q6 |
| 2069 Bhadra | Q6, Q7 |
| 2069 Chaitra | Q5, Q6 |
| 2068 Bhadra | Q6, Q7 |
| 2067 Mangsir | Q6, Q7 |
| 2066 Magh | Q8 |

---

## Chapter 5 — FIR Filter Design

**Chapter type: Both — HIGHEST MARKS CHAPTER (15 marks)**

---

### Theory Topics

| Topic | Frequency |
|---|---|
| Optimum filter definition + Remez exchange algorithm + flowchart | 22 |
| Gibbs phenomenon — definition, cause, minimization | 11 |
| Kaiser window advantages over fixed windows | 9 |
| Window method overview + characteristics of different windows | 7 |
| FIR vs IIR — when to choose which | 5 |
| Rectangular window + Gibb's oscillation in detail | 5 |
| Linear phase FIR condition h[n]=h[N-1-n] — show/prove | 4 |

> Remez exchange algorithm appears in EVERY single set without exception.
> Always comes with flowchart. Prepare definition + math expression + flowchart.

---

### Numerical Types

```
Type 1 — FIR Design by Window Method (Non-Kaiser Windows)
Frequency: 15
Pattern:
  Given: Passband/stopband magnitude specs + edge frequencies
         Window type specified: Hanning, Hamming, Blackman, or "suitable window"
  Find:  (a) Select appropriate window based on stopband attenuation
         (b) Compute filter order M from window main lobe width
         (c) Compute ideal h_d[n] using inverse DTFT of desired response
         (d) Multiply h_d[n] by window w[n] to get h[n]
Sub-type 1a — Hanning window: specified as Hd(W)=e^(-jwτ), |W|≤Wc [2080 Bhadra Q6]
Sub-type 1b — Blackman window: ωp=0.24π, ωs=0.34π [2068 Bhadra Q9]
Sub-type 1c — "Suitable window" student selects based on given attenuation [most common]
⚠️ Spec: 0.99≤|H|≤1.01 for 0≤|w|≤0.3π, |H|≤0.01 for 0.35π≤|w|≤π in
   2081 Bhadra Q6, 2081 Baishakh Q6, 2080 Baishakh Q7 — EXACT SAME
⚠️ Spec: 0.899≤|H|≤1, |w|≤0.2π; |H|≤0.01, 0.4π≤w≤π in
   2079 Bhadra Q7, 2076 Chaitra Q8, 2076 Ashwin Q9 — SAME
⚠️ FIR LPF ωp=0.1π, ωs=0.5π, αs=40dB in 2069 Bhadra Q9, 2069 Chaitra Q7 — SAME
```

```
Type 2 — FIR Design by Kaiser Window
Frequency: 16
Pattern:
  Given: Passband magnitude, stopband magnitude, edge frequencies
  Find:  (a) Compute δ = min(δp, δs) and αs = -20log(δ)
         (b) Compute shape parameter β from αs
         (c) Compute window length N = ⌈(αs-7.95)/(2.285·Δω)⌉+1
         (d) Compute ideal h_d[n]
         (e) Multiply by Kaiser window w[n] = I₀(β√(1-(2n/M-1)²))/I₀(β)
⚠️ Spec: 0.95≤|H|≤1.05, 0.35π≤|w|≤0.6π; |H|≤0.01 for |w|<0.25π and |w|>0.65π
   in 2078 Bhadra Q7 AND 2078 Back Q7 — SAME (same paper)
⚠️ Spec: 0.99≤|H|≤1.01 for 0≤w≤0.19π; |H|≤0.01 for 0.21π≤w≤π
   in 2074 Chaitra Q8 AND 2074 Ashwin Q7 — SAME
⚠️ Spec: ωp=0.2π, ωs=0.5π, αs=41dB in 2074 Ashwin Q6, 2072 Chaitra Q8 — close
⚠️ Spec: 0.899≤|H|≤1, |H|≤0.01, |w|≤0.2π / 0.4π in 2079 Bhadra Q7 — standalone
```

```
Type 3 — FIR Lattice Coefficients from Given Polynomial
Frequency: 8
Pattern:
  Given: H(z) = FIR polynomial OR given K₁,K₂,K₃ values
  Find:  Compute Kₘ via backward Levinson OR find H(z) from K values,
         draw lattice structure, sometimes check stability
⚠️ H(z)=1+2z⁻¹+z⁻² in 2072 Chaitra Q7 — simple 2-stage
⚠️ H(z)=1+3.1z⁻¹+5.5z⁻²+4.2z⁻³+2.3z⁻⁴ in 2070 Chaitra Q7 AND 2070 Ashad Q5 — SAME
```

---

### Chapter 5 Questions by Set

| Set | Questions |
|---|---|
| 2082 Bhadra | Q7, Q8 |
| 2082 Baishakh | Q6, Q7 |
| 2081 Bhadra | Q6, Q7 |
| 2081 Baishakh | Q6, Q7 |
| 2080 Bhadra | Q6, Q7 |
| 2080 Baishakh | Q7, Q8 |
| 2079 Bhadra | Q7, Q8 |
| 2079 Baishakh | Q7, Q8 |
| 2078 Bhadra | Q7, Q8 |
| 2076 Chaitra | Q8, Q9 |
| 2076 Ashwin | Q9 |
| 2075 Chaitra | Q5 |
| 2075 Ashwin | Q7 |
| 2074 Chaitra | Q8 |
| 2074 Ashwin | Q7 |
| 2073 Shrawan | Q6, Q7 |
| 2072 Chaitra | Q8, Q9 |
| 2072 Kartik | Q8 |
| 2071 Shawan | Q6, Q7 |
| 2071 Chaitra | Q7, Q8 |
| 2070 Chaitra | Q8, Q9 |
| 2070 Ashad | Q7, Q8 |
| 2069 Bhadra | Q9, Q10 |
| 2069 Chaitra | Q7, Q8 |
| 2068 Bhadra | Q9 |
| 2067 Mangsir | Q11 |
| 2066 Magh | Q11 |

---

## Chapter 6 — IIR Filter Design

**Chapter type: Both — HIGHEST MARKS CHAPTER (15 marks)**

---

### Theory Topics

| Topic | Frequency |
|---|---|
| Compare bilinear transformation vs impulse invariance method | 12 |
| Frequency warping / pre-warping — what it is and why needed | 6 |
| Advantages of bilinear transformation over IIM | 5 |
| Spectral transformation: LP→HP, LP→BP (digital domain) | 5 |
| Chebyshev / elliptic / Bessel filter properties | 1 |

---

### Numerical Types

```
Type 1 — Butterworth IIR Design using Bilinear Transformation
Frequency: 22
Pattern:
  Given: Specs in one of two forms:
    Form A — magnitude constraints: a≤|H(e^jw)|≤1 and |H|≤b for two bands
    Form B — ripple form: ωp, ωs (rad), δp, δs (sampling freq given)
  Find:  (a) Pre-warp digital freqs to analog: Ω=2/T·tan(ω/2)
         (b) Compute filter order N = ⌈log(selectivity)/log(transition)⌉
         (c) Find analog cutoff frequency Ωc
         (d) Find analog Butterworth poles → H(s)
         (e) Apply bilinear s=(2/T)(1-z⁻¹)/(1+z⁻¹) to get H(z)
⚠️ 0.9≤|H|≤1 for 0≤w≤π/2; |H|≤0.2 for 3π/4≤w≤π, fs=1Hz in
   2081 Bhadra Q8, 2081 Baishakh Q8, 2080 Bhadra Q8 — EXACT SAME (3 SETS)
⚠️ 0.8≤|H|≤1 for 0≤w≤0.2π; |H|≤0.2 for 0.6π≤w≤π in
   2075 Chaitra Q7, 2073 Shrawan Q8, 2070 Chaitra Q10, 2070 Ashad Q10
   — SAME IN 4 SETS — memorize this one
⚠️ ωp=0.25π, ωs=0.55π, δp=0.11, δs=0.21, fs=0.5Hz in
   2079 Bhadra Q9, 2071 Chaitra Q9, 2069 Chaitra Q9 — EXACT SAME (3 SETS)
⚠️ ωp=0.26π, ωs≈0.57-0.58π, max dev≈0.98-1dB, fs=0.5Hz in
   2079 Baishakh Q9, 2072 Kartik Q9 — nearly identical
⚠️ ωp=0.25π, ωs=0.45π, δp=0.17, δs=0.27 in 2068 Bhadra Q8 — standalone
⚠️ ωp=0.3π, ωs=0.4π, δp=0.11, δs=0.21 in 2066 Magh Q10 — standalone
```

```
Type 2 — Butterworth IIR Design using Impulse Invariance Method (IIM)
Frequency: 8
Pattern:
  Given: Passband and stopband in Hz, attenuation in dB, sampling freq in Hz
  Find:  (a) Design analog Butterworth prototype filter
         (b) Find analog poles sₖ
         (c) Map to digital: H(z) = Σ Aₖ/(1-e^(sₖT)z⁻¹)
⚠️ Passband 200Hz, stopband 500Hz, 5dB/12dB attenuation, fs=5000Hz in
   2078 Bhadra Q9, 2078 Back Q9, 2072 Chaitra Q10, 2074 Chaitra Q7
   — EXACT SAME DATASET IN 4 SETS — memorize this completely
```

```
Type 3 — LP → HP / BP Spectral Transformation (Digital Domain)
Frequency: 5
Pattern:
  Given: LP filter H(z) or design LP first then convert
  Find:  HP filter using z⁻¹ → -z⁻¹ substitution or general mapping formula
e.g. H(Z)=(0.1+0.4z⁻¹)/(1-0.6z⁻¹+0.1z⁻²) → design HP at w'c=0.3567π [2070 Chaitra Q11]
e.g. Design LP at ωp=0.25π then convert to HP at w'p=0.45π [2079 Bhadra Q9, 2071 Ch Q9]
```

---

### Chapter 6 Questions by Set

| Set | Questions |
|---|---|
| 2082 Bhadra | Q9 |
| 2082 Baishakh | Q8 |
| 2081 Bhadra | Q8 |
| 2081 Baishakh | Q8 |
| 2080 Bhadra | Q8 |
| 2080 Baishakh | Q9, Q10 |
| 2079 Bhadra | Q9 |
| 2079 Baishakh | Q9 |
| 2078 Bhadra | Q9 |
| 2076 Chaitra | Q10 |
| 2076 Ashwin | Q7 |
| 2075 Chaitra | Q7 |
| 2075 Ashwin | Q6 |
| 2074 Chaitra | Q7 |
| 2074 Ashwin | Q6 |
| 2073 Shrawan | Q8, Q9 |
| 2072 Chaitra | Q10 |
| 2072 Kartik | Q9 |
| 2071 Shawan | Q8 |
| 2071 Chaitra | Q9 |
| 2070 Chaitra | Q10, Q11 |
| 2070 Ashad | Q9, Q10 |
| 2069 Bhadra | Q8 |
| 2069 Chaitra | Q9 |
| 2068 Bhadra | Q8 |
| 2067 Mangsir | Q9 |
| 2066 Magh | Q10 |

---

## Chapter 7 — Discrete Fourier Transform

**Chapter type: Both — HIGH MARKS CHAPTER (15 marks)**

---

### Theory Topics

| Topic | Frequency |
|---|---|
| Why DFT — need and advantages over DTFT | 14 |
| How FFT reduces computational complexity vs direct DFT | 13 |
| DFT vs DTFT differences | 5 |
| DFT properties — circular convolution (state and prove) | 5 |
| DFT multiplication property | 4 |
| Zero padding — definition and purpose | 5 |
| Circular convolution vs linear convolution — differentiate | 4 |

---

### Numerical Types

```
Type 1 — 8-Point DFT using DIF-FFT (Decimation In Frequency)
Frequency: 16
Pattern:
  Given: 8-point sequence x[n] (zero-pad if shorter)
  Find:  X[k] via DIF butterfly diagram (3 stages for N=8)
         Bit-reverse output at the end
⚠️ x[n]={1,2,3,3,5,0,4,6} in 2076 Chaitra Q11 AND 2076 Ashwin Q8 — SAME
⚠️ x[n]={2,1,2,1,1,2,1,2} in 2080 Bhadra Q9 — standalone
⚠️ x[n]={1,1/2,-1,-1/2,2,-3/2} in 2082 Bhadra Q11 — standalone
```

```
Type 2 — 8-Point DFT using DIT-FFT (Decimation In Time)
Frequency: 14
Pattern:
  Given: 8-point sequence x[n] (zero-pad if shorter)
  Find:  X[k] via DIT butterfly diagram
         Bit-reverse input first, then 3 stages of butterflies
⚠️ x[n]={1,-2,-4,3,0,1} zero-padded in 2081 Bhadra Q9 — standalone
⚠️ x[n]=u[n]-u[n-4] in 2078 Bhadra Q11 AND 2078 Back Q11 — SAME
⚠️ x[n]={1,1,2,4,3,1,2,1} in 2072 Chaitra Q11 — standalone
⚠️ x[n]={1,-1,2,2,1,1,2,2} in 2073 Shrawan Q10 — standalone
```

```
Type 3 — 4-Point DFT using DIT or DIF
Frequency: 6
Pattern:
  Given: 3–4 point sequence (zero-pad to 4)
  Find:  4-point DFT via butterfly diagram, sometimes only specific X(k) values
⚠️ x[n]={2,2,4} zero-padded to 4 in 2081 Baishakh Q9 (both Reg and Back) — SAME
⚠️ x[n]={1,4,-1} 4-point DIF in 2082 Baishakh Q9 — standalone
⚠️ x[n]={1,-2,3,2} find X(3) and X(5) in 2075 Chaitra Q8 — standalone
```

```
Type 4 — Circular Convolution
Frequency: 22
Pattern:
  Given: Two finite sequences x₁[n] and x₂[n]
  Find:  N-point circular convolution (zero-pad shorter sequence to N)
         Method: direct matrix/concentric circle OR via DFT: Y=X₁·X₂ then IDFT
⚠️ h(n)={1,2,1,-1,1}, x(n)={1,2,3,1} in
   2082 Bhadra Q10 AND 2072 Chaitra Q12 — EXACT SAME ⚠️
⚠️ x₁[n]={2,1,2,1}, x₂[n]={1,2,3,4} in
   2078 Bhadra Q10 AND 2078 Back Q10 — SAME ⚠️
⚠️ x₁[n]={1,2,3,1}, x₂[n]={4,3,2,2} in
   2080 Bhadra Q10, 2080 Baishakh Q12 — SAME ⚠️
⚠️ x[n]={1,2} and y[n]=u[n]-u[n-4] in
   2071 Chaitra Q10 AND 2070 Ashad Q11 — SAME ⚠️
⚠️ x₁[n]={1,2,4,5}, x₂[n]={2,1,6,8} in
   2081 Baishakh Q10 (Reg and Back) — SAME ⚠️
⚠️ x₁[n]={1,0,1}, x₂[n]={1,0,2,1} in
   2069 Bhadra Q11 AND its Back Q11 — SAME ⚠️
```

```
Type 5 — Find x₃[n] from X₃(k) = X₁(k)·X₂(k)
Frequency: 12
Pattern:
  Given: Two sequences x₁[n] and x₂[n]
  Find:  Compute N-point DFT of each, multiply pointwise,
         take IDFT to get x₃[n] (= circular convolution of x₁ and x₂)
⚠️ x₁[n]=3ⁿ (0≤n≤3), x₂[n]=2ⁿ (0≤n≤4) in
   2081 Bhadra Q10 AND 2081 Baishakh Q10 — SAME
⚠️ x₁[n]={1,2,-2}, x₂[n]={1,2,3,-1} in
   2069 Bhadra Q12, 2069 Chaitra Q11 — SAME
⚠️ x₁[n]={1,-2,2,1,4}, x₂[n]={2,1,-3,-1} in 2073 Shrawan Q11 — standalone
```

```
Type 6 — Zero Padding: Linear Convolution via Circular Convolution
Frequency: 4
Pattern:
  Given: Two short sequences x[n] and h[n]
  Find:  Determine appropriate N (≥ L+M-1), zero-pad,
         compute circular convolution to get linear convolution result
⚠️ x[n]={1,1,1,1}, h[n]={2,3} in
   2074 Chaitra Q10 AND 2074 Ashwin Q9 — SAME
```

---

### Chapter 7 Questions by Set

| Set | Questions |
|---|---|
| 2082 Bhadra | Q10, Q11 |
| 2082 Baishakh | Q9, Q10 |
| 2081 Bhadra | Q9, Q10 |
| 2081 Baishakh | Q9, Q10 |
| 2080 Bhadra | Q9, Q10 |
| 2080 Baishakh | Q11, Q12 |
| 2079 Bhadra | Q10, Q11 |
| 2079 Baishakh | Q10, Q11 |
| 2078 Bhadra | Q10, Q11 |
| 2076 Chaitra | Q11, Q12 |
| 2076 Ashwin | Q8 |
| 2075 Chaitra | Q8, Q9 |
| 2075 Ashwin | Q8, Q9 |
| 2074 Chaitra | Q9, Q10 |
| 2074 Ashwin | Q8, Q9 |
| 2073 Shrawan | Q10, Q11 |
| 2072 Chaitra | Q11, Q12 |
| 2072 Kartik | Q10, Q11 |
| 2071 Shawan | Q9, Q10 |
| 2071 Chaitra | Q10, Q11 |
| 2070 Chaitra | Q12, Q13 |
| 2070 Ashad | Q11, Q12 |
| 2069 Bhadra | Q11, Q12, Q13 |
| 2069 Chaitra | Q10, Q11 |
| 2068 Bhadra | Q10 |
| 2067 Mangsir | Q12 |
| 2066 Magh | Q5, Q6 |

---

## Chapter Summary

| Chapter | Type | Most Important to Practice | Repeated Datasets to Memorize |
|---|---|---|---|
| 1 | Both | Periodicity check + LTI convolution | x[n]=cos(2πn/5)+sin(πn/3) → N=30 |
| 2 | Both | Inverse Z-transform partial fractions (3-ROC variant) | H(z)=z/(3z²-4z+1); (1+2z⁻¹+z⁻²)/(1-1.5z⁻¹+0.5z⁻²) |
| 3 | Both (numerical dominant) | Pole-zero plot + magnitude response from diff eq | Poles 0.45±j1.6, zeros 0.58±j2.06 (4 sets) |
| 4 | Both (numerical dominant) | Lattice-Ladder IIR structure | H=(2-0.7z⁻¹+0.5z⁻²)/(1-0.3z⁻¹+0.25z⁻²); IIM 200/500Hz |
| 5 | Both | Kaiser window design + Remez algorithm (flowchart) | 0.99/0.01 spec (3 sets); 0.899/0.01 spec (3 sets) |
| 6 | Both (numerical dominant) | Bilinear Butterworth design | ωp=0.25π, ωs=0.55π, δp=0.11, δs=0.21 (3 sets); 0.8/0.2 spec (4 sets) |
| 7 | Both (numerical dominant) | 8-pt DIT+DIF butterfly + circular convolution | h={1,2,1,-1,1}★x={1,2,3,1}; x₁={2,1,2,1}★x₂={1,2,3,4} |

---

## High Priority Exam Preparation

### Must-Know Algorithms (in every or near-every set)
1. Partial fraction inverse Z-transform — 3-ROC variant
2. Pole-zero plot from difference equation + magnitude sketch
3. FIR lattice coefficients from H(z) polynomial
4. IIR lattice-ladder coefficient extraction + structure
5. Kaiser window FIR design — full 5-step procedure
6. Bilinear transformation Butterworth — full 6-step procedure
7. Remez exchange algorithm — definition + math + flowchart
8. 8-point DIT-FFT butterfly diagram
9. 8-point DIF-FFT butterfly diagram
10. Circular convolution — matrix or DFT method

### Highest-Repeat Datasets (memorize completely)

| Dataset | Ch | Times |
|---|---|---|
| Poles 0.45±j1.6, zeros 0.58±j2.06 | 3 | 4 sets |
| H(z)=(2-0.7z⁻¹+0.5z⁻²)/(1-0.3z⁻¹+0.25z⁻²) lattice-ladder | 4 | 3+ sets |
| IIM: 200Hz/500Hz, 5dB/12dB, fs=5000Hz | 6 | 4 sets |
| BLT: 0.8≤\|H\|≤1, 0≤w≤0.2π; \|H\|≤0.2, 0.6π≤w≤π | 6 | 4 sets |
| BLT: ωp=0.25π, ωs=0.55π, δp=0.11, δs=0.21, fs=0.5Hz | 6 | 3 sets |
| BLT: 0.9≤\|H\|≤1, 0≤w≤π/2; \|H\|≤0.2, 3π/4≤w≤π | 6 | 3 sets |
| Circ conv: h={1,2,1,-1,1} and x={1,2,3,1} | 7 | 2 sets |
| Circ conv: x₁={2,1,2,1} and x₂={1,2,3,4} | 7 | 2 sets |
| FIR: 0.99≤\|H\|≤1.01, 0≤w≤0.3π; \|H\|≤0.01, 0.35π≤w≤π | 5 | 3 sets |
| Z-inv: H(z)=z/(3z²-4z+1), ROC 1/3<\|z\|<1 | 2 | 2 sets |
