---

## Robotic Manipulator Control System - I/O Interface
System Overview
This repository contains the documentation, source code, and hardware schematics for an automated robotic system designed for pick-and-place operations. The system integrates an industrial robot controller with a pneumatic array comprising cylinders and grippers, managed through a central I/O terminal.

---

Hardware Architecture
The control logic is based on the interaction between the Robot I/O Terminal (NPN configuration) and external field devices. The architecture is defined by the attached I/O diagram and includes the following subsystems:

Power Supply
Source: AC 110V input converted to DC 24V.

Distribution: Supplies power to the I/O Box, sensors, and solenoid valves.

Pneumatic Actuation & Feedback
The system controls movement through solenoid valves and monitors status via position sensors:

Cylinder X: Controlled by Solenoid #1; monitored by Sensors 1 & 2.

Cylinder Y: Controlled by Solenoid #2 (Extend) and Solenoid #3 (Retract); monitored by Sensors 1 & 2.

Gripper: Controlled by Solenoid #4; monitored by Gripper Sensors 1 & 2.

Connectivity
Network: PC and Teach Pendant connected via WiFi HUB.

Terminal: NPN Robot I/O Terminal handling discrete Input/Output signals (Common pins 0-7, 8-15, etc.).

---

Operator Interface Pinout
The system includes a hardwired I/O Box for manual operator control. The wiring configuration links physical buttons to specific signal names within the robot controller.

Pin 2 (Green): Start - Signal 0
Pin 3 (White): Task 1 - Signal 1
Pin 4 (Blue): Task 2 - Signal 2
Pin 5 (Orange): Maintenance Point - Signal 3
Pin 6 (Red): Stop - Signal 4

---

Usage Notes
When configuring the robot controller, ensure the input signals correspond to the Signal Name values listed in the table above. All sensors and solenoids operate on a 24V logic level compatible with the NPN terminal specification.

---
