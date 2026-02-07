# Hexapod Robotics Platform

## Overview

This project is a large-scale 24-servo hexapod robotic platform designed to study multi-actuator coordination, power distribution, and locomotion control in high-DOF walking robots.

Built as a long-term experimental system, the platform focuses on solving real engineering challenges involved in synchronizing large numbers of servos under load while maintaining stable power delivery and structural integrity.

The project is currently in the hardware-complete, software-development phase, with gait programming and coordinated motion control under active development.

---

## Key Specifications

| Parameter          | Value                                                 |
| ------------------ | ----------------------------------------------------- |
| Total Actuators    | 24 servos                                             |
| Degrees of Freedom | 18+ DOF locomotion system                             |
| Leg DOF            | 3 per leg (+ base joints)                             |
| Structure          | ABS 3D printed (40% infill)                           |
| Controller         | Arduino Mega                                          |
| Servo Type         | MG996R metal gear                                     |
| Size               | ~42 × 35 cm                                           |
| Status             | Hardware complete, locomotion software in development |

---

# Why this project exists

Most small robotics projects use only a few actuators and avoid complex coordination problems.

This platform was built to explore:

* Multi-servo synchronization at scale
* Power delivery for 20+ actuators
* Mechanical load distribution
* Gait programming fundamentals
* Future autonomous walking systems

The goal is to develop a **stable and scalable locomotion platform** capable of evolving toward autonomous multi-legged robotics.

---

# Mechanical Architecture

## Structure

* Full ABS 3D printed body
* 40% infill for strength-to-weight balance
* Dual-color structural segmentation
* Reinforced joints using brass heat-set inserts
* M3 hardware throughout

Each leg uses a multi-link articulated design for realistic walking motion.

## DOF Configuration

* 6 legs
* 3 primary DOF per leg
* Additional base articulation
* Total: 24 servo actuators

This enables full multi-axis locomotion capability once gait control is implemented.

---

# Actuation System

* 24 × MG996R metal gear servos
* High torque hobby servo architecture
* Uniform actuator selection simplifies control mapping
* Metal gear trains for durability under load

The system is intentionally built at scale to study real multi-servo behavior.

---

# Power Architecture (Critical Design Area)

High servo count systems fail primarily due to unstable power delivery.

This platform uses:

## Development Power

* External regulated variable bench supply
* Stable high-current output
* Used during testing and calibration

## Final Power Plan

* 3S LiPo (11.1V, 4500mAh, 50C)
* 200W buck converter
* Dedicated 5–6V high-current servo rail

## Distribution

Custom high-current servo distribution PCB:

* Handles 24 servos simultaneously
* Bulk capacitors for surge handling
* Wide power traces
* Eliminates wiring complexity
* Prevents brownouts and voltage sag

This PCB solved major multi-servo stability issues typical in large hexapods.

---

# Control Architecture

## Current Stage

Hardware complete
Control software not yet implemented

Planned development approach:

* Begin with pre-programmed gait sequences
* Gradual multi-leg synchronization
* Stability testing
* Smooth motion profiling
* Advanced gait experimentation

Development intentionally staged to avoid instability in large multi-actuator systems.

---

# Engineering Challenges Solved

### Multi-Servo Wiring Complexity

Traditional PCA9685-based wiring becomes unmanageable beyond ~12 servos.

Solution:
Custom stacked servo control PCB enabling clean routing and stable connections for all 24 servos.

### Power Stability

Large servo arrays cause:

* Voltage drop
* Reset loops
* Brownouts

High-current regulated supply + distribution PCB eliminated these risks during testing.

---

# Current Status

✔ Mechanical structure complete
✔ All 24 servos installed
✔ Power distribution system validated
✔ Control hardware ready

 Locomotion control software in development
 Gait programming phase pending

---

# Future Development

## Short Term

* Basic walking gait implementation
* Multi-leg synchronization
* Stability testing
* Current draw analysis

## Mid Term

* Advanced gait patterns
* Smooth trajectory motion
* Battery-powered untethered operation

## Long Term Vision

* Autonomous navigation
* Sensor integration
* Terrain adaptation
* Vision-assisted locomotion

---

# Why this project matters

Large multi-actuator robots introduce engineering challenges not seen in small hobby systems:

* Power integrity at scale
* Multi-servo coordination
* Structural load distribution
* Gait mathematics
* Stability under motion

This platform serves as a foundation for exploring these problems in a real hardware environment.
