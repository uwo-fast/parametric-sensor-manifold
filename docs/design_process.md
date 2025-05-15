# Engineering Design Process

## Problem

inserting probes directly into the main bioreactor vessel poses several challenges and issues

- general (electro)mechanical integration
- small vessels there are size contraints
- large vessels sampling a single area may be inaccurate
- large vessels using external mounting (not submerged within vessel) may not yield measurements that are reflective of the inner (bulk) volume of the vessel
  - one option is submersion, but waterproofing is is inherintly difficult and adds significant complexity if the sensor is not already submersible
  - another option is extending mounting into the (center of the) vessel, but this adds additional integration complexity, material cost,...
- every sensor / probe has its own requirements and constraints for interfacing, storage, calibration, minimum sample size,...

## Goal

Design a modular, parametric flow‑cell manifold for multiplexed sensor probes that:

- Is low-cost and accessible
- Is easy to use, modify and reproduce for the target user [group]
- Is printable on an average low‑cost, desktop resin printer
- Minimizes dead‑volume (sample waste)
- Has reliable, secure, and leak‑free mechanical connections
- Can accomadate a wide range of commercial and custom sensors with unique requirements and constraints

## Literature Review & SotA

Only key references are included here, for the full literature review see the [Zotero library](https://).

## Requirements

### Functional

- **Flow splitting**: distribution satisfies the input requirements of each sensor probe module
- **Probe interface**: accommodates constrains of sensor geometry & it's unique requirements (e.g. calibration, storage, maintainance)
- **Connection sealing**: all fluid connection points seal effectively and reliably to prevent any fluid leaks

### Performance

- **Max back‑pressure**: < sensor’s allowable pressure drop
- **Min channel diameter**: ≥ resin print minimum feature size (~0.5 mm)
- **Min dead‑volume**: ≤ probe’s required sample volume (e.g. 50 µL)

### Non‑functional

- **Material compatibility**: biologically compatible and chemically resistant to sample & cleaning agents
- **Surface finish**: internal channels smooth enough for laminar flow (Ra < 10 µm)
- **Ease of cleaning**: flushable with standard sanitizing fluids and all key points are accessible for direct physical cleaning

## Constraints

- No larger than 100mmx50mmx120mm to be [printable on the average desktop resin printer](./resin_printer_comparison.md)
  - XY resolution ~50 µm, Z layer height ≥ 25 µm
- All connection points are semi-permenant (e.g. no adhesives)
- All surfaces that come in contact with the fluid sample must be biocompatible
-

## Conceptual Design

1. **Manifold Head**
   - Central inlet port → short plenum → radial “spokes” (equal‑length branches)
   - Negative‑tolerance holes at end of each branch for tubing
2. **Probe Modules**
   - Small blocks that slide onto tubing ends (OD = 1.6 mm)
   - Internal port aligns with sensor measurement chamber
   - Optional additional port for buffer/calibration fluid
3. **Tubing Connection**
   - Branch holes sized 0.05 mm smaller than tubing OD → press‑fit seal
   - Tubing length standardized for consistent dead‑volume

## Detailed Design
