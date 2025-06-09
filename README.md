# Prometheus & Grafana Monitoring Setup

## Overview
This project sets up a complete monitoring stack using **Prometheus**, **Node Exporter**, and **Grafana** via Docker Compose.  
It enables collection and visualization of system metrics on your host machine.

## Project Structure

prometheus-grafana-monitoring/
├── docker-compose.yml # Docker Compose file to launch services
├── prometheus/
│ └── prometheus.yml # Prometheus configuration file
├── prometheus.yaml # Grafana datasource provisioning config
└── grafana/ # Grafana data and provisioning files
└── provisioning/


## Components

- **Prometheus**: Open-source metrics collection and storage  
- **Node Exporter**: Exposes hardware and OS metrics from the Linux host  
- **Grafana**: Dashboard and visualization tool

## Prerequisites

- Docker and Docker Compose installed on your machine

## How to Run

1. Start the stack:

```bash
docker-compose up -d
Access the services in your browser:

Prometheus UI: http://localhost:9090

Node Exporter metrics: http://localhost:9100/metrics

Grafana UI: http://localhost:3000 (default login: admin/admin)

Grafana is preconfigured with Prometheus as the data source via provisioning.
