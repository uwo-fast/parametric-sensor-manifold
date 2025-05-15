# Engineering Design Process

## 1. Problem Statement

Inserting probes directly into the main bioreactor vessel poses several challenges:

- **Integration complexity**: mechanical, electrical and sealing issues for (electro)mechanical integration
- **Size constraints**: small vessels limit probe dimensions; large vessels risk poor representative sampling
- **Measurement fidelity**: external or peripheral measurements may not reflect bulk conditions
  - Waterproofing submersible sensors adds complexity and cost
  - Extended‐mount probes require complex fixtures and introduce dead volume
- **Sensor‐specific needs**: each probe has its own geometry, minimum sample volume, calibration and storage requirements

## 2. Goal

Design a **modular, parametric flow‑cell manifold** for multiplexed sensor probes that:

- Is low‑cost, accessible and reproducible by target user(s)
- Prints on an average desktop resin printer
- Minimizes dead‑volume
- Provides reliable, leak‑free, semi‑permanent connections (no adhesives)
- Accommodates a wide range of commercial and custom sensors

## 3. Literature Review & SotA

Only key references are included here, for the full literature review see the [Zotero library](https://).

## 4. Requirements

### 4.1 Functional

- **Flow splitting**: deliver equalized sample flow to each probe
- **Probe interface**: support sensor geometry, calibration/buffer ports and ease of replacement
- **Connection sealing**: press‑fit or clamp seals at all tubing and module interfaces

### 4.2 Performance

- **Max back‑pressure**: below the sensor’s allowable pressure drop
- **Channel diameter**: ≥ 0.5 mm (resin print minimum feature size)

### 4.3 Non‑functional

- **Material compatibility**: biocompatible and chemically resistant to samples and cleaning agents
- **Surface finish**: Ra < 10 µm inside channels for laminar flow
- **Cleanability**: flushable with standard sanitizing fluids; no blind spots

## 5. Constraints

- **Print volume**: use volume ≤ 100 × 50 × 120 mm (XY resolution ~50 µm, Z layer ≥ 25 µm)
- **No adhesives**: all joints rely on mechanical seals (press‑fit tubing, O‑rings)
- **Biocompatibility**: all wetted surfaces must meet biocompatibility standards

## 6. Conceptual Design

1. **Manifold Head**
   - Central inlet port → short plenum → radial “spokes” (equal‑length branches)
   - Negative‑tolerance holes at end of each branch for tubing
2. **Probe Modules**
   - Internal port aligns with sensor measurement chamber
   - Slightly offset angle from the normal to prevent air pockets on sensor
   - Optional additional port for buffer/calibration fluid
3. **Tubing Connection**
   - Branch holes sized 0.05 mm smaller than tubing OD → press‑fit seal

## Detailed Design
