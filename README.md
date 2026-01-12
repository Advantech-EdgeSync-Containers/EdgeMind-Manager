# DeviceOn-EIM Overview
DeviceOn-EIM is a one-stop industrial IoT solution dedicated to addressing remote device management, device monitoring and operation & maintenance, as well as industrial data collection and visualization. The
management interface is web-based, offering a simple, convenient, and feature-rich experience that is easy to
integrate. It effectively enhances the management and maintenance efficiency of edge devices in industrial
environments, significantly reducing operational costs.
<img width="1920" height="1080" alt="屏幕截图(93)" src="https://github.com/user-attachments/assets/5446aa78-26b3-4ee4-ac58-75c91baa944f" />
<img width="1920" height="1080" alt="屏幕截图(91)" src="https://github.com/user-attachments/assets/5dda84b7-0892-4c4a-8cec-bb84bacb4154" />
<img width="1920" height="1080" alt="屏幕截图(92)" src="https://github.com/user-attachments/assets/68d420e1-cfc0-4253-a396-4e59915c58b3" />


# Demo

![DeviceOn EIM](https://github.com/user-attachments/assets/d7cc302f-3cdd-4c24-b0f4-fe0e3320db86)



# DeviceOn-EIM Deployment Guide

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
| 8024  | TCP       | Terminal              |

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
### 3.2 Deploy EIM Server
```bash
git clone https://github.com/Advantech-EdgeSync-Containers/DeviceOn-EIM.git
cd DeviceOn-EIM   
chmod +x  start.sh
# Execute installation (may take 10-20 minutes)
./start.sh 
```
> Note: The script will:
>  Pull Docker images
>  Configure container networks
>  Initialize database schemas

## 4. Accessing EIM Server
 After successful installation, access the web interface:  
`http://<SERVER_IP>:8080`  

You will see the login page with following default credentials: 

**Default Account**:  
- Username: `admin`  
- Password: `admin`  


