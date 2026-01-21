# Active Directory Lab – 2 Domain Controllers & 1 Client

This repository contains documentation for an Active Directory lab environment. The lab consists of two domain controllers for redundancy and a Windows client joined to the domain.

The purpose of the lab is to demonstrate both basic and advanced AD concepts such as domain structure, replication, DNS, and client integration.

---

## 🧱 Lab Architecture

| Machine | Role | Operating System |
|--------|------|-----------------|
| DC01   | Primary Domain Controller | Windows Server |
| DC02   | Secondary Domain Controller | Windows Server |
| CLIENT01 | Domain-joined Client | Windows 10/11 |

**Domain Name:** `lab.local`  
**Forest Functional Level:** Windows Server  
**Domain Functional Level:** Windows Server  

---

## 🎯 Lab Objectives

- Install and configure Active Directory Domain Services (AD DS)  
- Create a redundant AD environment with two domain controllers  
- Configure DNS for internal name resolution  
- Join a client to the domain  
- Verify AD replication between domain controllers  

---

## 🛠 Prerequisites

- Hypervisor (e.g., Hyper-V, VMware, or VirtualBox)  
- ISO images for:
  - Windows Server (2019/2022)
  - Windows 10 or Windows 11
- Basic knowledge of Windows Server and networking

---

## ⚙️ Installation & Configuration

### 1. Domain Controller 1 (DC01)
- Installed **Active Directory Domain Services**  
- Created a new forest and domain (`lab.local`)  
- Installed and verified DNS  
- Restarted after installation

### 2. Domain Controller 2 (DC02)
- Joined the domain `lab.local`  
- Installed AD DS  
- Promoted to additional domain controller  
- Verified DNS replication  

### 3. Client (CLIENT01)
- Configured DNS to point to DC01/DC02  
- Joined the domain  
- Successfully logged in with a domain account  

---

## 🔄 Replication & Verification

- AD replication verified between DC01 and DC02  
- DNS zones synchronized correctly  
- Client can authenticate against both DCs  

Common commands used:
- `dcdiag`  
- `repadmin /replsummary`  
- `nslookup`  

---

## 📸 Screenshots

> *(Optional – add screenshots here)*  
Examples:
- AD Users and Computers  
- DNS Manager  
- Client login  

---

## 🧹 Cleanup / Reset

- Client can be removed from the domain  
- DC02 can be demoted if needed  
- Lab can be easily recreated using snapshots  

---

## 📝 Notes

- The lab is intended for educational and testing purposes  
- No production traffic or external services are used  
- All accounts and passwords are for lab use only  

---

## 📄 License

This project is free to use for educational and demonstration purposes.
