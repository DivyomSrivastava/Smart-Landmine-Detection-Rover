# Smart-Landmine-Detection-Rover

An Arduino-based smart rover that detects buried metallic objects using a custom-built metal detection coil, triggers an immediate buzzer alert, and automatically sends the GPS coordinates of the detected location to the operator's phone as an SMS with a Google Maps link — all without approaching the hazardous area.

## ✨ Features

- Real-time metal detection using a custom-built coil
- Immediate buzzer alert on metal detection
- Automatic GPS location retrieval on detection
- SMS alert with latitude, longitude, and a Google Maps URL
- ESP8266-based wireless data transmission
- Arduino-controlled rover navigation via L298N motor driver
- Fully remote operation — no physical approach required

## 🔩 Components Used

| Component | Quantity |
|---|---|
| Arduino UNO | 1 |
| ESP8266 Wi-Fi Module | 1 |
| GPS Module (Neo-6M) | 1 |
| Metal Detection Coil (Custom-built) | 1 |
| L298N Motor Driver Module | 1 |
| DC Gear Motors | 4 |
| Active Buzzer | 1 |
| Robot Chassis with Wheels | 1 |
| 11.1V Li-ion Battery Pack | 1 |
| Buck Converter (LM2596) | 1 |
| Jumper Wires | As required |

## ⚙️ Working Principle

The custom-built metal detection coil continuously scans the ground as the rover moves across the target area. When a metallic object is detected, the coil sends a signal to the Arduino, which immediately triggers a buzzer alert and activates the GPS module to retrieve the current coordinates.

The ESP8266 module then transmits an SMS to the operator's phone containing the latitude, longitude, and a direct Google Maps link to the detected location. The operator can view the exact detection point on Google Maps without needing to approach the area.

### 🔄 System Architecture

```
        Metal Detection Coil
                │
                ▼
          Arduino UNO
                │
   ┌────────────┼────────────┐
   │            │            │
   ▼            ▼            ▼
Buzzer Alert GPS Module  Motor Driver
                │               │
          Lat & Long      Rover Movement
                │
                ▼
         ESP8266 Module
                │
                ▼
      SMS + Google Maps Link
                │
                ▼
        User's Mobile Phone
```

## 🛠 Methodology

1. Rover is remotely operated across the target area.
2. Metal detection coil continuously scans the ground beneath the rover.
3. On detecting metal → Arduino triggers the buzzer immediately.
4. GPS module retrieves current latitude and longitude.
5. ESP8266 formats the coordinates into a message with a Google Maps URL.
6. SMS is sent to the operator's phone.
7. Operator views the exact location on Google Maps without approaching the area.

## 🔌 Block Diagram

<img width="774" height="713" alt="Screenshot 2026-07-15 224458" src="https://github.com/user-attachments/assets/eec25460-8d17-4def-bcb0-6b43e106df2b" />


The entire system runs on an **11.1V Li-ion battery pack**, stepped down via a buck converter to power the Arduino and logic circuitry. The ESP8266 and GPS module communicate with the Arduino over serial, while the L298N motor driver handles rover movement directly from the 11.1V supply.


## 🤖 Rover Images

<img width="1270" height="600" alt="Screenshot 2026-07-15 223251" src="https://github.com/user-attachments/assets/68c8315a-870f-46d0-9621-4268832699ec" />

<img width="600" height="800" alt="circuit" src="https://github.com/user-attachments/assets/edcb6d24-6b57-4c5d-b320-ba2c0ca18339" />


## 📲 SMS Output Format

```
⚠️ Metal Detected!

Latitude  : 26.4499
Longitude : 80.3319

📍 Location:
https://maps.google.com/?q=26.4499,80.3319
```

## 💻 Software Implementation

The firmware is written in Arduino C++ using the TinyGPS++ library for GPS coordinate parsing and ESP8266 AT commands for wireless SMS transmission.

Key functions:
- `detectMetal()` — reads the coil signal and triggers the buzzer on detection.
- `getLocation()` — parses GPS NMEA data using TinyGPS++ to extract latitude and longitude.
- `sendSMS()` — formats the coordinates and Google Maps URL and transmits the SMS via ESP8266.
- `loop()` — continuously checks for metal detection and triggers the alert + location workflow.

## 🌍 Applications

- Landmine detection simulation and research
- Border surveillance and defense applications
- Hazardous area inspection without human risk
- Embedded systems and IoT education

## 🚀 Future Improvements

- Replace coil-based sensing with Ground Penetrating Radar (GPR)
- Add autonomous navigation using ROS 2
- Integrate obstacle avoidance for fully independent operation
- Live GPS tracking on a real-time web dashboard
- Camera-based remote monitoring
- Solar-powered operation for extended field deployment

## 👥 Team

**Divyom Srivastava** ([LinkedIn](https://www.linkedin.com/in/divyom-srivastava-260b95342/))  


B.Tech – PSIT Kanpur · 2025

⭐ If you found this project useful, consider giving it a star!
