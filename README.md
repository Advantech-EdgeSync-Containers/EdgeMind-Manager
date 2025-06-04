# EdgeMind-Manager Overview
<img width="960" alt="EdgeMind-Manager" src="https://github.com/user-attachments/assets/a9ade67b-bfa7-4028-b705-a3957348d3c2" />
<img width="960" alt="EdgeMind-Manager-Diagram" src="https://github.com/user-attachments/assets/51685087-d58b-47c7-aa3c-0aacbff9849f" />
<img width="960" alt="EdgeMind-Manager-Server" src="https://github.com/user-attachments/assets/7228e421-25c2-42f6-8a06-8ec50043915e" />

# EdgeMind Manager Deployment Guide

## Supported Environments
Deployable to:
- On-premise Linux servers  
- Local virtual machines (VMs)  
- Cloud VMs (Alibaba Cloud, Microsoft Azure, AWS, etc.)  

## 1. System Requirements
### Minimum Specifications:
- **CPU**: 2 vCPU cores   
- **Memory**: 4GB RAM  
- **Storage**: 32GB SSD  
- **OS**: Ubuntu 18.04 or newer 

> Other Linux distributions also can be supported 

## 2. Network Configuration
### Required Open Ports:

| Port  | Protocol  | Service               |
|-------|-----------|-----------------------|
| 8080  | HTTP      | Web Interface         |
| 8082  | HTTP      | Message and ithing      |
| 30001 | HTTP      | For OTA               |
| 9000  | HTTP      | For OTA               |
| 1883  | TCP       | MQTT Broker           |
| 5500  | TCP       | VNC Server            |
| 9191  | Websocket | VNC                   |
| 8024,50500-50510  | TCP       | Terminal           |

## 3. Installation Procedure

### 3.1 Install Prerequisites
```bash
# Update system packages
sudo apt update && sudo apt upgrade

# Install Git
sudo apt install git

# Install Docker (official script)
curl -fsSL https://get.docker.com | sudo sh

# Install Docker-Compose
sudo apt install docker-compose

# Verify installations
docker --version
docker-compose version
```
### 3.2 Deploy EdgeMind-Manager
```bash
git clone https://github.com/Advantech-EdgeSync-Containers/EdgeMind-Manager.git
cd EdgeMind-Manager   
chmod +x  start.sh
# Execute installation (may take 10-20 minutes)
./start.sh 
```
> Note: The script will:
>  Pull Docker images
>  Configure container networks
>  Initialize database schemas

## 4. Accessing EdgeMind-Manager
 After successful installation, access the web interface:  
`http://<SERVER_IP>:8080`  

You will see the login page with following default credentials: 

**Default Account**:  
- Username: `admin`  
- Password: `admin`  


