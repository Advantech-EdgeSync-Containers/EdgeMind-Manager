# DeviceOn-EIM Overview
DeviceOn-EIM(**E**dge **I**ntelligence **M**anagement) is a one-stop industrial IoT solution dedicated to addressing remote device management, device monitoring and operation & maintenance, as well as industrial data collection and visualization. The
management interface is web-based, offering a simple, convenient, and feature-rich experience that is easy to
integrate. It effectively enhances the management and maintenance efficiency of edge devices in industrial
environments, significantly reducing operational costs.
<img width="1920" height="1080" alt="EIM-1" src="https://github.com/user-attachments/assets/fa9c8b46-0f61-4a26-a57c-93581360ebea" />
<img width="1920" height="1080" alt="EIM-2" src="https://github.com/user-attachments/assets/b31e77c4-fdc5-4cd5-b47c-6fa0bbcdcfea" />
<img width="1920" height="1080" alt="EIM-3" src="https://github.com/user-attachments/assets/3f03fbed-58e9-4bf8-92e2-74ebcd63ae08" />

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

# Contact

If you are interested in this project, have questions, or would like to discuss potential collaborations, feel free to reach out via email:

**Email:** [jianfeng.dai@advantech.com.cn](mailto:jianfeng.dai@advantech.com.cn)

We welcome feedback, suggestions, and collaboration！
