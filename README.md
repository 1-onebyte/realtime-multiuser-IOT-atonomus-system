# realtime-multiuser-IOT-atonomus-system

A real‑time **ESP32‑based IoT system** that continuously monitors multiple sensors, detects faults, automatically switches to backup mechanisms, and visualizes system health on a **live Firebase‑powered dashboard**.

This project demonstrates **self‑healing automation**, **fault tolerance**, and **real‑time cloud synchronization**, suitable for smart factories, power systems, and industrial automation.

---

## 🚀 Problem Statement

Traditional IoT systems fail silently when:
- A sensor stops working
- Network connectivity is lost
- Overload conditions occur

This leads to downtime, unsafe operation, and delayed human intervention.

---

## 💡 Solution Overview

Our system introduces:
- **Primary & Backup Sensors**
- **Automatic fault detection**
- **Local fallback when network fails**
- **Cloud‑based real‑time monitoring**
- **Clear system status visualization**

The system continues operating safely even during failures.

---

## 🧠 Key Features

- ✅ Real‑time sensor monitoring (ESP32)
- 🔁 Automatic switch to backup sensor
- ⚠️ Fault & overload detection
- 🛡️ Safe mode activation
- 🌐 Firebase Realtime Database sync
- 📊 Live web dashboard (Digital Twin)
- 👥 Multi‑user real‑time access

---

## 🧩 System Architecture

```mermaid
flowchart LR
    A[ESP32 Controller] --> B[Primary Sensor]
    A --> C[Backup Sensor]
    A --> D[Load Sensor]

    A -->|WiFi| E[Firebase Realtime DB]
    E --> F[Web Dashboard]

    A -->|Fallback| G[Local Control Mode]
