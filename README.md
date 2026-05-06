# Ratish Gupta

**Computer Engineering @ McMaster University**  
Digital IC Design · RTL Verification · ML Hardware Acceleration

I design and verify digital hardware — RTL to silicon timing closure. My focus is on compute architectures for ML workloads: systolic arrays, dataflow optimization, and FPGA prototyping. I'm targeting roles in Digital IC Design, RTL Verification, and ASIC/FPGA engineering.

---

## Featured Projects

### [INT8 Systolic MAC Array for Transformer Acceleration](https://github.com/ratshgupta-guptar76/int8-systolic-mac-array)
`SystemVerilog` `cocotb` `Verilator` `Vivado`

Parameterized output-stationary INT8 systolic MAC array targeting Q/K/V/O projections in transformer attention. Designed to address the memory bandwidth bottleneck in CPU-based matmul for LLM inference.

- **Verified:** 10,000 random INT8 matmuls at 4×4 and 8×8 against NumPy golden model via cocotb + Verilator — zero failures, zero RTL changes between parameter sweeps
- **Synthesized:** Nexys A7-100T (`xc7a100tcsg324-1`) — 64 DSP48E1 units, timing closed at 100 MHz target with **160 MHz Fmax** (WNS = +3.76 ns)
- **Interfaces:** AXI-S style serial wrapper with 6-state FSM (IDLE → LOAD_A → LOAD_B → DELAY → COMPUTE → OUTPUT)
- Milestone 1 of 7 in a Compute-In-Memory transformer accelerator project

---

### [Traffic Light FSM Controller](https://github.com/ratshgupta-guptar76/traffic-light-controller)
`Verilog` `QuestaSim`

FSM-based traffic light controller for a 2-way intersection, implemented on FPGA. Covers state encoding, timing logic, and simulation with directed testbenches in QuestaSim.

---

## Skills

| Domain | Tools & Languages |
|---|---|
| RTL Design | SystemVerilog, Verilog |
| Verification | cocotb, Verilator, QuestaSim, directed & random testbenches |
| Synthesis & P&R | Vivado, Quartus |
| Scripting & Automation | Python, Tcl, Make |
| Numerical Verification | NumPy golden models, bit-exact comparison |

---

## Currently Working On

- **Milestone 2** of the systolic array project: BRAM-tiled double-buffered input staging for K > array size
- Building out my [personal portfolio site](https://ratishgupta.com) — source at [`ratish-portfolio`](https://github.com/ratshgupta-guptar76/ratish-portfolio)

---

## Contact

- **LinkedIn:** [in/ratish-gupta](https://www.linkedin.com/in/ratish-gupta/)
- **Website:** [ratishgupta.com](https://ratishgupta.com)
- **Blog:** [ratishg2005.blogspot.com](https://ratishg2005.blogspot.com)
