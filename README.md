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
```c
S = Σ(a + i·r) for i=0 to N-1
```


## 🚀 Getting Started

### 1. Install Digital Simulator
```bash
# For Debian/Ubuntu Linux:
sudo apt update && sudo apt install openjdk-17-jdk git
git clone https://github.com/hneemann/Digital
cd Digital
java -jar Digital.jar
```
    Note: For Windows/Mac, download the prebuilt JAR from Digital's Releases
### 2. Clone this repository
### 3. Open Main.dig and run


<br>

# Instruction Set Architecture (ISA)

## 🖥️ Processor Instruction Table

| Opcode | Mnemonic | Semantics                  | Description                          |
|--------|----------|----------------------------|--------------------------------------|
| **0**  | `nop`    | `–`                        | No operation                         |
| **1**  | `li`     | `R(c) ← imm`               | Load immediate into register         |
| **2**  | `add`    | `R(c) ← R(a) + R(b)`       | Add registers                        |
| **3**  | `sub`    | `R(c) ← R(a) - R(b)`       | Subtract registers                   |
| **4**  | `mult`   | `R(c) ← R(a) * R(b)`       | Multiply registers                   |
| **5**  | `and`    | `R(c) ← R(a) AND R(b)`     | Bitwise AND                          |
| **6**  | `or`     | `R(c) ← R(a) OR R(b)`      | Bitwise OR                           |
| **7**  | `xor`    | `R(c) ← R(a) XOR R(b)`     | Bitwise XOR                          |
| **8**  | `sll`    | `R(c) ← R(a) « R(b)`       | Shift left logical                   |
| **9**  | `addi`   | `R(c) ← R(a) + extZero(imm)` | Add immediate (zero-extended)       |
| **10** | `subi`   | `R(c) ← R(a) - extZero(imm)` | Subtract immediate (zero-extended)  |
| **11** | `jump`   | `IP ← E`<br>`E ← IP + extSign(imm)` | Unconditional jump                |
| **12** | `branch` | `if (R(a) == R(b)) {IP ← E}`<br>`E ← IP + extSign(imm)` | Conditional branch |
| **13** | `show`   | `Display R(a)`             | Register output display              |
| **14** | `halt`   | `IP ← IP + 0`              | Terminate execution                  |


