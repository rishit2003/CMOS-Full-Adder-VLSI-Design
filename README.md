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

**Schematic And Layout**
Below are the key schematic and layout views so reviewers can validate the core design without opening the report.

NAND gate views are shown first.

Shown below is **Figure 3: CMOS NAND Gate Schematic**.
![Figure 3](docs/images/extracted/img_022_979x821.png)

Shown below is **Figure 4: NAND Gate Layout**.
![Figure 4](docs/images/extracted/img_026_894x816.png)

Full adder views are shown next.

Shown below is **Figure 7: Full Adder Schematic with Numbered Gates**.
![Figure 7](docs/images/extracted/img_038_2048x730.png)

Shown below is **Figure 8: Full Adder Layout**.
![Figure 8](docs/images/extracted/img_042_2048x730.png)

**Toolchain**
- Cadence Virtuoso for schematic and layout
- Spectre for simulation
- Calibre for DRC, LVS, and PEX
- 180 nm PDK and rule decks (not included)

**For Full Details**
For full simulations, PEX netlists, DRC/LVS reports, plots, and analysis, see `docs/Report.pdf`.

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
