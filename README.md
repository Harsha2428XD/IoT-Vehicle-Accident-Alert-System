# IoT-Based Real-Time Vehicle Accident Detection and Alert System

An embedded systems project designed to automatically detect vehicle collisions using an accelerometer, retrieve precise geographic coordinates via GPS, and instantly dispatch emergency SMS alerts with a Google Maps tracking link using a GSM module.

## 🛠️ Features
* **Impact Detection:** Utilizes an ADXL335/GY-61 analog accelerometer to monitor high-G deceleration forces.
* **False Alarm Safeguard:** Features an interactive buzzer and a cancel push-button giving the user a 10-second countdown window to abort a false trigger.
* **Precise GPS Tracking:** Captures live latitude and longitude using the NEO-6M GPS module.
* **Cellular Telemetry:** Interfaces with a SIM800L GSM module powered by a 3.7V 18650 battery to broadcast emergency SMS data.
* **Local UI Status:** Displays real-time system status and GPS lock telemetry on an I2C 16x2 LCD screen.

## 🔌 Hardware Circuit Schematic
Here is the complete wiring diagram connecting all peripherals to the Arduino Nano[cite: 1]:

![Circuit Wiring Diagram](assets/accident-alert-wiring.jpg)

### Pin Mapping Overview
* **Arduino Nano & Accelerometer:** X/Y/Z outputs connected to analog pins `A1`, `A2`, `A3`[cite: 1].
* **I2C LCD:** SDA and SCL connected to `A4` and `A5`[cite: 1].
* **NEO-6M GPS:** TX/RX connected to digital pins `D3` and `D2`[cite: 1].
* **SIM800L GSM:** TX/RX connected to digital pins `D5` and `D4`[cite: 1], powered by an external 3.7V 18650 battery[cite: 1].
* **Alert & Control:** Buzzer on `D10`[cite: 1]; Cancel push-button on `D12`[cite: 1].

## 📦 Dependencies & Libraries
Make sure to install the following libraries via the Arduino IDE Library Manager:
* [TinyGPS++](https://github.com/mikalhart/TinyGPSPlus)
* [LiquidCrystal_I2C](https://github.com/marcoschwartz/LiquidCrystal_I2C)

## 🚀 How to Run
1. Clone the repository or download the source files.
2. Open `IoT-Vehicle-Accident-Alert-System.ino` in the Arduino IDE.
3. Select **Arduino Nano** as your board and configure the correct COM port.
4. Upload the firmware to your microcontroller.
