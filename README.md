# RouBotix-Advance-LineFollower-BoardV1

**High-performance line follower robot baseboard integrating motor control, turbine support, and sensor interfacing, designed for competitive robotics applications.**


<img width="1287" height="740" alt="PCB BoardUP" src="https://github.com/user-attachments/assets/9e36d173-a3af-4646-8e1e-ef6921757ea2" />


<div align="center">

#  RouBotix Line Follower Board

### Competition-Grade · High-Speed · Custom PCB Platform

[![Hardware](https://img.shields.io/badge/Hardware-PCB%20Design-E7352C?style=for-the-badge&logo=altiumdesigner&logoColor=white)](.)
[![Microcontroller](https://img.shields.io/badge/MCU-Arduino%20Nano-00979D?style=for-the-badge&logo=arduino&logoColor=white)](.)
[![Motor Driver](https://img.shields.io/badge/Driver-TB6612FNG-FF6B00?style=for-the-badge&logo=data:image/png;base64,&logoColor=white)](.)
[![Sensors](https://img.shields.io/badge/Sensors-16%20Channel%20IR-8A2BE2?style=for-the-badge&logoColor=white)](.)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

<br/>

> A high-performance, competition-grade line follower robotics platform integrating  
> motor control, turbine propulsion support, and multi-channel sensor interfacing on a single optimized PCB.

</div>

---

##  Table of Contents

- [Introduction](#-introduction)
- [System Overview](#-system-overview)
- [Key Features](#-key-features)
- [Hardware Architecture](#-hardware-architecture)
- [PCB Design Details](#-pcb-design-details)
- [Bill of Materials](#-bill-of-materials)
- [Screenshots](#-screenshots--pcb-preview)
- [Project Structure](#-project-structure)
- [Author](#-author)

---

##  Introduction

The **RouBotix Advance Line Follower Board** is a custom-designed embedded hardware platform built for high-speed line following robots.

The system combines **motor driving, sensor interfacing, and power management** into a compact and efficient baseboard — reducing wiring complexity and improving real-time performance.

This design is specifically optimized for **robotics competitions** where precision, speed, and reliability are critical.

---

##  System Overview

The system consists of **two major hardware modules:**

```
┌──────────────────────────────────────────────────────────┐
│               RouBotix Complete System                   │
│                                                          │
│   ┌─────────────────────┐   ┌────────────────────────┐  │
│   │  RouBotix Baseboard │   │  16 Sensor Array V1    │  │
│   │        V1           │◀──│  (External Module)     │  │
│   │  (Main Control)     │   │  QRE1113GR IR Sensors  │  │
│   └─────────────────────┘   └────────────────────────┘  │
│            │                                             │
│    ┌───────┼────────┐                                    │
│    ▼       ▼        ▼                                    │
│  Motors  Turbine  Sensors                                │
└──────────────────────────────────────────────────────────┘
```

Together, these modules provide a **complete solution** for advanced line follower robots.

---

##  Key Features

| Feature | Description |
|---|---|
|  **Dual Motor Control** | TB6612FNG driver for precise left/right motor management |
|  **Turbine Propulsion** | External ESC interface for additional thrust & high-speed stability |
|  **16-Channel IR Sensing** | Multiplexed sensor reading via 74HC4067 for wide line detection |
|  **Modular Connectivity** | Reduced wiring with plug-and-play sensor array interface |
|  **Triple Power Input** | Separate VIN, VIN2S, VIN_T for noise-free power distribution |
|  **Compact PCB Layout** | Symmetric, optimized design for robot balance and stability |
|  **Competition Ready** | Designed for high-speed robotics competition environments |

---

##  Hardware Architecture

### 4.1 Control Unit

```
┌─────────────────────────────────┐
│         Arduino Nano            │
│                                 │
│  • Sensor Data Acquisition      │
│  • PID Control Algorithm        │
│  • Motor & Turbine Control      │
└─────────────────────────────────┘
```

### 4.2 Sensor System

| Parameter | Detail |
|---|---|
| **Sensor IC** | QRE1113GR IR Reflectance Sensor |
| **Channels** | Up to 16 via 74HC4067 Multiplexer |
| **Detection Method** | Surface reflectivity (line vs background) |
| **Interface** | Analog / Digital configurable |

### 4.3 Motor Driver

| Parameter | Detail |
|---|---|
| **IC** | TB6612FNG |
| **Left Motor** | MM1 |
| **Right Motor** | MM2 |
| **Advantage** | Efficient, low-loss motor driving |

### 4.4 Turbine System

```
External ESC Interface
        │
        ▼
┌───────────────┐
│  YT Turbine   │  ── Additional Thrust
│               │  ── High-Speed Stability
│  VIN_T Power  │  ── Isolated Power (noise-free)
└───────────────┘
```

### 4.5 Power Distribution

```
┌─────────┐    ┌─────────┐    ┌─────────┐
│  VIN    │    │ VIN2S   │    │ VIN_T   │
│  Main   │    │Secondary│    │Turbine  │
│  Power  │    │  Power  │    │  Power  │
└────┬────┘    └────┬────┘    └────┬────┘
     │              │              │
     ▼              ▼              ▼
  Logic &        Motors         Turbine
  Sensors        (isolated)     (isolated)
```

> Separation of noisy loads (motors/turbine) from logic ensures **stable, interference-free operation.**

---

##  PCB Design Details

| Design Choice | Purpose |
|---|---|
| **Wide copper traces** | Handle high current paths safely |
| **Optimized routing** | Minimal electrical noise |
| **Dedicated ground paths** | Maximum signal stability |
| **Compact symmetric layout** | Balanced weight distribution on robot chassis |
| **Mounting holes** | Secure integration with robot frame |
| **Labeled silkscreen** | Easy and error-free assembly |

---

##  Bill of Materials

### RouBotix Baseboard V1

| Category | Component | Quantity |
|---|---|:---:|
| **Resistor** | 10kΩ | 1 |
| **Motor Driver** | TB6612FNG | 1 |
| **ESC** | Electronic Speed Controller | 1 |
| **Motors** | DC Motors | 2 |
| **Turbine** | YT Turbine | 1 |
| **Sensors** | Sensor Interface | 1 |
| **Switches** | Push Button + 2 Switches | 3 |
| **Power** | VIN / VIN2S / VIN_T | 3 |
| **Misc** | Connectors / Headers | Multiple |

### 16 Sensor Array V1

| Category | Component | Quantity |
|---|---|:---:|
| **IR Sensor** | QRE1113GR | 16 |
| **Multiplexer** | 74HC4067 | 1 |
| **Resistors** | Pull-up/Pull-down | Multiple |
| **Connector** | Interface Header | 1 |



##  Author

<div align="center">

**Raunak Choudhary**  
*Robotics · PCB Design · Embedded Systems · AI*

</div>

---

<div align="center">
<i>Built with Raunak for the Robotics Competition Community</i>
</div>
