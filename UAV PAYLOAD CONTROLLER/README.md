# UAV Payload Controller

A compact, four-layer embedded controller designed for UAV payload dispensing applications. Built around the **STM32F411RET6** microcontroller, the controller integrates navigation, wireless communication, sensor monitoring, onboard data logging, and payload actuation into a single hardware platform.

Designed for UAVs with payload capacities of **1–2 kg**, the controller provides a reliable and modular solution for precision agriculture, autonomous liquid dispensing, and UAV research applications.

---

## Overview

The UAV Payload Controller serves as the central electronics unit responsible for coordinating all onboard peripherals required for payload operations.

The controller interfaces with navigation sensors, communication modules, storage devices, payload sensors, and actuators to enable autonomous or remotely controlled dispensing operations.

The hardware architecture follows a modular design, allowing individual subsystems to be developed, tested, and upgraded independently.

---

## Key Features

- STM32F411RET6 ARM Cortex-M4 Microcontroller
- Four-layer PCB architecture
- LoRa wireless telemetry communication
- GPS navigation interface
- IMU motion sensing
- SD Card onboard data logging
- Flow sensor monitoring
- Tank level sensing
- External pump driver interface
- Protected 12 V power input
- Regulated 5 V and 3.3 V power rails
- Reverse polarity protection
- TVS surge protection
- USB programming interface
- SWD debugging interface
- Modular and expandable hardware architecture

---

## Applications

The controller is intended for UAV platforms carrying payloads of approximately **1–2 kg**.

Typical applications include:

- Precision pesticide spraying
- Fertilizer dispensing
- Herbicide spraying
- Precision liquid application
- Agricultural field trials
- UAV payload research
- Autonomous dispensing experiments
- Flight telemetry logging
- Embedded systems development

---

## System Architecture

The controller is composed of the following hardware modules:

- STM32F411 Control Unit
- Power Supply & Protection
- LoRa Communication Module
- GPS Module
- IMU Module
- SD Card Module
- Flow Sensor Interface
- Tank Level Sensor Interface
- Pump Driver Unit
- USB Programming Interface

## Hardware Specifications

| Parameter | Specification |
|------------|----------------|
| Microcontroller | STM32F411RET6 |
| Architecture | ARM Cortex-M4 |
| PCB Layers | 4 |
| Input Voltage | 12 V |
| Logic Voltage | 3.3 V |
| Communication Interfaces | SPI, UART, USB |
| Wireless Communication | LoRa |
| Navigation | GPS |
| Motion Sensor | IMU |
| Data Logging | Micro SD Card |
| Payload Monitoring | Flow Sensor |
| Tank Monitoring | Tank Level Sensor |
| Actuation | Pump Driver |
| Programming | USB, SWD |

---

# Functional Modules

## STM32F411 Control Unit

The STM32F411RET6 acts as the central controller responsible for coordinating all peripheral modules.

### Responsibilities

- Executes embedded firmware
- Reads sensor data
- Controls payload dispensing
- Manages communication interfaces
- Stores mission data
- Coordinates system peripherals

---

## Power Supply & Protection

Provides regulated and protected power to every subsystem.

### Features

- Protected 12 V Input
- 5 V Voltage Regulation
- 3.3 V Voltage Regulation
- Reverse Polarity Protection
- TVS Surge Protection

---

## GPS Module

Provides real-time positioning information for navigation and mission tracking.

### Interface

- UART

### Data

- Latitude
- Longitude
- Altitude
- Speed
- UTC Time

---

## IMU Module

Measures the UAV's motion and orientation.

### Interface

- SPI

### Measurements

- Linear Acceleration
- Angular Velocity
- Orientation

---

## LoRa Communication Module

Provides long-range wireless communication with the ground station.

### Interface

- SPI

### Functions

- Telemetry Transmission
- Remote Monitoring
- Mission Status Updates

---

## SD Card Module

Provides onboard non-volatile storage for mission data.

### Interface

- SPI

### Functions

- GPS Data Logging
- Sensor Data Logging
- Mission Log Storage
- Telemetry Backup
- Flight Data Recording

---

## Flow Sensor Interface

Monitors liquid flow during payload dispensing.

### Interface

- GPIO

### Functions

- Flow Rate Measurement
- Dispensing Verification
- Payload Monitoring

---

## Tank Level Sensor Interface

Monitors liquid availability inside the payload tank.

### Functions

- Tank Level Detection
- Empty Tank Detection
- Payload Availability Monitoring

---

## Pump Driver Unit

Controls the external liquid dispensing pump.

### Functions

- Pump ON/OFF Control
- Payload Dispensing
- External MOSFET Driver Interface

---

## USB Interface

Provides programming and communication with a host computer.

### Functions

- Firmware Upload
- Serial Communication
- Diagnostics

---

## Programming & Debugging

Firmware development is supported through the SWD interface.

### Interface

- SWDIO
- SWCLK
- NRST

---

# System Workflow

```
                    Protected 12 V Input
                            │
                            ▼
              Power Supply & Protection
                            │
                            ▼
                   STM32F411 Microcontroller
       ┌─────────────┬─────────────┬──────────────┐
       │             │             │              │
       ▼             ▼             ▼              ▼
      GPS           IMU          LoRa         SD Card
       │             │             │              │
       └─────────────┴─────────────┴──────────────┘
                             │
                             ▼
                  Navigation & Sensor Processing
                             │
                  ┌──────────┴──────────┐
                  ▼                     ▼
           Flow Sensor          Tank Sensor
                  │                     │
                  └──────────┬──────────┘
                             ▼
                    Payload Monitoring
                             │
                             ▼
                       Pump Driver
                             │
                             ▼
                    Liquid Dispensing
```

---

# Peripheral Interfaces

| Peripheral | Interface |
|------------|-----------|
| GPS Module | UART |
| LoRa Module | SPI |
| IMU | SPI |
| SD Card | SPI |
| Flow Sensor | GPIO |
| Tank Sensor | GPIO |
| Pump Driver | GPIO |
| USB | USB |
| SWD | SWD |

---

# PCB Stackup

| Layer | Description |
|---------|-------------------------|
| F.Cu | Signal Routing |
| In1.Cu | Ground Plane |
| In2.Cu | 3.3 V Power Plane |
| B.Cu | Signal Routing |

The four-layer stackup provides:

- Improved signal integrity
- Low impedance ground return
- Better power distribution
- Reduced EMI
- Simplified routing

---

# Manufacturing Files

This repository includes all files required for PCB fabrication.

- Gerber Files
- Drill Files
- Bill of Materials (BOM)

Compatible with standard PCB manufacturers such as JLCPCB, PCBWay, and OSH Park.

---

# Development Environment

## Hardware Design

- KiCad 9

## Firmware Development

- STM32CubeIDE
- STM32CubeMX

## Programming

- ST-Link V2
- SWD Interface

---

# Future Improvements

Future hardware revisions may include:

- PWM-based variable pump speed control
- Battery voltage monitoring
- Current sensing
- RTC backup battery
- RTK GPS support
- CAN Bus interface
- Additional UART/I²C/SPI expansion
- Multiple payload channels
- Redundant power input
- Remote firmware updates
- Autonomous waypoint-based payload dispensing

---

# Project Status

| Module | Status |
|----------|-----------|
| Schematic Design | Complete |
| PCB Layout | Complete |
| ERC Verification | Complete |
| DRC Verification | Complete |
| Gerber Generation | Complete |
| PCB Fabrication | Planned |
| Hardware Testing | Planned |
| Firmware Development | In Progress |

---

# License

This project is licensed under the MIT License.

---

# Author

**V G Manasa & Shruthi Narayanan**

B.Tech Electronics and Communication Engineering

Vellore Institute of Technology, Chennai

---

## Acknowledgements

This project was developed as part of an embedded systems initiative focused on designing a reliable, modular, and compact UAV payload controller for precision liquid dispensing applications. The architecture emphasizes scalability, maintainability, and seamless integration into small UAV platforms used for research and agricultural automation.
