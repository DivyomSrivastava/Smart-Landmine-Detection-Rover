# Smart-Landmine-Detection-Rover

An Arduino-based smart rover that detects metallic objects using a custom-built metal detection coil and automatically shares the detected location via GPS and ESP8266 as an SMS with a Google Maps link.

---

## ✨ Features

- Real-time metal detection using a custom-built coil
- Immediate buzzer alert on metal detection
- GPS location retrieval on detection
- SMS alert with latitude, longitude, and Google Maps URL
- Fully remote operation — no physical approach needed

## Components Used

| Component | Quantity |
|---|---|
| Arduino UNO | 1 |
| ESP8266 Wi-Fi Module | 1 |
| GPS Module (Neo-6M) | 1 |
| Metal Detection Coil (Custom-built) | 1 |
| L298N Motor Driver | 1 |
| DC Gear Motors | 4 |
| Active Buzzer | 1 |
| Robot Chassis + Wheels | 1 |
| 11.1V Li-ion Battery Pack | 1 |
| Buck Converter (LM2596) | 1 |
| Jumper Wires | As required |

## ⚙️ Working Principle

The rover is remotely operated across a target area while the metal detection coil continuously scans the ground. When a metallic object is detected, the Arduino triggers a buzzer and activates the GPS module to retrieve the current coordinates. The ESP8266 then sends an SMS to the operator's phone containing the latitude, longitude, and a direct Google Maps link to the detected location.

### System Flow

```
Metal Detection Coil
        │
        ▼
  Buzzer Alert
        │
        ▼
  GPS retrieves coordinates
        │
        ▼
  ESP8266 sends SMS
        │
        ▼
  User views location on Google Maps
```

## 🛠 Methodology

1. Rover scans the area remotely via motor control.
2. Detection coil signals the Arduino when metal is detected.
3. Arduino triggers buzzer and reads GPS coordinates.
4. ESP8266 formats and sends SMS with a Google Maps link.
5. Operator views the exact detection location on their phone.

## 🔌 Circuit Diagram

*(Add circuit diagram image here)*

## 📷 Project Images

*(Add rover and team images here)*

## 💻 Software Implementation

Written in Arduino C++ using the TinyGPS++ library for GPS parsing and ESP8266 AT commands for wireless SMS transmission. Core logic handles detection signal reading, coordinate extraction, message formatting, and transmission.

## 🌍 Applications

- Landmine detection simulation and research
- Hazardous area inspection
- Defense and border surveillance
- Embedded systems and IoT education

## 🚀 Future Improvements

- Replace coil with Ground Penetrating Radar (GPR)
- Add autonomous navigation and obstacle avoidance
- Live GPS tracking on a web dashboard
- Camera-based remote monitoring


