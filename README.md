# 🔒 Phase Locked Loop (PLL) Design using 45nm CMOS Technology

> VLSI System Design Project | Cadence Virtuoso | 45nm CMOS Technology

![License](https://img.shields.io/badge/Technology-45nm%20CMOS-blue)
![EDA](https://img.shields.io/badge/EDA-Cadence%20Virtuoso-red)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

## 📖 Project Overview

This project presents the design and simulation of a **Phase Locked Loop (PLL)** using **45nm CMOS technology** in Cadence Virtuoso.

A Phase Locked Loop (PLL) is a closed-loop feedback system that synchronizes the phase and frequency of an output signal with a reference input signal. PLLs are widely used in:

- Clock Generation
- Clock Synchronization
- Frequency Synthesis
- Data Recovery
- Wireless Communication Systems
- High-Speed Digital Systems

The project implements each PLL building block individually and integrates them into a complete PLL architecture.

---

## 🎯 Objectives

- Design a complete PLL using CMOS technology.
- Implement all major PLL building blocks.
- Simulate the complete circuit.
- Verify frequency locking behavior.
- Analyze PLL performance.

---

# 🏗 PLL Architecture

The designed PLL consists of the following blocks:

```
Reference Clock
       │
       ▼
+------------------+
| Phase Frequency  |
| Detector (PFD)   |
+------------------+
       │
       ▼
+------------------+
| Charge Pump      |
+------------------+
       │
       ▼
+------------------+
| Loop Filter      |
+------------------+
       │
       ▼
+------------------+
| Voltage          |
| Controlled Osc.  |
| (VCO)            |
+------------------+
       │
       ▼
 Frequency Divider
       │
       └──────────────► Feedback to PFD
```

---

# ⚙ Components

## 1️⃣ Phase Frequency Detector (PFD)

The PFD compares:

- Reference Clock (Vref)
- Feedback Clock (Vdiv)

Outputs:

- UP
- DOWN

Functions:

- Detects phase difference
- Detects frequency difference
- Controls Charge Pump

---

## 2️⃣ Charge Pump

The Charge Pump converts UP/DOWN signals into current pulses.

Functions:

- Charges Loop Filter capacitor
- Discharges Loop Filter capacitor
- Generates control voltage (Vc)

---

## 3️⃣ Voltage Controlled Oscillator (VCO)

The VCO converts the control voltage into oscillation frequency.

Characteristics:

- Higher Vc → Higher Frequency
- Lower Vc → Lower Frequency

Output Frequency:

Approximately

3.6 GHz – 4.9 GHz

---

## 4️⃣ TSPC Flip-Flop

True Single Phase Clock Flip-Flop used inside divider.

Advantages:

- High Speed
- Low Power
- Single Clock
- Suitable for PLL applications

---

## 5️⃣ Frequency Divider (÷48)

Divider reduces VCO frequency before feedback.

Purpose:

- Maintains PLL Lock
- Generates feedback clock

Division Ratio:

```
÷48
```

---

# 🛠 Design Flow

```
Specification

↓

Circuit Design

↓

Schematic Design

↓

Simulation

↓

Waveform Analysis

↓

PLL Lock Verification

```

---

# 💻 Software Used

- Cadence Virtuoso
- 45nm CMOS Technology
- Analog Design Environment (ADE)
- Spectre Simulator

---

# 📊 Simulation Results

Simulation verified:

✔ Phase Lock

✔ Stable Frequency

✔ Stable Control Voltage

✔ Frequency Multiplication

---

# 📈 Performance

| Parameter | Value |
|-----------|--------|
| Technology | 45nm CMOS |
| Supply Voltage | 1V |
| Frequency Range | 3.6 GHz – 4.9 GHz |
| Lock Time | 120–150 µs |
| Settling Time | 35–45 µs |
| Divider | ÷48 |

---

# 📂 Repository Structure

```
PLL-VLSI-Design/

│

├── README.md

├── Report/
│      PLL_Report.pdf

├── Images/
│      BlockDiagram.png
│      PFD.png
│      ChargePump.png
│      VCO.png
│      Divider.png
│      FinalCircuit.png
│      OutputWaveform.png

├── Schematics/
│      PFD
│      ChargePump
│      VCO
│      Divider

├── Simulation/
│      Waveforms
│      Results

└── LICENSE
```

---

# 📷 Project Screenshots

- Phase Frequency Detector
- Charge Pump
- Voltage Controlled Oscillator
- Divider Circuit
- Final PLL Circuit
- Output Waveforms

---

# 🚀 Applications

- Clock Recovery
- Frequency Synthesizers
- Microprocessors
- Wireless Communication
- RF Systems
- Digital Signal Processing
- High-Speed Serial Interfaces

---

# 📚 Conclusion

The PLL was successfully designed and simulated using **45nm CMOS technology** with a **1V supply voltage**. The VCO achieved an operating range of **approximately 3.6–4.9 GHz**. The PLL demonstrated stable phase and frequency lock, with a lock time of **120–150 µs** and a settling time of **35–45 µs**, confirming correct operation of the integrated system.

---

# 👨‍💻 Author

**Tharun Ravuru**

B.Tech – Electronics and Communication Engineering

VIT University, Vellore

GitHub: https://github.com/THARUN2939

LinkedIn: https://linkedin.com/in/yourprofile

---

## ⭐ If you found this project useful, consider giving it a Star!
