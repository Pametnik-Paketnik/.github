# 📦 Smart Delivery Box (Capstone Project)

**Capstone project (2025)** · *IoT × Mobile × Cloud*  
🚀 Developed as part of a 2-semester team course at FERI  

---

## 🌍 Overview
This project was created as part of a **2-semester capstone course** where the main challenge was to design an **information system around the [Direct4.me](https://www.direct4.me/) Smart Box**.  
The company provides an innovative technology for **voice-token–based parcel delivery**.  

Our team expanded the idea into a **self check-in/out system** for **Airbnb/Booking apartments**, allowing guests to arrive at any time without manual key exchange.  
Compared to existing lockbox solutions (owners send a code via WhatsApp), our approach enables **better analytics** and **real-time insight into check-ins** using the Smart Box technology as the core.

---

## 🛠️ Constraints & Learning Goals
We were **limited by the course requirements**, which forced us to explore multiple technologies instead of choosing our own stack:
- Mobile app had to be built in **Kotlin (Jetpack Compose)** (not React Native).  
- **Face authentication** had to be built from scratch (no external libraries).  
- Everything had to run on a **self-managed server** with **CI/CD pipelines**.  

This was intentional: the focus was on **learning diverse tools** and **pushing into new areas**, not just delivering a perfect product.  

---

## 🛠️ Tech Stack
- **Frontend:** React 18, Tailwind, shadcn/ui  
- **Backend:** NestJS (enterprise-grade Node.js framework)  
- **Microservice:** FastAPI (Python) for face authentication  
- **Mobile:** Kotlin (Jetpack Compose) mobile app  
- **Infra:** Dockerized microservices, Nginx reverse proxy, Redis caching  
- **Database:** PostgreSQL  
- **Object storage:** MinIO (for images & AI models)  
- **Auth:** Firebase OTP + custom 2FA (OTP or face recognition)  
- **Deployment:** CI/CD pipelines → Amazon EC2 (free student tier)  

---

## ✨ Features
- 📦 **Parcel delivery integration** with Direct4.me smart boxes  
- 🏡 **Self check-in/out** for Airbnb & Booking hosts  
- 📊 **Dashboard** for hosts (React web app)  
- 📱 **Mobile app** for guests & cleaners ([repo](https://github.com/Pametnik-Paketnik/mobile-app-paketnik))  
- 🔐 **Custom face authentication** (trained from scratch, Jupyter-based research → [repo](https://github.com/Pametnik-Paketnik/paketnik-face-auth-research-model))  
- 👩‍🔧 **Cleaner support** – dedicated mobile interface for housekeeping  
- 🔄 **CI/CD pipelines** for automatic deployment on EC2  
- 🗄️ **Redis caching & MinIO storage**  
- 🧩 Modular **monorepo setup** ([main repo](https://github.com/Pametnik-Paketnik/paketnik-monorepo))  

---

## 🤖 Face Authentication
A special part of the course required building **face recognition without external libraries**:  
- We trained a **custom model** in Jupyter notebooks.  
- Repo with research & training code: [paketnik-face-auth-research-model](https://github.com/Pametnik-Paketnik/paketnik-face-auth-research-model).  
- Due to GPU cost limits, the production service was excluded (fallback = always `true`).  
- Live system uses **Firebase OTP** for real login security.  

---

## 📷 Demo & Presentation
- 🎥 [Slovenian project presentation (Figma slides)](https://www.figma.com/slides/GTmqxMEJ5KXXeeOPh3tcQR/Dark-slides?node-id=1-618&t=GaQgyti9qHnbMNgr-1)  

---

## 🔗 Repositories
- 📱 [Mobile app (Kotlin)](https://github.com/Pametnik-Paketnik/mobile-app-paketnik)  
- 🤖 [Face auth research model](https://github.com/Pametnik-Paketnik/paketnik-face-auth-research-model)  
- 🖥️ [Main monorepo (dashboard + backend)](https://github.com/Pametnik-Paketnik/paketnik-monorepo)  

---

## 🎯 Takeaways
This project was less about AI and more about **teamwork, architecture, and full-stack problem solving**:
- Learned **new tech under pressure** (NestJS, FastAPI, MinIO).  
- Understood the importance of **pipelines, automation, and infra**.  
- Experienced **cross-team coordination** (frontend, backend, mobile, research).  
- Delivered a solution that **addresses a real problem** (self check-in/out).  

Even with limitations, the project pushed us into **cutting-edge tools** and gave us confidence to tackle enterprise-level development.

---
