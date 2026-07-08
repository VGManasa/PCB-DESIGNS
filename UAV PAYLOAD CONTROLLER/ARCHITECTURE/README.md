# UAV Payload Controller Architecture

## Overview

The UAV Payload Controller is a modular embedded hardware platform designed for UAV-based liquid payload dispensing applications. The architecture is centered around the **STM32F411RET6** microcontroller, which coordinates sensing, navigation, communication, data logging, and payload actuation through dedicated hardware interfaces.

The design follows a modular approach, enabling each subsystem to operate independently while being managed by the central controller. This architecture improves system reliability, simplifies debugging, and allows future hardware expansion with minimal design changes.

---

## Architecture Overview

The controller consists of the following functional modules:

- Power Supply & Protection
- STM32F411 Control Unit
- Communication Interfaces
- Navigation Module
- Sensor Interfaces
- Data Logging
- Actuation Module
- Programming & Debug Interface

Each module performs a dedicated function while communicating with the STM32F411 through SPI, UART, GPIO, USB, or SWD interfaces.

---

# Functional Modules

## 1. Power Supply & Protection

The power subsystem supplies regulated voltage to all onboard peripherals and protects the hardware against electrical faults.

### Features

- Protected 12 V Input
- 5 V Voltage Regulation
- 3.3 V Voltage Regulation
- Reverse Polarity Protection
- TVS Surge Protection

---

## 2. STM32F411 Control Unit

The STM32F411RET6 serves as the central processing unit of the controller.

### Responsibilities

- Executes embedded firmware
- Manages peripheral interfaces
- Processes sensor data
- Controls payload dispensing
- Coordinates communication
- Handles onboard data logging

---

## 3. Communication

### LoRa Module

Provides long-range wireless communication between the UAV and the ground station.

**Interface:** SPI

**Functions**

- Telemetry Transmission
- Remote Monitoring
- Mission Status Updates

---

### USB Interface

Provides wired connectivity for firmware upload and serial communication.

**Functions**

- Firmware Programming
- Serial Communication
- Diagnostics

---

## 4. Navigation

### GPS Module

Provides real-time positioning information for navigation and mission tracking.

**Interface:** UART

**Outputs**

- Latitude
- Longitude
- Altitude
- Speed
- UTC Time

---

## 5. Sensors

### IMU Module

Measures the UAV's motion and orientation.

**Interface:** SPI

**Measurements**

- Linear Acceleration
- Angular Velocity
- Orientation

---

### Flow Sensor

Monitors the liquid flow during payload dispensing.

**Interface:** GPIO

**Functions**

- Flow Rate Measurement
- Dispensing Verification
- Payload Monitoring

---

### Tank Level Sensor

Monitors the liquid level inside the payload tank.

**Functions**

- Tank Level Detection
- Empty Tank Detection
- Payload Availability Monitoring

---

## 6. Data Logging

### SD Card Module

Provides onboard storage for mission and sensor data.

**Interface:** SPI

**Functions**

- Flight Data Logging
- GPS Coordinate Storage
- Sensor Data Logging
- Mission Log Storage
- Telemetry Backup

---

## 7. Actuation

### Pump Driver Unit

Controls the external liquid dispensing pump.

**Functions**

- Pump ON/OFF Control
- Payload Dispensing
- External Driver Interface

---

## 8. Programming & Debug Interface

Supports firmware development, programming, and debugging.

### Interface

- SWDIO
- SWCLK
- NRST

---

# Module Interfaces

| Module | Interface |
|---------|-----------|
| LoRa Module | SPI |
| GPS Module | UART |
| IMU Module | SPI |
| SD Card | SPI |
| Flow Sensor | GPIO |
| Tank Level Sensor | GPIO |
| Pump Driver | GPIO |
| USB Interface | USB |
| SWD Interface | SWD |

---

# System Workflow

```text
                    Protected 12 V Input
                            │
                            ▼
              Power Supply & Protection
                            │
                            ▼
                 STM32F411 Control Unit
      ┌──────────┬──────────┬──────────┬──────────┐
      │          │          │          │          │
      ▼          ▼          ▼          ▼          ▼
     GPS        IMU       LoRa     SD Card      USB
      │          │          │          │
      └──────────┴──────────┴──────────┘
                   Sensor & Navigation Data
                            │
                 ┌──────────┴──────────┐
                 ▼                     ▼
          Flow Sensor         Tank Level Sensor
                 │                     │
                 └──────────┬──────────┘
                            ▼
                   Payload Monitoring
                            │
                            ▼
                       Pump Driver
                            │
                            ▼
                   Liquid Payload Dispensing
```

---

# System Functions

The integrated hardware architecture enables the following operations:

- GPS-based navigation
- Motion and orientation monitoring
- Long-range telemetry communication
- Onboard flight data logging
- Flow rate monitoring
- Tank level monitoring
- Payload dispensing control
- Firmware programming
- Hardware debugging

---

# Design Philosophy

The architecture has been developed with the following objectives:

- Modular subsystem organization
- Reliable power distribution
- Efficient peripheral integration
- Simplified firmware development
- Scalable hardware design
- Easy maintenance and debugging
- Support for future hardware expansion

---

# Future Enhancements

The modular architecture allows future integration of additional hardware without significant redesign.

Potential enhancements include:

- RTK GPS
- PWM-based variable pump control
- Battery voltage and current monitoring
- CAN Bus interface
- Additional sensor expansion headers
- Multi-channel payload control
- Remote firmware updates
- Autonomous waypoint-based dispensing
