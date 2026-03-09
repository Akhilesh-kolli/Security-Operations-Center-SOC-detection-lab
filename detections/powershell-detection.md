## Suspicious PowerShell Execution Detection



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

## Detection Logic

Attackers frequently use PowerShell to execute malicious scripts on compromised
Windows systems. To evade detection, they often encode commands using Base64
with the `-enc` or `-EncodedCommand` parameter.

This detection monitors Sysmon process creation logs (Event ID 1) and identifies
instances where the PowerShell executable is launched. The command line
arguments are inspected to identify suspicious or encoded PowerShell commands.

By analyzing the command-line arguments associated with PowerShell execution,
SOC analysts can detect potentially malicious scripts, obfuscated payloads,
or unauthorized administrative activity on the endpoint.

## MITRE ATT&CK Mapping

Technique: T1059.001 – PowerShell  
Tactic: Execution



Sysmon Event ID 1 will log the process creation of powershell.exe including the encoded command in the CommandLine field.

