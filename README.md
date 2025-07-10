# Virtual-Home-Lab-
A virtual home lab built using VirtualBox for learning cybersecurity, network setup and hands on configuration.
# 🛡 My Cybersecurity Home Lab

## 🔍 Overview
This is a beginner friendly cybersecurity home lab I built using VirtualBox to simulate a real world network environment. It’s designed to help me practice log analysis, system monitoring, and other blue-team skills in a hands-on way.
---

## 🧱 Lab Structure

| Group        | Machines                             | Purpose                             |
|--------------|---------------------------------------|-------------------------------------|
| *Operation*| HR PC, Audit PC, Sales PC, Server     | Simulate internal company network   |
| *IT*       | Kali Linux, Parrot OS, Ubuntu         | Tools for monitoring and simulation |
| *Firewall* | pfSense                               | Will segment and protect the network|

---

## 🌐 Network Design

- All machines are connected through *NAT Network* 
- This allows all Windows VMs to stay on the same subnet 
- Machines are grouped logically under:
  - *Operation*: HR, Sales, Audit, Windows Server
  - *IT*: Kali, Ubuntu, Parrot OS
- *pfSense* will be added to segment traffic between internal zones (Operation ↔ IT)

---

## ⚙ Tools Used

- *Oracle VirtualBox* (Virtualization platform)
- *Windows 8.1* for HR, Sales, Audit
- *Windows Server* for central services
- *Ubuntu* for log collection and SIEM setup (in future)
- *Kali Linux* and *Parrot OS* for red/blue team simulation
- *pfSense* (for firewall and network segmentation)

---

## 🛠 How I Built the Lab

### 1. 📥 Downloads

| OS           | Download Link |
|--------------|---------------|
| *VirtualBox* | [https://www.virtualbox.org](https://www.virtualbox.org) |
| *Windows 8.1 ISO* | [https://www.microsoft.com/en-us/software-download/windows8ISO](https://www.microsoft.com/en-us/software-download/windows8ISO) |
| *Windows Server 2022* | [https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2022](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2022) |
| *Ubuntu ISO* | [https://ubuntu.com/download/desktop](https://ubuntu.com/download/desktop) |
| *Kali Linux ISO* | [https://www.kali.org/get-kali/](https://www.kali.org/get-kali/) |
| *Parrot OS ISO* | [https://www.parrotsec.org/download/](https://www.parrotsec.org/download/) |
| *pfSense ISO* | [https://www.pfsense.org/download/](https://www.pfsense.org/download/) |

---

### 2. 🖥 Installing the VMs

#### ✅ Step-by-Step Setup for Each Machine

1. *Create New VM in VirtualBox*
   - Open VirtualBox → Click *"New"*
   - Name: e.g., "HR-PC" or "Ubuntu-LogServer"
   - Type: Microsoft Windows or Linux (depending on ISO)
   - Version: Select matching version (e.g., Windows 8.1, Ubuntu 64-bit)

2. *Assign Resources*
   - RAM: 2GB–4GB (depending on your PC’s total RAM)
   - CPU: 1–2 Cores
   - Storage: 30GB or more (VDI or VHD format)

3. *Attach ISO File*
   - Under *Settings → Storage* → Click the empty optical drive
   - Choose “Choose a Disk File” and select your ISO
   - Save settings

4. *Install the OS*
   - Start the VM and follow the installation steps as you would on a physical PC
   - For Windows:
     - Choose language and partition setup
     - Use default credentials (e.g., admin / your password)
   - For Linux:
     - Choose installation options, username, timezone
     - Accept default partitioning and complete setup

5. *Set Up NAT Network*
   - In *VirtualBox → Preferences → Network → NAT Networks*
   - Create a NAT Network and name it (e.g., SOC-Network)
   - Assign this network to all VMs under *Settings → Network → Adapter 1 → NAT Network*

6. *Group VMs*
   - Drag and drop related VMs under labels like “Operation” and “IT”
   - Helps keep the lab visually organized

---

## 🧱 Next Steps (Planned)

- ✅ Finish VM installations
- 🔜 Install and configure *pfSense* firewall
- 🔜 Assign static IPs and segment networks (Operation ↔ IT)
- 🔜 Start sending logs and monitoring systems
- 🔜 Run basic attacks using Kali and detect them using Ubuntu

---

## 👤 About Me

*Abiodun Alamin* (aka Bibi)  
Cybersecurity Beginner | SOC Analyst in Training  
This repo documents my learning journey in building a full virtual home lab from scratch.

📍 Based in Nigeria  
🔗 Let’s connect on [LinkedIn](#https://www.linkedin.com/in/
biodun-alameen-)


---

## 📎 License

*MIT License*  
