# Design of a Bluetooth-Controlled Four-Wheel Electric Vehicle Using ESP32 and Joystick

An embedded systems project that designs and implements a **Bluetooth-controlled four-wheel electric vehicle** using **ESP32**, a **joystick controller**, and an **L298N motor driver**. The system enables real-time remote navigation, allowing the vehicle to move forward, backward, turn left, turn right, and rotate with low latency and reliable wireless communication.

The project demonstrates the integration of embedded hardware, Bluetooth communication, motor control algorithms, and mobile robotics for educational and research purposes.

---

# 🌟 Project Highlights

The project combines embedded systems and wireless communication technologies to build a low-cost remote-controlled mobile robot.

### Key Features

* Bluetooth-based wireless control
* ESP32 microcontroller
* Dual ESP32 architecture (Client & Server)
* Real-time joystick control
* Four-wheel differential drive
* Compact and lightweight vehicle design
* Low power consumption
* Low-cost implementation

---

# 🚗 System Overview

The system consists of two ESP32 boards communicating through Bluetooth.

```text
Joystick
     │
     ▼
ESP32 Client
     │
 Bluetooth
     │
     ▼
ESP32 Server
     │
     ▼
L298N Motor Driver
     │
     ▼
DC Motors
     │
     ▼
4-Wheel Electric Vehicle
```

The client reads joystick inputs and sends movement commands via Bluetooth. The server receives the commands, processes them, and drives the motors through the L298N motor driver.

---

# 🎯 Project Objectives

The project aims to design a compact four-wheel robotic vehicle capable of stable wireless navigation.

The objectives include:

* Develop a reliable Bluetooth communication system
* Implement joystick-based remote control
* Design a robust four-wheel chassis
* Build a stable motor control system
* Minimize manufacturing cost and power consumption
* Achieve responsive vehicle navigation within a communication range of approximately **10 meters**

---

# ⚙️ Technical Specifications

| Specification             | Value                                       |
| ------------------------- | ------------------------------------------- |
| Microcontroller           | ESP32                                       |
| Communication             | Bluetooth 2.4 GHz (Bluetooth v2.0 Protocol) |
| Motor Driver              | L298N                                       |
| Input Voltage             | 7–12 VDC                                    |
| Logic Level               | 3.3V / 5V TTL Compatible                    |
| Maximum Dimensions        | 30 × 20 × 10 cm                             |
| Wheel Diameter            | 5 cm                                        |
| Communication Range       | ~10 meters                                  |
| Typical Bluetooth Current | 8 mA                                        |

---

# 🔧 Hardware Components

* ESP32 Development Board (Client)
* ESP32 Development Board (Server)
* Bluetooth Module (Integrated ESP32 Bluetooth)
* L298N Motor Driver
* DC Motors
* Four-Wheel Chassis
* Analog Joystick Module
* Power Supply (7–12V DC)

---

# 🧩 Software Architecture

The software is divided into two independent applications.

## ESP32 Client

Responsible for

* Reading joystick inputs
* Detecting movement directions
* Establishing Bluetooth connection
* Transmitting control commands

---

## ESP32 Server

Responsible for

* Receiving Bluetooth commands
* Processing movement instructions
* Controlling motor directions
* Driving the L298N motor driver

---

## Motor Control Logic

The implemented control algorithm supports:

* Forward
* Backward
* Left Turn
* Right Turn
* Rotate Left
* Rotate Right
* Stop

The Bluetooth callback function (`btCallback()`) handles communication events, while the main loop continuously processes incoming commands and updates the motor outputs.

---

# 📂 Project Structure

```text
├── ESP32_Client/
│   ├── ESP32_Client/
│   └── ESP32_Client.ino      # Joystick transmitter firmware
│
├── ESP32_Server/
│   └── ESP32_Server.ino      # Vehicle controller firmware
│
├── README.md
├── LICENSE
├── Video_BTL_Nhung_L01.mp4   # Demonstration video
└── Thesis_Report.pdf         # Project report
```

---

# 🚀 Getting Started

## Hardware Setup

1. Assemble the four-wheel vehicle chassis.
2. Connect the L298N motor driver to the ESP32 Server.
3. Connect the joystick module to the ESP32 Client.
4. Power both ESP32 boards.
5. Pair the devices via Bluetooth.

---

## Software Installation

Clone the repository

```bash
git clone <repository_url>
```

Open the corresponding Arduino sketches:

```text
ESP32_Client/ESP32_Client.ino
ESP32_Server/ESP32_Server.ino
```

Compile and upload each sketch to its respective ESP32 development board using the Arduino IDE.

---

# 🧪 Experimental Evaluation

The prototype was evaluated based on the following criteria:

* Bluetooth communication stability
* Joystick responsiveness
* Vehicle maneuverability
* Direction control accuracy
* Power consumption
* Wireless operating distance

The developed vehicle successfully demonstrated stable operation under indoor conditions with a communication distance of approximately **10 meters**.

---

# 🔮 Future Improvements

* [ ] Mobile application control (Android/iOS)
* [ ] Wi-Fi remote control
* [ ] Camera-based FPV streaming
* [ ] Obstacle avoidance using ultrasonic sensors
* [ ] Line-following capability
* [ ] Autonomous navigation
* [ ] PID speed control
* [ ] Battery monitoring system
* [ ] ROS integration
* [ ] ESP-NOW communication

---

# 📚 References

1. Hồ Chí Minh City University of Technology. *Embedded System Design*. 2016.

2. Microchip Technology. *ATmega328P 8-bit AVR Microcontroller Datasheet*. https://ww1.microchip.com/downloads/en/DeviceDoc/Atmel-7810-Automotive-Microcontrollers-ATmega328P_Datasheet.pdf

3. Arduino. *Arduino Nano User Manual*. https://www.arduino.cc/

4. Espressif Systems. *ESP32-WROOM-32 Datasheet*. 2018.

5. Espressif Systems. *ESP32 DevKitC V4 Schematic*.

6. Arduino Việt Nam. *H-Bridge Motor Control Using SN754410*. http://arduino.vn/bai-viet/281-mach-cau-h-va-dieu-khien-dong-co-voi-sn754410

7. STMicroelectronics. *L298N Dual Full-Bridge Driver Datasheet*. https://www.st.com/

8. Bluetooth SIG. *Bluetooth Technology Overview*. https://www.bluetooth.com/learn-about-bluetooth/tech-overview/

---

# 📄 License

This project was developed for **educational**, **research**, and **embedded systems learning** purposes. It demonstrates Bluetooth-based wireless control of a four-wheel robotic vehicle using ESP32 and embedded motor control techniques.
