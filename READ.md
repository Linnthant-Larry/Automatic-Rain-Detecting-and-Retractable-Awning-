# Automatic Rain-Detecting and Retractable Awning System

An automated mechatronic roof system built using **Arduino (C++)**, a **PCA9685 servo driver**, and a rain sensor module. Developed as a Bachelor of Engineering (Hons) Final Year Project at Coventry University[cite: 3, 4].

---

##  Project Overview
In tropical environments with frequent and unpredictable rainfall (e.g., Singapore), manual outdoor shade adjustment is inefficient. This project implements a smart, automated awning system featuring:
* **Automatic Rain Detection:** Real-time sensor input triggers motor deployment upon precipitation detection.
* **Manual Override:** A debounced physical switch allows user control when needed.
* **I2C Servo Driver Integration:** Controls multiple servo motors smoothly via a PCA9685 PWM driver with capacitor filtering to prevent voltage jitters.

---

##  System Architecture & Hardware Specs

### Key Hardware
* **Microcontroller:** Arduino UNO R3
* **Sensor:** Analogue/Digital Rain Sensor Module
* **Actuators:** 4x Servo Motors driven via PCA9685 I2C Servo Driver
* **Power Supply:** 5V 5A external power adapter with 16V 470µF decoupling capacitors

### Circuit & Logic Flow
1. **Rain Sensor Input:** Reads precipitation signals via digital/analogue pins.
2. **Debounce Logic:** Switches between automatic mode and manual override with non-blocking edge detection.
3. **Actuation Command:** Communicates over I2C (`SDA`/`SCL`) to the PCA9685 driver to execute precise servo rotations.

---

##  Key Results & Performance
* **Sensor Response Time:** ~0.5 – 0.7 seconds upon moisture contact.
* **Full Deployment Time:** 3.12 seconds average (under structural load).
* **Full Retraction Time:** 2.68 seconds average.
* **Structural FEA Verification:** FEA stress analysis in SolidWorks confirmed all Von Mises stress levels remained below the material yield strengths (6061/6005/6063 Aluminium Alloys & Zincalume) under 25 m/s wind loads[cite: 28, 34, 40, 42].

---

##  Repository Structure
* `/src/`: Contains the complete Arduino C++ code (`awning_control.ino`).
* `/docs/`: Complete Final Year Project Thesis in PDF format.

---

##  Author
**Linn Thant Aung**  
* Graduate Mechanical & Automotive Engineer 
* MSc Automotive Engineering (Coventry University) | BEng (Hons) Mechanical Engineering (First Class) 
