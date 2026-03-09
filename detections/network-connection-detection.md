\# Suspicious Network Connection Detection



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

\- Destination IP

\- Destination port

