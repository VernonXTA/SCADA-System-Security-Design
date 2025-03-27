# Water Treatment SCADA Security Design

## 📌 Project Overview
This project focuses on designing a **secure architecture** for a **Water Treatment Supervisory Control and Data Acquisition (SCADA) system**. The design follows the **Purdue Model**, integrating **defensive cybersecurity measures** to protect against cyber threats targeting industrial control systems (ICS).

## 🏗️ Architecture Breakdown
The SCADA system is structured according to the **Purdue Model**:

### **Level 0 – Physical Process**
- Sensors, actuators, and industrial control hardware.
- Monitors water treatment processes (e.g., flow rates, chemical dosing, pressure sensors).
- Connected to **Programmable Logic Controllers (PLC)/Distributed Control Systems (DCS)** for process automation.

### **Level 1 – Control Level**
- **Programmable Logic Controllers (PLC)** & **Distributed Control Systems (DCS)**.
- Real-time control of water treatment operations.
- Communication with Level 2 through industrial protocols (**Modbus**, **Distributed Network Protocol 3 (DNP3)**, **Open Platform Communications Unified Architecture (OPC UA)**).

### **Level 2 – Supervisory Control**
- **Supervisory Control and Data Acquisition (SCADA) servers** handling process visualization & data logging.
- **Human-Machine Interfaces (HMI)** for operators.
- Secure communication enforced via **firewalls** & **network segmentation**.

### **Level 3 – Operations & Control Center**
- **Historian servers** for long-term data storage.
- Engineering workstations for configuring PLCs/DCS.
- Application servers for alarms, trends, and reports.

### **Level 4 – Business Network**
- IT services supporting business operations (e.g., Customer Relationship Management (CRM), reporting tools).
- **Separation from operational technology (OT) using a Demilitarized Zone (DMZ)**.

### **Level 5 – Enterprise Network**
- **Corporate IT infrastructure** (email, databases, Enterprise Resource Planning (ERP) systems).
- Isolated from OT networks to prevent cross-domain attacks.

## 🔐 Security Measures Implemented
### **1️⃣ Network Segmentation & Firewalls**
- **Firewalls between each Purdue Model level** to control data flow.
- **DMZ for external access management**.
- VLANs (Virtual Local Area Networks) to isolate critical components.

### **2️⃣ Access Control & Authentication**
- **Role-Based Access Control (RBAC)** for operators & administrators.
- **Multi-Factor Authentication (MFA)** for SCADA system login.
- **Jump servers** for remote access with strict logging.

### **3️⃣ Intrusion Detection & Monitoring**
- **Intrusion Detection Systems/Intrusion Prevention Systems (IDS/IPS)** (e.g., Snort, Suricata) for real-time anomaly detection.
- **Security Information and Event Management (SIEM)** for centralized logging.
- **Honeypots** deployed to detect unauthorized access attempts.

### **4️⃣ Secure Protocols & Encryption**
- **Transport Layer Security (TLS) encryption** for SCADA communications.
- **Virtual Private Network (VPN) tunnels** for remote engineers accessing SCADA.
- **Disable legacy insecure protocols (e.g., Telnet, File Transfer Protocol (FTP))**.

### **5️⃣ Patch Management & System Hardening**
- Regular software & firmware updates for SCADA devices.
- **Least privilege principle** applied to all accounts.
- Disable unnecessary services & enforce security policies.

## 🏗️ Implementation & Testing
- **Test environment in VMware** to simulate SCADA security threats.
- Conducted **penetration testing** on PLCs & HMI.
- Validated **resilience against ransomware, phishing, and insider threats**.

## 🚀 Future Enhancements
- Implement **Artificial Intelligence (AI)-driven threat detection** for real-time anomaly detection.
- Deploy **zero-trust architecture** for critical assets.
- Strengthen incident response with **automated playbooks**.

## 📜 Conclusion
This SCADA security design ensures **robust protection** of water treatment systems against cyber threats while maintaining operational efficiency and regulatory compliance.

---
✍️ **Author:** Dante Worthington  
🔗 **GitHub:** [GitHub Repository](https://github.com/VernonXTA)  
📅 **Last Updated:** March 2025