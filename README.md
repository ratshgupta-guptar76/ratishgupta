# Ratish Gupta

Computer Engineering student at McMaster University. Interested in digital IC design, RTL verification, and hardware for ML workloads.

I'm looking for internships and new grad roles in digital design and verification. Most of my projects right now are FPGA prototyping and SystemVerilog work, with a focus on getting the verification flow right rather than just writing RTL that compiles.

## Projects

### [INT8 Systolic MAC Array](https://github.com/ratshgupta-guptar76/int8-systolic-mac-array)
`SystemVerilog` `cocotb` `Verilator` `Vivado`

Parameterized output stationary INT8 systolic MAC array, sized for the Q/K/V/O projections in transformer attention. The array uses signed INT8 inputs accumulating into INT32, with a counter based skew unit feeding an N by N PE mesh.

What I actually verified and measured:

* 10,000 random matmul tests pass at both 4x4 and 8x8 against a NumPy reference, run through cocotb on Verilator. Same RTL, only parameters change between the two configurations.
* Synthesized for the Nexys A7-100T (`xc7a100tcsg324-1`). The 8x8 array uses 64 DSP48E1 blocks and closes timing at the 100 MHz target with about 3.76 ns of positive slack, which works out to roughly 160 MHz Fmax.
* Wrote a 6 state FSM wrapper around the bare array so it has a serial AXI Stream style interface instead of the unrealistic 3,000+ port parallel load. Not fully AXI-S compliant (no TLAST), but the protocol pattern is there.

### [Traffic Light Controller](https://github.com/ratshgupta-guptar76/traffic-light-controller)
`Verilog` `QuestaSim`

FSM based controller for a 2-way intersection, written in Verilog and simulated in QuestaSim. Simulation only, no board bring up. Smaller learning project from earlier on.

## Tools and Languages

| Area | What I use |
|---|---|
| RTL | SystemVerilog, Verilog |
| Verification | cocotb, Verilator, QuestaSim, directed testbenches, NumPy golden models |
| Synthesis | Vivado, Quartus |
| Scripting | Python, Tcl, Make |

## Contact

* LinkedIn: [in/ratish-gupta](https://www.linkedin.com/in/ratish-gupta/)
* Personal site: [ratishgupta.com](https://ratishgupta.com)
