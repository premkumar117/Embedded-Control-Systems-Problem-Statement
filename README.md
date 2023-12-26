# Embedded-Control-Systems-Problem-Statement
Embedded/Control Systems Problem Statement

1. Introduction
This report outlines the design of a motor control system using an 
ESP32 microcontroller, an H-Bridge driver, and an OE-37 encoder. The 
system aims to regulate motor speed through closed-loop control, 
allowing for user-specified speed and direction via serial commands.
2. System Overview
Block Diagram:
             ┌─────────┐
             │ Host PC │
             └───┬─────┘
                 │ Serial Commands
                 ▼
             ┌─────────┐
             │ ESP32   │
             └──────┬───┘
                   │
      ┌─────────────┴─────────────┐
      │                          │
      │       ┌─────────┐        │
      │       │ Encoder │       │
      │       └────┬─────┘       │
      │            │             │
      │       Speed Feedback       │
      │            │             │
      │       ┌─────────┐        │
      └───────┤ H-Bridge │───────┘
             └────┬─────┘
                   │
                   ▼
             ┌─────────┐
             │ Motor   │
             └─────────┘
Components:
• Host PC: Sends serial commands to control speed and direction.
• ESP32: Microcontroller for processing commands and 
implementing control algorithms.
• Encoder: OE-37 Hall effect encoder, providing speed feedback.
• H-Bridge: Drives the motor based on PWM signals from the 
ESP32.
• Motor: The specific motor type and specifications are yet to be 
provided.
3. Assumptions and Theoretical Basis
Motor:
• A brushed DC motor is assumed, but confirmation and 
specifications are needed.
Control Algorithm:
• A simple proportional control algorithm is currently 
implemented, but PID control is likely to provide better 
performance. A decision on the final control algorithm is pending.
Feedback:
• The OE-37 encoder provides speed feedback for closed-loop 
control.
Communication:
• Serial communication is used for setting speed and direction.
4. Engineering Calculations (Placeholders)
• Encoder Resolution: Calculation based on motor speed range and 
desired accuracy will be provided once motor specifications are 
available.
• PWM Frequency: Selection based on motor characteristics and 
control requirements will be determined after motor specifications 
are known.
• H-Bridge Driver: Selection based on motor voltage and current 
ratings will be made once motor specifications are provided.
5. Implementation (Partial)
• Hardware Setup:
o Connections between ESP32, encoder, H-Bridge, and motor 
(details pending).
o Power supply configuration (details pending).
• Software Code:
o Code for reading serial commands, controlling PWM 
output, and reading encoder feedback has been provided.
6. Testing and Results (Pending)
• Testing procedures and results will be documented once the 
system is implemented.
7. Conclusion (Pending)
• Summary of key findings and recommendations for further 
improvements will be provided upon completion of the design and 
testing phases.
