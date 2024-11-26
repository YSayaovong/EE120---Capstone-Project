# Synchronous Sequential Machines

This repository documents the design, development, and simulation of a synchronous sequential machine to control a motorized wheelchair based on stakeholder requirements. The project emphasizes user-friendly design, safety, compactness, and minimal use of logic gates.

## Project Overview

The project was undertaken as part of coursework in Spring 2022. The objective was to design a finite state machine to control the motion of a wheelchair. The design considers inputs from a joystick to determine motor directions while incorporating safety and functional requirements.

## Features

- **Joystick Control**: Implements joystick-based input for intuitive forward, backward, left, and right movement.
- **Safety Mechanisms**: Includes features such as error indicators for invalid joystick inputs.
- **LED Indicators**: Displays movement status and error signals.
- **Compact Design**: Optimized state transitions with minimal logic gates.
- **User-Centric Design**: Designed with stakeholder feedback to ensure ease of use and practical functionality.

## Design Process

### 1. Stakeholder Interviews
- Identified user needs, including lightweight design, safety straps, and joystick controls.
- Incorporated feedback into the machine's design criteria.

### 2. State Definitions
- Designed states for movement (e.g., center, first left, first right, etc.).
- Developed a state definition table:

| State | Binary | Description    |
|-------|--------|----------------|
| S0    | 000    | Center         |
| S1    | 001    | First Left     |
| S2    | 010    | Second Left    |
| S3    | 011    | Third Left     |
| S4    | 100    | First Right    |
| S5    | 110    | Second Right   |
| S6    | 111    | Third Right    |

### 3. Design Evaluation
- Developed multiple designs and evaluated them using criteria such as:
- Minimal gates (15%)
- Safety (30%)
- Compactness (20%)
- User-friendliness (30%)
- Chose the best design based on the weighted evaluation.

### 4. Implementation and Simulation
- Simulated the winning design using Digital simulation software.
- Verified state transitions, outputs, and functionality through rigorous testing.

## Final Equations and Logic Gates
The following equations were implemented to achieve the desired state transitions:
- Q2: `Q1Y’ + Q1’X’ + Q0X’ + QZQ0X + Q1’Q0’XY + Q2’QZ’Q0XY`
- Q1: `Q0’X’Q2 + Q2’Q1’Q0X + Q2’Q1Q0’Y’ + Q2’Q1Q0X’ + Q2Q1Q0Y’ + Q2Q1’Q0’Y`
- Q0: `Q0X’Y’ + Q0XY + Q0’X’Y + Q0XY’`

## Testing
The circuit was tested under various scenarios to ensure proper functionality. Testing included:
- Validating joystick input handling.
- Checking expected vs. actual outputs.
- Ensuring the error indicator activated for invalid inputs.

## Video Demonstration
A demonstration video of the final design is available:
- [YouTube Link](https://youtu.be/DAnCLOoJpyQ)

## Repository Contents
- **Design Documentation**: Includes state diagrams, Karnaugh maps, and transition tables.
- **Simulation Files**: Digital simulation files for the winning design.
- **Test Results**: Testing plans and results for the circuit.

## Conclusion
This project demonstrates the successful implementation of a synchronous sequential machine tailored to stakeholder needs. The design balances technological, societal, and environmental considerations, ensuring practicality and reliability.

---
