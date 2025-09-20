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


---

## System Requirements
- Ubuntu 20.04+ (on VirtualBox or native VM)
- RAM: 6GB, CPU: 4vCPU, HDD: 50GB
- Windows users can use Ubuntu VM or WSL

---

## Installed Tools
- 
-  1. Yosys – RTL Synthesis Tool
      
Purpose: Converts RTL code into gate-level representations.
✅ Yosys Installation

\
## Yosys

```Yosys
$ sudo apt-get update
$ git clone https://github.com/YosysHQ/yosys.git
$ cd yosys
$ sudo apt install make (If make is not installed please install it)
$ sudo apt-get install build-essential clang bison flex \
 libreadline-dev gawk tcl-dev libffi-dev git \
 graphviz xdot pkg-config python3 libboost-system-dev \
 libboost-python-dev libboost-filesystem-dev zlib1g-dev
$ make config-gcc
$ make
$ sudo make install
 ```
📷 Installation Verification
<img width="940" height="711" alt="image" src="https://github.com/user-attachments/assets/5ce0f9ee-4d4a-4e2c-80a1-833026bd2ff6" />
                          ✅ Yosys Successfully Installed

 📟 2. Iverilog – Verilog Simulator
 
Purpose: Compiles and simulates Verilog designs for functional verification.

Iverilog Installation
$sudo apt-get update
$sudo apt-get install iverilog 

📷 Installation Verification
<img width="940" height="703" alt="image" src="https://github.com/user-attachments/assets/0927849d-bbee-4e99-ade4-0c48a6e91add" />
                        ✅ Iverilog Successfully Installed
 
GTKWave Installation

$sudo apt-get update
$sudo apt install gtkwave

📷 Installation Verification
 <img width="940" height="356" alt="image" src="https://github.com/user-attachments/assets/616c4a6f-3e9a-4482-9aa3-1eff0bdb3baf" />
       ✅ GTKWave Successfully Installed
       
4. Ngspice – Circuit Simulator

Purpose: Performs analog and mixed-signal circuit simulation.
Ngspice Installation
$ sudo apt update
$ sudo apt install ngspice
📷 Installation Verification
<img width="940" height="686" alt="image" src="https://github.com/user-attachments/assets/ef835d3f-9f5a-4fa2-8245-ffbf8d68c24a" />
                   ✅ Ngspice Successfully Installed
 5. Magic VLSI Installation
Purpose:Magic VLSI is an open-source VLSI layout tool widely used for IC design, DRC, and visualization.

Magic Installation
$ sudo apt-get install m4
$ sudo apt-get install tcsh
$ sudo apt-get install csh
$ sudo apt-get install libx11-dev
$ sudo apt-get install tcl-dev tk-dev
$ sudo apt-get install libcairo2-dev
$ sudo apt-get install mesa-common-dev libglu1-mesa-dev
$ sudo apt-get install libncurses-dev
git clone https://github.com/RTimothyEdwards/magic
cd magic
./configure
make
make install 
📷 Installation Verification  
<img width="940" height="744" alt="image" src="https://github.com/user-attachments/assets/8db26ebb-a8f4-40fa-b176-0c98ea2f9d4a" />
        ✅ Magic VLSI Successfully Installed


- **OpenLane** (ASIC Flow)  
- **Docker**  

---


