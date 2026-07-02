RISC-V Processor: SystemVerilog Implementation

A RISC-V processor implemented in SystemVerilog, developed as part of the Computer Architecture Lab (EE-475L) at UET Lahore. The repository contains two implementations: a single-cycle processor and a 3-stage pipelined processor with full FPGA deployment on Nexys A7.


Repository Structure:
├── Single cycle/        # Single-cycle RISC-V processor
├── 3 Stage Pipeline/    # Pipelined processor with FPGA & UART
│   ├── pipeline/        # RTL source files
│   ├── FPGA/            # Nexys A7 top-level and constraints
│   ├── UART/            # UART integration modules
│   ├── TBs/             # Testbenches (with/without hazard)
│   └── Diagram/         # Pipeline block diagram

Single-Cycle Processor:

A baseline RISC-V processor where each instruction completes in one clock cycle.
Key modules:
- ALU, Register File, Instruction Memory, Data Memory
- Immediate Generator, Instruction Decoder
- Datapath and MUX logic

3-Stage Pipelined Processor:

An optimized RISC-V processor with a 3-stage pipeline: **Fetch → Execute → Writeback**

**Key features:**
- Hazard detection and data forwarding (verified across 2 hazard scenarios)
- UART integration for serial communication (MMIO-based)
- 7-segment display output
- FPGA implementation on Nexys A7 (Vivado)

Tools used: QuestaSim, Vivado, SystemVerilog

How to Run (Simulation)
1. Open QuestaSim
2. Compile all `.sv` files in the relevant folder
3. Run the testbench (`tb_with_hazard.sv` or `tb_without_hazard.sv`)
4. Load `.hex` memory files when prompted

Tools & Technologies

- Language: SystemVerilog
- Simulation: QuestaSim
- Synthesis: Vivado
- FPGA Board: Nexys A7 (Artix-7)
- ISA: RISC-V (RV32I subset)

 BS Electrical Engineering, UET Lahore (2022–2026)
