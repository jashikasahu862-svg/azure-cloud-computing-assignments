# Azure Cloud Computing & Infrastructure Portfolio

**Student Name:** Jashika Sahu  
**Platform:** Microsoft Azure  
**Domain:** Cloud Infrastructure & Web Architecture

---

## 📂 Project 1: Azure Virtual Machine Deployment & Web Hosting

### 📌 Objective
To deploy a Linux Virtual Machine (Ubuntu) on Microsoft Azure, access it securely using SSH keys, configure an Apache Web Server, and host a custom HTML website accessible via a public IP address.

### 🛠️ Infrastructure Blueprint
* **Resource Group:** `RG-Practice-VM`
* **VM Name:** `PracticeVM`
* **Region:** `Central India`
* **Image:** `Ubuntu Linux 24.04 LTS`
* **Inbound Ports Allowed:** `SSH (22)`, `HTTP (80)`
* **Public IP Address:** `20.xxx.xx.xx` *(Masked for Security)*

### 🚀 Step-by-Step Implementation

1. **Resource Group Creation:** Logged into the Microsoft Azure Portal and provisioned a new resource group named `RG-Practice-VM` in the Central India region.
2. **Virtual Machine Provisioning:** Deployed an Ubuntu Linux Virtual Machine instance configured with SSH Key Pair authentication for enhanced root security.
3. **Network Security Group (NSG) Configuration:** Configured inbound security rules to allow traffic through Port 80 (HTTP) for public web access and Port 22 (SSH) for secure remote management.
4. **Server Access & Configuration:** Secured the private key file (`.pem`) and established a remote terminal connection to the cloud instance using the following commands:
   ```bash
   chmod 400 PracticeVM_key.pem
   ssh -i PracticeVM_key.pem azureuser@20.xxx.xx.xx
