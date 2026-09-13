# MITRE ATT&CK-Oriented Mapping

This is a conservative mapping of behaviors explicitly described in the simulated scenario. It is intended as a portfolio analysis aid, not a claim that every ATT&CK technique was independently validated from raw telemetry.

| Scenario Behavior | ATT&CK Tactic / Technique Family |
|---|---|
| Targeted spear-phishing email with malicious attachment | Initial Access - Phishing |
| Malicious macro launches PowerShell | Execution - Command and Scripting Interpreter: PowerShell |
| Credential-dumping tool used against memory | Credential Access - OS Credential Dumping |
| Stolen hashes used without cracking passwords | Lateral Movement / Credential Access - Pass the Hash |
| RDP used to access additional systems | Lateral Movement - Remote Services: RDP |
| SMB used for internal movement | Lateral Movement - Remote Services / SMB-related activity |
| Scheduled tasks used to maintain access | Persistence / Execution - Scheduled Task/Job |
| Nmap used to identify hosts, ports, and services | Discovery - Network Service Scanning |
| Encrypted outbound C2 traffic | Command and Control - Encrypted Channel |
| Security tools/services disabled | Defense Evasion - Impair Defenses |
| Data removed from the environment | Exfiltration |
| Logs wiped late in the intrusion | Defense Evasion - Indicator Removal / Clear Logs |

## Why the Mapping Is Conservative
The original report describes scenario behavior rather than supplying raw telemetry for every step. Accordingly, this file maps only behavior that is explicitly described and avoids inventing technique IDs or unsupported evidence.
