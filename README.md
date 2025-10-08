# Verilog-8-bit-RISC-Processor
A modular 8-bit RISC processor designed in Verilog, featuring a custom instruction set and validated on an FPGA.
# 8-bit RISC Processor in Verilog for FPGA Implementation

This repository contains the Verilog source code for a modular 8-bit RISC (Reduced Instruction Set Computer) processor. [cite_start]This project demonstrates a comprehensive understanding of computer architecture, from instruction set design to hardware implementation and validation on an FPGA. 

## Processor Architecture
The processor is designed with a classic 5-stage pipeline in mind (Fetch, Decode, Execute, Memory, Writeback), though this implementation is a simpler multi-cycle design for clarity.

### Core Modules
The design is highly modular to promote code reuse and clarity:
- **`processor_top.v`**: The top-level module that integrates all components.
- **`control_unit.v`**: A finite-state machine (FSM) that decodes instructions and generates control signals for all other modules.
- **`alu.v`**: An 8-bit Arithmetic Logic Unit supporting operations like ADD, SUB, AND, OR, and SLT.
- **`reg_file.v`**: An 8-register file, where each register is 8 bits wide.
- **`pc_module.v`**: The Program Counter, responsible for tracking the address of the next instruction.
- **`instruction_memory.v`**: A ROM module to store the program.
- **`data_memory.v`**: A RAM module for data storage.

### Custom Instruction Set Architecture (ISA)
A simple but functional 8-bit ISA was designed, including:
- **R-Type Instructions**: (e.g., `ADD`, `SUB`) for register-to-register operations.
- **I-Type Instructions**: (e.g., `ADDI`, `LW`, `SW`) for immediate and memory operations.
- **J-Type Instructions**: (e.g., `JMP`, `BEQ`) for control flow.

## Verification & Implementation
- **Simulation**: The design was thoroughly simulated using a Verilog testbench in ModelSim to verify the functionality of each instruction.
- **FPGA Validation**: The processor was synthesized using Xilinx Vivado and implemented on an FPGA. [cite_start]A simple program was executed to demonstrate real-world functionality. 

## Key Learnings
This project provided end-to-end experience in digital system design: from architectural definition and Verilog coding to simulation, synthesis, and hardware validation.
