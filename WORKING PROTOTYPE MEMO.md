# 🔧 Working Prototype – Real‑Time Multi‑User IoT Self‑Healing System

## 1. Overview
This prototype demonstrates a **self‑healing IoT automation system** using an ESP32 controller that continuously monitors multiple sensors, detects faults, and automatically switches to backup or safe modes.  
All system states are synchronized in **real time** with a **Firebase Realtime Database** and visualized on a **web dashboard (Digital Twin)**.

---

## 2. Prototype Components

### 🔌 Hardware (Simulated on Wokwi)
- ESP32 Dev Module
- Primary Sensor (Potentiometer – Analog)
- Backup Sensor (Potentiometer – Analog)
- Load / Current Sensor (Potentiometer – Analog)
- Status LEDs:
  - Green → Normal Operation
  - Yellow → Backup Active
  - Red → Fault / Safe Mode
  - Blue → Network Status
- WiFi (Simulated)

### ☁️ Software & Services
- Arduino Framework (ESP32)
- Firebase Realtime Database
- HTML + CSS + JavaScript Dashboard
- Wokwi Online Simulator

---

## 3. System Working Logic

1. ESP32 reads values from:
   - Primary Sensor
   - Backup Sensor
   - Load Sensor
2. Sensor health is validated using thresholds.
3. If **Primary Sensor fails**, system:
   - Switches to **Backup Sensor**
   - Updates status in Firebase
4. If **both sensors fail**:
   - System enters **Safe Mode**
   - Local fallback control is activated
5. All states are pushed to Firebase in real time.
6. Web dashboard reflects live system status.

---

## 4. Self‑Healing Behavior

| Condition | System Action |
|---------|---------------|
| Primary sensor healthy | Normal operation |
| Primary fails | Switch to backup |
| Primary + Backup fail | Safe mode ON |
| Network lost | Local control fallback |
| Load overload | Output limited |

---

## 5. Data Flow (Live)

