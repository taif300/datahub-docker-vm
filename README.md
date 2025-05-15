# DataHub on Docker (VM Setup)

This project sets up [Acryl DataHub](https://datahubproject.io/) on a virtual machine using Docker and Docker Compose.

## ✅ Prerequisites

- Ubuntu VM
- Docker & Docker Compose installed
- Python 3.11 (optional if using CLI)
- Internet access

---

## 🚀 Quick Start

### 1. Clone this repository

```bash
git clone https://github.com/your-username/datahub-project.git
cd datahub-project
```
### 2. Run DataHub using Docker

`datahub docker quickstart`

## 🐳 Docker Ports Used

| Service       | Port |
| ------------- | ---- |
| Frontend (UI) | 9002 |
| GMS API       | 8080 |
| Elasticsearch | 9200 |
| Kafka         | 9092 |
| MySQL         | 3306 |


## Make sure these ports are allowed through your VM's firewall:

`sudo ufw allow 9002`
`sudo ufw allow 8080`
`sudo ufw allow 9200`
`sudo ufw allow 9092`
`sudo ufw allow 3306`

## Stopping DataHub

# To stop all containers:

`docker compose down`

# Or if you used the CLI:

`datahub docker nuke`

## Project Structure

datahub-project/
├── docker-compose.yml      # Docker configuration (auto-managed by CLI)
├── .datahub/               # Optional: ingestion configs, CLI settings
├── .gitignore              # Ignore virtual env and cache files
└── README.md               # You're reading it!

## Security Notes

Make sure to:

Disable root login via SSH
Disable password authentication
Use firewall (UFW) to restrict access to necessary ports only

## Credits

[DataHub](https://github.com/datahub-project/datahub)

Setup by Taif Alahmadi



