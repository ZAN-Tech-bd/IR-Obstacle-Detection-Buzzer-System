# IR Obstacle Detection Buzzer System

A simple electronic obstacle detection and alert system using an Infrared (IR) Sensor, BC557 PNP transistor, and buzzer.

## 📌 Project Overview

This project detects nearby objects using an Infrared Obstacle Avoidance Sensor. When an object is detected, the sensor activates a BC557 PNP transistor, which turns on the buzzer and produces an alert sound.

The system does not require any Arduino, ESP32, or microcontroller.

## ✨ Features

- Automatic obstacle detection
- Buzzer alert when an object is detected
- No microcontroller required
- Simple and low-cost circuit
- Adjustable IR sensor detection range
- Easy to build on a breadboard

## 🧰 Components Required

| Component | Quantity |
|---|---:|
| Infrared Obstacle Avoidance IR Sensor Module | 1 |
| BC557 PNP Transistor | 1 |
| Active Buzzer | 1 |
| 1kΩ Resistor | 1 |
| Breadboard | 1 |
| Jumper Wires | As required |
| 5V Power Supply | 1 |

## ⚙️ How It Works

1. The IR sensor continuously checks for nearby objects.
2. When an object is detected, the sensor output changes state.
3. The BC557 transistor acts as an electronic switch.
4. The transistor supplies power to the buzzer.
5. The buzzer produces an alert sound.
6. When the object is removed, the buzzer turns off.
