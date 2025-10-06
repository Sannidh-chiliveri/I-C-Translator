# 🧠 FPGA-Based Dual-Level I²C Address Translator  
**Author:** Chiliveri Sannidh  
**Task Assigned By:** Vicharak  
**Date:** October 2025  

---

## 🔍 Project Highlights

| Feature | Description |
|----------|-------------|
| **Project Type** | RTL Design & FPGA Implementation |
| **Protocol** | I²C Dual-Level Address Translation |
| **Language Used** | Verilog HDL |
| **Tool Used** | Xilinx Vivado 2023.1 |
| **Status** | RTL Implementation Verified ✅ |
| **Testbench** | Under Development 🔧 |
| **Submitted To** | Vicharak |

---

## 🧾 1. Abstract

The **I²C Address Translator** is a digital communication bridge designed to resolve address conflicts between multiple I²C slave devices sharing the same physical address.  
In a standard I²C system, multiple devices with identical addresses cannot coexist on the same bus.  
This project overcomes that limitation by introducing an **FPGA-based translation layer** that maps unique *virtual addresses* to a *common physical address*.

The translator acts as:
- **I²C Slave** to the external master (e.g., microcontroller or processor).  
- **I²C Master** to two target slave devices.

This allows seamless and transparent read/write communication between the external master and the target slaves through address translation logic.

---

## 🧩 2. Introduction

The **I²C (Inter-Integrated Circuit)** protocol is a widely used two-wire serial communication standard that enables multiple devices to share a common bus.  
However, when two or more devices have identical slave addresses, only one can communicate at a time — a serious limitation in multi-sensor or modular systems.

This project implements a **Dual-Level I²C Address Translator** using Verilog HDL on an FPGA platform to eliminate address conflicts.  
It introduces a layer that translates **virtual addresses (0x49, 0x4A)** into a **common physical address (0x48)**, allowing two identical devices to function simultaneously under a single master.

### 🔧 Key Applications
- Multi-sensor systems using identical I²C devices.  
- Industrial control setups with repeated device types.  
- Redundant communication systems requiring mirrored sensors.

---

## ⚙️ 3. System Overview

The translator monitors transactions from the external master, decodes the 7-bit address, and determines which target device to communicate with.  

| Virtual Address | Physical Address | Target |
|-----------------|------------------|--------|
| 0x49 | 0x48 | Target 1 |
| 0x4A | 0x48 | Target 2 |

This address mapping ensures that each device appears unique to the master, even if they share the same internal hardware address.

---

## 🧱 4. System Architecture

