# RouBotix-Advance-LineFollower-BoardV1
High-performance line follower robot baseboard integrating motor control, turbine support, and sensor interfacing, designed for competitive robotics applications.


<img width="1287" height="740" alt="PCB BoardUP" src="https://github.com/user-attachments/assets/9e36d173-a3af-4646-8e1e-ef6921757ea2" />



# RouBotix Line Follower Board

A high-performance, competition-grade line follower robotics platform integrating motor control, turbine propulsion support, and multi-channel sensor interfacing on a single optimized PCB.



## 1. Introduction

The RouBotix Advance Line Follower Board is a custom-designed embedded hardware platform developed for high-speed line following robots. The system combines motor driving, sensor interfacing, and power management into a compact and efficient baseboard, reducing wiring complexity and improving real-time performance.

This design is specifically optimized for robotics competitions where precision, speed, and reliability are critical.

---

## 2. System Overview

The system consists of two major hardware modules:

- RouBotix Baseboard V1 (Main Control Board)
- 16 Sensor Array V1 (External Sensor Module)

Together, these modules provide a complete solution for advanced line follower robots.

---

## 3. Key Features

- Dual DC motor control using TB6612FNG driver
- Support for turbine propulsion using external ESC
- Interface for 8/16 channel IR sensor arrays
- Multiplexed sensor reading support
- Compact PCB optimized for high-speed robotics
- Dedicated power inputs for logic, motors, and turbine
- Onboard switches for control and operation
- Reduced wiring and modular connectivity

---

## 4. Hardware Architecture

### 4.1 Control Unit
- Microcontroller: Arduino Nano / compatible
- Responsible for:
  - Sensor data acquisition
  - PID control algorithm
  - Motor and turbine control

---

### 4.2 Sensor System
- External sensor array using QRE1113GR IR sensors
- Supports up to 16 sensors via multiplexer (74HC4067)
- Detects line based on surface reflectivity

---

### 4.3 Motor Driver
- IC: TB6612FNG
- Controls:
  - Left Motor (MM1)
  - Right Motor (MM2)
- Provides efficient and low-loss motor driving

---

### 4.4 Turbine System
- External ESC interface
- Used for:
  - Additional thrust
  - High-speed stability
- Powered separately to avoid noise interference

---

### 4.5 Power Distribution
- VIN: Main power input
- VIN2S: Secondary power input
- VIN_T: Turbine power input

Design ensures:
- Stable voltage supply
- Separation of noisy loads (motors/turbine) from logic

---

## 5. PCB Design Details

- Wide copper traces for high current paths
- Optimized routing for minimal electrical noise
- Dedicated ground paths for stability
- Compact and symmetric layout for robot balance
- Mounting holes for secure chassis integration
- Clearly labeled silkscreen for easy assembly

---

## 6. Bill of Materials

### RouBotix Baseboard V1

| Category | Component | Quantity |
|----------|----------|----------|
| Resistor | 10kΩ     | 1        |
| Motor Driver | TB6612FNG | 1 |
| ESC | Electronic Speed Controller | 1 |
| Motors | DC Motors | 2 |
| Turbine | YT Turbine | 1 |
| Sensors | Sensor Interface | 1 |
| Switches | Push Button + 2 Switches | 3 |
| Power | VIN / VIN2S / VIN_T | 3 |
| Misc | Connectors / Starter | Multiple |

---


## 7. Repository Structure
