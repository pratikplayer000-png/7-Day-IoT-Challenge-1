# 7-Day IoT & Electronics Challenge - Day 1: 5V Regulated Power Supply with Switch

## 📌 Project Overview
This project is Day 1 of a 7-day hardware and IoT learning track. It demonstrates how to build a clean, stable **5V DC regulated power supply** from a 9V battery using an **LM7805 Linear Voltage Regulator**, **ceramic decoupling capacitors**, and a **tactile push button power switch**.

This power supply rail will be used to power 5V components (servos, relays, ICs) alongside a 3.3V NodeMCU ESP8266 microcontroller.

---

## 🛠️ Hardware Components
* **1x** LM7805 Voltage Regulator (TO-220 package)
* **1x** 9V Battery with connector clip
* **1x** Push Button Switch (Power Control)
* **1x** 0.33 µF Ceramic Capacitor (Input filter)
* **1x** 0.1 µF Ceramic Capacitor (Output decoupling filter)
* **1x** 220 Ω Resistor
* **1x** Green LED (Power indicator)
* **1x** Breadboard & Jumper Wires

---

## ⚡ Circuit Schematic & Connections

### LM7805 Pinout Configuration
1. **Pin 1 (Left) - Input ($V_{IN}$):** Accepts raw +9V DC from battery through the switch.
2. **Pin 2 (Center) - Ground ($GND$):** Common system ground reference.
3. **Pin 3 (Right) - Output ($V_{OUT}$):** Regulated +5V DC output.

### Features & Modifications
* **Power Switch:** Added a push-button switch in series with the power rail, allowing convenient toggling of power without disconnecting the battery.
* **Filtering:** Ceramic capacitors placed close to input and output pins filter out voltage spikes and unwanted noise.

---

## 📷 Circuit Setup
![5V Power Supply Circuit](WhatsApp Image 2026-09-14 at 9.15.06 PM.jpg)

---

## 🔬 Verification
* Pressing the power switch engages the 5V line, immediately turning on the Green indicator LED.
* Checked board voltages and regulator surface temperature to confirm safe operation.
