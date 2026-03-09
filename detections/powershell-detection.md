\# Suspicious PowerShell Execution Detection



\## Log Source

Sysmon Event Logs



\## Event ID

Sysmon Event ID 1 (Process Creation)



\## Description

Detects suspicious PowerShell execution, including encoded commands often used by attackers to obfuscate malicious scripts.



\## Detection Query



index=sysmon EventCode=1 Image="\*powershell\*"

| table \_time host Image CommandLine



\## Attack Simulation



Suspicious encoded PowerShell command executed on the Windows endpoint.



Example command used:



powershell -enc aGVsbG8=



\## Expected Logs



Sysmon Event ID 1 will log the process creation of powershell.exe including the encoded command in the CommandLine field.

