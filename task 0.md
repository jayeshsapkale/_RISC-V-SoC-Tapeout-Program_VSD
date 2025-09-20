WEEK0: SETUP AND TOOLS
Overview

This repository provides a step-by-step guide for setting up the environment, installing necessary tools, and verifying installations for the RISC-V SoC Tapeout Program. It uses open-source tools and includes scripts, snapshots, and notes for each step.
## Table of Contents
1. [System Requirements](#system-requirements)  
2. [Installed Tools](#installed-tools)  
3. [Installation Scripts](#installation-scripts)  


---

## System Requirements
- **OS:** Ubuntu 20.04+ (VM or native)  
- **RAM:** 6GB  
- **CPU:** 4 vCPU  
- **HDD:** 50GB  
- **Windows Users:** Use Ubuntu VM or WSL  

## Installed Tools

| Tool          | Purpose                                              | Installation Status |
|---------------|------------------------------------------------------|------------------|
| Yosys         | RTL Synthesis Tool                                   | Installed ✅      |
| Iverilog      | Verilog Simulator                                    | Installed ✅      |
| GTKWave       | Waveform Viewer                                     | Installed ✅      |
| Ngspice       | Analog & Mixed-Signal Simulator                     | Installed ✅      |
| Magic VLSI    | Layout Tool for IC design, DRC, Visualization       | Installed ✅      |
| OpenLane      | Automated ASIC Flow (RTL → GDSII)                    | Installed ✅      |
| Dependencies  | Git, Docker, Python3, Make, pip, venv              | Checked ✅        |

---
## Yosys – RTL Synthesis Tool

Purpose: Converts RTL code into gate-level representations.

Installation:
```
sudo apt-get update
git clone https://github.com/YosysHQ/yosys.git
cd yosys
sudo apt install make build-essential clang bison flex \
libreadline-dev gawk tcl-dev libffi-dev git \
graphviz xdot pkg-config python3 libboost-system-dev \
libboost-python-dev libboost-filesystem-dev zlib1g-dev
make config-gcc
make
sudo make install

```
Verification:
<img width="940" height="711" alt="image" src="https://github.com/user-attachments/assets/f9b75781-c3d4-4ed2-9d02-10b5dc1bc047" />

✅ Yosys successfully installed

## 2. IVerilog  – Verilog Simulator

Purpose: Compiles and simulates Verilog designs for functional verification.

Installation:
```
sudo apt-get update
sudo apt-get install iverilog
```

Verification:
<img width="940" height="703" alt="image" src="https://github.com/user-attachments/assets/1c4f3375-43d3-4009-92b1-022a10e2bdd0" />

✅ Iverilog successfully installed

## 3. GTKWave – Waveform Viewer

Purpose: Visualizes simulation waveforms.

Installation:
```
sudo apt-get update
sudo apt install gtkwave

```
Verification:
<img width="940" height="356" alt="image" src="https://github.com/user-attachments/assets/0c896396-3f5c-4fc1-8436-3e84464d25da" />

✅ GTKWave successfully installed

## 4. Ngspice – Circuit Simulator

Purpose: Performs analog and mixed-signal circuit simulations.

Installation:
```
sudo apt update
sudo apt install ngspice
```

Verification:

<img width="940" height="686" alt="image" src="https://github.com/user-attachments/assets/cdbc5630-abd6-45cd-9d0c-5ef6519f00ce" />

✅ Ngspice successfully installed

## 5. Magic VLSI – Layout Tool

Purpose: Open-source VLSI layout tool for IC design, DRC, and visualization.

Installation:
```
sudo apt-get install m4 tcsh csh libx11-dev tcl-dev tk-dev \
libcairo2-dev mesa-common-dev libglu1-mesa-dev libncurses-dev
git clone https://github.com/RTimothyEdwards/magic
cd magic
./configure
make
sudo make install
```

Verification:

<img width="940" height="744" alt="image" src="https://github.com/user-attachments/assets/cd485110-2de2-405c-a255-79add7d2ad36" />

✅ Magic VLSI successfully installed

## 6. OpenLane – ASIC Flow

Purpose: Fully automated open-source digital ASIC design flow from RTL → GDSII.

Installation:
```
sudo apt-get update
sudo apt-get upgrade
sudo apt install -y build-essential python3 python3-venv python3-pip make git
sudo apt install apt-transport-https ca-certificates curl software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt update
sudo apt install docker-ce docker-ce-cli containerd.io
sudo docker run hello-world
sudo groupadd docker
sudo usermod -aG docker $USER
sudo reboot
# After reboot
docker run hello-world

```
Install OpenLane tools and PDKs:
```
cd $HOME
git clone https://github.com/The-OpenROAD-Project/OpenLane
cd OpenLane
make
make test
```

Verification:
<img width="940" height="516" alt="image" src="https://github.com/user-attachments/assets/361c1b81-0d4d-4e46-a2c2-b3814e1e231e" />

✅ OpenLane successfully installed

7. Check Dependencies
 ```
git --version
docker --version
python3 --version
python3 -m pip --version
make --version
python3 -m venv -h
```

Verification:
<img width="940" height="774" alt="image" src="https://github.com/user-attachments/assets/f7425bda-8545-4dad-ae35-ffb1e71eb978" />


✅ All dependencies successfully checked
