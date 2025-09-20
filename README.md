# _RISC-V-SoC-Tapeout-Program_VSD
This repository documents my week-by-week progress with tasks inside each week for_RISC-V-SoC-Tapeout-Program_VSD
# _RISC-V-SoC-Tapeout-Program_VSD

## Overview
Documenting the full RISC-V SoC tapeout program: tool setup, RTL-to-GDS flow, and snapshots.

## Table of Contents
1. [System Requirements](#system-requirements)
2. [Installed Tools](#installed-tools)
3. [Installation Scripts](#installation-scripts)
4. [Snapshots](#snapshots)
5. [OpenLane Setup](#openlane-setup)
6. [References](#references)

## System Requirements
- Ubuntu 20.04+
- 6GB RAM, 4 vCPU, 50GB HDD
- VirtualBox or native VM

## Installed Tools
- Yosys, Iverilog, GTKWave, ngspice, Magic, OpenLane, Docker

## Installation Scripts
Scripts are in the `commands/` folder. Run them sequentially:

```bash
cd commands
chmod +x *.sh
./00_yosys.sh
