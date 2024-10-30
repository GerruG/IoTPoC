# Secure IoT Solution Proof of Concept (PoC)

## Overview

This project demonstrates a secure IoT solution for remote monitoring of devices, designed to meet security standards outlined in the Cyber Resilience Act (CRA). The PoC features secure data transmission, basic infrastructure, and Zero Trust principles.

## Project Components

This project is split into two repositories:

1. **Raspberry Pi Repository (Current)**: Contains all Raspberry Pi setup files, including Docker configurations for `Mosquitto`, `Node-RED`, `InfluxDB`, and `Grafana`.

2. **ESP32 Code Repository**: The ESP32 code for reading data from the `DHT11` sensor and transmitting it via `MQTT` is located in a separate repository:
   - [ESP32 DHT11 Repository](https://github.com/GerruG/esp32dht11)

## Security and Compliance

### Zero Trust Architecture

This PoC follows a **Zero Trust** approach:

- **Least Privilege**: Only necessary access permissions are granted.
- **Monitoring**: `Node-RED` handles data flow, logging for security insights.

### Cyber Resilience Act (CRA) Compliance

1. **Security-by-Design**: Structured for secure protocols (e.g., `TLS`).
2. **Updatability**: Supports future security updates and vulnerability patches.
3. **Vulnerability Management**: Designed for easy patching and updates.

## Setup

1. Clone this repository and flash the ESP32 using `PlatformIO` and `ESP-IDF`.
2. Run Docker containers on Raspberry Pi for `InfluxDB`, `Grafana`, and `Node-RED`.
3. Set up `MQTT` broker and connect ESP32 for data transmission.
4. Configure `Grafana` to display data from `InfluxDB`.

## Future Enhancements

- Implement `mTLS` or `TLS` for secure `MQTT`.
- Continue CRA compliance with vulnerability scanning and regular updates.
- Expand Zero Trust with continuous authorization checks.
