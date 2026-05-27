# Azure Cloud Computing & Infrastructure Portfolio

**Student Name:** Jashika Sahu  
**Platform:** Microsoft Azure  
**Domain:** Cloud Infrastructure & Architecture

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
5. **Apache Web Server Deployment:** Initialized, updated, and activated the Apache HTTP server components within the Linux environment:
   ```bash
   sudo apt update
   sudo apt install apache2 -y
   sudo systemctl start apache2
   sudo systemctl enable apache2
6. **Website Hosting:** Validated successful public web hosting by accessing the cloud instance's Public IP address and verifying the Apache welcome landing page.

---

## 📂 Project 2: High Availability Architecture Using Azure Availability Sets

### 📌 Objective
To design and implement a highly resilient and available cloud infrastructure using Azure Availability Sets, integrate virtual machine instances, automate server initialization via startup scripts (User Data), handle security maintenance, and perform vertical resource scaling.

### 🛠️ Key Architectural Components
* **Availability Set Name:** `MyAS`
* **Fault Domains:** `2` *(Hardware failure protection across racks)*
* **Update Domains:** `5` *(Scheduled maintenance downtime protection)*
* **Instance Size:** `Standard_B1s`
* **Subscription ID:** `772ad338-xxxx-xxxx-xxxx-xxxxxxxxxxxx` *(Masked for Security)*

### 🚀 Step-by-Step Implementation

1. **Availability Set (AS) Configuration:** Provisioned an Availability Set named `MyAS` on the Microsoft Azure Portal to eliminate single-points-of-failures and satisfy enterprise uptime SLA standards.
2. **VM Integration:** Deployed the active virtual machine instance under the constraints of the configured availability domain structure, ensuring physical isolation across data center hardware.
3. **Automated User Data Injection:** Injected custom bash startup/configuration scripts during the initial provisioning phase to automate software deployment tasks upon the first boot of the server.
4. **Security & Administrative Control:** Executed and validated administrative operations by leveraging Azure's built-in security features to test password reset mechanisms on the active deployment.
5. **Vertical Scaling (Instance Resizing):** Demonstrated infrastructure flexibility and scaling techniques by modifying the compute capacity and tier of the running instance dynamically to accommodate changing production workloads.

---

### 📸 Project Deployment Proof
![Apache Web Server Live](./apache-proof.jpeg)

---

## 📁 Project Source Documents
* Detailed step-by-step screenshots and laboratory proofs are organized in the folders below:
  * [Assignment 1 - VM & Web Hosting Docs](./Assignment-1-VM-Deployment/)
  * [Assignment 2 - Availability Sets Docs](./Assignment-2-Availability-Sets/)
