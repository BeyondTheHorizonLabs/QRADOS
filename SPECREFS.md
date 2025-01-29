# QRADOS SPECREFS - Specification References

## **Overview**
This document outlines the key specifications, reference materials, and technical requirements for the **QRADOS Core Research System**.

## **1. System Architecture**
- **Framework:** Node.js (Backend), React.js (Frontend)
- **Database:** PostgreSQL (Primary), JSON-based Log Storage (Secondary)
- **Communication Protocols:** WebSockets (Real-time Streaming), REST API (Data Retrieval)
- **Deployment:** Docker-based with `docker-compose`
- **Supported Platforms:** macOS, Linux, Windows (via WSL)

## **2. Hardware Specifications**
- **Primary Computing Unit:** Raspberry Pi 5 / x86-64 Linux Server
- **Power Supply:** 48V 600W PSU (configurable)
- **Sensors:**
  - Electromagnetic Field (EMF) Sensors
  - RF Spectrum Analyzer (HackRF / RTL-SDR)
  - Ultrasonic Microphone Array
  - Optical Spectrum Analyzer
  - Temperature, Humidity, and Pressure Sensors
  - GPS & Magnetometer for Geospatial Logging

## **3. QRADOS Log Format (CLF-Derived)**
QRADOS introduces a **customized log format** derived from **Common Log Format (CLF)**, specifically structured for **anomaly tracking and AI training**.

### **QRADOS Log Entry Structure**
```json
{
  "timestamp": "2025-01-30T12:45:00Z",
  "device_id": "QRADOS-01",
  "sensor_type": "EMF",
  "value": 35.2,
  "unit": "µT",
  "status": "NORMAL",
  "location": "Earth-Lab",
  "metadata": {
    "frequency": 7.83,
    "resonance": 1.25,
    "AI_flag": false
  }
}
```

### **How to Use QRADOS Logs**
- **AI Training:** Logs feed into **machine learning models** to detect anomaly patterns.
- **Real-Time Alerts:** Anomalies trigger **automated alerts** based on predefined thresholds.
- **Data Correlation:** Cross-referenced with **geospatial & electromagnetic data** to identify patterns.

## **4. Grafana Dashboard Concepts**
QRADOS integrates with **Grafana** for real-time visualization of **sensor data & anomaly tracking**.

### **Grafana Panel Configurations**
- **EMF Flux Monitoring Panel:** Displays real-time fluctuations.
- **RF Spectrum Dashboard:** Detects **unusual signal spikes**.
- **Heatmap for Anomaly Density:** Highlights locations with high anomaly frequency.
- **AI Flagged Events Log:** Provides an **alert feed for AI-classified anomalies**.

## **5. Future Enhancements**
- Expansion of **multi-node sensor synchronization** for high-accuracy anomaly triangulation.
- **Cloud-based anomaly correlation with global research datasets.**
- **Neural network-based real-time anomaly classification.**


