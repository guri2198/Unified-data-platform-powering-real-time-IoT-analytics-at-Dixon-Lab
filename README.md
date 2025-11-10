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

### Data Flow
1. **IoT Edge Devices** generate continuous telemetry and media streams.  
2. **Producers** push structured metadata to **Cassandra** and unstructured data (e.g., images, videos) to **MinIO**.  
3. **Consumers / Analytics Services** query Cassandra for real-time metrics and retrieve objects from MinIO for deeper insights or model training.  

---

## 🏗️ Tech Stack
| Component | Technology | Purpose |
|------------|-------------|----------|
| **Database** | Apache Cassandra | Distributed, scalable time-series storage |
| **Object Store** | MinIO S3 | Binary data storage (video, images, ML outputs) |
| **Data Stream** | Apache Kafka *(optional)* | Real-time ingestion pipeline |
| **Visualization** | Grafana / Flask App | Monitoring and analytics dashboard |

---

## 📂 Repository Structure

dixon-iot-dataverse/
├── cassandra/
│ ├── schema/ # CQL files defining keyspaces and tables
│ ├── config/ # Cassandra node configuration files
│ └── scripts/ # Deployment & maintenance scripts
├── minio/
│ ├── bucket-setup/ # S3 bucket creation and access scripts
│ ├── credentials/ # Secure access configs
│ └── utils/ # File upload/download helpers
├── docs/
│ ├── architecture.md # System design and component overview
│ └── usage-guide.md # How to connect, query, and monitor
└── README.md



---

## 🚀 Key Features
- **High Availability** with multi-node Cassandra cluster  
- **Object-Level Scalability** via MinIO distributed buckets  
- **Real-Time Ingestion** from edge devices and camera feeds  
- **Unified Query Access** for structured + unstructured data  
- **Secure Data Management** with role-based access and versioned backups  

---

## 📊 Example Use Case
- Store real-time **sensor telemetry** (temperature, GPS, speed, etc.) in Cassandra  
- Save **video frames** and **ML annotations** in MinIO S3 buckets  
- Query recent events and visualize camera health or object detection results through Grafana or Flask dashboards  

---

## 🧠 Maintained By
**Dixon IoT Lab**  
Plaksha University  
Research focus: *Intelligent IoT Systems, Edge AI, and Real-Time Data Infrastructure*

---

## 🛡️ License
This project is for internal research and deployment use under the Dixon IoT Lab.  
All rights reserved © 2025 Dixon IoT Lab.


