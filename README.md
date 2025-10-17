# 🚀 Vexkor Ansible – IoT Stack & Backup Automation

**Ansible-based automation for deploying the Vexkor IoT Edge–Cloud stack**, including Dockerized services for **Node-RED**, **TimescaleDB**, and **Grafana**, with automatic database backup, monitoring, and infrastructure provisioning.

---

## 🧩 Project Overview

Vexkor’s IoT platform enables industrial and building systems to operate under a **hybrid Edge–Cloud architecture**, providing real-time monitoring, predictive maintenance, and smart automation.

This repository contains the **Ansible playbooks and roles** used to deploy and maintain the core IoT stack automatically on cloud or edge devices.

### ✨ Features

- 🧱 **Automated Docker setup** for Node-RED, TimescaleDB, and Grafana  
- 📡 **IoT Data Flow** from Node-RED → TimescaleDB → Grafana dashboards  
- 💾 **Automated backups** (`pg_dump` + cron + rotation)  
- ☁️ **Ready for cloud deployment** (AWS / Oracle / Timescale Cloud)  
- 🔒 **Secure configuration** (SSH keys, UFW, container isolation)  
- 🧰 **Extendable roles** for monitoring, replication (`pglogical`), and VPN  

---

## 🏗️ Stack Architecture

     ┌──────────────┐
     │   Node-RED   │
     │  (IoT Logic) │
     └──────┬───────┘
            │ MQTT / REST
     ┌──────▼───────┐
     │ TimescaleDB  │
     │ (Time-Series │
     │   Database)  │
     └──────┬───────┘
            │ SQL / Grafana
     ┌──────▼───────┐
     │   Grafana    │
     │ Dashboards & │
     │   Alerts     │
     └──────────────┘
