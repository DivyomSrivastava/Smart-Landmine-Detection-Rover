# 🚜 Smart Landmine Detection Rover using Arduino, GPS & ESP8266

<p align="center">

![Arduino](https://img.shields.io/badge/Arduino-UNO-blue?style=for-the-badge)
![ESP8266](https://img.shields.io/badge/ESP8266-WiFi-success?style=for-the-badge)
![GPS](https://img.shields.io/badge/GPS-Neo--6M-red?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

</p>

---

## 📖 Overview

The **Smart Landmine Detection Rover** is an IoT-enabled robotic system developed to simulate the detection of buried landmines using a **custom-built metal detection coil**. The project combines **embedded systems, robotics, GPS positioning, and wireless communication** to identify metallic objects and instantly notify the user with the exact location.

Whenever the rover detects a metallic object, the system activates a buzzer, retrieves the current GPS coordinates, and sends the location to the user's mobile phone as an **SMS containing the latitude, longitude, and a Google Maps link**. This enables remote identification of potentially hazardous locations without requiring a person to approach the area.

This project was developed as part of our college exhibition to demonstrate how low-cost embedded systems can be integrated into practical safety and defense-oriented applications.

---

## 📷 Project Preview

<p align="center">
<img src="Images/Rover.jpg" width="700">
</p>

---

# ✨ Features

- 🚜 Remote controlled rover
- 🔍 Custom-built metal detection coil
- 📍 Real-time GPS location tracking
- 📲 Automatic SMS notification
- 🌍 Google Maps location sharing
- 🔊 Instant buzzer alert on metal detection
- ⚡ Arduino-based embedded system
- 📡 Wireless communication using ESP8266

---

# 🛠 Hardware Used

| Component | Quantity |
|------------|----------|
| Arduino UNO | 1 |
| ESP8266 Wi-Fi Module | 1 |
| GPS Module (Neo-6M) | 1 |
| L298N Motor Driver | 1 |
| Custom Metal Detection Coil | 1 |
| Buzzer | 1 |
| DC Motors | 4 |
| Robot Chassis | 1 |
| Wheels | 4 |
| Battery Pack | 1 |

---

# 💻 Software Used

- Arduino IDE
- Embedded C
- TinyGPS++ Library
- ESP8266 Library

---

# ⚙ Working Principle

1. The rover is remotely driven across the target area.

2. The custom-built metal detection coil continuously scans the ground for metallic objects.

3. Once a metallic object is detected, the buzzer immediately generates an alert.

4. The detection event activates the GPS module to obtain the current latitude and longitude.

5. The ESP8266 module processes the GPS data.

6. An SMS containing the GPS coordinates along with a Google Maps URL is automatically sent to the user's mobile phone.

7. Opening the Google Maps link displays the exact detected location.

---

# 🔄 System Architecture

```
                 Metal Detection Coil
                         │
                         ▼
                  Arduino UNO
                         │
        ┌────────────────┼────────────────┐
        │                │                │
        ▼                ▼                ▼
    Buzzer Alert      GPS Module      Motor Driver
        │                │                │
        │         Latitude & Longitude   │
        │                │                │
        └──────────────┬─┘                │
                       ▼                  ▼
                  ESP8266 Module      Rover Movement
                       │
                       ▼
              SMS + Google Maps Link
                       │
                       ▼
                  User's Mobile Phone
```

---

# 🔌 Circuit Diagram

<p align="center">
<img src="Images/Circuit_Diagram.png" width="900">
</p>

---

# 🔗 Hardware Connections

| Arduino Pin | Connected Device |
|--------------|-----------------|
| D2 | Metal Detection Coil |
| D3 | Buzzer |
| D4 | GPS TX |
| D5 | GPS RX |
| D6 | ESP8266 TX |
| D7 | ESP8266 RX |
| D8 | L298N IN1 |
| D9 | L298N IN2 |
| D10 | L298N IN3 |
| D11 | L298N IN4 |
| 5V | GPS Module |
| GND | Common Ground |

---

# 📲 SMS Output

Example message received after detecting a metallic object:

```
⚠ Metal Detected!

Latitude : 26.44991

Longitude : 80.33162

Google Maps

https://maps.google.com/?q=26.44991,80.33162
```

---

# 📸 Project Gallery

## 🔧 Internal Electronics

<p align="center">
<img src="Images/Circuit.jpg" width="700">
</p>

---

## 🚜 Final Rover

<p align="center">
<img src="Images/Rover.jpg" width="700">
</p>

---

## 👨‍💻 Team Presentation

<p align="center">
<img src="Images/Team.jpg" width="700">
</p>

---

# 🌍 Applications

- Landmine Detection Research
- Hazardous Area Monitoring
- Defense Demonstrations
- Metal Object Detection
- Robotics Education
- Embedded Systems Projects

---

# 🚀 Future Scope

- Autonomous Navigation using ROS 2
- Camera Integration
- AI-based Object Classification
- Live Cloud Dashboard
- Mobile Application Integration
- Solar Powered Operation
- Improved Metal Detection Range




# ⭐ Acknowledgements

We sincerely thank our faculty mentors and the Department of Computer Science & Engineering at **PSIT Kanpur** for their continuous guidance and encouragement throughout the development and presentation of this project.

---

## 📬 Connect With Me

**Divyom Srivastava**

- 💼 LinkedIn: *(https://www.linkedin.com/in/divyom-srivastava-260b95342/)*
---

### ⭐ If you found this project interesting, don't forget to star the repository!
