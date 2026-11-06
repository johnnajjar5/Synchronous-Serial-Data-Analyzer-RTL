# Synchronous Serial Data Analyzer | VHDL & RTL Design ⚙️

## 📚 Project Overview

This project implements a synchronous serial data analysis system developed as a final project for the **Programmable Logic Devices (31551)** course at Braude Academic College of Engineering.

The system receives blocks of serial data, converts incoming data into parallel format, and performs statistical analysis on each block. For every block of 64 data values, the system calculates the minimum, maximum, average, and median values, while also counting transmission errors using even-parity checking.

The design is implemented using **VHDL** and follows a modular, hierarchical RTL architecture. It is intended for implementation and verification on an Intel/Altera Cyclone V FPGA development board.

## 🎯 Key Features

- **Synchronous Serial Communication:** Receives data through a serial input interface.
- **Serial-to-Parallel Conversion:** Converts incoming 9-bit serial frames into 8-bit data words.
- **Parity Error Detection:** Implements even-parity checking to identify transmission errors.
- **Statistical Computation:** Calculates five results for every 64-value data block:
  - Maximum value
  - Minimum value
  - Average value
  - Median value
  - Total number of parity errors
- **Median Calculation:** Computes the median as the average of the two middle values after ordering the 64 values.
- **Finite State Machine (FSM):** Controls the system operation through idle, receive, calculate, and display phases.
- **FPGA-Based Result Display:** Displays calculated results using four 7-segment displays and LED indicators.

## 🏗️ System Architecture

The system consists of several interconnected RTL modules:

1. **Serial Data Generator:** Generates synchronous serial data for system testing.
2. **Serial-to-Parallel Converter:** Receives serial data and reconstructs parallel 8-bit words.
3. **Main Controller:** Controls data reception, calculation sequencing, and result presentation.
4. **Statistical Processing:** Performs minimum, maximum, average, and median calculations, alongside parity error counting.
5. **Display Interface:** Converts numerical results into a format suitable for 7-segment displays.
6. **Top-Level Integration:** Connects the system modules and manages the external FPGA interfaces.

## ⚙️ Data Format & Specifications

| Parameter | Specification |
|---|---|
| Design Language | VHDL |
| FPGA Platform | Intel/Altera Cyclone V |
| System Clock | 50 MHz |
| Reset | Active-Low at top level |
| Data Block Size | 64 values |
| Data Width | 8 bits |
| Serial Frame Width | 9 bits |
| Parity Scheme | Even Parity |
| Data Range | 0–255 |
| Result Display | Four 7-segment displays |

## 🔄 System Operation

The system operates through four main phases:

1. **Idle:** Waits for the user to initiate a new data acquisition process.
2. **Receive:** Requests and receives a block of 64 serial data values.
3. **Calculate:** Computes the statistical results and counts parity errors.
4. **Display:** Presents the calculated results, allowing the user to cycle between maximum, minimum, average, median, and error count.

A new acquisition cycle can be initiated after returning the system to the idle state.

## 🧩 RTL Design & Verification

The project follows a modular RTL development methodology, with individual functional blocks and top-level integration.

- VHDL implementation of the system modules.
- Dedicated testbenches for the required individual modules.
- Functional simulation using ModelSim.
- Full-chip simulation to verify system-level behavior.
- Quartus compilation and FPGA resource utilization analysis.
- Timing analysis and RTL Netlist Viewer inspection.

## 🛠️ Technologies & Tools

- **VHDL** – RTL design and hardware description.
- **Intel Quartus Prime** – FPGA compilation and design analysis.
- **ModelSim** – Functional simulation and verification.
- **Intel/Altera Cyclone V** – FPGA development platform.
- **RTL Design** – Modular and hierarchical digital system architecture.
- **Finite State Machines (FSM)** – Sequential control logic.
- **Digital Signal Processing Concepts** – Statistical data analysis and parity checking.

## 📸 Project Results

This section will include:

- RTL block diagrams.
- Serial-to-parallel converter simulation waveforms.
- Parity error detection simulation.
- Statistical calculation results.
- Main controller state transitions.
- Full-chip ModelSim simulation.
- Quartus RTL Netlist Viewer.
- FPGA resource utilization and timing reports.

## 🎓 Project Objectives

- Develop a complete digital system using VHDL.
- Apply RTL design principles and hierarchical hardware architecture.
- Implement synchronous serial communication.
- Design and verify sequential and combinational logic.
- Perform statistical calculations using digital hardware.
- Develop testbenches and verify functionality through simulation.
- Gain practical experience with FPGA design and verification workflows.

## 👨‍💻 Author

**John Najjar**  

**Omar Majdoub**

**Oday Haj**

Electrical & Electronics Engineering Graduate  
Braude Academic College of Engineering
