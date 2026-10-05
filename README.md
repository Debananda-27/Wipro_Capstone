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
```

## Motor States

| State | Condition | RPM | Temperature |
|-------|-----------|-----|-------------|
| 0 | Normal Operation | 1400–1499 | 60–74°C |
| 1 | Overheating | 1450–1499 | 95–114°C |
| 2 | Motor Stopped / Fault | 0–9 | 80–89°C |

## Project Components

### `conveyor_driver.c`

Linux kernel character-device driver responsible for generating and providing motor telemetry.

### `dashboard.cpp`

C++ application responsible for reading and displaying the motor telemetry.

### `Makefile`

Used to build the project.

### `setup.sh`

Used for project setup and execution.

## Working

1. The Linux kernel driver is loaded.
2. The driver registers the `conveyor_motor` character device.
3. The driver generates RPM and temperature values according to the selected motor state.
4. The C++ dashboard reads the telemetry from the driver.
5. The dashboard displays the motor information.
6. The motor state can be changed to simulate different fault conditions.

## Fault Simulation

The motor state can be changed using the following values:

- `0` → Normal Operation
- `1` → Overheating
- `2` → Motor Stopped / Fault

## Build and Run

```bash
make
./setup.sh
```

## Expected Output

The dashboard displays:

- RPM
- Temperature
- Motor State

The displayed values change according to the selected motor state.

## Conclusion

The Industrial Conveyor Motor Monitor demonstrates the use of a Linux kernel character-device driver to simulate industrial motor telemetry and a C++ application to monitor the motor's operating condition and simulate different fault states.
