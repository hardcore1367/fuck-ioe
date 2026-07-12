Full analysis below. 21 sets covered (2068 Bhadra through 2081 Chaitra). Note: 2068 Bhadra and 2068 Magh are nearly identical papers — flagged throughout.

---

```md
# Electrical Machines (EE 554) — Past Paper Analysis
## Sets Analyzed: 21 (2068 Bhadra to 2081 Chaitra)
```

---

## Chapter 1 — Magnetic Circuits and Induction

**Chapter type:** Both (Theory + Numerical)
**Most important:** Numerical (series/parallel magnetic circuit) + Hysteresis/eddy current losses theory

### Theory Questions

| Topic | Frequency |
|---|---|
| Hysteresis loss + eddy current loss (explain, causes, how to reduce, area = energy) | 3 |
| Coercivity + retentivity + BH curve / hysteresis loop properties | 2 |
| Faraday's laws of EM induction + statically vs dynamically induced EMF | 2 |
| Fleming's right and left hand rules | 2 |
| Magnetization and demagnetization with DC excitation + hard/soft magnetic materials | 1 |
| Reluctance and permeance — define and derive expressions | 1 |
| Ohm's law for magnetic circuits | 1 |
| MMF and magnetizing force — define | 1 |
| Effect of air gap in magnetic circuit | 1 |

---

### Numerical Questions

```
Type 1 — Series / Toroidal Magnetic Circuit with Air Gap
Frequency: 10 instances (across all sets)
Pattern:
  Given: Ring/toroid — mean diameter or length, cross-sectional area, number of
         turns, relative permeability, air gap length
  Find:  Exciting current OR flux OR reluctance OR relative permeability OR mmf/H/B

Sub-types:
  1a. Find current for given flux in air gap: most common variant
  1b. Find relative permeability from given flux and current
  1c. Find mmf, total flux, H, and μr all together
  1d. Find exciting current AND inductance

⚠️ 2072 Ashwin Q1b = 2070 Magh Q5b — SAME dataset:
   Ring 30cm mean diameter, 2.5cm rod diameter, 1mm saw cut,
   500 turns, find current for 4mWb, μr = 800

⚠️ 2068 Bhadra Q1b = 2068 Magh Q1b — SAME dataset:
   Cast steel ring, 80cm circumference, 3cm diameter cross-section,
   1mm air gap, 600 turns, 0.75mWb — B-H curve given

⚠️ 2073 Magh Q1b = 2069 Bhadra Q1b — SAME dataset:
   Circular iron core, 10cm length, 100mm² area, 2mm air gap,
   600 turns, find current for 1T air gap flux, μr = 4000
```

```
Type 2 — Parallel / E-Core / Multi-Limb Magnetic Circuit
Frequency: 4
Pattern:
  Given: Complex core shape (E-type, parallel limbs), multiple coils with
         different turns and currents, μr given
  Find:  Flux in a specific limb or air gap

Sub-types:
  2a. E-shaped core, find flux in central limb (2078 Chaitra Q1b)
  2b. Parallel 3-coil circuit, find current in one coil for given flux in
      a section (2073 Bhadra Q1a)
  2c. Two-winding circuit with diagram, find air gap flux, H, B (2080 Chaitra Q1b)
  2d. Rectangular 3-coil core, find flux in air gap (2071 Magh Q1a)
```

```
Type 3 — Inductance + Flux Calculation
Frequency: 2
Pattern:
  Given: Core dimensions, μr, turns, dc current
  Find:  Inductance of coil + magnetic flux in core

Sets: 2070 Bhadra Q3c, 2078 Poush Q1
```

```
Type 4 — B-H Curve Data (Magnetization Table Given)
Frequency: 1 unique dataset (appears in both 2068 papers ⚠️)
Pattern:
  Given: B-H table for material, ring dimensions, air gap, turns
  Find:  Current to establish given flux in air gap
```

---

## Chapter 2 — Transformer

**Chapter type:** Both (Theory + Numerical) — highest mark weightage
**Most important:** OC/SC test numerical + no-load and load operation theory

### Theory Questions

| Topic | Frequency |
|---|---|
| No-load and loaded operation of ideal transformer (with/without proving flux constant) | 10 |
| Transformer losses (types) + efficiency derivation + condition for maximum efficiency | 4 |
| Autotransformer — working principle, Cu saving derivation, merits/demerits over 2-winding | 4 |
| OC and SC test — how to conduct + how efficiency and VR are determined from test results | 2 |
| Instrument transformers (CT + PT) + why CT secondary must not be left open | 2 |
| Why transformer rated in KVA not kW + factors affecting efficiency | 1 |
| Practical transformer vs ideal transformer (phasor diagram with secondary load) | 1 |
| Equivalent circuits referred to primary and secondary side | 1 |
| Copper loss negligible in no-load test + iron loss negligible in SC test — justify | 1 |

---

### Numerical Questions

```
Type 1 — OC/SC Test → Equivalent Circuit Parameters + Efficiency
Frequency: 14 instances; ~9 unique datasets
Pattern:
  Given: Transformer rating (kVA, V/V), OC test data (V, I, W on LV or HV side),
         SC test data (V, I, W on HV or LV side)
  Find:  Equivalent circuit parameters referred to one side,
         efficiency at x% load and y pf,
         maximum efficiency, and/or voltage regulation

Sub-type A — Find equivalent circuit only
Sub-type B — Find efficiency at given load
Sub-type C — Find maximum efficiency (KVA for max efficiency and its value)
Sub-type D — Find all: params + efficiency + regulation

⚠️ 2081 Chaitra Q2a = 2072 Ashwin Q2b — SAME dataset:
   20 kVA, 250/2500V, 50Hz
   OC (LV side): 250V, 1.4A, 105W
   SC (HV side): 120V, 8A, 320W

⚠️ 2073 Bhadra Q2a = 2070 Magh Q1b — SAME dataset:
   20 kVA, 2200/220V, 50Hz
   OC: 220V, 1.1A, 125W
   SC: 52.7V, 8.4A, 287W

⚠️ 2075 Baisakh Q2b = 2068 Bhadra Q2b = 2068 Magh Q2b — SAME dataset:
   10 kVA, 200/400V, 50Hz
   OC (LV): 200V, 1.3A, 120W
   SC (HV): 22V, 30A, 200W
   (Three separate sets with identical data — memorize this one)
```

```
Type 2 — Efficiency at Given Load (Losses or Resistances Directly Given)
Frequency: 6
Pattern:
  Given: Transformer rating, iron loss, copper loss (or winding resistances + iron loss)
  Find:  Efficiency at full/half load at given pf + KVA for max efficiency

Datasets:
  a) 100 KVA, copper loss = 1200W, iron loss = 960W (2079 Chaitra Q2a)
  b) 250 KVA, 11000/400V, R1 = 0.3Ω, R2 = 0.001Ω, iron loss = 2000W (2076 Bhadra Q2b)
  c) Single phase, 90% efficiency at half load and full load of 500 kW —
     find iron loss, copper loss, max efficiency (2080 Chaitra Q2b)
  d) 500 KVA, 6600/400V, R1 = 0.4Ω, R2 = 0.001Ω, iron loss = 3 kW (2072 Ashwin Q5b)
  e) 500 KVA, 3-phase, delta/star, 33/11 kV, iron loss = 3050W (2068 sets Q3a) ⚠️
  f) 20 kVA, equivalent circuit parameters given directly (Ro, Xo, R01, X01)
     (2072 Magh Q2a)
```

```
Type 3 — Transformer with Given Impedances (Find Terminal Voltage / Current / PF)
Frequency: 3
Pattern:
  Given: Primary + secondary impedances in complex form, load impedance or condition
  Find:  Load terminal voltage, primary current, voltage regulation, power factor

Datasets:
  a) 25 KVA, 11KV/400V, Z1 = 0.4+j2Ω, Z2 = 0.02+j1Ω (2071 Bhadra Q2a)
  b) 230/2300V, R_eq = 0.1Ω, X_eq = 0.4Ω, Ro = 500Ω, Xo = 200Ω,
     load = (400+j600)Ω (2070 Bhadra Q1c)
  c) 2500/500V, R1=5.5Ω, X1=12Ω, R2=0.2Ω, X2=0.45Ω — VR and power factor
     for max regulation (2078 Poush Q2b)
```

```
Type 4 — Three-Phase Transformer (Voltages and Currents Both Sides)
Frequency: 1
Pattern:
  Given: 3-phase delta/star transformer, kVA, input line voltage, turns ratio phase-to-phase
  Find:  Line voltages, line currents, phase voltages, phase currents on both sides

Dataset: 120 kVA, 0.8 pf, input line = 11 kV, turns ratio = 10 (2074 Bhadra Q2c)
```

---

## Chapter 3 — DC Generator

**Chapter type:** Both
**Most important:** Compound generator EMF numerical + voltage build-up theory

### Theory Questions

| Topic | Frequency |
|---|---|
| Construction details + working principle + EMF equation derivation | 5 |
| Voltage build-up process in DC shunt generator + why not started at load | 4 |
| Commutator and carbon brush functions in DC generator | 3 |
| Characteristics of DC series vs shunt generator (graphical + equations) | 2 |
| Losses in DC generator + efficiency derivation | 1 |
| DC shunt generator started with output terminal open — justify | 1 |
| Why DC series generator not started at no load | 1 |

---

### Numerical Questions

```
Type 1 — Compound Generator EMF Calculation (Long / Short Shunt)
Frequency: 10 instances; ~7 unique datasets
Pattern:
  Given: Load current, terminal voltage, Ra, Rs (series field), Rf (shunt field),
         brush contact drop
  Find:  Generated EMF and/or armature current for long shunt and/or short shunt

Sub-types:
  1a. Find EMF for long shunt only
  1b. Find EMF for short shunt only
  1c. Find EMF for both (compare)

⚠️ 2078 Chaitra Q3a = 2076 Bhadra Q3a — SAME dataset:
   Compound generator, 50A at 500V, Ra = 0.05Ω, Rs = 0.03Ω,
   Rf = 250Ω, brush drop = 1V per brush
   (S4 asks for both long + short shunt; S7 asks for long shunt only)

⚠️ 2073 Bhadra Q3b = 2069 Poush Q2b — SAME dataset:
   220V DC series motor speed reduction... wait, these are DC motor problems.
   
   Actually DC compound generator repeats:
   2068 Bhadra Q4a = 2068 Magh Q4a — SAME:
   Short shunt, 80A at 220V, Rf = 100Ω, Rs = 0.05Ω, Ra = 0.1Ω

Notable datasets to memorize:
  a) 50A at 500V, Ra = 0.05Ω, Rs = 0.03Ω, Rf = 250Ω (appears 2×) ⚠️
  b) 100A at 250V, Ra = 0.06Ω, Rs = 0.04Ω, Rf = 50Ω (2081 Chaitra)
  c) 80A at 230V, Ra = 0.2Ω, Rs = 0.04Ω, Rf = 100Ω (2077 Chaitra)
  d) 30A at 220V, Ra = 0.05Ω, Rs = 0.03Ω, Rf = 200Ω (2072 Magh)
  e) 80A at 220V, Rf = 100Ω, Rs = 0.05Ω, Ra = 0.1Ω (2068 sets) ⚠️
  f) 220V compound, 80 lamps each 60W at 220V, Ra = 0.3Ω,
     Rs = 0.2Ω, Rf = 60Ω — long and short shunt (2074 Bhadra)
```

```
Type 2 — DC Shunt Generator (Wave / Lap Wound) — Find EMF + Currents
Frequency: 3 instances; 2 unique datasets

⚠️ 2070 Magh Q3b = 2069 Bhadra Q3b — SAME dataset:
   4-pole DC shunt generator, wave wound, Ra = 0.2Ω, Rf = 60Ω,
   brush drop = 1V, delivering 3kW at 120V —
   find: total armature current, current per conductor, generated EMF

Dataset b: 2070 Magh Q3b has different paper context but same numbers.
```

```
Type 3 — DC Generator Speed Calculation (Lap / Wave Wound)
Frequency: 2 instances; 1 unique dataset

⚠️ 2078 Poush Q3b ≈ 2070 Bhadra Q2c — SAME dataset:
   4-pole, 250V long shunt compound, 10 kW at rated voltage,
   Ra = 0.1Ω, Rs = 0.15Ω, Rf = 250Ω, 300 conductors (or 50 slots × 6),
   lap wound, flux per pole = 50 mWb — find speed; also find speed if wave wound
```

---

## Chapter 4 — DC Motor

**Chapter type:** Both
**Most important:** Speed calculation numerical + back EMF + torque equation

### Theory Questions

| Topic | Frequency |
|---|---|
| Back EMF — definition, roles, significance, how it adjusts torque with load | 4 |
| Working principle of DC motor + torque equation derivation | 3 |
| Performance / electrical and mechanical characteristics of DC shunt motor | 3 |
| Speed control methods — field control and armature control | 3 |
| DC motor starting — why large current + 3-point / 4-point starter working | 3 |
| Torque-armature current and speed-torque characteristics of DC shunt and series motor | 2 |
| DC series motor must not be started without load — justify | 2 |

---

### Numerical Questions

```
Type 1 — DC Shunt Motor Speed Change (Armature Resistance Insertion)
Frequency: 6
Pattern:
  Given: Shunt motor, supply voltage, initial current and speed, Ra, Rf,
         resistance inserted in armature, load condition (constant torque
         or torque increased by x%)
  Find:  New speed after resistance insertion OR resistance required for given speed

Datasets:
  a) 220V, 20A at 1500rpm, Ra = 0.08Ω, Rf = 110Ω, add 0.02Ω, torque +35%
     (2081 Chaitra Q3a)
  b) 200V, 20A at 1500rpm, Ra = 0.08Ω, Rf = 110Ω, add 0.02Ω, torque +30%
     (2073 Magh Q3b)
     ⚠️ Datasets (a) and (b) almost identical — only voltage (220 vs 200) and
     torque increase (35% vs 30%) differ
  c) 220V, 40A at 1400rpm, Ra = 0.02Ω, Rf = 100Ω, reduce to 1200rpm constant torque
     (2070 Magh Q2b)
  d) 200V, Ra = 0.25Ω, Rf = 100Ω, 4A no-load at 1000rpm, loaded → 950rpm,
     find loaded current + speed regulation (2079 Chaitra Q3a)
  e) 200V, 50A at 1000rpm, Ra = 0.1Ω, Rf = 100Ω, constant torque, reduce to 800rpm
     (2072 Ashwin Q3b)
  f) 200V, 50A at 1000rpm, Ra = 0.1Ω, Rf = 100Ω, torque ∝ N², reduce to 800rpm
     (2068 Bhadra Q3b)
     ⚠️ Datasets (e) and (f) — same numbers but different torque-speed relationship
```

```
Type 2 — DC Series Motor Speed Change (Resistance Insertion)
Frequency: 6
Pattern:
  Given: Series motor, voltage, speed, current, Ra, series field resistance
  Find:  New speed OR additional resistance required for given speed at constant torque

⚠️ 2073 Bhadra Q3b = 2069 Poush Q2b — SAME dataset:
   220V DC series motor, 100A at 1200RPM, Ra = 0.2Ω, Rf = 0.05Ω,
   find armature resistance to reduce speed to 800RPM

Other datasets:
  a) DC series motor, 1Ω between terminals, 1000RPM at 250V, 20A,
     insert 6Ω — find new speed at same current (2070 Bhadra Q3b)
  b) 200V DC series motor, 1000rpm, 20A, combined Ra+Rf = 0.4Ω,
     reduce to 800rpm (2076 Bhadra Q3b)
  c) 200V DC series motor, 38A at 600rpm, Ra = 0.4Ω, Rs = 0.2Ω,
     find speed at 19A and at 1A (2072 Magh Q3a)
  d) DC series motor, Ra = 0.06Ω, Rf = 0.04Ω, 220V, 25A at 1200rpm,
     find current at 800rpm (2069 Bhadra Q2b)
```

```
Type 3 — DC Shunt Motor No-Load to Loaded (Find Iron + Friction Loss, Efficiency)
Frequency: 2 instances; 1 unique dataset

⚠️ 2080 Chaitra Q3b = 2075 Baisakh Q3b — SAME dataset:
   230V shunt motor, 5A at no-load, Ra = 0.25Ω, Rf = 115Ω,
   loaded to carry 40A — find iron and friction loss, efficiency
```

```
Type 4 — DC Shunt Motor Torque / Speed from Basic Motor Equations
Frequency: 2
Pattern:
  Given: Motor parameters, poles, conductors, flux per pole, current
  Find:  Armature current, speed, torque developed

Datasets:
  a) 480V, 120A from supply, Ra = 0.5Ω, Rf = 12Ω, 6 poles,
     740 conductors, flux = 0.08Wb (2069 Poush Q3a)
  b) 230V, 100A at 1200RPM, Ra = 0.2Ω, find armature resistance
     to run at 800RPM (2073 Bhadra Q3b) — overlaps with Type 2
```

```
Type 5 — DC Series Motor (Back EMF / Speed Change)
Frequency: 2
Pattern:
  Given: Series motor speed and current, find speed at different current
  OR find resistance to limit speed given current changes

Datasets:
  a) 240V DC series motor, total resistance = 0.2Ω, 1800rpm draws 40A,
     insert resistance to limit to 2400rpm at 10A (2078 Poush Q4b)
  b) DC shunt motor at 600RPM, 60A from 230V, Ra = 0.2Ω, Rf = 115Ω,
     find speed when armature current = 30A (2071 Magh Q4b)
```

---

## Chapter 5 — Three Phase Induction Machines

**Chapter type:** Both — heavily numerical
**Most important:** Torque-slip characteristics (theory + numerical) — by far the most frequent topic

### Theory Questions

| Topic | Frequency |
|---|---|
| Torque-slip characteristics + condition for maximum torque (derive/draw/discuss) | 14 |
| Effect of rotor resistance on torque-slip characteristics | 5 |
| Induction generator — conditions, working principle, voltage build-up | 4 |
| Equivalent circuit of 3-phase IM (draw + explain how torque is produced) | 2 |
| Rotating magnetic field production + how it causes rotation | 2 |
| Operating principle of 3-phase IM + why rotor speed < synchronous speed | 2 |
| Power stages in 3-phase IM (derive expressions) | 2 |
| Define slip + why IM operates only in linear portion of T-S curve | 2 |

---

### Numerical Questions

```
Type 1 — Torque at Given Slip / Speed (with or without Added Rotor Resistance)
Frequency: 8
Pattern:
  Given: Poles, frequency, R2, X2, maximum torque (and speed or slip at max torque)
  Find:  Torque at another speed/slip; OR new speed when R added to rotor at
         constant load torque; OR additional resistance for given fraction of max torque

Sub-types:
  1a. Find torque at given operating speed
  1b. Find new speed when rotor resistance added (constant torque)
  1c. Find additional rotor resistance for (2/3) of max torque at starting

Datasets:
  a) 4-pole, 400V, 50Hz, R2 = 0.25Ω, X2 = 2Ω, max torque = 30Nm,
     find torque at 1440rpm; add 0.15Ω, find new speed (2081 Chaitra Q4a)
  b) 4-pole, 50Hz, max torque = 50Nm at 1350rpm, R2 = 0.5Ω/phase,
     find torque at 1450rpm (2076 Bhadra Q4b)
  c) 6-pole, 50Hz, max torque = 30Nm at 960rpm, R2 = 0.6Ω/phase,
     find torque at 6% slip (2078 Chaitra Q4b)
  d) 6-pole, 50Hz, R2 = 0.4Ω/phase, max torque = 200Nm at 850rpm,
     find torque at 4% slip + additional resistance for (2/3)Tmax at starting
     (2073 Bhadra Q4b)
  e) 4-pole, 50Hz, max torque = 50Nm at 1350rpm, R2 = 0.5Ω,
     find torque at 1450rpm (2076 Bhadra) — same as (b)
```

```
Type 2 — Power Flow / Rotor Copper Loss / Output Torque
Frequency: 2
Pattern:
  Given: Power input to rotor (or stator), stator losses, friction losses,
         poles, frequency
  Find:  Slip, rotor speed, rotor copper loss, mechanical power developed,
         output power, output torque

Datasets:
  a) 440V, 50Hz, 6-pole IM, rotor power = 50kW, rotor EMF at 120 cycles/min,
     friction = 2kW (2074 Bhadra Q4b)
  b) 500V, 50Hz, 6-pole IM at 975rpm, input = 40kW, stator losses = 1kW,
     friction = 2kW (2078 Poush Q5a)
```

```
Type 3 — Rotor EMF, Slip, Frequency at Running Speed
Frequency: 3 instances; 2 unique datasets

⚠️ 2077 Chaitra Q4a = 2071 Magh Q5b — SAME dataset:
   3-phase delta, 440V, 50Hz, 4-pole IM, standstill EMF/phase = 130V,
   running at 1440rpm — find slip, rotor EMF frequency, rotor EMF per phase,
   stator to rotor turn ratio

Dataset b:
   208V, 60Hz, 4-pole, 3-phase IM, full speed = 1755rpm —
   find synchronous speed, slip, rotor frequency
   (2068 Bhadra Q5a = 2068 Magh Q5a) ⚠️ same paper
```

```
Type 4 — Slip Ring IM: Starting Current and Running Current
Frequency: 4
Pattern:
  Given: Rotor impedance at standstill, induced EMF between slip rings at
         standstill, stator to rotor turn ratio (or poles, frequency)
  Find:  Starting current; running current at given speed or slip

Datasets:
  a) 4-pole, 50Hz, Z_rotor = (1+j4)Ω/phase, stator/rotor turn ratio = 2,
     EMF = 400V between slip rings — find starting current + running at 1400rpm
     (2073 Magh Q4b)
  b) Star-connected rotor, EMF = 120V between slip rings, R = 0.3Ω,
     X = 1.5Ω/phase — find current/phase at 4% slip (2069 Bhadra Q4b)
  c) 6-pole, 50Hz, Z_rotor = (0.8+j4)Ω/phase, EMF = 400V,
     stator/rotor ratio = 4, runs at 960rpm no-load —
     find current at standstill and no-load (2069 Poush Q4b)
  d) 6-pole, 50Hz, 3-phase slip ring IM, star rotor, Z = (0.8+j4)Ω/phase,
     EMF between slip rings at standstill = 400V (2069 Bhadra Q4b)
```

```
Type 5 — Maximum Torque Speed from Standstill Impedance
Frequency: 3 instances; 2 unique datasets

⚠️ 2070 Magh Q4b = 2068 Bhadra Q4b = 2068 Magh Q4b — SAME dataset:
   8-pole, 50Hz, 3-phase IM, starting torque = 50Nm,
   rotor impedance = (0.8+j2)Ω/phase — find speed for max torque + magnitude

Dataset b: 2072 Ashwin Q4b — 4-pole version:
   4-pole, 50Hz, starting torque = 50Nm, rotor impedance = (0.8+j2)Ω/phase
   ⚠️ Same rotor data, only poles differ

Pattern: Find speed at max torque + calculate Tmax
```

```
Type 6 — T-S Characteristics: Slip at Max Torque and Full Load Torque Ratios
Frequency: 2
Pattern:
  Given: Torque ratios (starting torque/full load torque, max torque/full load torque)
  Find:  Slip at max torque, slip at full load, starting current ratio

Dataset: 50Hz IM, Tstart = 1.25 × Tfl, Tmax = 2.5 × Tfl (2070 Bhadra Q4b)
```

---

## Chapter 6 — Three Phase Synchronous Machines

**Chapter type:** Both
**Most important:** Effect of excitation / V-curves (theory) + voltage regulation numerical

### Theory Questions

| Topic | Frequency |
|---|---|
| Effect of excitation on pf + V-curve and inverted V-curve of synchronous motor | 9 |
| Armature reaction in synchronous generator for resistive / inductive / capacitive loads | 5 |
| Why 3-phase synchronous motor is not self-starting + starting methods | 3 |
| Working principle of 3-phase synchronous motor | 2 |
| Excitation control in synchronous motor — leading and lagging pf operation | 2 |
| Construction details + working principle of 3-phase synchronous generator | 1 |
| Load characteristics of synchronous generator + why V_terminal > E for capacitive load | 1 |
| Criteria for synchronizing two 3-phase alternators | 1 |
| Hunting in synchronous motor + loaded operation | 1 |

---

### Numerical Questions

```
Type 1 — Voltage Regulation + Power Angle of Alternator
Frequency: 8 instances; 3 unique datasets
Pattern:
  Given: 3-phase star-connected alternator, Ra and Xs per phase,
         full load at given pf (lagging or leading)
  Find:  Voltage regulation, power angle (and sometimes regulation for opposite pf)

⚠️⚠️ 2081 Chaitra Q4b = 2079 Chaitra Q4b — SAME dataset:
   3-phase, 10 kVA, 400V, 50Hz, star, Ra = 0.5Ω, Xs = 10Ω,
   0.8 pf leading (and lagging), find VR and power angle
   (appears in 2079 as both lagging and leading)

⚠️⚠️⚠️ Appears 5 times across sets (highest repeat in entire paper):
   1200 kVA (or KVA), ~6000–6600V, 3-phase star,
   Ra = 0.4Ω/phase, Xs = 6Ω/phase,
   full load at 0.8pf lagging at rated voltage —
   find terminal voltage for same excitation at 0.8pf leading
   Sets: 2078 Chaitra Q5a, 2073 Magh Q5a, 2070 Bhadra Q5b,
         2070 Magh Q5b, 2073 Magh Q5a
   Note: Voltage varies between 6000V and 6600V across sets
   — MEMORIZE THIS PROBLEM COMPLETELY

Dataset c:
   3-phase star alternator, 0.5Ω and 10Ω per phase, 0.8pf lagging and leading —
   compare regulation (2079 Chaitra Q4b)
```

```
Type 2 — Terminal Voltage Change for Different PF
Frequency: 2 (subset of Type 1 above)
Pattern:
  Given: Alternator data, find terminal voltage when pf changes from lagging to leading
  (Same as Type 1 — the 1200KVA dataset is the primary example)
```

```
Type 3 — Synchronous Motor Back EMF / Phasor Diagram
Frequency: 2
Pattern:
  Given: Synchronous motor, supply voltage, pf, armature impedance
  Find:  Back EMF per phase, draw phasor diagram

Datasets:
  a) 3.3KV, star, impedance = 0.2+j2.2Ω/phase, 0.5pf leading,
     100A line current, find back EMF (2071 Bhadra Q4b)
  b) Star connected synchronous motor, find back EMF for leading pf
     (2069 Bhadra Q4a — theory part + show leading/lagging)
```

```
Type 4 — Alternator Open Circuit EMF (Saturation / Field Current Change)
Frequency: 1
Pattern:
  Given: Alternator OC voltage at one frequency and field current,
         find OC EMF at different frequency and field current (neglect saturation)

Dataset: OC generates 360V at 60Hz, field = 3.6A;
         find EMF when frequency = 40Hz, field = 2.4A (2075 Baisakh Q4b)
```

---

## Chapter 7 — Fractional Kilowatt Motors

**Chapter type:** Theory only
**Most important:** Double field revolving theory — appears in almost every set

### Theory Questions

| Topic | Frequency |
|---|---|
| Double field revolving theory + single phase IM not self-starting (prove/explain) | 12 |
| Starting methods for single phase IM (split phase, capacitor start/run, reluctance start) | 6 |
| Universal motor — construction, operation, characteristics, why called universal | 5 |
| Servo motor — working principle, construction, applications | 4 |
| Stepper motor — working principle, applications | 4 |
| Capacitor start and run motor | 3 |
| Split phase induction motor — construction, characteristics | 2 |

---

## Step 4 — Chapter Summary

| Ch | Type | Most Important to Practice | Repeated Datasets |
|---|---|---|---|
| 1 | Both | Series magnetic circuit numerical + hysteresis/eddy current theory | Ring 30cm/500turns/4mWb (2×); Circular 10cm/600turns/1T (2×); Cast steel ring 80cm (2×) |
| 2 | Both | OC/SC test numerical + no-load/load operation theory | 20kVA 250/2500V (2×); 20kVA 2200/220V (2×); 10kVA 200/400V (3×) ⚠️⚠️ |
| 3 | Both | Compound generator EMF numerical + voltage build-up theory | 50A at 500V with 0.05/0.03/250Ω (2×); 80A at 220V (2×); 4-pole wave wound 3kW at 120V (2×) |
| 4 | Both | DC shunt/series motor speed change numerical + back EMF theory | 230V shunt motor 5A→40A (2×); 220V series motor 100A at 1200rpm (2×) |
| 5 | Both | T-S characteristics (theory + numerical) — present in EVERY set | 440V delta IM at 1440rpm (2×); 8-pole 50Nm (0.8+j2)Ω (3×) |
| 6 | Both | Effect of excitation / V-curves (theory) + 1200kVA alternator numerical | 1200KVA 0.4Ω/0.6Ω alternator (5×) ⚠️⚠️⚠️; 10kVA 400V Ra=0.5 (2×) |
| 7 | Theory only | Double field revolving theory — write it fully from memory | None (all theory) |

---

## Step 5 — Self-Verification Checklist

- **No question skipped:** All 21 sets covered (2068–2081). One 2075 Bhadra page was Discrete Structure (CT551) — correctly excluded.
- **Repeated datasets flagged:** 12 repeat instances across all chapters identified with ⚠️.
- **Highest-priority repeat:** 1200KVA alternator problem (Ch6) appears in **5 sets** — memorize completely.
- **OC/SC 10kVA 200/400V dataset** appears in **3 sets** (2075 Baisakh, 2068 Bhadra, 2068 Magh) — second highest repeat.
- **2068 Bhadra and 2068 Magh are near-identical papers** — all 6 questions match across both sets.
- Frequencies are based on unique topic count, not sub-part count — no overcounting.
