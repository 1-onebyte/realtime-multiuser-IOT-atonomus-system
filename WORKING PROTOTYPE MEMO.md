# WORKING PROTOTYPE MEMO  
## Realtime Multiplayer Typing Test Platform

---

## 1. Project Title
**Realtime Multiplayer Typing Test Website**

---

## 2. Problem Statement
Most typing practice platforms are **single‑player** and do not provide real‑time competition, engagement, or instant comparison with others.  
This makes typing practice less interactive and less motivating, especially for students and competitive learners.

---

## 3. Proposed Solution
We built a **real‑time multiplayer typing test platform** where multiple users can:

- Join the same room
- Start typing simultaneously
- See **live leaderboard updates**
- Compare **WPM, accuracy, and progress** in real time

The system uses **WebSockets** to ensure instant updates with minimal delay.

---

## 4. Objective of the Prototype
The working prototype aims to demonstrate:

- Real‑time communication between users
- Live synchronization of typing stats
- Scalable room‑based multiplayer system
- Fair and responsive gameplay

---

## 5. Key Features Implemented
✅ Real‑time multiplayer rooms  
✅ Live leaderboard (WPM, accuracy, progress)  
✅ Server‑controlled game timer  
✅ Auto room creation and deletion  
✅ Real‑time updates using Socket.IO  
✅ Simple, clean, responsive UI  

---

## 6. Technology Stack

### Frontend
- HTML
- CSS
- JavaScript
- Socket.IO Client

### Backend
- Node.js
- Express.js
- Socket.IO Server

### Communication
- WebSockets (via Socket.IO)

---

## 7. System Architecture (High Level)
