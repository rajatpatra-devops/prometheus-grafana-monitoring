# Homelab Monitoring: Prometheus + Grafana

## 🚀 Overview
This project sets up a complete observability stack on **my personal Ubuntu homelab** using Docker Compose.  
It includes:

- **Prometheus** for scraping and storing system metrics  
- **Node Exporter** to expose CPU, memory, disk, and network stats  
- **Grafana** for real-time dashboards and insights  

Everything is containerized for portability, reproducibility, and automation.

---

## 📁 Project Structure

prometheus-grafana-monitoring/
├── docker-compose.yml # Compose file to deploy all services
├── prometheus/
│ └── prometheus.yml # Scrape config for Prometheus
├── prometheus.yaml # Grafana provisioning for Prometheus data source
└── grafana/
└── provisioning/ # Grafana config for auto data source setup


---

## ⚙️ Getting Started

### Prerequisites
- Docker & Docker Compose installed (see [Docker docs](https://docs.docker.com/get-docker/))

### Launch the Stack
```bash
docker-compose up -d
Access the Services
Prometheus UI: http://localhost:9090

Node Exporter metrics: http://localhost:9100/metrics

Grafana UI: http://localhost:3000

Default login: admin / admin

Grafana is ready to use with Prometheus auto-configured via prometheus.yaml.

🔭 Future Enhancements
Integrate Alertmanager for automated alerts

Develop custom Grafana dashboards for specific services

Automate setup and backups using Ansible or CI/CD pipelines

🛠️ Troubleshooting Tips
Use docker logs <container> to check for issues

Confirm Prometheus is scraping metrics via its UI
