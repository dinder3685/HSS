# 🎯 STNM PTU System (Pan-Tilt Unit)

A modular embedded system for controlling a **Pan-Tilt Unit (PTU)** using Arduino.

---

## 🚀 Features

- Custom UART communication protocol
- CRC16 data verification
- Stepper motor control (Pan & Tilt)
- Telemetry and ACK system
- Modular embedded architecture

---

## 🧠 System Overview

```
Jetson / PC
     │
     ▼
 UART (CRC Protocol)
     │
     ▼
 Arduino
 ├── Motor Control
 ├── Lidar (optional)
 └── Telemetry
```

---

## 📂 Project Structure

```
STNM_PTU_System/
│
├── STNM_PTU_System.ino
├── inc/
│   ├── stnm_protocol.h
│   ├── stnm_crc.h
│   ├── stnm_motor.h
│
├── stnm_protocol.cpp
├── stnm_crc.cpp
├── stnm_motor.cpp
├── stnm_lidar.cpp
├── docs/
```

---

## ⚙️ Hardware Requirements

- Arduino (Uno / Mega)
- 2x Stepper Motors
- Stepper Drivers (A4988 / DRV8825)
- Lidar sensor (optional)
- External power supply

---

## 📡 Communication Protocol

### Packet Types

- COMMAND
- TELEMETRY
- ACK

### Packet Format

```
[SOP][TYPE][SEQ][DATA...][CRC]
```

- SOP: Start of Packet  
- CRC: Data integrity check  

---

## 🔄 Workflow

1. Receive command via UART  
2. Verify CRC  
3. Execute motor movement  
4. Send ACK  
5. Send telemetry  

---

## ▶️ Getting Started

### Clone the repository

```
git clone https://github.com/dinder3685/HSS.git
```

### Open in Arduino IDE

Open:

```
STNM_PTU_System.ino
```

### Upload

Make sure to initialize serial:

```cpp
Serial.begin(115200);
```

---

## 🧪 Usage

- Send pan/tilt commands via UART  
- System moves motors  
- Receive telemetry (position + sensor data)  

---

## 📈 Future Work

- PID control  
- Jetson / ROS integration  
- Computer vision tracking  
- Autonomous scanning  
- Safety features  

---

## 👨‍💻 Author

Ahmed Eltayeb  
Embedded Systems Engineer  

---

## 📜 License

Open-source for educational use  

---

## 💡 Notes

- Calibrate motors before use  
- Ensure stable power supply  
- Match CRC on sender side  

---

🔥 Part of a larger robotics and embedded systems development journey.