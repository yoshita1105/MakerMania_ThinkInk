# MAKERMANIA 2026 | ThinkInk
## Innovation Project Workbook

> Program Duration: 1 June 2026 – 4 July 2026
>
> Location: MBF Tinkerers' Lab 007
>
> Team Size: 3–5 Students
>
> Goal: Identify a real-world problem and develop an innovative, patentable, and implementable solution.

---

# 1. Team Identity

## 1.1 Team Name and Photo
ThinkInk

<img width="1600" height="1131" alt="image" src="images/Team Members.jpeg" />

---

## 1.2 Team Members

| Name | Role | Year/Branch |
| ---- | ---- | ------ |
|Yoshita Vishwakarma     |      |2nd Year - AURO        |
|Tejasva Chaudhary      |      |2nd - ECS        |
|Vishal Gupta      |      |1st - EXTC        |

Useless product video link : https://youtu.be/rLFXh65uxHs?si=dfBaRAERnktvgRVW
---

# 2. Problem Discovery

## 2.1 Observation Area

Where did you conduct your observations?

* Hostel
* Canteen
* Workshop
* Hospital
* Public Transport
* Home
* Other

---

## 2.2 AEIOU Observation Sheet

### Activities

What are users doing?

Users actively move around outdoor play areas, aiming and shooting opponents using laser guns. They take cover, strategize with teammates, and monitor their health and game status through the wristband during gameplay.

### Environment

What conditions affect them?

The game can be played in both indoor and outdoor environments such as halls, playgrounds, parks, and open fields. Factors like lighting conditions, obstacles, available space, weather, and terrain can influence gameplay, player movement, and sensor performance.

### Interactions

Who or what are they interacting with?

Players interact with teammates, opponents, laser guns, sensor vests, and wristbands throughout the game. They also use surrounding obstacles strategically to hide, defend, and attack.

### Objects

What tools or products are used?

The system consists of a smart laser gun, sensor-equipped vest, wristband display, ESP32 microcontrollers, batteries, and protective eyewear. These components work together to detect hits, track scores, and provide player feedback.

### Users

Who are the primary users?

The primary users are students, teenagers, gaming enthusiasts, and participants in outdoor recreational activities. The system is designed for individuals who enjoy competitive, team-based, and physically engaging games.

---

## 2.3 Observation Log

| Observation | Evidence | Pain Point |
| ----------- | -------- | ---------- |
|             |          |            |
|             |          |            |

---

# 3. User Research

## 3.1 Interview Summary

Number of users interviewed: ______

## 3.2 Key Quotes

1.

2.

3.

---

## 3.3 User Persona

### Name

### Age

### Occupation

### Goals

### Frustrations

### Needs

---

# 4. Problem Framing

## Problem Statement

User __________ needs a way to __________ because __________.

---

## How Might We Questions

1.

2.

3.

---

## Opportunity Ranking

| Criteria         | Score |
| ---------------- | ----- |
| Severity         |       |
| Frequency        |       |
| Feasibility      |       |
| Novelty          |       |
| Market Potential |       |
| Total            |       |

---
## 5. Solution Ideation

## Brainstormed Ideas

| Idea                                     | Advantages                                        | Challenges                                   |
| ---------------------------------------- | ------------------------------------------------- | -------------------------------------------- |
| IR-Based Laser Tag System                | Low cost, easy implementation                     | Sensitive to ambient IR interference         |
| Camera-Based Hit Detection               | High accuracy                                     | Expensive and computationally intensive      |
| RFID-Based Health & Power-Up System      | Easy player identification and game customization | Requires RFID integration                    |
| Visible Laser + Optical Sensor Detection | Realistic gameplay, visible shooting effects      | Requires accurate filtering of ambient light |

---

## Selected Concept

**Visible Laser-Based Smart Laser Tag System with RFID Integration**

### Why was this concept chosen?

The selected concept provides an immersive laser tag experience while remaining affordable and easy to manufacture. The system combines visible laser hit detection using optical sensors with RFID-based player identification and power-up functionality. It offers real-time health tracking, wireless communication, visual feedback, and long battery life, making it suitable for both recreational and educational applications.

---

# 6. System Design

## High-Level Description

The project consists of two main units:

1. **Laser Gun (Transmitter Unit)**

   * Fires a visible laser beam when the trigger is pressed.
   * Sends shooting data wirelessly using ESP-NOW communication.

2. **Player Wristband (Receiver Unit)**

   * Detects laser hits using optical sensors.
   * Identifies players using RFID cards/tags.
   * Tracks health points.
   * Displays health status on an OLED screen.
   * Activates vibration feedback when hit.
   * Communicates game data wirelessly.

When a player is hit, the wristband decreases health points and provides visual and vibration feedback. RFID cards can be used for player registration, health boosts, or special game modes.

---

## Block Diagram

Laser Trigger → ESP32 Transmitter → Laser Module

↓

Visible Laser Beam

↓

Optical Sensor (TCS34725) → ESP32 Receiver → Health Processing

↓

OLED Display + Vibration Motor + ESP-NOW Communication

↓

RFID Reader → Player Identification / Power-Ups

---

## Inputs

* Trigger Button
* TCS34725 Color Sensor (Laser Detection)
* RFID Reader
* RFID Tags/Cards
* Battery Status Data

---

## Outputs

* OLED Display (Health Points, Status)
* Vibration Motor (Hit Feedback)
* LED Indicators
* Wireless ESP-NOW Data Transmission
* Game Statistics

---

# 7. Technical Planning

## Electronics

| Component                     | Purpose                         |
| ----------------------------- | ------------------------------- |
| ESP32-C3 Super Mini           | Main controller                 |
| TCS34725 Sensor               | Laser hit detection             |
| RFID Reader Module            | Player identification           |
| RFID Tags/Cards               | Player ID and power-ups         |
| OLED Display (128x64)         | Health and status display       |
| Coin Vibration Motor          | Hit feedback                    |
| Laser Module                  | Shooting mechanism              |
| Li-Po Battery (1200–1500 mAh) | Portable power source           |
| TP4056 Charging Module        | Battery charging and protection |
| LEDs                          | Visual indicators               |
| Push Buttons                  | Trigger and controls            |

---

## Software

| Tool                     | Purpose                |
| ------------------------ | ---------------------- |
| Arduino IDE              | Firmware development   |
| ESP-NOW Protocol         | Wireless communication |
| Adafruit GFX Library     | OLED graphics          |
| Adafruit SSD1306 Library | OLED display control   |
| RFID Library             | RFID communication     |
| EasyEDA/Fritzing         | Circuit design         |
| Fusion 360               | 3D CAD modeling        |

---

## Mechanical / CAD

The wristband contains a custom-designed circular sensor patch with:

* Outer Diameter: 60 mm
* Inner Diameter: 50 mm
* TCS34725 sensor mounted at the center
* Translucent diffusion film for improved laser detection
* Integrated LED ring around the perimeter
* Internal supports for sensor mounting
* Cable routing channels for electronics connections
* Lightweight wearable enclosure designed using CAD and 3D printing

---

# 8. Prototype Development

## Version 1


https://github.com/user-attachments/assets/563d130e-1305-47c8-bd2d-03f9c2435ef3



https://github.com/user-attachments/assets/354fc109-a8ec-4b6e-959a-7027e6643bb9


<video src="videos/Video1.mp4" controls width="700"></video>




### Description

The first prototype consisted of an ESP32-C3 based receiver connected to a TCS34725 optical sensor and OLED display. Initial testing focused on detecting laser light under different ambient lighting conditions. Health values were displayed on the OLED, and vibration feedback was implemented for hit indication.

### Lessons Learned

* Ambient light significantly affects sensor readings.
* A translucent diffusion film improves laser detection reliability.
* OLED display provides effective real-time feedback.
* ESP-NOW communication enables low-latency wireless gameplay.
* Proper sensor shielding improves detection accuracy.
* Battery-powered operation requires efficient power management for extended gameplay duration.

---

## Version 2

Description:

Lessons Learned:

---

## Final Prototype

Description:

---

# 9. Testing & Validation

## Testing Plan

| Test | Success Criteria |
| ---- | ---------------- |
|      |                  |
|      |                  |

---

## User Feedback

| User | Feedback | Action Taken |
| ---- | -------- | ------------ |
|      |          |              |

---

# 10. Innovation Assessment

## Existing Solutions

List competing products.

---

## What Makes This Different?

---

## Innovation Score

| Parameter       | Score |
| --------------- | ----- |
| Novelty         |       |
| Technical Depth |       |
| Feasibility     |       |
| Impact          |       |
| Scalability     |       |

---

# 11. Intellectual Property

## Prior Art Search

Patents / Products Found:

---

## Novel Features

1.

2.

3.

---

## Provisional Patent Draft

### Title

### Abstract

### Problem

### Solution

### Claims

---

# 12. Business & Deployment

## Target Users

---

## Estimated Cost

---

## Market Opportunity

---

## Sustainability Considerations

---

# 13. Final Demonstration

## Prototype Images

Insert photos.

---

## Demonstration Video Link

---

## GitHub Repository

---

## Presentation Link

---

# 14. Reflection

## What Worked Well?

---

## What Failed?

---

## Key Learnings

---

## Next Steps

* Patent Filing
* Startup Exploration
* Product Development
* Research Publication
* Competition Submission

---

# 15. Final Deliverables Checklist

* Problem Discovery Complete
* User Interviews Complete
* Persona Created
* Problem Statement Finalized
* System Design Complete
* Prototype Demonstrated
* Testing Completed
* Patent Draft Prepared
* Presentation Submitted
* GitHub Repository Updated

---

# MAKERMANIA FINAL PITCH

Each team will present:

1. Problem
2. User Research
3. Insights
4. Solution
5. Prototype Demo
6. Innovation & Patentability
7. Future Roadmap

Presentation Time: 5 Minutes

Q&A: 3 Minutes
