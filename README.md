# 📊 Install and Configure Monitoring Stack

A fully automated **centralized monitoring stack** built using **Ansible** and **Podman**, featuring **Prometheus**, **Node Exporter**, **Alertmanager**, and **Grafana**.

This project demonstrates a real-world DevOps monitoring setup with **infrastructure automation**, **containerized services**, and **zero manual configuration**, including automated Grafana datasource and dashboard import using the **Grafana HTTP API**.

---

## 🏗️ Architecture Overview

- 📊 **Prometheus** – Metrics collection and scraping engine  
- 🖥️ **Node Exporter** – Host-level system and hardware metrics  
- 🚨 **Alertmanager** – Alert routing and notification management  
- 📈 **Grafana** – Metrics visualization and dashboards  
- 📦 **Podman** – Rootless container runtime  
- 🤖 **Ansible** – Infrastructure automation and configuration management  

All services run as containers and communicate over a **dedicated Podman network**.

---

## 📸 Screenshots

- Fully automated deployment using **Ansible roles**
- Centralized monitoring stack deployed via a single playbook
- Separate playbook for **Node Exporter** deployment
- Grafana **datasource and dashboards imported automatically via API**
- No manual UI configuration required
- Production-ready project structure following Ansible best practices

---
## ⚙️ Automation Highlights
### 📊 Grafana Dashboard Overview
<img width="1718" height="885" alt="image" src="https://github.com/user-attachments/assets/1d432847-208f-412f-a9a2-0ef424bd0886" />

---
### 🧠 Memory Usage Metrics
<img width="1723" height="889" alt="image" src="https://github.com/user-attachments/assets/b8c30105-50c4-4f73-884e-679f330a0b58" />

---

### 🖥️ CPU Usage Metrics
<img width="1728" height="901" alt="image" src="https://github.com/user-attachments/assets/eec2ee31-a6a7-44aa-9ebd-2dba6febd971" />

---

### 🔗 Grafana Data Sources
<img width="1724" height="888" alt="image" src="https://github.com/user-attachments/assets/d9788e74-1a49-46aa-96f8-ff479f02155c" />

---

### 🚨 Alertmanager Alerts
<img width="1713" height="893" alt="image" src="https://github.com/user-attachments/assets/89086610-2d69-4bfd-aead-526e00946751" />

---

### 🎯 Prometheus Targets
<img width="1721" height="891" alt="image" src="https://github.com/user-attachments/assets/0cfc9d93-3079-4c33-9238-43dcf1d31d52" />

---
## 📂 Project Structure

```text
ansible-monitoring-stack/
├── ansible.cfg
├── inventory/
│   └── hosts
├── playbooks/
│   ├── monitoring-stack.yml     
│   └── node-exporter.yml         
├── roles/
│   ├── network/
│   ├── prometheus/
│   │   ├── tasks/
│   │   └── files/
│   │       ├── prometheus.yml
│   │       └── rules/
│   │           └── node-alerts.yml
│   ├── alertmanager/
│   │   ├── tasks/
│   │   └── files/
│   │       └── alertmanager.yml
│   ├── grafana/
│   │   ├── tasks/
│   │   │   ├── run-grafana.yml
│   │   │   ├── import-datasource-api.yml
│   │   │   └── import-dashboard-api.yml
│   │   └── files/
│   │       └── api-dashboards/
│   │           └── node-exporter.json
│   └── node_exporter/
│       └── tasks/
│           └── main.yml
└── README.md
