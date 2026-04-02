# MQTT Broker (EMQX)

## Overview

EMQX is used as the MQTT broker to handle communication between embedded devices and the cloud backend.

---

## Role in System

* Receives data from devices via MQTT
* Routes messages to backend services
* Acts as central communication hub

---

## Configuration

### Broker Setup

* EMQX deployed on GCP VM using Docker
* MQTT protocol version 3.1.1 used
* Client initialized via embedded firmware

---

### Client Configuration

* Client ID generated from device ID
* No authentication used (can be extended)
* QoS level: EXACTLY_ONCE

---

## Message Flow

1. Device connects to EMQX
2. Sensor data published as JSON
3. EMQX processes message
4. Data forwarded to storage system

---

## MQTT Workflow

* Connect → Publish → Disconnect
* Reconnection handled before each transmission

---

## Key Features

* Lightweight messaging protocol
* Reliable data delivery (QoS 2)
* Decoupled architecture
* Scalable broker system

---

## Integration

* Integrated with embedded firmware
* Connected to MongoDB backend via GCP

---

## Summary

EMQX enables:

* Real-time communication
* Reliable message delivery
* Scalable IoT data pipeline

---
