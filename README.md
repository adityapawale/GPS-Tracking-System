# GPS-Tracking-System
# 📍 GPS Tracking System using ESP8266 and GPS Module

This project is a real-time GPS tracking system using the **ESP8266 (NodeMCU)** and a **GPS module** (such as NEO-6M). The system reads GPS data and can send it to a web server, cloud service, or display it on a serial monitor for live location tracking.

---

## 🚀 Features

- 📡 Real-time GPS data (latitude, longitude, speed, time)
- 🌐 ESP8266 sends GPS data over WiFi to a web server or cloud
- 🔋 Portable and low-power design using a rechargeable battery
- 💬 Simple serial monitor output for debugging and testing
- 🧩 Easy to expand with IoT platforms (like Firebase, Thingspeak, Blynk, etc.)

---

## 🧰 Hardware Components

| Component              | Purpose                            |
|-----------------------|------------------------------------|
| ESP8266 (NodeMCU)      | WiFi-enabled microcontroller       |
| GPS Module (NEO-6M)    | Provides location data             |
| Battery (Li-ion/Li-Po) | Portable power                     |
| TP4056 Module          | Battery charging circuit (optional)|
| Connecting wires       | Hardware connections               |

---

## ⚙️ Wiring Connections

| GPS Module | ESP8266 |
|------------|---------|
| VCC        | 3.3V or 5V (via external supply) |
| GND        | GND     |
| TX         | GPIO3 (RX) |
| RX         | GPIO1 (TX) *(optional, use SoftwareSerial)* |

> ⚠️ **Tip:** Use `SoftwareSerial` to avoid interfering with default serial debugging pins.

---

## 📦 Libraries Required

Install the following libraries in Arduino IDE:

- [`TinyGPS++`](https://github.com/mikalhart/TinyGPSPlus) – for parsing GPS data  
- [`SoftwareSerial`](https://www.arduino.cc/en/Reference/softwareSerial) – for serial communication with GPS  
- `ESP8266WiFi.h` – for connecting to WiFi  
- `ESP8266HTTPClient.h` – to send HTTP requests (if needed)

---

## 💻 Sample Output (Serial Monitor)

```text
Latitude: 18.5204
Longitude: 73.8567
Speed: 0.54 km/h
Date: 12/05/2025
Time: 12:45:30
