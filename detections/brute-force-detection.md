## Brute Force Login Detection



\## Log Source

Windows Security Event Logs



\## Event ID

4625 (Failed Login)



\## Description

Detects multiple failed login attempts from a single IP address which may indicate a brute-force attack against a Windows host.



\## Detection Query



index=windows EventCode=4625

| stats count by Source\_Network\_Address

| where count >= 5



\## Attack Simulation



Attack simulated from Kali Linux using repeated SMB login attempts.



Example command used:



smbclient //192.168.0.13/C$ -U administrator%wrongpass



\## Expected Logs


## Detection Logic

This rule identifies potential brute-force attacks by detecting multiple
failed authentication attempts from the same source IP address within
a short time window.

Attackers often attempt multiple password combinations when trying to
compromise accounts via SMB or RDP authentication.

## MITRE ATT&CK Mapping

Technique: T1110 – Brute Force  
Tactic: Credential Access



Windows Security Event ID 4625 will be generated for each failed login attempt.

