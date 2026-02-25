# NAND-Based Full Adder (180 nm CMOS)

## Overview
This project implements a 1-bit NAND-based full adder in 180 nm CMOS, including schematic design, layout, DRC/LVS, parasitic extraction (Calibre PEX), and post-layout simulation. The design is built from 9 NAND gates (36 transistors total).

## Highlights
- Post-layout average dynamic power: 62.6 uW
- Post-layout propagation delay to Sum (with load): 353.5 ps
- Layout silicon area: 26007.59 um^2
- DRC/LVS clean; PEX-based post-layout simulations

## Results (Full Adder Specifications)
Values are reported in the project report table for schematic/layout and with/without output load.

| Metric | Schematic (No Load) | Schematic (With Load) | Layout (No Load) | Layout (With Load) |
| --- | --- | --- | --- | --- |
| Delay to Sum (ps) | 142.3 | 161.6 | 298.9 | 353.5 |
| Delay to Carry (ps) | 42.37 | 53.43 | 144.146 | 179.46 |
| Avg. Dynamic Power (uW) | - | - | - | 62.6 |
| Silicon Area (um^2) | - | - | 26007.59 | - |

## Flow Summary
1. CMOS NAND gate sizing and schematic design.
2. Full adder built from 9 NAND gates.
3. Layout completed and validated with DRC/LVS.
4. Parasitic extraction (Calibre PEX) and post-layout transient simulation.

## Repository Structure
- `FULLADDER/FULL_ADDER/`: full adder cell/library data
- `FULLADDER/NAND/`: NAND gate cell/library data
- `FULLADDER/*_TESTBENCH/`: testbenches
- `*.sp`, `*.pex.netlist`: netlists (generated)
- `*_drc*`, `*_lvs*`, `*_erc*`: verification outputs

## Notes
- Foundry PDK and proprietary rule decks are not included.
- The full report can be placed under `docs/` (sanitized if needed).
