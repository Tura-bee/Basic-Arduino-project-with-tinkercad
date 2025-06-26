# Ultrasonic Distance Sensor with Arduino (HC-SR04)

This project demonstrates how to use an **HC-SR04 ultrasonic distance sensor** with an **Arduino** to measure distance by sending ultrasonic pulses and timing their echoes.

## 📷 Hardware Used

- Arduino Uno (or compatible board)
- HC-SR04 Ultrasonic Sensor
- Jumper Wires
- Breadboard (optional)

## 🛠️ Circuit Connections

| HC-SR04 Pin | Arduino Pin |
|-------------|-------------|
| VCC         | 5V          |
| GND         | GND         |
| TRIG        | 10          |
| ECHO        | 9           |

> ⚠️ Note: Ensure TRIG and ECHO pins match the definitions in your code.

## 📄 Code Overview

The Arduino sketch:

- Initializes the TRIG and ECHO pins
- Sends a 10-microsecond pulse from the TRIG pin
- Measures the time for the echo to return on the ECHO pin
- Prints the pulse duration and calculated distance to the Serial Monitor

## 🔢 Distance Calculation

The time measured (in microseconds) is converted to distance using:

```cpp
distance_cm = duration * 0.0343 / 2;
