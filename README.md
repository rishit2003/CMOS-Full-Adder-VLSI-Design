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

I started by sizing CMOS NAND devices to balance rise/fall behavior, then built the full adder from NAND primitives and completed the layout. The schematic, layout, and extracted netlists are shown below.

Shown below is **Figure 1: Effect of NMOS Gate Width on Adder Sum Output Fall Time**.

![Figure 1](docs/images/extracted/img_015_951x827.png)

Shown below is **Figure 2: Effect of PMOS Gate Width on Adder Sum Output Rise Time**.

![Figure 2](docs/images/extracted/img_016_948x826.png)

Shown below is **Figure 3: CMOS NAND Gate Schematic**.

![Figure 3](docs/images/extracted/img_022_979x821.png)

Shown below is **Figure 4: NAND Gate Layout**.

![Figure 4](docs/images/extracted/img_026_894x816.png)

Shown below is **Figure 5: NAND PEX Extracted Netlist**.

![Figure 5](docs/images/extracted/img_030_1504x1027.png)

Shown below is **Figure 7: Full Adder Schematic with Numbered Gates**.

![Figure 7](docs/images/extracted/img_038_2048x730.png)

Shown below is **Figure 8: Full Adder Layout**.

![Figure 8](docs/images/extracted/img_042_2048x730.png)

Shown below is **Figure 9: Full Adder PEX Extracted Netlist**.

![Figure 9](docs/images/extracted/img_043_2048x1228.png)

**NAND Characterization**

I characterized the NAND gate with and without output load and recorded delay, power, and DC operating points. The testbenches and waveforms are shown below.

Shown below is **Figure 10: NAND Gate Simulation Testbench (Without Load)**.

![Figure 10](docs/images/extracted/img_048_1009x914.png)

Shown below is **Figure 12: NAND Gate Simulation Waveform**.

![Figure 12](docs/images/extracted/img_057_1714x777.png)

Shown below is **Figure 13: Delay and Average Power of NAND Layout**.

![Figure 13](docs/images/extracted/img_058_1239x818.png)

Shown below is **Figure 14: Delay and Average Power of NAND Schematic**.

![Figure 14](docs/images/extracted/img_063_1602x828.png)

Shown below is **Figure 15: NAND Gate Layout Static Power Dissipation**.

![Figure 15](docs/images/extracted/img_067_758x514.png)

Shown below is **Figure 16: NAND Gate Layout DC Simulation Outputs**.

![Figure 16](docs/images/extracted/img_068_758x514.png)

**Full Adder Characterization**

I ran transient and DC simulations for the full adder (schematic and extracted views) and summarized power/delay trends. The key simulation views are shown below.

Shown below is **Figure 19: Full Adder Simulation Testbench (With Load)**.

![Figure 19](docs/images/extracted/img_074_1916x828.jpg)

Shown below is **Figure 20: Full Adder Schematic Simulation**.

![Figure 20](docs/images/extracted/img_075_712x514.png)

Shown below is **Figure 21: Full Adder Extracted Simulation**.

![Figure 21](docs/images/extracted/img_076_1916x828.png)

Shown below is **Figure 23: Average Power and Delay of Full Adder Schematic (With Output Load)**.

![Figure 23](docs/images/extracted/img_081_1731x828.png)

Shown below is **Figure 24: Average Power and Delay of Full Adder Layout (Without Output Load)**.

![Figure 24](docs/images/extracted/img_082_1731x828.png)

Shown below is **Figure 25: Average Power and Delay of Full Adder Layout (With Output Load)**.

![Figure 25](docs/images/extracted/img_086_1916x828.png)

Shown below is **Figure 26: Full Adder DC Simulation Results**.

![Figure 26](docs/images/extracted/img_087_1602x828.png)

Shown below is **Figure 27: Full Adder Voltage Levels**.

![Figure 27](docs/images/extracted/img_095_712x514.png)

Shown below is **Figure 28: Full Adder Silicon Area**.

![Figure 28](docs/images/extracted/img_096_601x514.png)

Shown below is **Figure 29: Comparing Power Consumption to Reference Design**.

![Figure 29](docs/images/extracted/img_097_712x514.png)

Shown below is **Figure 30: Comparing Delay to Reference Design**.

![Figure 30](docs/images/extracted/img_098_601x514.png)

**Verification (DRC/LVS)**

Final sign-off checks confirm the layout is manufacturable and matches the schematic. The DRC and LVS results are shown below.

Shown below is **Figure 33: NAND Layout DRC Results**.

![Figure 33](docs/images/extracted/img_132_545x632.png)

Shown below is **Figure 34: Full Adder Layout DRC Results**.

![Figure 34](docs/images/extracted/img_133_871x632.png)

Shown below is **Figure 35: NAND Layout LVS Results**.

![Figure 35](docs/images/extracted/img_134_871x632.png)

Shown below is **Figure 36: Full Adder Layout LVS Results**.

![Figure 36](docs/images/extracted/img_135_871x632.png)

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
