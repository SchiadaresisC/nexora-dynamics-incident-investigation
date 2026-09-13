# Attack Chain

This reconstruction is based on the simulated evidence described in the academic report.

1. **Initial Access** - A contractor received a targeted spear-phishing email containing a malicious macro-enabled document.
2. **Execution** - Opening the document triggered a PowerShell script that downloaded additional payloads and established a reverse shell.
3. **Credential Access / Privilege Escalation** - Credential-dumping activity extracted passwords or hashes; cached administrator credentials accelerated privilege escalation.
4. **Lateral Movement** - Stolen credentials were used with RDP and SMB. The scenario later included pass-the-hash activity.
5. **Persistence** - Scheduled tasks were created on multiple systems to re-execute tooling.
6. **Discovery** - Nmap-style internal scanning identified hosts, ports, services, and higher-value targets.
7. **Command and Control** - Encrypted outbound traffic was consistent with command-and-control activity, including scenario references to Cobalt Strike infrastructure.
8. **Defense Evasion** - Security tools and services were disabled on multiple machines.
9. **Impact / Exfiltration** - Later phases included large-scale data exfiltration and log wiping.

## Analyst Takeaway
The phishing event provided the initial foothold, but the broader compromise depended on failures in credential governance, segmentation, endpoint detection, and centralized monitoring.
