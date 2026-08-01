# Wazuh-monitoring-lab

# 🚀 Distributed SIEM & SOAR Platform with Wazuh

> **Implementation of a Distributed Security Information and Event Management (SIEM) Platform and Security Incident Automation using SOAR Technologies**

---

## 📖 Project Overview

This project demonstrates the implementation of a **Distributed Security Information and Event Management (SIEM)** platform using **Wazuh**, deployed in a **Docker-based environment** hosted on a **cloud server**.

The platform centralizes security logs, detects threats in real time, and automates incident response through the integration of **Shuffle SOAR**, **TheHive**, and **Cortex**.

The objective is to build a modern Security Operations Center (SOC) environment using open-source technologies capable of detecting, analysing, and responding to security incidents automatically.

---

## 🎯 Objectives

- Deploy a distributed Wazuh SIEM platform.
- Containerize the entire infrastructure using Docker.
- Host the platform on a cloud server.
- Collect and centralize security logs.
- Detect malicious activities in real time.
- Develop custom Wazuh detection rules.
- Automate incident response using SOAR.
- Reduce Mean Time to Detect (MTTD) and Mean Time to Respond (MTTR).

---

## 🏗️ Architecture

```text
                    +----------------------+
                    |     Cloud Server     |
                    +----------+-----------+
                               |
                        Docker Engine
                               |
        +----------------------+----------------------+
        |                      |                      |
        |                      |                      |
+---------------+      +----------------+     +--------------+
| Wazuh Manager |----->| Wazuh Indexer  |<----| Wazuh Dashboard |
+---------------+      +----------------+     +--------------+
        |
        |
        +-----------------------------+
                                      |
                             Security Alerts
                                      |
                                      ▼
                              Shuffle SOAR
                                      |
               +----------------------+----------------+
               |                                       |
               ▼                                       ▼
          TheHive                               Cortex
      (Case Management)                  (Threat Intelligence)
````

---

## 🛠️ Technologies Used

| Technology     | Purpose                    |
| -------------- | -------------------------- |
| Wazuh          | SIEM / XDR                 |
| Docker         | Containerization           |
| Docker Compose | Multi-container Deployment |
| Shuffle        | SOAR Automation            |
| TheHive        | Incident Response Platform |
| Cortex         | Observable Analysis        |

---

## 📂 Repository Structure

```text
.
├── README.md
├── docker/
│   ├── docker-compose.yml
│   └── configurations/
│
├── wazuh/
│   ├── custom-rules/
│   ├── active-response/
│   └── configurations/
│
├── shuffle/
│
├── thehive/
│
├── cortex/
│
├── screenshots/
│
├── architecture/
│
├── docs/
│   ├── installation.md
│   ├── architecture.md
│   ├── detection-rules.md
│   ├── monitoring.md
│   ├── use-cases.md
│   └── troubleshooting.md
│
└── scripts/
```

---

## 🔍 Security Monitoring

The platform is capable of monitoring:

* SSH Authentication Events
* SSH Brute Force Attacks
* Linux and Windows System Logs
* Docker Activity
* Docker Container Creation
* Docker Container Deletion
* Privileged Docker Containers
* File Integrity Monitoring (FIM)
* Authentication Logs
* System Events
* Custom Security Events

---

## 🤖 Automated Incident Response

The incident response workflow is fully automated.

Attacker
    │
    ▼
Security Event
    │
    ▼
Wazuh SIEM
    │
Generate Alert
    │
    ▼
Shuffle SOAR
    │
    ├──────────────► Cortex
    │                  │
    │                  ▼
    │         Threat Intelligence
    │
    ▼
TheHive
    │
Case Creation
    │
    ▼
SOC Analyst


### Workflow

1. Wazuh detects a security event.
2. An alert is generated.
3. Shuffle receives the alert via Webhook.
4. Shuffle executes an automated workflow.
5. Cortex enriches observables (IPs, Domains, Hashes).
6. TheHive automatically creates an investigation case.
7. SOC analysts review and respond.

---

## 🚨 Detection Use Cases

* SSH Brute Force Detection
* Docker Monitoring
* Docker Privileged Container Detection
* Docker Container Creation Monitoring
* File Integrity Monitoring
* Linux Authentication Monitoring
* Custom Wazuh Rules
* Automated Incident Case Creation
* Threat Intelligence Enrichment

---

## 📸 Screenshots

### Wazuh Dashboard

> *()*

### Security Alerts

> *(Add screenshot here)*

### Shuffle Workflow

> *(Add screenshot here)*

### TheHive Case Management

> *(Add screenshot here)*

### Cortex Analysis

> *(Add screenshot here)*

---

## ✨ Features

* Distributed SIEM Architecture
* Cloud Deployment
* Docker Containerization
* Centralized Log Collection
* Real-Time Threat Detection
* Custom Detection Rules
* Automated Incident Response
* SOAR Integration
* Threat Intelligence Enrichment
* Scalable Architecture
* Open-Source Security Stack

---

## 🚀 Future Improvements

* Suricata IDS Integration
* Sigma Rule Support
* MITRE ATT&CK Mapping
* Email Notifications
* Microsoft Teams Integration
* Threat Hunting Dashboards
* Multi-Tenant Support
* Machine Learning-Based Detection

---

## 📚 References

* Wazuh Documentation
* Docker Documentation
* Shuffle Documentation
* TheHive Documentation
* Cortex Documentation

---

## 👨‍💻 Author

**Aimen Rahou - Aimen Khelil**

Cybersecurity | SOC Analyst 

This repository was developed as an academic cybersecurity project to demonstrate the implementation of a distributed SIEM infrastructure and the automation of security incident response using open-source technologies.

```
```
