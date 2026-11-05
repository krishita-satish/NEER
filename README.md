# NEER
### A Compact Floating Robotic System for Water-Surface Waste Collection

**Clean Water. Greener Tomorrow.**

![Project Status](https://img.shields.io/badge/Status-Design%20%26%20Development-orange)
![Controller](https://img.shields.io/badge/Controller-ESP32-blue)
![Communication](https://img.shields.io/badge/Communication-Bluetooth%20LE-blue)
![Domain](https://img.shields.io/badge/Domain-Embedded%20Robotics-green)
![Budget](https://img.shields.io/badge/Target%20Budget-₹3000-brightgreen)

---

## 1. Overview

NEER is a compact, low-cost floating robotic system designed to collect lightweight solid waste accumulating on the surface of small, contained water bodies.

The system integrates a twin-hull floating platform, differential propulsion, a motorised rotating mesh scoop and an onboard removable waste collection basket.

Powered by an ESP32-based embedded control system, NEER uses Bluetooth Low Energy (BLE) for wireless navigation and independent operation of its waste collection mechanism.

Unlike conventional floating platforms that only provide mobility, NEER combines navigation with an active mechanical collection system that captures, lifts and stores floating debris.

The project explores the practical application of embedded systems, robotics and mechanical design to an environmental maintenance problem.

## 2. Problem Statement

Floating waste such as plastic wrappers, bottle caps, leaves and lightweight packaging frequently accumulates on the surfaces of ponds, swimming pools and other contained water bodies.

Conventional manual cleaning requires repeated human effort and may be inconvenient when waste is distributed across different areas of a water surface.

NEER aims to address this problem through an affordable, reusable and remotely operated robotic system capable of navigating a contained water surface and mechanically collecting floating solid waste.

## 3. Project Objectives

- Design a compact and stable floating robotic platform.
- Implement wireless navigation using an ESP32 controller.
- Develop a differential propulsion system using two independently controlled motors.
- Design a rotating mesh-based mechanism for collecting floating debris.
- Transfer collected waste into an onboard removable storage basket.
- Implement independent control of navigation and waste collection.
- Develop protected, organised and maintainable electronics.
- Keep the design affordable, modular and suitable for repeated operation.

## 4. System Architecture

NEER consists of six primary subsystems:

| Subsystem | Function |
|---|---|
| Floating Platform | Provides buoyancy and structural support |
| Propulsion System | Enables forward, reverse and directional movement |
| Collection Assembly | Captures and lifts floating debris |
| Waste Storage | Retains collected debris in a removable basket |
| Embedded Controller | Processes commands and controls motor operation |
| Power System | Supplies regulated power to electronic and mechanical components |

### 4.1 Floating Platform

A twin-hull catamaran-style configuration provides buoyancy and lateral stability.

The two sealed hulls support a central deck containing the electronics enclosure, battery and mechanical assemblies.

### 4.2 Propulsion System

Two independently controlled rear propulsion motors provide differential steering.

| Motor operation | Movement |
|---|---|
| Both forward | Forward |
| Both reverse | Reverse |
| Left slower than right | Left turn |
| Right slower than left | Right turn |
| Both stopped | Stop |

### 4.3 Waste Collection Mechanism

The front collection assembly consists of:

- V-shaped debris-guiding panels.
- A rotating mesh scoop with four proposed collection pockets.
- A geared DC motor.
- A shaft and supporting bearings.
- A waste-transfer opening.

The guide panels direct floating debris towards the rotating scoop. The scoop lifts the debris above the waterline and transfers it into the storage basket while allowing water to drain through the mesh.

### 4.4 Waste Storage

A removable mesh basket retains collected debris and allows excess water to drain.

The basket is designed for convenient removal, emptying and reinstallation.

## 5. Working Principle

1. **Initialisation:** The operator switches on the system. The ESP32 initialises its control interfaces and keeps all motor outputs disabled.
2. **Wireless Connection:** A compatible mobile device connects to the ESP32 through Bluetooth Low Energy.
3. **Navigation:** Movement commands are processed by the ESP32, which controls the two propulsion motors through a motor driver.
4. **Collection:** The operator activates the collection mechanism independently of propulsion.
5. **Waste Transfer:** The rotating mesh scoop lifts floating debris and transfers it into the onboard basket.
6. **Safety:** A communication timeout stops propulsion if valid movement commands are no longer received.

## 6. Proposed Technical Specifications

The following values represent the initial design targets. They are subject to component selection, fabrication constraints and physical validation.

| Parameter | Proposed Specification |
|---|---|
| Project Name | NEER |
| Controller | ESP32 Development Board |
| Communication | Bluetooth Low Energy |
| Floating Configuration | Twin Hull / Catamaran |
| Propulsion | Dual Propeller |
| Steering | Differential Propulsion |
| Collection Mechanism | Rotating Mesh Scoop |
| Waste Storage | Removable Mesh Basket |
| Target Length | 400 mm |
| Target Width | 280 mm |
| Target Height | 160 mm |
| Individual Hull | 350 × 70 × 80 mm |
| Collection Drum | 150 mm width × 90 mm diameter |
| Power Source | Protected Rechargeable Battery |
| Target Budget | ₹3,000 |

**Note:** The dimensions are preliminary design targets, not approved production dimensions. Final drawings must be updated to match selected components and validated mechanical clearances.

## 7. Hardware Architecture

The proposed electronics architecture includes:

- ESP32 development board.
- Dual-channel propulsion motor driver.
- Separate collection motor driver.
- Two propulsion motors.
- One geared collection motor.
- Rechargeable protected battery pack.
- DC-DC voltage regulator.
- Main power switch.
- Fuse and power distribution connections.

The ESP32 coordinates the motor systems using dedicated control signals.

The propulsion and collection mechanisms operate independently.

## 8. Software Architecture

The embedded firmware is responsible for:

- GPIO initialisation.
- BLE communication.
- Command reception and processing.
- Differential motor control.
- PWM-based speed regulation where supported.
- Independent collection motor operation.
- Communication-loss detection.
- Safe motor shutdown.

### Proposed Command Mapping

| Command | Operation |
|---|---|
| F | Forward |
| B | Reverse |
| L | Left |
| R | Right |
| S | Stop propulsion |
| C | Start collection |
| X | Stop collection |

## 9. Safety and Reliability

The design incorporates the following safety requirements:

- Protected electronics enclosure.
- Appropriate battery protection.
- Correctly rated fuse and motor drivers.
- Insulated and secured electrical connections.
- Propeller guards.
- Protected rotating collection mechanism.
- Communication-loss safety stop.
- Hull leakage and buoyancy checks.
- Waterproofing validation before operation.

The system is intended for controlled testing in small water bodies.

## 10. Development Roadmap

| Phase | Development Activity | Status |
|---|---|---|
| 01 | Problem identification and research | In progress |
| 02 | System architecture and product design | Proposed |
| 03 | Component selection and budgeting | Pending |
| 04 | Mechanical fabrication | Pending |
| 05 | Electronics integration | Pending |
| 06 | ESP32 firmware development | Pending |
| 07 | Wireless control implementation | Pending |
| 08 | Mechanical and electrical integration | Pending |
| 09 | Water testing and validation | Pending |
| 10 | Performance evaluation and documentation | Pending |

## 11. Testing and Validation

The completed system will be evaluated through:

- Buoyancy and stability testing.
- Forward and reverse propulsion testing.
- Differential steering testing.
- Collection mechanism performance testing.
- Waste transfer and basket drainage testing.
- Bluetooth communication testing.
- Communication-loss safety testing.
- Continuous operation and leakage testing.

Performance measurements and test results will be documented as they become available.

## 12. Applications

Potential applications include:

- Swimming pools.
- Ornamental ponds.
- Small artificial water bodies.
- Accessible water storage tanks.
- Educational and research water environments.

NEER is not currently designed or validated for open rivers, lakes or industrial waterways.

## 13. Current Limitations

- Designed primarily for lightweight floating solid waste.
- Does not collect submerged debris or dissolved pollutants.
- Navigation is remotely controlled rather than autonomous.
- Collection efficiency depends on debris characteristics and mechanical configuration.
- Performance and operating duration require experimental validation.

## 14. Future Enhancements

Potential future improvements include:

- Autonomous navigation.
- Obstacle detection and avoidance.
- Battery-level monitoring.
- Collection basket fill detection.
- Improved debris collection capacity.
- Solar-assisted charging.
- Advanced waste detection and classification.

These features are outside the scope of the initial implementation.

## 15. Repository Structure

```text
NEER/
│
├── README.md
├── LICENSE
├── CONTRIBUTING.md
│
├── docs/
│   ├── project-overview.md
│   ├── problem-statement.md
│   ├── system-architecture.md
│   ├── working-principle.md
│   ├── mechanical-design.md
│   ├── electrical-design.md
│   ├── software-design.md
│   ├── bill-of-materials.md
│   ├── fabrication-guide.md
│   ├── testing-and-validation.md
│   ├── risk-assessment.md
│   └── development-log.md
│
├── hardware/
│   ├── mechanical/
│   │   ├── drawings/
│   │   ├── cad-models/
│   │   └── fabrication-files/
│   │
│   ├── electronics/
│   │   ├── circuit-diagrams/
│   │   ├── pcb-design/
│   │   └── pinout/
│   │
│   └── bom/
│       └── component-list.csv
│
├── firmware/
│   ├── src/
│   ├── include/
│   ├── lib/
│   └── README.md
│
├── mobile-controller/
│   ├── src/
│   └── README.md
│
├── media/
│   ├── concept-design/
│   ├── cad-renders/
│   ├── fabrication/
│   ├── prototype/
│   └── testing/
│
└── reports/
    ├── design-report/
    ├── test-reports/
    └── final-report/
```

## 16. Project Status

NEER is currently in its initial design and development stage.

The project has an established product concept and preliminary system architecture. Component procurement, detailed mechanical drawings, fabrication, firmware implementation and experimental validation are planned development activities.

This repository will serve as the central technical record of the project's design decisions, implementation, testing and future improvements.

## 17. Acknowledgements

Developed as an embedded robotics and environmental technology project.

---

**NEER — Clean Water. Greener Tomorrow.**
