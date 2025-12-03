# Secure IoT Gateway with OTA, MQTT TLS & Docker – Final Project (Sprint 3)

**Student:** [Ismingiz Familiangiz]  
**Course:** Linux for Embedded Systems – Final Project Sprint 3  
**Date:** December 2025

## Project Overview
Raspberry Pi based secure IoT gateway that:
- Reads sensor data (DHT22 or any)
- Publishes/subscribes via MQTT with TLS client certificates
- Supports secure, power-fail-safe OTA updates (A/B + OverlayFS)
- Runs everything inside Docker containers
- Includes simple web dashboard

## Sprint 3 – New Features (Docker Containerization)
- [x] Full application containerized
- [x] Multi-stage Dockerfile (small final image)
- [x] docker-compose.yml (gateway + mosquitto broker + dashboard)
- [x] Works on Raspberry Pi (arm64) and x86 PC
- [x] OTA updates work inside container
- [x] Automatic startup of all services

## Directory Structure
/iot-gateway-final/
├── docker-compose.yml
├── Dockerfile
├── gateway/             # MQTT client + sensor code
├── ota-system/          # OTA scripts + signer
├── dashboard/           # Simple web dashboard
├── mosquitto/           # Config with TLS
├── updates/             # Sample signed update packages
└── README.md

## Quick Start (Docker)
```bash
git clone https://github.com/username/iot-gateway-final.git
cd iot-gateway-final
docker-compose up --build
