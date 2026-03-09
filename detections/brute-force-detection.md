\# Brute Force Login Detection



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



Windows Security Event ID 4625 will be generated for each failed login attempt.

