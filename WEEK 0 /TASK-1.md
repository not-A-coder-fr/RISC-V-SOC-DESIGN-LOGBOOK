## WEEK 0 (TASK-1)

---

## 📌 Overview

An introductory lecture, delivered by **Kunal Ghosh**, introduced the **fundamental concepts of chip modeling and SoC design flow** — setting the stage for our journey from RTL to GDSII.

We learned how :
- Model chips using **C language (C model)**
- Understand the **SoC design flow**
- Integrate processors and peripherals
- See real-world applications of custom chips

---

## 🎯 Key Concepts from the Lecture

### 🔹 1. Chip Modeling Using C (C Model)

> "The testbench is in C language" — Kunal Ghosh

Instead of writing complex Verilog testbenches early, we use **C models** to simulate chip behavior at a high level.

```c
// Example: Simple C model for O0 = O1
int O0 = O1; // Functional equivalence
```

✅ **Why?**  
- Faster simulation  
- Easier to verify functionality  
- Helps define specs before RTL

---

### 🔹 2. SoC Design Flow: From Specs to Silicon

The full flow is broken into stages:

| Stage | Description |
|------|-------------|
| **O1: C Model** | High-level functional verification using C code |
| **O2: RTL Design** | Writing Verilog/VHDL for processor and peripherals |
| **O3: SoC Integration** | Combining processor, macros, analog IPs |
| **O4: RTL2GDS** | Floorplanning, placement, routing → GDSII |

> 💡 **Key Insight**: `O1 = O2 = O3 = O4` — All outputs must be functionally equivalent!

---

### 🔹 3. Components Explained:
- **Processor**: Can be soft logic (RTL) or hard macro (P1)
- **Peripherals**: UART, GPIO, SPI, etc.
- **Macros**: Hardened blocks like memory
- **Analog IPs**: Clock generators, ADCs, etc.

---

### 🔹 4. Real-World Applications

Chips designed using this flow power everyday devices:

| Application | Frequency Range | Use Case |
|-----------|------------------|--------|
| iWatch | 100MHz – 130MHz | Wearable tech |
| Arduino Boards | ~16MHz | DIY electronics |
| TV Panels | ~50–100MHz | Display control |
| AC Applications | ~50Hz | Motor control |



---

## 🙏 Acknowledgments

> ### 🌟 Special Thanks to **Kunal Ghosh** & Team VSD

Thank you, **Kunal Ghosh**, for an **exceptional and insightful lecture** that demystified the entire SoC design process.

Your ability to explain complex concepts with clarity and passion has inspired thousands of engineers across India. You’re not just teaching VLSI — you’re **building a semiconductor revolution**.

> *"A single idea can change the future of a nation."*  
> — Kunal Ghosh

---

