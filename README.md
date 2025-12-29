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

