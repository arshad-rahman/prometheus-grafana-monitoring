<p align="center">
  <a href="https://github.com/arshad-rahman/prometheus-grafana-monitoring">
    <img src="https://img.shields.io/badge/Monitoring-Prometheus%20%26%20Grafana-blue?style=for-the-badge" alt="Prometheus & Grafana Monitoring">
  </a>
</p>

<p align="center">
  <strong>Docker-Compose setup for end-to-end monitoring of your services</strong><br>
  <em>Spin up Prometheus, Node Exporter & Grafana in minutes</em>
</p>

<p align="center">
  <a href="https://github.com/arshad-rahman/prometheus-grafana-monitoring/actions">
    <img src="https://img.shields.io/github/actions/workflow/status/arshad-rahman/prometheus-grafana-monitoring/build.yml?branch=main&style=flat-square" alt="CI Status">
  </a>
  <a href="https://github.com/arshad-rahman/prometheus-grafana-monitoring/issues">
    <img src="https://img.shields.io/github/issues/arshad-rahman/prometheus-grafana-monitoring.svg?style=flat-square" alt="Open Issues">
  </a>
  <a href="https://github.com/arshad-rahman/prometheus-grafana-monitoring/blob/main/LICENSE">
    <img src="https://img.shields.io/github/license/arshad-rahman/prometheus-grafana-monitoring.svg?style=flat-square" alt="License">
  </a>
</p>

---

## 📋 Table of Contents

- [🛠️ Features](#️-features)  
- [🔌 Prerequisites](#-prerequisites)  
- [🚀 Installation](#-installation)  
- [🎯 Usage](#-usage)  
- [🛑 Stop & Cleanup](#-stop--cleanup)  
- [📊 Endpoints](#-endpoints)  
- [🎨 Grafana Dashboards](#-grafana-dashboards)  
- [⚙️ Customization](#-customization)  
- [🤝 Contributing](#-contributing)  
- [📄 License](#-license)

---

## 🛠️ Features

- 🚀 **One-command bring-up**: `docker-compose up -d`  
- 🔍 **Prometheus** for metrics collection  
- 📡 **Node Exporter** for host & container stats  
- 📈 **Grafana** for rich, customizable dashboards  

---

## 🔌 Prerequisites

- **Docker** & **Docker Compose** installed  
- Ports **9090**, **9100**, **3000** available  

---

## 🚀 Installation

```bash
# 1. Clone the repo
git clone https://github.com/arshad-rahman/prometheus-grafana-monitoring.git
cd prometheus-grafana-monitoring

# 2. Launch the stack
docker-compose up -d
````

---

## 🎯 Usage

After a few seconds, access:

* Prometheus UI → `http://localhost:9090`
* Node Exporter metrics → `http://localhost:9100/metrics`
* Grafana UI → `http://localhost:3000`

  * **Default login:** admin / admin

---

## 🛑 Stop & Cleanup

To stop the monitoring stack:

```bash
docker-compose down
```

To stop and remove all containers, networks, and volumes:

```bash
docker-compose down -v
```

To relaunch the stack after stopping:

```bash
docker-compose up -d
```

---

## 📊 Endpoints

| Service       | URL                             |
| ------------- | ------------------------------- |
| Prometheus    | `http://localhost:9090`         |
| Node Exporter | `http://localhost:9100/metrics` |
| Grafana       | `http://localhost:3000`         |

---

## 🎨 Grafana Dashboards

1. **Add Data Source** → Prometheus (`http://prometheus:9090`)
2. **Import Dashboard**

   * Use community dashboard ID **1860** for Node Exporter
3. **Explore metrics**: CPU, memory, disk, network, etc.

---

## ⚙️ Customization

* Edit `prometheus.yml` to adjust `scrape_interval` or targets
* Add more exporters under `docker-compose.yml` (e.g., cAdvisor)
* Provision Grafana dashboards via `/provisioning` folder

---

## 🤝 Contributing

1. Fork this repo
2. Create a branch:

   ```bash
   git checkout -b feature/your-feature
   ```
3. Commit changes:

   ```bash
   git commit -m "Add awesome feature"
   ```
4. Push & open a PR:

   ```bash
   git push origin feature/your-feature
   ```

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

<p align="center">
  Built with ❤️ by <a href="https://github.com/arshad-rahman">arshad</a>
</p>

