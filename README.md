# Temperature & Humidity Controller

An embedded climate control system simulated in Proteus, featuring multi-sensor DHT22 data acquisition, FSM-based control logic, and multi-level heating, cooling, and humidity regulation.

## Overview

This project implements an embedded climate control system designed to monitor and regulate environmental conditions using three DHT22 temperature and humidity sensors.

The system continuously collects sensor measurements, calculates average temperature and humidity values, and controls a heater, cooler, and humidifier according to predefined thresholds. The control strategy is implemented using Finite State Machines (FSMs), enabling automatic environmental regulation with multiple operating levels.

The complete system was designed and verified in Proteus.

## Features

- Three DHT22 sensors for temperature and humidity monitoring
- Multi-sensor data acquisition and averaging
- FSM-based control architecture
- Parallel temperature and humidity control
- Multi-level heater operation (OFF, LOW, HIGH)
- Multi-level cooler operation (OFF, LOW, HIGH)
- Multi-level humidifier operation (OFF, LOW, HIGH)
- Real-time monitoring through a virtual terminal
- LED-based visualization of actuator states
- Complete simulation and validation in Proteus

## System Architecture

The system consists of three major subsystems:

### Sensors

Three DHT22 sensors measure:

- Temperature
- Relative Humidity

Average temperature and humidity values are calculated from all sensor readings and used as inputs to the controller.

### Control Logic

The system is divided into two parallel FSM-based control sections:

1. Temperature Control
   - Heater Controller
   - Cooler Controller

2. Humidity Control
   - Humidifier Controller

Both sections operate simultaneously and continuously update actuator states based on the average environmental measurements.

### Actuators

The system controls:

- Heater
- Cooler
- Humidifier

Each actuator supports OFF, LOW, and HIGH operating modes.

## FSM-Based Environmental Control

### Cooler Control

| Average Temperature | State |
|---------------------|--------|
| T > 38°C | HIGH |
| 32°C < T ≤ 38°C | LOW |
| T < 28°C | OFF |

### Heater Control

| Average Temperature | State |
|---------------------|--------|
| T < 15°C | HIGH |
| 15°C ≤ T < 20°C | LOW |
| T > 23°C | OFF |

### Humidifier Control

| Average Humidity | State |
|------------------|--------|
| H < 70% | HIGH |
| 70% ≤ H < 80% | LOW |
| H > 85% | OFF |

The FSM continuously monitors environmental conditions and updates the actuator states accordingly.

## Proteus Simulation

The simulation environment includes:

- Three DHT22 sensors
- Heater indicators
- Cooler indicators
- Humidifier indicators
- Virtual terminal
- FSM-based control logic

The virtual terminal displays sensor measurements and calculated average environmental values during system operation.

## Technologies & Concepts

- C/C++
- Embedded Systems
- Proteus Design Suite
- DHT22 Sensors
- Finite State Machines (FSM)
- Multi-Sensor Data Acquisition
- Environmental Monitoring
- Temperature Control
- Humidity Control
- Digital Control Systems
- Embedded Programming

## Documentation

A detailed project report containing FSM diagrams, system design, implementation details, and simulation results is provided in:

```text
Report.pdf
```
