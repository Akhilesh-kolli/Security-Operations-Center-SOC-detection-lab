## suspicious Network Connection Detection



\## Log Source

Sysmon Event Logs



\## Event ID

Sysmon Event ID 3 (Network Connection)



\## Description

Detects processes establishing outbound network connections from a Windows endpoint.  

This behavior can indicate reverse shells, command-and-control communication, or unauthorized network activity.



\## Detection Query



index=sysmon EventCode=3

| table \_time host Image DestinationIp DestinationPort



\## Attack Simulation



Simulated outbound connection from the Windows endpoint to the Kali attacker machine.



Kali listener:



nc -lvnp 4444



Windows connection test:



Test-NetConnection 192.168.0.13 -Port 4444



\## Expected Logs



Sysmon Event ID 3 will log the network connection, including:



\- Source process


## Detection Logic

Malware, reverse shells, and command-and-control (C2) frameworks often establish
outbound network connections from compromised endpoints to attacker-controlled
servers.

This detection monitors Sysmon network connection events (Event ID 3) to identify
processes initiating outbound connections from the host.

By analyzing the process name, destination IP address, and destination port,
SOC analysts can identify suspicious communication patterns such as reverse
shell connections, unauthorized remote access attempts, or malware beaconing
activity.

Unusual processes communicating with external systems should be investigated
further to determine if the activity is legitimate or indicative of compromise.


## MITRE ATT&CK Mapping

Technique: T1071 – Application Layer Protocol  
Tactic: Command and Control



\- Destination IP

\- Destination port

