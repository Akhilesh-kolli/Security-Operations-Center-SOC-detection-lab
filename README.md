# SOC Threat Detection & Incident Response Lab

<p align="center">
  <img src="https://img.shields.io/badge/SOC-Threat_Detection-blue">
  <img src="https://img.shields.io/badge/SIEM-Splunk-green">
  <img src="https://img.shields.io/badge/Endpoint-Sysmon-brightgreen">
  <img src="https://img.shields.io/badge/Attack-Simulation-orange">
  <img src="https://img.shields.io/badge/Kali-Linux-red">
  <img src="https://img.shields.io/badge/Logs-Windows_Event_Logs-yellow">
  <img src="https://img.shields.io/badge/Incident-Response-darkblue">
  <img src="https://img.shields.io/badge/VMware-LabEnvironment-purple">
</p>

---

# Project Overview

This project is a SOC (Security Operations Center) Threat Detection and Incident Response Lab developed in a virtualized cybersecurity environment.

The lab simulates real-world cyber attack scenarios using Kali Linux as the attacker machine and Windows as the target system. Sysmon is used for endpoint telemetry generation, while Splunk is used as the SIEM platform for centralized log monitoring, threat hunting, and incident investigation.

The primary objective of the project is to analyze attacker behavior, detect malicious activities through security monitoring, and understand SOC workflows used in real-world security operations.

---

# Objectives

- Simulate cyber attacks in a controlled environment
- Monitor endpoint activity using Sysmon
- Analyze logs using Splunk SIEM
- Detect suspicious attacker behavior
- Perform incident investigation workflows
- Understand SOC threat detection processes
- Develop detection queries for malicious activity
- Analyze attacker tactics and techniques

---

# Lab Environment

| Component | Purpose |
|---|---|
| Kali Linux | Attack simulation |
| Windows VM | Victim machine |
| Splunk | SIEM platform |
| Sysmon | Endpoint telemetry |
| VMware | Virtual lab environment |

---

# Technologies Used

| Category | Technologies |
|---|---|
| Operating Systems | Kali Linux, Windows |
| SIEM Platform | Splunk |
| Endpoint Monitoring | Sysmon |
| Virtualization | VMware |
| Log Analysis | Windows Event Logs |
| Scripting | Python, PowerShell |

---

# Attack Simulations Performed

The following activities were simulated in the lab environment:

- Port scanning
- Enumeration
- Reverse shell execution
- Suspicious PowerShell execution
- Brute-force login attempts
- Unauthorized command execution
- Process monitoring
- Privilege escalation testing

---

# Detection Workflow

```text
Kali Linux Attacker
          ↓
Attack Simulation
          ↓
Windows Target System
          ↓
Sysmon Event Generation
          ↓
Windows Event Logs
          ↓
Splunk Log Ingestion
          ↓
Threat Detection & Analysis
```

---

# Sysmon Monitoring

Sysmon was configured to monitor:

- Process creation events
- Network connections
- PowerShell activity
- File creation events
- Registry modifications
- Command-line execution
- Parent-child process relationships

These logs were forwarded to Splunk for centralized monitoring and analysis.

---

# Splunk Analysis

Splunk was used for:

- Security event monitoring
- Threat hunting
- Detection query creation
- Attack timeline analysis
- Log investigation
- Suspicious process analysis
- Incident response investigation

---

# Detection Use Cases

- Detecting PowerShell abuse
- Monitoring suspicious commands
- Identifying brute-force activity
- Tracking reverse shell execution
- Detecting abnormal network behavior
- Monitoring unauthorized process execution

---

# Project Structure

```text
SOC-Threat-Detection-Lab/
│
├── screenshots/
├── reports/
├── splunk_queries/
├── sysmon_configs/
├── attack_simulations/
├── scripts/
├── README.md
└── requirements.txt
```

---

# Installation & Setup

## 1. Configure Virtual Machines

- Create Kali Linux VM
- Create Windows VM
- Configure networking between VMs

## 2. Install Sysmon

Install Sysmon on the Windows machine using Sysinternals tools.

## 3. Install Splunk

Install Splunk Enterprise or Splunk Free Edition.

## 4. Configure Logging

- Enable Windows Event Logging
- Configure Sysmon event collection
- Forward logs to Splunk

## 5. Perform Attack Simulation

Run controlled attack simulations from Kali Linux.

## 6. Analyze Logs

Use Splunk dashboards and search queries to investigate attack activity.

---

# Learning Outcomes

Through this project:

- Understood SOC operations workflow
- Performed SIEM-based monitoring
- Practiced threat hunting techniques
- Learned endpoint telemetry analysis
- Improved incident response understanding
- Developed attack detection logic
- Analyzed attacker behavior and techniques

---

# Future Enhancements

- ELK Stack integration
- Advanced threat correlation
- Automated alert generation
- Sigma rule integration
- Real-time SOC dashboards
- Network traffic analysis
- IDS/IPS integration

---

# Author

## Akhilesh Kolli

Cybersecurity | SOC Analysis | Threat Detection | Incident Response

GitHub:
https://github.com/Akhilesh-kolli

---

# License

This project is intended for educational and cybersecurity research purposes.
