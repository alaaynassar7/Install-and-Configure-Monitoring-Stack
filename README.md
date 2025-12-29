# 📊 Install and Configure Monitoring Stack

An automated **centralized monitoring stack** built using **Ansible** and **Podman**, featuring **Prometheus**, **Node Exporter**, **Alertmanager**, and **Grafana**.  
This project demonstrates a real-world DevOps monitoring setup with infrastructure automation and containerized services.

---

## 🏗️ Architecture Overview

- 📊 **Prometheus** – Metrics collection and scraping engine  
- 🖥️ **Node Exporter** – Host-level system metrics exporter  
- 🚨 **Alertmanager** – Alert processing and notification handling  
- 📈 **Grafana** – Metrics visualization and dashboards  
- 📦 **Podman** – Container runtime  
- 🤖 **Ansible** – Infrastructure automation and configuration management  

All services run as containers and communicate over a dedicated Podman network.

---
## 📂 Images

### 📈 Grafana Dashboard

<img width="100%" alt="Grafana Dashboard" src="https://github.com/user-attachments/assets/341d6f7b-12f8-4d6b-b09c-2412f06749f6" />

---

### 📊 Prometheus Targets

<img width="100%" alt="Prometheus Targets" src="https://github.com/user-attachments/assets/fa7ba37f-c5e4-417d-9b3c-64eacc02e671" />

---

### 🚨 Alertmanager UI

<img width="100%" alt="Alertmanager UI" src="https://github.com/user-attachments/assets/a21a78b7-a10b-4fd3-8e7a-e671ea93bbfb" />

---

### 🖥️ Node Exporter Metrics

<img width="100%" alt="Node Exporter Metrics" src="https://github.com/user-attachments/assets/05d58f93-408f-4222-96ff-8a7b09dfa6a5" />

---

### 🌐 Prometheus Overview

<img width="100%" alt="Prometheus Overview" src="https://github.com/user-attachments/assets/f72bffe5-293b-4e3e-a746-73e4f9cf3644" />

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
│   ├── prometheus/
│   │   ├── tasks/
│   │   │   └── main.yml
│   │   └── files/
│   │       └── prometheus.yml
│   ├── alertmanager/
│   │   ├── tasks/
│   │   │   └── main.yml
│   │   └── files/
│   │       └── alertmanager.yml
│   ├── grafana/
│   │   └── tasks/
│   │       └── main.yml
│   └── node_exporter/
│       └── tasks/
│           └── main.yml
└── README.md

---


