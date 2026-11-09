# NEER – Floating Water Waste Collection Robot

**A Low-Cost ESP32-Based Robotic System for Floating Waste Collection**

![Project](https://img.shields.io/badge/Project-NEER-087E8B)
![Platform](https://img.shields.io/badge/Platform-ESP32-blue)
![Language](https://img.shields.io/badge/Language-Arduino%20C%2B%2B-orange)
![Domain](https://img.shields.io/badge/Domain-Robotics%20%7C%20Sustainability-green)
![Status](https://img.shields.io/badge/Status-Prototype-yellow)

---

## 1. Introduction

NEER is a low-cost floating robotic system developed to address the problem of floating solid waste in water bodies. The robot is designed to navigate across the water surface and collect floating debris through a motor-driven mechanical collection mechanism.

The system integrates embedded electronics, wireless control, mechanical propulsion and a waste collection assembly into a compact floating platform.

An ESP32 microcontroller serves as the central controller, enabling wireless operation through a Wi-Fi-based web interface. Geared DC motors facilitate navigation, while a rotating mesh-based collection mechanism is intended to retrieve floating waste and transfer it into a dedicated collection compartment.

NEER demonstrates how accessible robotics and embedded technologies can be applied to environmental conservation and water surface cleaning.

## 2. Problem Statement

Water bodies such as ponds, lakes, reservoirs and drainage channels frequently accumulate floating waste, particularly plastic packaging, wrappers, leaves and other lightweight debris.

Manual waste collection can be repetitive, labour-intensive and difficult to perform continuously, particularly in areas that are difficult to access.

There is a need for affordable, compact and mechanically simple systems that can assist in collecting floating waste without requiring large-scale cleaning equipment.

NEER aims to address this problem by developing a floating robotic platform that combines remote navigation with a mechanical waste collection mechanism.

## 3. Project Objectives

- Design and develop a lightweight floating robotic platform.
- Implement motor-driven navigation using an ESP32 microcontroller.
- Enable wireless control through a Wi-Fi-based interface.
- Develop a mechanical mechanism for collecting floating solid waste.
- Integrate a collection compartment for storing retrieved waste.
- Use affordable and accessible components to keep the prototype economical.
- Demonstrate the application of robotics and embedded systems in environmental sustainability.

## 4. System Overview

NEER consists of four primary subsystems:

### 4.1 Floating Structure
The robot uses a lightweight supporting frame and buoyant materials to remain afloat. The structure supports the electronics, propulsion system and waste collection assembly.

### 4.2 Propulsion System
Geared DC motors provide movement and directional control. The robot uses differential motor control to achieve forward, backward and turning movements.

### 4.3 Waste Collection Mechanism
A rotating mesh-based mechanical assembly is designed to collect floating debris from the water surface and move it towards the collection compartment.

### 4.4 Control System
An ESP32 microcontroller manages the motor control operations and provides a Wi-Fi-based interface for remotely operating the robot.

## 5. Working Principle

The intended operation of NEER follows these stages:

1. **Power activation:** The rechargeable battery supplies power to the electronic and mechanical systems.
2. **Wireless connection:** The ESP32 establishes the Wi-Fi control interface.
3. **Navigation:** The operator sends movement commands through the control interface.
4. **Motor operation:** The motor control circuit drives the propulsion motors according to the received commands.
5. **Waste collection:** The collection mechanism is operated to retrieve floating waste from the water surface.
6. **Waste storage:** Retrieved waste is transferred into the collection compartment.
7. **Stopping and unloading:** The robot is stopped and the collection compartment can be emptied.

## 6. Hardware Components

The following components form the project's identified hardware inventory. Final quantities and exact models should be documented according to the assembled prototype.

| Component | Function |
|---|---|
| ESP32 Development Board | Main microcontroller |
| DC Geared Motors | Propulsion |
| Motor Driver | Controls propulsion motor direction |
| Relay Module | Electrical switching for the collection mechanism |
| Conveyor Motor | Drives the collection mechanism |
| Lithium-ion Battery | Main power source |
| Voltage Regulator | Voltage regulation |
| Foam Board | Structural support |
| PVC Pipes and Connectors | Mechanical framework |
| Plastic Floats | Buoyancy |
| Mesh Fabric | Waste collection surface |
| Rollers and Shafts | Mechanical rotation |
| Waste Collection Tray | Stores collected debris |
| Waterproof Enclosure | Protects electronics |
| Connecting Wires | Electrical connections |
| Switch | Power control |
| Fasteners and Cable Ties | Mechanical assembly |

## 7. Software and Technologies

| Technology | Application |
|---|---|
| ESP32 | Embedded control |
| Arduino IDE | Firmware development |
| Arduino C/C++ | Programming language |
| WiFi.h | Wireless connectivity |
| WebServer.h | HTTP web server |
| GPIO Control | Motor and relay switching |
| HTTP | Wireless command communication |

## 8. Firmware and Control

The firmware is developed using Arduino C/C++ and runs on the ESP32 development board.

The current implementation uses Wi-Fi and an HTTP web server to receive remote control commands.

### Implemented control operations

- Forward
- Backward
- Left
- Right
- Stop
- Collection relay ON
- Collection relay OFF

### Current GPIO configuration

| ESP32 GPIO | Connected function |
|---|---|
| GPIO 26 | Left motor input A |
| GPIO 27 | Left motor input B |
| GPIO 14 | Right motor input A |
| GPIO 12 | Right motor input B |
| GPIO 25 | Relay control |

The exact motor-driver wiring, relay polarity and conveyor motor connections must be verified against the final physical circuit.

## 9. System Architecture

```text
          USER / OPERATOR
                 |
                 v
        Wi-Fi CONTROL INTERFACE
                 |
                 v
          ESP32 CONTROLLER
                 |
          +------+------+
          |             |
          v             v
    MOTOR CONTROL   RELAY CONTROL
          |             |
          v             v
    PROPULSION      COLLECTION
      MOTORS         MOTOR
          |             |
          v             v
    NAVIGATION     MESH CONVEYOR
                        |
                        v
                 WASTE COLLECTION
                      TRAY
```

## 10. Mechanical Design

The mechanical structure is designed around a floating platform that supports the electronic and collection systems.

The major mechanical assemblies include:

- Buoyant support structure.
- Lightweight mounting frame.
- Motor mounting arrangement.
- Propulsion assembly.
- Rotating mesh collection mechanism.
- Waste storage compartment.
- Protective enclosure for electronic components.

The mechanical design must maintain sufficient buoyancy, stability and clearance between moving components and the water surface.

## 11. Applications

NEER is intended for potential applications such as:

- Small ponds and artificial water bodies.
- Lakes and reservoirs.
- Campus water bodies.
- Controlled water tanks used for testing.
- Drainage channels with suitable operating conditions.
- Environmental demonstration and educational projects.

Its current prototype should be validated in controlled water environments before considering deployment in natural water bodies.

## 12. Testing and Validation

The prototype should be evaluated through the following tests:

| Test | Parameter to evaluate |
|---|---|
| Buoyancy test | Ability to remain afloat |
| Stability test | Tilting and load distribution |
| Forward movement | Straight-line movement |
| Reverse movement | Reverse propulsion |
| Turning test | Directional control |
| Wi-Fi test | Command communication |
| Motor test | Motor operation and response |
| Collection test | Ability to retrieve floating debris |
| Storage test | Waste transfer and retention |
| Endurance test | Operating duration |
| Waterproofing test | Protection of electronics |

Actual test results, photographs and observations should be added to the testing documentation.

## 13. Current Limitations

- The current implementation relies on remote Wi-Fi control.
- Autonomous navigation has not been implemented.
- Automatic waste detection has not been implemented.
- Obstacle detection and avoidance are not yet integrated.
- Collection efficiency and operating endurance require experimental validation.
- Water resistance and long-term durability require further testing.
- Performance may vary depending on waste type, water conditions and payload.

## 14. Future Enhancements

Potential improvements include:

- Autonomous navigation using GPS or suitable positioning methods.
- Ultrasonic or other obstacle detection sensors.
- Camera-based floating waste detection.
- Improved collection mechanism and mesh design.
- Water-quality monitoring sensors.
- Battery level monitoring.
- Improved waterproof electronics enclosure.
- Solar-assisted charging.
- Improved stability and load distribution.
- Live telemetry and performance monitoring.

These are proposed enhancements and are not part of the currently established implementation.

## 15. Project Significance

NEER demonstrates the integration of embedded systems, mechanical design and wireless communication to address an environmental challenge.

The project provides a foundation for exploring affordable robotic solutions for surface waste management and encourages the application of engineering principles towards sustainable environmental practices.

## 16. Repository Structure

```text
NEER/
├── README.md
├── firmware/
│   └── neer_controller/
│       └── neer_controller.ino
├── hardware/
│   ├── components.md
│   ├── circuit-connections.md
│   └── pin-configuration.md
├── mechanical-design/
│   ├── structure.md
│   └── waste-collection-mechanism.md
├── documentation/
│   ├── project-overview.md
│   ├── working-principle.md
│   ├── system-architecture.md
│   ├── methodology.md
│   ├── testing-and-results.md
│   └── future-enhancements.md
├── images/
├── report/
└── LICENSE
```

## 17. Getting Started

### Requirements

- ESP32 Development Board
- Arduino IDE
- Appropriate ESP32 board package
- USB data cable
- Required hardware and motor driver circuits

### Installation

1. Clone or download this repository.
2. Open the firmware file in Arduino IDE.
3. Install the ESP32 board support package.
4. Select the appropriate ESP32 board and COM port.
5. Configure the Wi-Fi credentials using the local configuration instructions.
6. Verify the GPIO assignments against the actual circuit.
7. Upload the firmware.
8. Connect to the configured Wi-Fi network and access the control interface.

**Security note:** Never publish real Wi-Fi passwords, private network credentials or other secrets in the repository. Use local configuration values or a separate untracked secrets file.

## 18. Project Status

NEER is a working-prototype development project. Its physical structure and Wi-Fi-based ESP32 control implementation have been developed. Further integration, testing, performance evaluation and validation of the mechanical waste collection mechanism remain important parts of the project.

## 19. Contributors

Developed as a collaborative robotics and environmental sustainability project.

Add the names, roles and GitHub profiles of all team members here.

## 20. License

This project may be released under the MIT License. Add a `LICENSE` file if the team chooses to distribute the project under those terms.

---

**NEER – Engineering a cleaner water surface through robotics.**
