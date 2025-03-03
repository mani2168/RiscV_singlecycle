# RISC-V Single-Cycle Processor

## Project Overview
This project implements a single-cycle RISC-V processor using Verilog on an FPGA. The processor follows the RISC-V instruction set architecture (ISA) and executes instructions in a single clock cycle. The design includes an ALU, a control unit, and a structured datapath to handle various instruction types.

## Features
- Supports RISC-V 32-bit instruction set (RV32I)
- Implements fundamental instruction types:
  - R-type (Register operations)
  - I-type (Immediate operations)
  - S-type (Store operations)
  - B-type (Branch operations)
- Arithmetic Logic Unit (ALU) capable of performing basic operations
- Control Unit with an instruction decoder
- Data memory and register file
- Single-cycle execution for all instructions

## Components
### 1. Arithmetic Logic Unit (ALU)
- Performs arithmetic and logical operations
- Generates a 32-bit result and a zero flag
- Controlled by a 3-bit ALUControl signal

### 2. Control Unit
- Decodes instruction opcodes and function fields
- Generates control signals for datapath elements
- Includes a main decoder and ALU decoder

### 3. Datapath
- Connects components for instruction execution
- Includes:
  - Program Counter (PC)
  - Instruction Memory
  - Register File
  - ALU
  - Data Memory
  - Control Signals

## Instruction Execution
1. Fetch: The instruction is fetched from memory.
2. Decode: The control unit interprets the instruction.
3. Execute: The ALU processes the operation.
4. Memory Access: Data is read/written to memory (for load/store instructions).
5. Writeback: Results are written to the register file.

## Block Diagrams
- ALU Structure
- Control Unit Structure
- Datapath for Load/Store and R-Type Instructions

## Implementation Details
- Developed using Verilog
- Simulated and tested using testbenches
- Synthesized for FPGA implementation

## Future Improvements
- Support for additional RISC-V instruction formats (U-type, J-type)
- Pipeline implementation for improved performance
- Enhanced debugging and performance monitoring tools

## References
- RISC-V Instruction Set Manual
- FPGA Development Tools Documentation


