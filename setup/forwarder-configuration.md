\# Splunk Universal Forwarder Configuration



\## Configure Event Log Collection



Edit inputs.conf



\[WinEventLog://Security]

disabled = 0

index = windows



\[WinEventLog://Microsoft-Windows-Sysmon%4Operational]

disabled = 0

index = sysmon



\## Restart Forwarder



splunk restart

