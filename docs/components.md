# Components

This document provides detailed information about the components used in the
**IR Obstacle Detection Buzzer System**.

## 1. Infrared Obstacle Avoidance IR Sensor Module

The IR obstacle sensor is used to detect objects placed in front of the system.

### Pins

| Pin | Connection | Description |
|---|---|---|
| VCC | +5V | Power supply |
| GND | GND | Ground |
| OUT | BC557 Base through 1kΩ resistor | Digital output signal |

### Working

The sensor contains an IR transmitter and an IR receiver.

The IR transmitter emits infrared light. When an object comes in front of the
sensor, the infrared light is reflected from the object and detected by the
receiver.

For many common obstacle avoidance modules:

- No obstacle → OUT is HIGH
- Obstacle detected → OUT is LOW

The onboard potentiometer can be used to adjust the detection sensitivity/range.

---

## 2. BC557 PNP Transistor

The BC557 is a PNP bipolar junction transistor (BJT). In this project, it is
used as an electronic switch to control the buzzer.

### Connections

| BC557 Terminal | Connection |
|---|---|
| Emitter (E) | +5V |
| Base (B) | IR Sensor OUT through 1kΩ resistor |
| Collector (C) | Buzzer positive (+) |

When the IR sensor output becomes LOW, current flows through the base circuit
and the BC557 turns ON.

This allows current to flow through the buzzer.

> **Important:** Always verify the Emitter, Base, and Collector pinout from the
> datasheet of your specific BC557 transistor before connecting it.

---

## 3. Active Buzzer

An active buzzer generates sound when DC voltage is applied.

### Connections

| Buzzer Terminal | Connection |
|---|---|
| Positive (+) | BC557 Collector |
| Negative (-) | GND |

An **active buzzer** is recommended because it contains an internal oscillator
and does not require a PWM or tone signal from a microcontroller.

---

## 4. 1kΩ Resistor

A 1kΩ resistor is connected between the IR sensor output and the base of the
BC557 transistor.

### Connection

IR Sensor OUT → 1kΩ Resistor → BC557 Base

The resistor limits the transistor base current and protects both the sensor
output and transistor.

---

## 5. Breadboard

A breadboard can be used to build and test the circuit without soldering.

It allows the components and jumper wires to be connected easily during
prototyping.

---

## 6. Jumper Wires

Jumper wires are used to make electrical connections between the IR sensor,
transistor, resistor, buzzer, breadboard, and power supply.

---

## 7. 5V Power Supply

The circuit is powered using a regulated 5V DC power source.

Possible power sources include:

- 5V USB supply
- Regulated 5V adapter
- 5V breadboard power supply

All components must share a **common GND**.

---

## Complete Component List

| Component | Quantity | Purpose |
|---|---:|---|
| IR Obstacle Avoidance Sensor | 1 | Detect obstacles |
| BC557 PNP Transistor | 1 | Switch the buzzer |
| Active Buzzer | 1 | Produce alert sound |
| 1kΩ Resistor | 1 | Limit base current |
| Breadboard | 1 | Circuit prototyping |
| Jumper Wires | As required | Electrical connections |
| 5V Power Supply | 1 | Power the circuit |