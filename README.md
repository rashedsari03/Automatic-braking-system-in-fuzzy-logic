[Illustration]([automatic braking system.jpg](https://github.com/rashedsari03/Automatic-braking-system-in-fuzzy-logic/blob/a0910d4807085374ecef95e4b03ece21fac98618/automatic%20braking%20system.jpg))
---

# Automatic Braking System Using Fuzzy Logic

## Table of Contents
1. [Introduction](#introduction)
2. [Overview](#overview)
3. [Fuzzy Logic Components](#fuzzy-logic-components)
    - [Inputs](#inputs)
    - [Fuzzy Inference Engine](#fuzzy-inference-engine)
    - [Rule Base](#rule-base)
    - [Defuzzification](#defuzzification)
4. [Advantages](#advantages)
5. [Example Scenario](#example-scenario)
6. [Conclusion](#conclusion)
7. [Libraries and Tools Used](#libraries-and-tools-used)

---

## Introduction
This project demonstrates the use of **fuzzy logic** in an **Automatic Braking System (ABS)**, which aims to improve vehicle safety by applying brakes based on real-time inputs like speed and distance to obstacles. Fuzzy logic provides a human-like reasoning process for decision-making in complex environments.

## Overview
The Automatic Braking System receives sensor data such as vehicle speed, distance to an obstacle, and relative velocity, and uses fuzzy logic to calculate the appropriate braking force. This allows the system to handle uncertain and imprecise inputs more effectively than traditional binary decision systems.

## Fuzzy Logic Components

### Inputs
The system takes the following inputs, which are converted into fuzzy sets:
- **Distance to Obstacle**: The distance between the vehicle and an obstacle (e.g., "Close," "Medium," "Far").
- **Vehicle Speed**: The current speed of the vehicle (e.g., "Slow," "Moderate," "Fast").
- **Relative Velocity**: The speed at which the vehicle is approaching an obstacle.

### Fuzzy Inference Engine
The fuzzy inference engine applies a set of **IF-THEN rules** to the fuzzy inputs to determine the level of braking force. Example rules include:
- IF the distance is "Close" AND the speed is "Fast", THEN apply "High Braking Force".
- IF the distance is "Far" AND the speed is "Slow", THEN apply "No Braking".

### Rule Base
The **rule base** contains the full set of rules that define how the system should behave based on different input conditions. These rules are designed to ensure safe and smooth braking in various scenarios.

### Defuzzification
Once the fuzzy rules are processed, the fuzzy output (e.g., "Strong Brake", "Moderate Brake") is converted into a precise braking force. This is done using a **defuzzification method**, such as the centroid or weighted average, resulting in a crisp braking value (e.g., 70% braking force).

## Advantages
- **Handles Uncertainty**: Fuzzy logic is well-suited for environments where sensor data is imprecise or uncertain.
- **Smooth Control**: Braking force is applied gradually based on fuzzy decisions, providing smoother vehicle control.
- **Human-Like Decision Making**: The system mimics human reasoning, leading to intuitive and adaptive braking.

## Example Scenario

1. **Fuzzification**: 
   - Distance to obstacle: 4 meters (fuzzy term: "Close").
   - Vehicle speed: 90 km/h (fuzzy term: "Fast").

2. **Rule Evaluation**: 
   - Based on predefined rules, the system determines that a "Close" distance and "Fast" speed require a "Strong Brake."

3. **Defuzzification**: 
   - The fuzzy output "Strong Brake" is converted into a precise braking force, such as 85% of the maximum brake power.

4. **Braking Output**: 
   - The system applies 85% of the brake force to slow the vehicle and avoid a collision.

## Conclusion
Fuzzy logic provides a flexible and reliable approach to building an automatic braking system that can handle real-world uncertainty. By combining sensor inputs with human-like decision-making, the system enhances vehicle safety and reduces the risk of collisions.

## Libraries and Tools Used
- **Python**
- **Fuzzy Logic Toolbox** (for simulation and implementation)
- **NumPy** (for numerical computations)
- **Matplotlib** (for visualizing results)

---
