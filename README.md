# Traffic Light Controller with Pedestrian Crossing

## 📌 Project Overview

This project implements a Traffic Light Controller with Pedestrian Crossing using Verilog HDL and a Finite State Machine (FSM). The controller manages traffic signals for a highway and a side road while supporting a pedestrian crossing request.

The design is simulated using Xilinx Vivado to verify the operation of traffic signals and pedestrian crossing functionality.

## 🎯 Objectives

- Design an FSM-based traffic light controller using Verilog HDL.
- Control highway and side road traffic signals.
- Support pedestrian crossing based on a pedestrian request.
- Verify the functionality using simulation.
- Analyze the RTL schematic and power analysis results.

## ⚙️ Technologies Used

- Hardware Description Language: Verilog HDL
- Design and Simulation Tool: Xilinx Vivado
- Design Methodology: Finite State Machine (FSM)
- Verification: Verilog Testbench

## 🔄 FSM States

The controller consists of four states:

State| Description
"HW_GREEN"| Highway green, side road red
"HW_YELLOW"| Highway yellow, side road red
"SR_GREEN"| Highway red, side road green
"PED_STATE"| Both traffic signals red and pedestrian walk enabled

## State Transitions

- The controller starts in "HW_GREEN" after reset.
- After the timer reaches its specified value, the controller moves to "HW_YELLOW".
- After the yellow phase, it checks the pedestrian request.
- If a pedestrian request is active, the controller enters "PED_STATE"; otherwise, it enters "SR_GREEN".
- After the side-road green phase, the controller returns to "HW_GREEN".
- After the pedestrian crossing phase, the controller proceeds to "SR_GREEN".

## 💡 Features

- FSM-based traffic signal control.
- Independent highway and side road signal outputs.
- Timer-based state transitions.
- Pedestrian request input.
- Dedicated pedestrian walk output.
- Asynchronous reset support.
- Testbench-based functional verification.

## 🧪 Simulation and Verification

The design includes a Verilog testbench to generate the clock, apply reset, and simulate pedestrian requests.

The following outputs are used to verify the controller's operation:

- Simulation Waveform: Shows traffic signal and pedestrian walk output behavior over time.
- RTL Schematic: Illustrates the RTL design structure.
- Console Output: Displays monitored signal values during simulation.
- Power Analysis: Shows power analysis results obtained in Vivado.

## 📸 Project Results

### 1. Vivado Simulation Waveform

"Vivado Simulation Waveform" (simulation_waveform.png)

### 2. RTL Schematic

"RTL Schematic" (rtl_schematic.png)

### 3. Console Output

"Console Output" (console_output.png)

### 4. Power Analysis

"Power Analysis" (power_analysis.png)

## 📁 Project Structure

Traffic-Light-Controller/
├── traffic_light_controller.v
├── tb_traffic_light_controller.v
│   ├── simulation_waveform.png
│   ├── rtl_schematic.png
│   ├── console_output.png
│   └── power_analysis.png
└── README.md

## ▶️ How to Run the Project

1. Open Xilinx Vivado.
2. Create or open a Verilog HDL project.
3. Add "traffic_light_controller.v" as the design source.
4. Add "tb_traffic_light_controller.v" as the simulation source.
5. Set "tb_traffic_light_controller" as the simulation top module.
6. Run behavioral simulation.
7. Observe the highway, side road, and pedestrian walk outputs in the waveform.
8. Generate the RTL schematic and perform power analysis if required.

## ✅ Conclusion

The Traffic Light Controller with Pedestrian Crossing was designed using Verilog HDL and an FSM-based approach. The simulation results demonstrate the operation of highway and side road traffic signals and the pedestrian crossing mechanism.

This project provides practical experience in digital system design, FSM implementation, Verilog coding, simulation, and RTL analysis.

👨‍💻 Author
Akshaya Reddy
B.Tech ECE Student
