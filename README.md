# Unified-data-platform-powering-real-time-IoT-analytics-at-Dixon-Lab

# Dixon IoT Dataverse

**Unified data platform powering real-time IoT analytics at Dixon Lab**

---

## 🧩 Overview
**Dixon IoT Dataverse** is the central data backbone of the Dixon IoT Lab — designed to collect, store, and serve massive volumes of real-time IoT sensor data.  
It integrates **Apache Cassandra** for distributed time-series storage and **MinIO S3** for scalable object data management such as images, video frames, and annotated datasets.

---

## ⚙️ Architecture

### Core Components
- **Apache Cassandra** — Distributed, fault-tolerant NoSQL database for structured and time-series sensor data.  
- **MinIO S3 Bucket** — High-performance object storage for large binary data (e.g., video frames, model outputs).  
- **Producers** — Edge and IoT devices streaming data to the backend.  
