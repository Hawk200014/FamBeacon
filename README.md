<div align="center">

# 🛰️ FamBeacon

**Privacy-first, self-hosted family location sharing.**

Share your family's location in real time—without relying on a third-party cloud.

[Features](#features) •
[Architecture](#architecture) •
[Roadmap](#roadmap) •

</div>

---

## About

FamBeacon is an open-source, self-hosted alternative to services like Life360.

Instead of storing your family's location on someone else's servers, FamBeacon allows you to host everything yourself.

Whether you run it on a Raspberry Pi, a home server, a VPS, or a NAS, **your location data stays under your control.**

## Why?

Modern family tracking applications often require:

- Third-party cloud services
- Monthly subscriptions
- Vendor lock-in
- Collection of sensitive location data

FamBeacon takes a different approach.

- 🔒 Privacy First
- 🏠 Self Hosted
- 🌍 OpenStreetMap
- 📱 Native Mobile Apps
- 🚀 Open Source

No ads.

No tracking.

No selling your data.

Just your own server.

---

# Features

### 📍 Live Location

View the real-time location of every family member.

---

### 👨‍👩‍👧 Family Groups

Create one or multiple family groups with role-based permissions.

---

### 🗺️ OpenStreetMap

Uses OpenStreetMap instead of proprietary map providers.

---

### 📲 QR Code Provisioning

Connect new devices by scanning a QR code.

No manual server configuration required.

---

### 🔐 Secure Authentication

- JWT Authentication
- Refresh Tokens
- Device Registration
- Optional Public Key Authentication

---

### 🚧 Geofences

Receive notifications when someone:

- arrives home
- leaves school
- enters work
- exits a custom area

---

### 🔔 Smart Notifications

Examples:

- Family member arrived home
- Device battery low
- Device offline
- SOS alerts

---

### 🔋 Battery Friendly

Adaptive location updates based on:

- Movement
- Speed
- Activity
- Battery level

---

### 📈 Location History

Browse previous locations and travel history.

---

### 🖥️ Web Dashboard

Manage:

- Users
- Devices
- Families
- Permissions
- Geofences
- QR Codes
- Server Settings

---

# Screenshots

*Coming soon*

---

# Architecture

```
                    Internet
                        │
                 Reverse Proxy
             (HTTPS / Let's Encrypt)
                        │
         ┌──────────────┴──────────────┐
         │                             │
      ASP.NET API              Web Dashboard
         │                             │
         └──────────────┬──────────────┘
                        │
                   PostgreSQL
                        │
                SignalR / WebSocket
                        │
        ┌───────────────┴──────────────┐
        │                              │
     Android App                  iOS App
```

---

# Technology Stack

## Backend

- ASP.NET Core
- Entity Framework Core
- SQLite
- SignalR
- JWT Authentication

## Frontend

- Blazor

## Mobile

- .NET MAUI

## Infrastructure

- Docker
- Docker Compose
- Nginx
- Let's Encrypt

## Maps

- OpenStreetMap
- Leaflet / MapLibre

---

# Security

FamBeacon is designed with privacy as a first-class feature.

- End-to-end encrypted communication (HTTPS)
- Password hashing
- JWT authentication
- Refresh tokens
- Device authentication
- Optional public/private key authentication
- Self-hosted data storage
- No analytics
- No telemetry
- No advertisements

---


# Roadmap

## Version 1.0

- [ ] Backend API
- [ ] Authentication
- [ ] Live Tracking
- [ ] Mobile App
- [ ] OpenStreetMap
- [ ] QR Provisioning

---

## Version 1.1

- [ ] Geofences
- [ ] Push Notifications
- [ ] Device Status
- [ ] Battery Monitoring

---

## Version 1.2

- [ ] Location History
- [ ] Web Dashboard
- [ ] Family Management
- [ ] Roles & Permissions

---

## Version 2.0

- [ ] Home Assistant Integration
- [ ] Webhooks
- [ ] Public API
- [ ] Multi-Server Federation
- [ ] WearOS Support
- [ ] Apple Watch Support

---

# Philosophy

FamBeacon is built on a few simple principles.

Your data belongs to you.

Your server should control your data.

Privacy should not require a subscription.

Family safety should not come at the expense of personal privacy.

---

# License

MIT License

---

<div align="center">

Made with ❤️ for the self-hosting community.

</div>
