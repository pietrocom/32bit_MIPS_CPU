# CI1210 - Digital Projects & Microprocessors (UFPR 2024/2)

Implementation of a simplified MIPS-based processor with custom ISA, developed in Digital.

## 📜 Project Overview

### Stage 1: Processor Design
**Custom ISA Implementation** (16 instructions):
- Arithmetic: `add`, `sub`, `mult`, `addi`, `subi`
- Logical: `and`, `or`, `xor`, `sll`
- Control Flow: `jump`, `branch`, `halt`
- I/O: `li`, `show`

**Key Components**:
- 16x32-bit register file (R0 hardwired to 0)
- 32-bit ALU with 7 operations (Table 2)
- Instruction memory (ROM)
- Control unit with state machine
- Zero/sign extension units

### Stage 2: Assembly Programming
**Arithmetic Progression Calculator**:
S = Σ(a + i·r) for i=0 to N-1


## 🛠️ How to Run
1. **Install Digital**:
   ```bash
   sudo apt install openjdk-17-jdk  # For Linux
   git clone https://github.com/hneemann/Digital
   cd Digital
   java -jar Digital.jar
2. Open Main.dig and run

🛠 Technical Specifications
Component	Details
Simulator	Digital 
Word Size	32-bit
Registers	16 (R0 always zero)
ALU Ops	Add, Sub, Mult, AND/OR/XOR, SLL
I/O	Display output via show

