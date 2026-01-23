# realtime-multiuser-IOT-atonomus-system

A real‑time **ESP32‑based IoT system** that continuously monitors multiple sensors, detects faults, automatically switches to backup mechanisms, and visualizes system health on a **live Firebase‑powered dashboard**.

This project demonstrates **self‑healing automation**, **fault tolerance**, and **real‑time cloud synchronization**, suitable for smart factories, power systems, and industrial automation.

---

## Problem Statement

Traditional IoT systems fail silently when:
- A sensor stops working
- Network connectivity is lost
- Overload conditions occur

This leads to downtime, unsafe operation, and delayed human intervention.

---

## Solution Overview

Our system introduces:
- **Primary & Backup Sensors**
- **Automatic fault detection**
- **Local fallback when network fails**
- **Cloud‑based real‑time monitoring**
- **Clear system status visualization**

The system continues operating safely even during failures.

---

## Key Features

- Real‑time sensor monitoring (ESP32)
- Automatic switch to backup sensor
- Fault & overload detection
- Safe mode activation
- Firebase Realtime Database sync
- Live web dashboard (Digital Twin)
- Multi‑user real‑time access
  
---

## Project Structure

dashboard/
   
   ├──([Dashboard](https://1-onebyte.github.io/realtime-multiuser-IOT-atonomus-system/))        # Live dashboard

 docs/
   
   ├── ([architecture diagram](<architecture diagram.png>))
   
   ├── ([demo flow chart](<demo flow chart.png>))
   
   ├── ([flow diagram](<flow diagram.png>))
   
   ├── ([WORKING PROTOTYPE](<WORKING PROTOTYPE MEMO.md>))

 simulation/
   
   ├──[Wokwi Simulation](https://wokwi.com/projects/453870955625455617)

---

## Team Contribution 

| Member | Role / Responsibility | Key Contributions |
|-------|-----------------------|------------------|
| Member 1 | Architecture & System Design | • Designed overall system architecture  
• Created architecture, flow, and data‑flow diagrams  
• Defined system components and interactions |
| Member 2 | Documentation & README | • Wrote README (problem → solution → architecture)  
• Explained working prototype and demo flow  
• Added diagrams and project explanation |
| Member 3 | Presentation & Demo | • Prepared presentation slides  
• Designed demo flow chart  
• Explained edge cases and system behavior  
• Aligned demo with project workflow |
| Member 4 | Project Management & Planning | • Created JIRA‑style task structure  
• Managed sprint planning and task tracking  
• Maintained project structure and planning docs |

---

## System Architecture

```mermaid
flowchart LR
    A[ESP32 Controller] --> B[Primary Sensor]
    A --> C[Backup Sensor]
    A --> D[Load Sensor]

    A -->|WiFi| E[Firebase Realtime DB]
    E --> F[Web Dashboard]

    A -->|Fallback| G[Local Control Mode]

