<h1 align="center">Penchalanarasaiah Kuncham</h1>

<p align="center">
  <b>PhD Research Scholar · IIT Bombay</b><br>
  GNSS signal processing · spoofing and jamming detection · FPGA / RTL design
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/penchalanarasaiah-kuncham"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:penchalanarasaiah.77@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Email"></a>
  <img src="https://img.shields.io/badge/Mumbai,%20India-2E7D32?style=flat-square&logo=googlemaps&logoColor=white" alt="Mumbai, India">
</p>

---

### About

I'm a PhD research scholar at **IIT Bombay**, working on GNSS receiver signal
processing, with a focus on detecting and mitigating spoofing and jamming
attacks on satellite navigation. My work spans the full receiver chain:
acquisition, tracking loops, and the PVT solution. Alongside that I work on
embedded systems for real-time signal processing.

Before the PhD I built a lot of sensor-driven embedded hardware. That work is in
[embedded-iot-projects](https://github.com/Penchal9959/embedded-iot-projects).

---

### Research interests

| Area | What I work on |
|------|----------------|
| **GNSS signal processing** | Acquisition, tracking loops, correlator design, PVT solution |
| **Spoofing and jamming** | Detection through spatial processing; interference characterisation |
| **FPGA / RTL** | Verilog datapaths and AXI4-Stream capture logic on Xilinx Zynq-7000 |
| **VLSI / physical design** | Full-custom CMOS layout and SPICE characterisation on SkyWater 130 nm; RTL-to-GDSII on 65 nm — synthesis, place and route, timing signoff |
| **Design automation** | Logic simulation, two-level minimisation and formal equivalence checking, built from scratch |
| **Embedded systems** | Real-time DSP on constrained hardware |

---

### Selected repositories

Every one of these opens with what is verified and by which command, and closes
with what is not.

| Repository | What it is |
|------------|-----------|
| [zynq-gnss-data-capture](https://github.com/Penchal9959/zynq-gnss-data-capture) | FPGA data acquisition for a GNSS RF front-end on a ZC706. Custom AXI4-Stream packer in the PL, capture to DDR3 and microSD from the PS |
| [zynq-hdmi-rasterizer](https://github.com/Penchal9959/zynq-hdmi-rasterizer) | Verilog triangle rasterizer driving HDMI directly on a PYNQ-Z2. Edge-function fill, one pixel per clock, no frame buffer |
| [kogge-stone-adder-16bit](https://github.com/Penchal9959/kogge-stone-adder-16bit) | 16-bit parallel prefix adder from Verilog to GDSII on 65 nm. Self-checking simulation, Genus synthesis, Innovus place and route, timing signoff |
| [sky130-standard-cell-library](https://github.com/Penchal9959/sky130-standard-cell-library) | Three CMOS standard cells with layout, LEF, netlists and Verilog. Two of the three reach the Liberty view; the README says why the third does not, and audits which measurements were fit to publish |
| [sky130-inverter-layout](https://github.com/Penchal9959/sky130-inverter-layout) | Full-custom CMOS cells drawn in Magic on SkyWater 130 nm. DRC and LVS clean, parasitic-extracted and re-simulated |
| [sky130-inverter-characterisation](https://github.com/Penchal9959/sky130-inverter-characterisation) | SPICE characterisation of a CMOS inverter. Delay, transfer curve, noise margins, and what transistor sizing actually buys |
| [combinational-equivalence-checker](https://github.com/Penchal9959/combinational-equivalence-checker) | Miter-based equivalence checking. A complete justification search and 64-bit-parallel random simulation, both differential-tested against an exhaustive oracle |
| [espresso-logic-minimizer](https://github.com/Penchal9959/espresso-logic-minimizer) | Two-level boolean minimisation. Expand, irredundant and reduce over cube covers, every result verified exhaustively against its input |
| [gate-level-logic-simulator](https://github.com/Penchal9959/gate-level-logic-simulator) | Levelised logic simulator for structural VHDL. Topological scheduling and three-valued gate evaluation, exhaustively tested on ISCAS-85 c17 |
| [verilog-digital-design](https://github.com/Penchal9959/verilog-digital-design) | RTL designs: FSM-controlled multiplier, sequence detectors, true dual-port RAM. Self-checking testbenches, all passing under Icarus Verilog |
| [embedded-iot-projects](https://github.com/Penchal9959/embedded-iot-projects) | Twelve microcontroller projects. GSM alerting, sensor-triggered actuation, solar-powered field deployment. All twelve compile under `arduino-cli` |
| [Robotic_Vending_Dispenser](https://github.com/Penchal9959/Robotic_Vending_Dispenser) | PyQt5 touchscreen interface for a self-service juice machine on a Raspberry Pi 4. The interface only: the motor control and the payment processing are elsewhere |

---

### Toolchain

<p>
  <img src="https://img.shields.io/badge/Verilog-B22222?style=flat-square&logo=v&logoColor=white" alt="Verilog">
  <img src="https://img.shields.io/badge/VHDL-4B0082?style=flat-square" alt="VHDL">
  <img src="https://img.shields.io/badge/MATLAB-0076A8?style=flat-square&logo=mathworks&logoColor=white" alt="MATLAB">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/C%2FC%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white" alt="C/C++">
</p>
