# Centralized Log Management Stack (ELK with Docker Compose)

This project implements a centralized log management system using Docker Compose.
It is used to collect, process, store, and visualize logs from servers or custom applications in one central place.

---

## Project Overview

The objective of this project is to centralize logs for effective monitoring and troubleshooting.
The complete log pipeline is built using the ELK stack with Filebeat.

---

## Technology Stack

- Docker
- Docker Compose
- Elasticsearch
- Logstash
- Kibana
- Filebeat
- AWS EC2 (Linux)

---

## Project Structure

centralized-log-stack/
│
├── docker-compose.yml
├── logstash/
│   └── logstash.conf
├── filebeat/
│   └── filebeat.yml
└── README.md

---

## Architecture & Data Flow

Application / System Logs  
        ↓  
     Filebeat  
        ↓  
     Logstash  
        ↓  
  Elasticsearch  
        ↓  
      Kibana  

---

## Prerequisites

- Docker installed
- Docker Compose installed
- Linux server or AWS EC2 instance
- Required ports open in Security Group:
  - 22 (SSH)
  - 5601 (Kibana)
  - 9200 (Elasticsearch)
  - 5044 (Logstash)

---

## Deployment Steps

1. Clone the repository
   git clone https://github.com/<your-username>/centralized-log-management-stack.git
   cd centralized-log-management-stack
2. Start the services
   docker-compose up -d
3. Verify running containers
   docker ps

## Access Services
   Kibana UI: http://:5601
   Elasticsearch API: http://:9200

## Features
   Centralized log collection
   Real-time log monitoring
   Easy log searching and filtering
   Docker-based deployment
   Scalable and reusable setup 
## Use Cases
   Application log monitoring
   System log analysis
   DevOps monitoring implementation
   Production issue troubleshooting  
