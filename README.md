# 💳 Fraud Detection & AML Big Data Architecture

## 🧭 Overview
This project presents a scalable **big data architecture** designed for a global financial institution to detect **real-time fraudulent transactions** and ensure **Anti-Money Laundering (AML)** compliance.  
The system leverages distributed computing, streaming ingestion, and machine learning analytics to identify suspicious activity within seconds of occurrence — protecting both customer assets and institutional integrity.

---

## 🎯 Objectives
- Develop a **real-time fraud detection pipeline** using open-source big data technologies.  
- Design an architecture capable of ingesting and analyzing **millions of daily transactions**.  
- Incorporate AML compliance components to meet regulatory requirements.  
- Demonstrate **data flow integration** across ingestion, storage, processing, and visualization layers.  

---

## 🏗️ Architecture Overview

| **Component** | **Purpose** |
|----------------|-------------|
| **Apache NiFi** | Ingests streaming data from transaction sources (ATMs, mobile apps, POS systems) in real time. |
| **HDFS (Hadoop Distributed File System)** | Serves as the distributed data lake for raw and processed transactional data. |
| **Apache Hive** | Provides data warehousing for querying and joining large-scale structured data. |
| **Apache HBase** | Enables low-latency lookups for known fraudulent accounts and flagged transactions. |
| **Apache Spark** | Processes, cleans, and analyzes data at scale; runs ML models for anomaly detection. |
| **Apache Solr** | Indexes fraud alerts and enables fast search for analysts and compliance teams. |

This architecture is fully containerized using **Docker Compose**, allowing modular deployment and horizontal scalability.

---

## 🔄 Data Flow

1. **Ingestion Layer** – NiFi captures incoming transaction streams and routes data to HDFS in real time.  
2. **Storage Layer** – HDFS stores raw and processed data; HBase holds customer and account references.  
3. **Processing Layer** – Spark cleans and analyzes data, applying fraud detection algorithms.  
4. **Query Layer** – Hive enables SQL-like analytics; results written to Solr for fraud case management.  
5. **Visualization Layer** – Dashboards and reports display alerts, risk scores, and regional fraud trends.

---

## 🧰 Tools & Technologies
- **Apache NiFi** – Data ingestion and routing  
- **HDFS (Hadoop)** – Distributed storage  
- **Apache Hive** – Data warehousing  
- **Apache HBase** – Real-time lookups  
- **Apache Spark** – Processing & machine learning  
- **Apache Solr** – Indexing and search  
- **Docker Compose** – Containerized environment  

---

## 🤖 Machine Learning Integration
Implemented Spark MLlib algorithms for anomaly detection:
- **Isolation Forest** – Detects outliers in transaction patterns  
- **Logistic Regression** – Binary classification of fraud vs. non-fraud  
- **Random Forest** – Ensemble approach improving precision and recall  

**Evaluation Metrics:** Precision, Recall, F1-score, and ROC-AUC  

---

## 🚀 Key Outcomes
- Built a **fully functional distributed architecture** connecting NiFi, HDFS, Hive, HBase, Spark, and Solr.  
- Achieved near real-time detection (under 5 seconds latency in simulated testing).  
- Designed scalable infrastructure capable of handling millions of records daily.  
- Integrated AML compliance workflows and reporting.

---

## 💡 Applications
- **Financial Institutions:** Detect and prevent fraud in real time.  
- **Regulatory Teams:** Automate AML/KYC compliance reporting.  
- **Data Science Teams:** Extend to include predictive modeling and streaming analytics.

---

## 🔧 Future Enhancements
- Integrate **Kafka** for enhanced message streaming.  
- Incorporate **Graph-based fraud detection** for relational pattern analysis.  
- Add **Power BI dashboards** for executive visualization.  

---

## 👤 Author
**Derek Lamb**  
_M.S. Data Science, Bellevue University_  
Project: **DSC650 – Big Data Architecture and Applications**  
📧 dereklamb@example.com *(optional)*  

---

## 🏁 Repository Structure
