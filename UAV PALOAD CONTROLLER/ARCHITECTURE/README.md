# UAV Payload Controller Architecture

## Overview

The UAV Payload Controller is a compact embedded system designed to manage payload dispensing, acquire sensor data, determine navigation information, and establish reliable communication with a ground station. The system is built around the **STM32F411** microcontroller, which serves as the central processing unit and coordinates all peripheral modules.

The architecture is organized into independent functional blocks to improve modularity, simplify debugging, and facilitate future hardware expansion.

---

## Functional Blocks

### 1. Power Supply & Protection

The power subsystem provides regulated and protected power to all onboard components. It ensures stable operation under varying input conditions while protecting the hardware from electrical faults.

**Features**
- 12 V Input
- 5 V Voltage Regulation
- 3.3 V Voltage Regulation
- Reverse Polarity Protection
- TVS Surge Protection

---

### 2. STM32F411 Microcontroller

The STM32F411 acts as the central controller responsible for executing firmware, processing sensor data, managing communication interfaces, and controlling payload operations.

**Responsibilities**
- Central Processing
- Sensor Interface
- Communication Management
- Actuator Control

---

### 3. Communication

The communication subsystem enables data exchange between the UAV and external systems.

**Interfaces**
- LoRa Module (SPI)
- GPS Module (UART)
- USB Interface

---

### 4. Sensors

The sensor subsystem provides real-time information required for payload monitoring and navigation.

**Sensors**
- IMU (SPI)
- Flow Sensor (GPIO)

---

### 5. Actuation

The actuation subsystem controls the payload dispensing mechanism through an external pump driver.

**Component**
- Pump Driver

---

### 6. Programming & Debug Interface

The programming interface supports firmware development, debugging, and device programming.

**Interface**
- SWD (Serial Wire Debug)

---

### 7. System Functions

The integration of all hardware modules enables the controller to perform the following high-level functions:

- Sensor Monitoring
- Payload Dispensing
- GPS Tracking
- Telemetry Transmission
- Remote Communication

---

## System Workflow

```text
Power Input
      │
      ▼
Power Supply & Protection
      │
      ▼
STM32F411 Microcontroller
      │
 ┌────┼───────────────┐
 │    │               │
 ▼    ▼               ▼
Sensors      Communication     Actuation
 │            │                 │
 └────────────┴─────────────────┘
              │
              ▼
      System Functions
```

---

## Design Objectives

The architecture has been developed with the following objectives:

- Modular hardware organization
- Reliable power distribution
- Efficient peripheral interfacing
- Long-range wireless communication
- Real-time sensor acquisition
- Scalable system design
- Simplified firmware development and debugging

---

## Hardware Summary

| Module | Purpose |
|---------|---------|
| STM32F411 | Central processing and peripheral control |
| Power Supply & Protection | Voltage regulation and circuit protection |
| LoRa Module | Long-range telemetry communication |
| GPS Module | Positioning and navigation |
| IMU | Motion and orientation sensing |
| Flow Sensor | Payload flow monitoring |
| Pump Driver | Payload dispensing control |
| SWD Interface | Programming and debugging |
| USB Interface | Firmware upload and serial communication |

---

## Notes

This architecture provides a modular foundation for UAV payload management applications. Each subsystem operates independently while being coordinated by the STM32F411 microcontroller, enabling reliable sensing, communication, navigation, and payload control suitable for autonomous and remotely operated UAV platforms.
