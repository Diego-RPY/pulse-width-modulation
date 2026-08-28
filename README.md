# Project Name: FPGA PWM motor controller
Designed a custom built PWM along with a state machine with logic gates. The PWM operated at a frequency of x Hz and was built using VERILOG language in Intel Quartus.

## Master Digital Circuit
<img width="1500" height="607" alt="image" src="https://github.com/user-attachments/assets/f7875efc-91ea-47b4-9cc7-d22e9a777e84" />

---

## System Specifications

### Modules/Hardware
Note: This project is meant to show the custom design of a PWM and a state machine, this means that the motor and power supply listed below are not needed in order to demonstrate the primary function of the project.
* **FPGA Board:** 10M50DAF484C7G
* **Motor Drivers:** L298N
* **Power:** Jesverty SPS-3010 
* **Motor:** Geartisan 12V (any model)
* **Main Circuit:** State Machine, 7447 BCD-7 Segment Display, Frequency Divider
* **PWM:** FPGA-based Pulse Width Modulation implemented using a counter and comparator to control the output duty cycle.
### Software & Dependencies
* **Development Environment:** Intel Quartus Prime
* **HDL:** Verilog

---

## Usage & Bringup

### Prerequisites
* Intel Quartus Prime
* Complete Setup: For more information for the complete software set up of the project refer to the file "SETUP.md"
* Open the quartus-project folder
* USB-Blaster connection
### 1. Hardware Checklist
1. Connect the USB cable to the onboard USB-Blaster port. The D1 (LOAD) status LED indicates USB-Blaster activity.
2. With the factory design loaded, the user LEDs display a binary counting pattern.
3. Connect the positive and negative terminals of the motor to the positive and negative leads of the battery and ensure the motor works.
### 2. Execution
1. Open the Project
2. The project is configured for the MAX 10 FPGA: 10M50DAF484C7G
3. The required FPGA pins are already assigned in the Quartus project.
Open: Assignments → Pin Planner
to review the assignments.
4. Compile
Run:
Processing → Start Compilation
5. Program the FPGA: Connect the DE10-Lite through the USB-Blaster port.
Open: Tools → Programmer
Select the detected USB-Blaster, select the generated `.sof` file,
and click Start.
