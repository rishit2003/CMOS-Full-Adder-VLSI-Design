# NAND-Based Full Adder (180 nm CMOS)

A 1-bit NAND-based full adder implemented in 180 nm CMOS, including schematic design, layout, DRC/LVS verification, parasitic extraction (Calibre PEX), and post-layout simulation. The full adder is built from 9 NAND gates (36 transistors total).

**Resume Summary**
- Designed a 1-bit NAND-based full adder (9 NAND gates, 36 transistors) in 180 nm CMOS using schematic-to-layout flow.
- Verified manufacturability with DRC/LVS and performed parasitic extraction (Calibre PEX) with post-layout simulations.
- Measured post-layout performance: 353.5 ps Sum delay (with load), 62.6 uW dynamic power, 26,007.59 um^2 area.

**Highlights**
- Post-layout average dynamic power: 62.6 uW
- Post-layout propagation delay to Sum (with output load): 353.5 ps
- Layout silicon area: 26,007.59 um^2
- DRC/LVS clean; PEX-based post-layout simulations

**Results (Full Adder Specifications)**
Values are reported in the project report table for schematic/layout and with/without output load.

| Metric | Schematic (No Load) | Schematic (With Load) | Layout (No Load) | Layout (With Load) |
| --- | --- | --- | --- | --- |
| Delay to Sum (ps) | 142.3 | 161.6 | 298.9 | 353.5 |
| Delay to Carry (ps) | 42.37 | 53.43 | 144.146 | 179.46 |
| Avg. Dynamic Power (uW) | - | - | - | 62.6 |
| Silicon Area (um^2) | - | - | 26007.59 | - |

**What I Did**
- Sized CMOS NAND devices and validated delay/power tradeoffs.
- Built the full adder from NAND primitives and verified logic correctness.
- Implemented full custom layout, ran DRC/LVS, and extracted parasitics.
- Ran post-layout transient simulations and compared against schematic results.
- Documented results and analysis in the report.

**Toolchain**
- Cadence Virtuoso for schematic and layout
- Spectre for simulation
- Calibre for DRC, LVS, and PEX
- 180 nm PDK and rule decks (not included)

**Figures (From the Report)**
All figures below are extracted from `docs/Report.pdf`, so the complete project can be reviewed directly in this README.

**Design and Layout**
**Figure 1: Effect of NMOS Gate Width on Adder Sum Output Fall Time**
![Figure 1](docs/images/extracted/img_015_951x827.png)
**Figure 2: Effect of PMOS Gate Width on Adder Sum Output Rise Time**
![Figure 2](docs/images/extracted/img_016_948x826.png)
**Figure 3: CMOS NAND Gate Schematic**
![Figure 3](docs/images/extracted/img_022_979x821.png)
**Figure 4: NAND Gate Layout**
![Figure 4](docs/images/extracted/img_026_894x816.png)
**Figure 5: NAND PEX Extracted Netlist**
![Figure 5](docs/images/extracted/img_030_1504x1027.png)
**Figure 6: NAND-based Full-Adder Schematic**
![Figure 6](docs/images/extracted/img_031_1504x1027.png)
**Figure 7: Full Adder Schematic with Numbered Gates**
![Figure 7](docs/images/extracted/img_038_2048x730.png)
**Figure 8: Full Adder Layout**
![Figure 8](docs/images/extracted/img_042_2048x730.png)
**Figure 9: Full Adder PEX Extracted Netlist**
![Figure 9](docs/images/extracted/img_043_2048x1228.png)
**NAND Simulation**
**Figure 10: NAND Gate Simulation Testbench (Without Load)**
![Figure 10](docs/images/extracted/img_048_1009x914.png)
**Figure 11: NAND Gate Simulation Testbench (With Load)**
![Figure 11](docs/images/extracted/img_049_1009x914.png)
**Figure 12: NAND Gate Simulation Waveform**
![Figure 12](docs/images/extracted/img_057_1714x777.png)
**Figure 13: Delay and Average Power of NAND Layout**
![Figure 13](docs/images/extracted/img_058_1239x818.png)
**Figure 14: Delay and Average Power of NAND Schematic**
![Figure 14](docs/images/extracted/img_063_1602x828.png)
**Figure 15: NAND Gate Layout Static Power Dissipation**
![Figure 15](docs/images/extracted/img_067_758x514.png)
**Figure 16: NAND Gate Layout DC Simulation Outputs**
![Figure 16](docs/images/extracted/img_068_758x514.png)
**Figure 17: NAND Gate Voltage Levels**
![Figure 17](docs/images/extracted/img_069_758x514.png)
**Full Adder Simulation**
**Figure 18: Full Adder Simulation Testbench (Without Load)**
![Figure 18](docs/images/extracted/img_070_758x514.png)
**Figure 19: Full Adder Simulation Testbench (With Load)**
![Figure 19](docs/images/extracted/img_074_1916x828.jpg)
**Figure 20: Full Adder Schematic Simulation**
![Figure 20](docs/images/extracted/img_075_712x514.png)
**Figure 21: Full Adder Extracted Simulation**
![Figure 21](docs/images/extracted/img_076_1916x828.png)
**Figure 22: Average Power and Delay of Full Adder Schematic (Without Output Load)**
![Figure 22](docs/images/extracted/img_077_712x514.png)
**Figure 23: Average Power and Delay of Full Adder Schematic (With Output Load)**
![Figure 23](docs/images/extracted/img_081_1731x828.png)
**Figure 24: Average Power and Delay of Full Adder Layout (Without Output Load)**
![Figure 24](docs/images/extracted/img_082_1731x828.png)
**Figure 25: Average Power and Delay of Full Adder Layout (With Output Load)**
![Figure 25](docs/images/extracted/img_086_1916x828.png)
**Figure 26: Full Adder DC Simulation Results**
![Figure 26](docs/images/extracted/img_087_1602x828.png)
**Figure 27: Full Adder Voltage Levels**
![Figure 27](docs/images/extracted/img_095_712x514.png)
**Figure 28: Full Adder Silicon Area**
![Figure 28](docs/images/extracted/img_096_601x514.png)
**Figure 29: Comparing Power Consumption to Reference Design**
![Figure 29](docs/images/extracted/img_097_712x514.png)
**Figure 30: Comparing Delay to Reference Design**
![Figure 30](docs/images/extracted/img_098_601x514.png)
**Verification**
**Figure 33: NAND Layout DRC Results**
![Figure 33](docs/images/extracted/img_099_712x514.png)
**Figure 34: Full Adder Layout DRC Results**
![Figure 34](docs/images/extracted/img_100_601x514.png)
**Figure 35: NAND Layout LVS Results**
![Figure 35](docs/images/extracted/img_101_712x514.png)
**Figure 36: Full Adder Layout LVS Results**
![Figure 36](docs/images/extracted/img_102_601x514.png)

**Repository Structure**
- `FULLADDER/FULL_ADDER/`: full adder cell/library data
- `FULLADDER/NAND/`: NAND gate cell/library data
- `FULLADDER/*_TESTBENCH/`: testbenches
- `docs/Report.pdf`: sanitized project report
- `docs/images/extracted/`: images extracted from the report
- `*.sp`, `*.pex.netlist`: netlists (generated)
- `*_drc*`, `*_lvs*`, `*_erc*`: verification outputs

**Notes**
- Foundry PDK and proprietary rule decks are not included.
- Netlists and verification outputs are generated artifacts and are typically excluded from version control.
