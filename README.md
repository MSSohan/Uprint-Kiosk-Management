<div align="center">

# 🛠️ Uprint Kiosk Management

### Run a city-wide printing network from one dashboard.

The control center behind **[Uprint](https://uprintbd.com)**, a network of 24/7 self-service printing kiosks across university campuses in Chattogram, Bangladesh. It manages kiosks, outlets, pricing, live device health and who can print where.

[![Platform](https://img.shields.io/badge/▶_Platform-uprintbd.com-FF6B00?style=for-the-badge)](https://uprintbd.com)
[![Status](https://img.shields.io/badge/status-in_production-2EA44F?style=for-the-badge)](https://uprintbd.com)

![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![MQTT](https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white)
![Raspberry Pi](https://img.shields.io/badge/Raspberry_Pi-A22846?style=flat-square&logo=raspberrypi&logoColor=white)
![jQuery](https://img.shields.io/badge/jQuery-0769AD?style=flat-square&logo=jquery&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap_4-7952B3?style=flat-square&logo=bootstrap&logoColor=white)

</div>

---

## ⚡ What it solves

> Many kiosks, many outlet owners, different prices, printers that go offline. Without one place to control it all, the network breaks.

**Kiosk Management** gives admins, sales and outlet owners one dashboard to add kiosks, set prices, watch device health and control availability.

```mermaid
flowchart LR
    A["➕ Add kiosk"] --> B["💰 Set page-wise prices"]
    B --> C["🟢 Monitor live status"]
    C --> D["🔒 Lock / unlock"]
    D --> E["🖨️ Students print via OTP or QR"]
    style A fill:#FFF4EB,stroke:#FF6B00
    style E fill:#FF6B00,color:#fff,stroke:#FF6B00
```

---

## ✨ Features

| | Feature | What it does |
|:-:|---|---|
| 🖨️ | **Kiosk CRUD** | Add, edit and remove kiosks under each outlet |
| 💰 | **Page-wise pricing** | Per-kiosk price ranges for B&W and colour, with separate two-sided rates |
| 🟢 | **Live device health** | Online, Printer Disconnected or Offline, reported by each device |
| 🔒 | **Active / Locked** | Lock a kiosk instantly so it cannot accept prints |
| 🔑 | **OTP + QR printing** | Each kiosk screen shows an OTP entry and a QR code for direct print |
| 🏪 | **Outlet management** | Outlet owners manage their own kiosks |
| 👥 | **Role-based access** | Admin, sales, outlet and student roles each see only what they need |

### 🚧 In progress
- 👁️ **Shown / Hidden** visibility for kiosks and whole outlets
- 🔍 **Searchable outlet and printer dropdowns** with device counts
- 🛡️ **Tighter role checks** on edit, delete and API endpoints

---

## 🏗️ Architecture

```mermaid
flowchart TB
    subgraph Admin["🛠️ Management dashboard"]
        A1["Admin / Sales"]
        A2["Outlet owners"]
    end
    Admin --> S["Django server + MySQL"]
    S <-->|"MQTT"| K1["🖨️ Kiosk (Raspberry Pi)"]
    S <-->|"MQTT"| K2["🖨️ Kiosk (Raspberry Pi)"]
    S --> W["🌐 Student web app"]
    S --> M["📱 Mobile app"]
```

---

## 👨‍💻 My role

- Built and maintain the kiosk, outlet and pricing management used in production
- Worked across the stack: Django views and models, Bootstrap templates, jQuery and device communication
- Prioritised **zero data loss** and **no downtime**: every schema change is backed up, reviewed and migrated safely on the live database

---

<div align="center">

**Part of the Uprint platform:**
[📄 Uprint Lab Sheet Builder](https://github.com/MSSohan/Uprint-Lab-Sheet-Builder) ·
[📍 Find Nearest Uprint Kiosk](https://github.com/MSSohan/Find-Nearest-Uprint-Kiosk) ·
[🛠️ Uprint Kiosk Management](https://github.com/MSSohan/Uprint-Kiosk-Management)

<sub>The production source code is private. This repository is a showcase of the feature.</sub>

</div>
