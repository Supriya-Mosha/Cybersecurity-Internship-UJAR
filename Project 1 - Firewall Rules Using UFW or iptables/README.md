# Firewall Rules Using UFW or iptables

## 📌 Introduction
Firewalls are a fundamental component of network security, serving as the first line of defence between trusted systems and untrusted networks.  
This project demonstrates how to configure and test firewall rules on a Linux environment using **UFW (Uncomplicated Firewall)** or **iptables**.  

The objective is to allow only trusted services such as **SSH (port 22)** and **HTTP (port 80)**, while blocking all other connections. This enforces the principle of least privilege and reduces the attack surface.

---

## 🎯 Project Objectives
- Configure firewall rules using **UFW** or **iptables**  
- Enforce **default deny (incoming)** and **default allow (outgoing)** policies  
- Allow only essential services (SSH, HTTP)  
- Test configurations using **Nmap** and **ping**  
- Analyze logs to confirm blocked connection attempts  

---

## 🛠 Tools & Technologies
- **Linux (Ubuntu/Debian / Kali Linux)**  
- **UFW (Uncomplicated Firewall)**  
- **iptables**  
- **OpenSSH-Server**  
- **Nmap**  
- **Ping utilities**  
- **VirtualBox / VMware Workstation Player**  

---

## ⚙️ Steps Implemented

### 1. Environment Setup
- Installed Kali Linux/Ubuntu on VM (VirtualBox/VMware)  
- Configured virtual networking for safe testing  

### 2. Package Installation

sudo apt update && sudo apt full-upgrade -y
sudo apt install ufw openssh-server -y

### 3. Firewall Configuration

sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw allow ssh
sudo ufw allow 80/tcp
sudo ufw enable

### 4. Verification

sudo ufw status verbose

### 5. Testing with Nmap & Ping

nmap -p 22 <IP>    # Expected: open
nmap -p 80 <IP>    # Expected: open
nmap -p 21 <IP>    # Expected: filtered
ping <IP>          # Expected: timed out

---

## ✅ Results

Ports 22 (SSH) and 80 (HTTP) were accessible

Unauthorized ports were blocked/filtered

ICMP echo requests (ping) were successfully blocked

---


## 📚 Key Learnings

Importance of default-deny firewall posture

Hands-on experience with UFW/iptables

How to verify firewall rules using Nmap

Balancing security and availability in firewall design

---


## 📌 Conclusion

This project successfully demonstrated the setup and testing of firewall rules in Linux using UFW/iptables.
It highlights how firewalls reduce exposure to attacks by enforcing the principle of least privilege.
