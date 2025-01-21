# Automatic-Door-Lock-Sysem

Introduction

The Automatic Door Controller project demonstrates a simple finite state machine (FSM) implementation in Verilog. It models the behavior of an automatic door system that opens and closes based on sensor input and user commands.

Features

State-Based Control: The door transitions through states like IDLE, OPENING, OPEN, and CLOSING based on input signals.

Reset Functionality: A reset input initializes the system to the IDLE state.

Input Handling: Inputs include a sensor to detect presence and a close button to command the door to close.

Output: A signal (door_open) indicates the door's current status (open or closed).

Design Overview

States

IDLE: The door remains closed until the sensor detects presence.
OPENING: The door transitions to an open state.
OPEN: The door remains open until the close button is pressed.
CLOSING: The door closes and transitions back to IDLE.

Inputs

clk: System clock signal.
rst: Reset signal to initialize the system.
sensor: Detects if someone is near the door.
close_button: Command to close the door manually.

Outputs

door_open: Indicates whether the door is open (1) or closed (0).

Simulation and Testing

Clock Signal: A clock signal with a 10 ns period drives the design.
Reset Behavior: The system initializes to the IDLE state on reset.

Test Scenarios:

Sensor activation leads to door opening.
The door remains open until the close button is pressed.
The close button triggers the door to close.

Tools and Requirements

Hardware Description Language: Verilog.
Simulation Software: Any standard HDL simulator (e.g., ModelSim, Xilinx Vivado, Synopsys VCS).
Environment: A workstation with an HDL simulation tool installed.

Steps to Run

Open your simulation tool and load the design files (RTL and testbench).
Compile the design to check for syntax and logic errors.
Run the simulation and observe the waveforms or monitor the output logs.
Verify that the door transitions through the expected states as per the input signals.

Key Observations

The FSM transitions smoothly between states based on the inputs.
The door_open signal reflects the correct state of the door at all times.
The reset signal (rst) effectively initializes the system to the IDLE state.

Conclusion

The Automatic Door Controller project effectively demonstrates an FSM implementation using Verilog. It highlights the basics of state-based design and can be extended for real-world applications.
