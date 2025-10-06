# 🧠  I²C Address Translator
Recruitment Task – Vicharak Technologies

# 🧾 1. Abstract
The I²C Address Translator is a digital communication bridge designed to resolve address conflicts between multiple I²C slave devices sharing the same physical address.
In a standard I²C system, multiple devices with identical addresses cannot coexist on the same bus.
This project overcomes that limitation by introducing an FPGA-based translation layer that maps unique virtual addresses to a common physical address.

The translator acts as:
      1. I²C Slave to the external master (e.g., microcontroller or processor).
      2. I²C Master to one or more target slave devices.

This allows seamless and transparent read/write communication between the external master and the target slaves through address translation logic.

# 🧩 2. Overview
This project implements an I²C Address Translator using Verilog HDL.
The module operates as an I²C slave on the main bus (connected to a host master) and as an I²C master on the target bus (connected to downstream slave devices).

It dynamically translates the address of the target device while maintaining data integrity, enabling communication between devices with conflicting I²C addresses.

# ⚙️ 3. Functional Description
Main Bus (Slave Side): Receives I²C transactions from the host master.

Target Bus (Master Side): Initiates I²C transactions to the selected slave device.

Translation Logic: Modifies the address field in the I²C packet while maintaining data consistency.

Bidirectional Data Handling: Supports both read and write operations.

Clock & Data Line Control: Maintains synchronization and timing according to I²C protocol standards (Standard / Fast Mode).

# 🧱 4. Design Structure
Top Module: i2c_translator.v

Submodules: FSM-based control, address decoding, and data path logic.

Synthesis Tool: Xilinx Vivado

Target FPGA: (e.g., Artix-7 XC7A35T – specify if applicable)

# 🧩 5. Current Status
✅ Design Implementation
Verilog design code successfully written and synthesized.

RTL elaboration and implementation completed without any errors.

🧪 Testbench Development
Testbench development is in progress.

Partial code written; debugging and refinement ongoing.

Incomplete or error-prone testbench code is not included to maintain clarity and quality.

With additional time, complete verification through simulation will be achieved.

# 🔮 6. Future Scope
Complete the testbench for full functional verification.

Perform waveform analysis for read/write transactions.

Extend design to support multi-slave dynamic translation.

Integrate timing analysis and clock stretching features for robustness and performance.

# 🧰 7. Tools Used
HDL Language: Verilog

IDE/Simulator: Xilinx Vivado





No file chosenNo file chosen
ChatGPT can make mistakes. Check important info. See Cookie Preferences.
