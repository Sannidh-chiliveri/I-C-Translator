# I-C-Translator
This project implements an I²C Address Translator in Verilog HDL. It acts as a slave on the main bus and a master on the target bus, enabling address translation with bidirectional read/write support. Designed using FSMs, verified on FPGA with Vivado for standard and fast I²C modes.

# 🧩 I²C Address Translator
Recruitment Task – Vicharak Technologies

# 📘 Overview
This project implements an I²C Address Translator using Verilog HDL.
The module acts as an I²C slave on the main bus (connected to a host master) and as an I²C master on the target bus (connected to one or more downstream slave devices).
It translates the address of the target device dynamically while keeping the data transmission intact, allowing communication between devices that have conflicting I²C addresses.

# ⚙️ Functional Description
Main Bus (Slave Side): Receives I²C transactions from the host master.

Target Bus (Master Side): Initiates I²C transactions to the selected slave device.

Translation Logic: Modifies the address field in the I²C packet while maintaining data integrity.

Bidirectional Data Handling: Supports both read and write operations.

Clock and Data Line Control: Ensures proper synchronization and timing according to I²C protocol (Standard/ Fast Mode).

# 🧱 Design Structure
Top Module: i2c_translator.v

Submodules: FSM-based control, address decoding, and data path logic.

Synthesis Tool: Xilinx Vivado

Target FPGA: (You can specify the board here, e.g., Artix-7 XC7A35T if applicable)

# 🧩 Current Status
✅ Design Implementation:

The Verilog design code has been successfully written and synthesized.

RTL implementation and elaboration were completed without any errors.

# 🧪 Testbench Development:

The testbench for functional verification is under progress.

Partial code has been developed, and debugging is ongoing to remove logical and syntax errors.

The final version will include proper I²C transaction simulations verifying address translation and data integrity.

Incomplete or error-prone code is not included in this submission to maintain report clarity and quality.

With additional time, the testbench will be refined to achieve complete simulation verification.

# 🔮 Future Scope
Complete the testbench for full functional verification.

Perform waveform analysis for read/write transactions.

Extend design to support multi-slave dynamic translation.

Integrate timing analysis and clock stretching features for robustness.

# 🧰 Tools Used
HDL Language: Verilog

IDE/Simulator: Xilinx Vivado

Version Control: Git & GitHub

# 👤 Author
Sannidh Chiliveri

RTL Design Enthusiast | FPGA Developer

Contact: (You may add your email or LinkedIn link)

# 🔒 Access
This repository is private and shared exclusively with Vicharak Technologies as part of the recruitment evaluation.
Collaborator added: recruit-vicharak

