# Cloud Infrastructure (GCP)

## Overview

The system uses Google Cloud Platform (GCP) to process and store incoming sensor data transmitted from embedded devices.

---

## Architecture

Device → LTE → MQTT (EMQX) → GCP VM → MongoDB

---

## GCP Setup

### Virtual Machine

* GCP VM used as central server
* Hosts MQTT broker (EMQX)
* Handles incoming device connections

---

### Docker Environment

* Docker used for containerized deployment
* EMQX broker runs inside container
* Simplifies deployment and scaling

---

### Firewall Configuration

* Open required ports (MQTT, dashboard)
* Ensure external access for device communication

---

## Data Flow

1. Device publishes data via MQTT
2. EMQX receives message
3. Data routed to backend
4. Stored in MongoDB

---

## Data Format

Sensor data is transmitted in JSON format:

```json
{
  "ID": "device_A",
  "pm25": 12.5,
  "temp": 25.3,
  "co2": 400,
  "Timestamp": "2025-01-01 12:00:00"
}
```

---

## Key Features

* Real-time data ingestion
* Scalable cloud infrastructure
* Containerized deployment
* Persistent data storage

---

## Summary

The cloud layer enables:

* Centralized data collection
* Scalable processing
* Long-term storage

---
