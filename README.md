# 32-bit Carry Look-Ahead Adder (CLA) Implementation

## Project Overview
This repository presents the design and implementation of a **32-bit Carry Look-Ahead Adder (CLA)** optimized for **high-speed operation and energy efficiency** using the **Electric EDA tool**. The design employs a modular approach, utilizing **2 units of 4-bit CLA modules and 4 units of 6-bit CLA modules**, improving computation speed while maintaining power efficiency.

The project systematically evaluates the impact of different process technologies and compares the performance with traditional CLA architectures. The primary objective is to minimize propagation delay and enhance computational efficiency, making it suitable for **digital signal processing, microprocessor arithmetic operations, and high-performance computing applications**.

---

## Features
- Optimized for speed through hierarchical carry modules, reducing propagation delay.
- Energy-efficient design, reducing overall power consumption.
- Scalable modular architecture, combining 4-bit and 6-bit CLA modules.
- Designed for digital systems, including DSP, ALUs, and microprocessors.
- Implemented using the Electric EDA tool with a CMOS-based design.

---

## System Architecture
### Carry Look-Ahead Adder (CLA) Mechanism
The CLA adder improves computation speed by **precomputing carry signals** through **Generate (G) and Propagate (P) signals**, eliminating sequential carry propagation delays.

### Modular Breakdown
- 4-bit CLA modules perform core addition operations.
- 6-bit CLA modules enhance performance and minimize delay.
- Hierarchical carry modules (**carry1, carry2, carry3**) ensure efficient carry computation.

### Implementation Using Electric EDA
- **Logic Gates Used**:
  - XOR Gates – Generate propagate signals.
  - NAND Gates – Optimize carry generation logic.
  - Inverter – Used for signal control.
- **Full Adder with Modified Carry Logic**:
  - Outputs **P (Propagate)** and **G (Generate)** signals instead of the traditional carry-out.

---

## Design Components
### Logic Gates
- **Inverter Gate** – PMOS/NMOS-based CMOS inverter.
- **NAND Gate** – Fundamental logic operation for CLA implementation.
- **XOR Gate** – Used for generating propagate signals.

### Full Adder Circuit
- Computes:
  - S – Sum of inputs.
  - G – Carry generation.
  - P – Carry propagation.

### Carry Generation Logic
- Carry1, Carry2, and Carry3 modules precompute carry signals to improve speed.
- Next_P4 and Next_P6 enhance parallel processing for high-speed operation.

---

## Performance Analysis
### Speed Evaluation
- Rise Time (tr) = 4.257 ns
- Fall Time (tf) = 4.999 ns
- Average Propagation Delay = 7.272 ns

### Power Dissipation
- Critical Path Power Consumption = 1.89286 × 10⁻⁵ µW
- Verified through circuit simulation in Electric EDA.

---

## Project Simulation and Verification
- **Schematic Design**:
  - Logic gates, full adder, and hierarchical carry logic modules.
- **Layout Implementation**:
  - CMOS-based design with transistor-level optimization.
- **Simulation Results**:
  - Timing analysis and power efficiency validation.

---

## Installation and Usage
### Prerequisites
- Install **Electric VLSI Design System** for schematic and layout visualization.
- Load the project files into **Electric EDA**.

### Running the Project
1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/CLA-Adder.git
   cd CLA-Adder
