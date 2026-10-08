# Temperature & Humidity Controller

An embedded climate control system simulated in Proteus, featuring multi-sensor DHT22 data acquisition, FSM-based control logic, and multi-level heating, cooling, and humidity regulation.

## Overview

This project implements an embedded climate control system designed to monitor and regulate environmental conditions using three DHT22 temperature and humidity sensors.

The system continuously collects sensor measurements, calculates average temperature and humidity values, and controls a heater, cooler, and humidifier based on predefined thresholds. The control strategy is implemented using Finite State Machines (FSMs), allowing stable and efficient environmental regulation through multiple operating modes.

## Features

- Multi-sensor temperature and humidity monitoring using three DHT22 sensors
- Sensor data averaging for improved measurement reliability
- FSM-based environmental control
- Independent temperature and humidity control logic
- Multi-level heater operation (OFF, LOW, HIGH)
- Multi-level cooler operation (OFF, LOW, HIGH)
- Multi-level humidifier operation (OFF, LOW, HIGH)
- Real-time monitoring through a virtual terminal
- Complete system simulation and verification in Proteus

## System Architecture

The system consists of three main subsystems:

### Sensors

Three DHT22 sensors are used to measure:

- Temperature
- Relative Humidity

The controller calculates average environmental values from all sensor readings before making control decisions.

### Control Logic

The control logic is implemented using Finite State Machines (FSMs) and is divided into two independent sections:

1. Temperature Control
   - Heater Controller
   - Cooler Controller

2. Humidity Control
   - Humidifier Controller

Each controller continuously evaluates sensor data and updates actuator states accordingly.

### Actuators

The system controls:

- Heater
- Cooler
- Humidifier

Each actuator supports multiple operating levels depending on environmental conditions.

## FSM-Based Control

The project employs Finite State Machines to manage actuator behavior and system transitions.

### Temperature Controller

#### Cooler States

| Average Temperature | State |
|---------------------|--------|
| T > 38°C | HIGH |
| 32°C < T ≤ 38°C | LOW |
| T < 28°C | OFF |

#### Heater States

| Average Temperature | State |
|---------------------|--------|
| T < 15°C | HIGH |
| 15°C ≤ T < 20°C | LOW |
| T > 23°C | OFF |

### Humidity Controller

| Average Humidity | State |
|------------------|--------|
| H < 70% | HIGH |
| 70% ≤ H < 80% | LOW |
| H > 85% | OFF |

The use of different activation and deactivation thresholds provides hysteresis behavior, reducing unnecessary switching and improving system stability.

## Proteus Simulation

The complete system was designed and verified in Proteus and includes:

- Three DHT22 sensors
- Microcontroller-based control logic
- Heater indicators
- Cooler indicators
- Humidifier indicators
- Virtual terminal for monitoring system operation

## Technologies & Concepts

- Embedded Systems
- C/C++
- Proteus Design Suite
- DHT22 Sensors
- Finite State Machines (FSM)
- Sensor Data Acquisition
- Environmental Monitoring
- Digital Control Systems
- Hardware/Software Integration

## Documentation

A detailed project report containing system design, FSM diagrams, implementation details, and simulation results is available in:

```text
Report.pdf
```
