# Industrial Conveyor Motor Monitor

## Project Overview

The Industrial Conveyor Motor Monitor is a software-based project designed to monitor the operating condition of an industrial conveyor motor.

The project uses a Linux kernel character-device driver to simulate motor telemetry such as RPM, temperature, and motor state. A C++ dashboard reads this information and displays the motor condition to the user.

The project also supports fault simulation by allowing different motor states to be tested.

## Objectives

- Develop a Linux character-device driver for a simulated conveyor motor.
- Generate motor telemetry such as RPM and temperature.
- Monitor the motor state.
- Simulate different motor operating and fault conditions.
- Develop a C++ dashboard to display motor telemetry.
- Demonstrate communication between a Linux kernel driver and a user-space application.

## Technologies Used

- C
- C++
- Linux Kernel
- Linux Character Device
- Makefile
- Shell Script
- Terminal

## System Architecture

```text
Conveyor Motor Simulation
          |
          v
Linux Kernel Driver
(conveyor_driver.c)
          |
          |-- RPM
          |-- Temperature
          |-- Motor State
          |
          v
C++ Dashboard
(dashboard.cpp)
          |
          v
Terminal
