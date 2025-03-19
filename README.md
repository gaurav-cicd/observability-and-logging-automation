<<<<<<< HEAD
# observability-and-logging-automation
=======
# Observability and Logging Automation

This project implements a comprehensive observability and logging solution for containerized applications using ELK Stack, Prometheus, and Grafana.

## Components

1. **ELK Stack**
   - Elasticsearch: For storing and indexing logs
   - Logstash: For log collection and processing
   - Kibana: For log visualization and analysis

2. **Prometheus & Grafana**
   - Prometheus: For metrics collection and storage
   - Grafana: For metrics visualization and dashboard automation
   - Alertmanager: For handling alerts and notifications

## Prerequisites

- Docker and Docker Compose
- At least 4GB of RAM available
- 20GB of free disk space

## Quick Start

1. Clone this repository
2. Run the following command to start all services:
   ```bash
   docker-compose up -d
   ```
3. Access the services:
   - Kibana: http://localhost:5601
   - Grafana: http://localhost:3000
   - Prometheus: http://localhost:9090
   - Alertmanager: http://localhost:9093

## Configuration

### ELK Stack
- Elasticsearch runs on port 9200
- Logstash runs on port 5044 (TCP) and 5044 (UDP)
- Kibana runs on port 5601

### Prometheus & Grafana
- Prometheus runs on port 9090
- Grafana runs on port 3000
- Alertmanager runs on port 9093

## Alert Configuration

Alerts are configured to trigger on:
- Container failures
- High CPU usage (>80%)
- High memory usage (>80%)
- High disk usage (>85%)

## Dashboard Automation

Grafana dashboards are automatically created using the provided configuration files in the `grafana/provisioning` directory.

## Monitoring

The system monitors:
- Container health
- Resource usage (CPU, Memory, Disk)
- Application logs
- System metrics

## Maintenance

To update configurations:
1. Modify the respective configuration files
2. Restart the affected services:
   ```bash
   docker-compose restart [service-name]
   ```

## Troubleshooting

1. Check service logs:
   ```bash
   docker-compose logs [service-name]
   ```
2. Verify service status:
   ```bash
   docker-compose ps
   ```
3. Check service health endpoints:
   - Elasticsearch: http://localhost:9200/_cluster/health
   - Prometheus: http://localhost:9090/-/healthy
   - Grafana: http://localhost:3000/api/health 
>>>>>>> f915e58 (Initial commit)
