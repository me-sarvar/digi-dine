<p align="center">
  <img src="shared/assets/vectors/DigiDine-Solo.svg" width="100" height="100" alt="App logo" />
</p>

<h1 align="center">🍽️ DigiDine - Smart Meal Ordering System</h1>

<p align="center">
  <i>Scalable, modern, multi-restaurant meal ordering with real-time tracking, table management, QR-based ordering, and robotic waiter integration.</i>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/build-passing-brightgreen" alt="Build Status" />
  <img src="https://img.shields.io/badge/license-proprietary-blue" alt="License" />
</p>

---

## ⚡ Overview

DigiDine enables seamless digital meal ordering for guests, efficient kitchen workflows, and full administrative control for restaurants. Designed to support over 50+ restaurant branches with robust backend, scalable frontend, and clear role separation.

---

## 🛠️ Tech Stack

<details>
<summary><b>View Tech Stack Table</b></summary>

| Component      | Tech                          |
|----------------|------------------------------|
| Frontend       | Flutter Web                  |
| Backend        | NestJS                       |
| Database       | PostgreSQL                   |
| ORM            | TypeORM                      |
| Auth           | JWT, Role-based Access       |
| Realtime       | WebSockets (for orders/live updates) |
| State Mgmt     | Riverpod (Frontend)          |
| Migrations     | TypeORM Migrations           |
| Packaging      | npm / yarn                   |
| Deployment     | Docker Ready (optional)      |
| QR Generation  | Backend-managed, rotating QR |
| Location Check | Browser-based, PIN security  |

</details>
---

## 🎯 Key Features

- Multi-restaurant system with isolated orders & sessions
- QR code & rotating PIN-based table management
- Real-time order updates to kitchen & admin dashboards
- Role-based interface: Guest, Table Captain, Admin, Kitchen
- Utensil inventory tracking per table
- "Sold Out" indicators synced across all menus
- Location & time-based order restrictions
- Integration-ready for robotic waiter systems

---

## 🖥️ Frontend Highlights (Flutter Web)

- Single codebase for Guest, Admin, Kitchen views
- Clean route separation for roles
- Riverpod state management
- Responsive design for mobile, tablet, desktop
- Location permission handling & PIN verification
- Smooth QR code onboarding flow

---

## ⚙️ Backend Highlights (NestJS)

- Modular, scalable architecture using TypeScript
- PostgreSQL relational data model with TypeORM
- Robust session & JWT token management
- WebSocket-based real-time communication
- Secure QR/PIN system with expiration & rotation
- Admin-controlled order override & table reset

---

## 🚀 Setup Instructions
For a detailed overview of the project setup instructions see [SETUP INSTRUCTIONS](SETUP.md)

---
## 📁 Folder Structure

For a detailed overview of the project directories and files, see [STRUCTURE](STRUCTURE.md).

---

## 🔐 Security Layers

✔ JWT authentication with role checks  
✔ Expiring table sessions & tokens  
✔ Rotating PIN system per table  
✔ Location-based order restrictions  
✔ QR code regeneration from admin panel  
✔ Admin role separation for sensitive actions  

---


## 📂 License

This project is proprietary and strictly for use by the DigiDine project team only.  
See the [LICENSE](LICENSE.md) file for full terms and restrictions.


---
