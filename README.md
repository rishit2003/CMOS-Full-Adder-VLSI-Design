# NAND-Based Full Adder (180 nm CMOS)

A 1-bit NAND-based full adder implemented in 180 nm CMOS, including schematic design, layout, DRC/LVS verification, parasitic extraction (Calibre PEX), and post-layout simulation. The full adder is built from 9 NAND gates (36 transistors total).

## Why This Matters
This project demonstrates end-to-end VLSI flow ownership: transistor-level design, physical layout, verification, parasitic-aware simulation, and performance analysis. It maps directly to core digital/ASIC design skills recruiters look for.

## Highlights
- Post-layout average dynamic power: 62.6 uW
- Post-layout propagation delay to Sum (with output load): 353.5 ps
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

## What I Did
- Designed CMOS NAND gate at transistor level and sized devices for delay/power tradeoffs.
- Built a 1-bit full adder using 9 NAND gates and verified logic correctness.
- Completed layout and ran DRC/LVS to confirm manufacturability and schematic match.
- Performed parasitic extraction (Calibre PEX) and post-layout transient simulations.
- Analyzed post-layout timing/power impact and documented results.

## Toolchain
- Cadence Virtuoso for schematic and layout
- Spectre for simulation
- Calibre for DRC, LVS, and PEX
- 180 nm PDK and rule decks (not included)

## Key Figures
A quick visual summary. Full figure set is below.

| | |
| --- | --- |
| ![Key figure](docs/images/extracted/img_043_2048x1228.png) | ![Key figure](docs/images/extracted/img_074_1916x828.jpg) |
| ![Key figure](docs/images/extracted/img_076_1916x828.png) | ![Key figure](docs/images/extracted/img_086_1916x828.png) |
| ![Key figure](docs/images/extracted/img_114_1916x828.png) | ![Key figure](docs/images/extracted/img_030_1504x1027.png) |
| ![Key figure](docs/images/extracted/img_031_1504x1027.png) | ![Key figure](docs/images/extracted/img_038_2048x730.png) |

## Full Figure Set (No Need to Open the Report)
All images were extracted from `docs/Report.pdf` so the entire project can be reviewed from here.

**Figure 01** (951x827)
![Figure 01](docs/images/extracted/img_015_951x827.png)
**Figure 02** (948x826)
![Figure 02](docs/images/extracted/img_016_948x826.png)
**Figure 03** (979x821)
![Figure 03](docs/images/extracted/img_022_979x821.png)
**Figure 04** (894x816)
![Figure 04](docs/images/extracted/img_026_894x816.png)
**Figure 05** (1504x1027)
![Figure 05](docs/images/extracted/img_030_1504x1027.png)
**Figure 06** (1504x1027)
![Figure 06](docs/images/extracted/img_031_1504x1027.png)
**Figure 07** (2048x730)
![Figure 07](docs/images/extracted/img_038_2048x730.png)
**Figure 08** (2048x730)
![Figure 08](docs/images/extracted/img_042_2048x730.png)
**Figure 09** (2048x1228)
![Figure 09](docs/images/extracted/img_043_2048x1228.png)
**Figure 10** (1009x914)
![Figure 10](docs/images/extracted/img_048_1009x914.png)
**Figure 11** (1009x914)
![Figure 11](docs/images/extracted/img_049_1009x914.png)
**Figure 12** (1714x777)
![Figure 12](docs/images/extracted/img_057_1714x777.png)
**Figure 13** (1239x818)
![Figure 13](docs/images/extracted/img_058_1239x818.png)
**Figure 14** (1602x828)
![Figure 14](docs/images/extracted/img_063_1602x828.png)
**Figure 15** (758x514)
![Figure 15](docs/images/extracted/img_067_758x514.png)
**Figure 16** (758x514)
![Figure 16](docs/images/extracted/img_068_758x514.png)
**Figure 17** (758x514)
![Figure 17](docs/images/extracted/img_069_758x514.png)
**Figure 18** (758x514)
![Figure 18](docs/images/extracted/img_070_758x514.png)
**Figure 19** (1916x828)
![Figure 19](docs/images/extracted/img_074_1916x828.jpg)
**Figure 20** (712x514)
![Figure 20](docs/images/extracted/img_075_712x514.png)
**Figure 21** (1916x828)
![Figure 21](docs/images/extracted/img_076_1916x828.png)
**Figure 22** (712x514)
![Figure 22](docs/images/extracted/img_077_712x514.png)
**Figure 23** (1731x828)
![Figure 23](docs/images/extracted/img_081_1731x828.png)
**Figure 24** (1731x828)
![Figure 24](docs/images/extracted/img_082_1731x828.png)
**Figure 25** (1916x828)
![Figure 25](docs/images/extracted/img_086_1916x828.png)
**Figure 26** (1602x828)
![Figure 26](docs/images/extracted/img_087_1602x828.png)
**Figure 27** (712x514)
![Figure 27](docs/images/extracted/img_095_712x514.png)
**Figure 28** (601x514)
![Figure 28](docs/images/extracted/img_096_601x514.png)
**Figure 29** (712x514)
![Figure 29](docs/images/extracted/img_097_712x514.png)
**Figure 30** (601x514)
![Figure 30](docs/images/extracted/img_098_601x514.png)
**Figure 31** (712x514)
![Figure 31](docs/images/extracted/img_099_712x514.png)
**Figure 32** (601x514)
![Figure 32](docs/images/extracted/img_100_601x514.png)
**Figure 33** (712x514)
![Figure 33](docs/images/extracted/img_101_712x514.png)
**Figure 34** (601x514)
![Figure 34](docs/images/extracted/img_102_601x514.png)
**Figure 35** (712x514)
![Figure 35](docs/images/extracted/img_109_712x514.png)
**Figure 36** (712x514)
![Figure 36](docs/images/extracted/img_110_712x514.png)
**Figure 37** (1916x828)
![Figure 37](docs/images/extracted/img_114_1916x828.png)
**Figure 38** (739x402)
![Figure 38](docs/images/extracted/img_118_739x402.png)
**Figure 39** (1200x742)
![Figure 39](docs/images/extracted/img_119_1200x742.png)
**Figure 40** (739x402)
![Figure 40](docs/images/extracted/img_120_739x402.png)
**Figure 41** (1426x742)
![Figure 41](docs/images/extracted/img_124_1426x742.png)
**Figure 42** (545x632)
![Figure 42](docs/images/extracted/img_132_545x632.png)
**Figure 43** (871x632)
![Figure 43](docs/images/extracted/img_133_871x632.png)
**Figure 44** (871x632)
![Figure 44](docs/images/extracted/img_134_871x632.png)
**Figure 45** (871x632)
![Figure 45](docs/images/extracted/img_135_871x632.png)
**Figure 46** (545x632)
![Figure 46](docs/images/extracted/img_145_545x632.png)
**Figure 47** (871x632)
![Figure 47](docs/images/extracted/img_146_871x632.png)
**Figure 48** (871x632)
![Figure 48](docs/images/extracted/img_147_871x632.png)
**Figure 49** (871x632)
![Figure 49](docs/images/extracted/img_148_871x632.png)

## Repository Structure
- `FULLADDER/FULL_ADDER/`: full adder cell/library data
- `FULLADDER/NAND/`: NAND gate cell/library data
- `FULLADDER/*_TESTBENCH/`: testbenches
- `docs/Report.pdf`: sanitized project report
- `docs/images/extracted/`: images extracted from the report
- `*.sp`, `*.pex.netlist`: netlists (generated)
- `*_drc*`, `*_lvs*`, `*_erc*`: verification outputs

## Notes
- Foundry PDK and proprietary rule decks are not included.
- Netlists and verification outputs are generated artifacts and are typically excluded from version control.
