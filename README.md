# _RISC-V-SoC-Tapeout-Program_VSD
This repository documents my week-by-week progress with tasks inside each week for_RISC-V-SoC-Tapeout-Program_VSD

WEEK0: SETUP AND TOOLS

## Overview
This repository documents the RISC-V SoC Tapeout Program (VSD) from **RTL to GDSII** using open-source tools. It includes installation scripts, snapshots, and notes for all steps.

---

## Table of Contents
1. [System Requirements](#system-requirements)
2. [Installed Tools](#installed-tools)
3. [Installation Scripts](#installation-scripts)
4. [Snapshots](#snapshots)
5. [OpenLane Setup](#openlane-setup)
6. [References](#references)

---

## System Requirements
- Ubuntu 20.04+ (on VirtualBox or native VM)
- RAM: 6GB, CPU: 4vCPU, HDD: 50GB
- Windows users can use Ubuntu VM or WSL

---

## Installed Tools
- **Yosys** (RTL Synthesis)  
- **Iverilog** (Simulation)  
- **GTKWAVE** (Waveform Viewer)  
- **ngspice** (SPICE Simulation)  
- **Magic** (VLSI Layout)  
- **OpenLane** (ASIC Flow)  
- **Docker**  

---

## Installation Scripts
Scripts are in the `commands/` folder. Run sequentially:

```bash
cd commands
chmod +x *.sh
./00_yosys.sh
./01_iverilog.sh
./02_gtkwave.sh
./03_ngspice.sh
./04_magic.sh
./05_openlane.sh
