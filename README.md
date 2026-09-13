# Nexora Dynamics Incident Investigation

**Academic Cybersecurity Investigation | Simulated Enterprise Environment**

## Overview
This portfolio project documents an academic investigation of a simulated enterprise compromise at the fictional organization Nexora Dynamics. The scenario begins with a targeted spear-phishing attack against a contractor and develops into a multi-stage intrusion involving malicious PowerShell execution, credential theft, privilege escalation, lateral movement, persistence, command-and-control activity, data exfiltration, and log wiping.

## Objective
Reconstruct the attack sequence, identify the security-control failures that allowed the compromise to expand, assess the operational impact, and recommend containment and long-term remediation measures.

## Skills Demonstrated
- Incident investigation and triage
- Attack-chain reconstruction
- Network and log analysis
- Windows security analysis
- Endpoint forensic reasoning
- Credential-theft and lateral-movement analysis
- Root-cause analysis
- Security-control evaluation
- Technical reporting

## Evidence Sources Considered
- Firewall and router logs
- Network traffic monitoring
- Threat-intelligence sources
- Load-balancer monitoring
- DNS and email-server logs
- Authentication and system logs
- Endpoint forensic evidence

## Investigation Highlights
The simulated compromise began with a malicious macro-enabled document delivered through spear phishing. Execution of a PowerShell script established unauthorized remote access. Credential dumping and cached administrator credentials enabled privilege escalation. The attacker then used RDP and SMB, including pass-the-hash techniques, for lateral movement; scheduled tasks for persistence; Nmap for internal reconnaissance; encrypted command-and-control communications; and later data exfiltration and log wiping.

## Key Findings
The investigation identified several systemic weaknesses that amplified the incident:
- Cached administrative credentials and weak privileged-access governance
- Insufficient network segmentation
- Limited endpoint detection and centralized log correlation
- Weak monitoring of privilege escalation and command-and-control activity
- Patch and vulnerability-management gaps

## Recommendations
Recommended improvements include MFA, EDR, application control, stronger firewall and rate-limiting controls, network segmentation, restricted RDP access, IDS/IPS, centralized SIEM monitoring, automated patch management, regular vulnerability assessments, incident-response exercises, penetration testing, and phishing simulations.

## Repository Contents
- `report/` - polished portfolio version of the investigation report
- `analysis/attack-chain.md` - concise reconstruction of the intrusion
- `analysis/findings.md` - major findings and root causes
- `analysis/mitre-attack-mapping.md` - conservative ATT&CK-oriented mapping based on scenario behavior
- `iocs/indicators-of-compromise.md` - IOC categories supported by the scenario

## Important Scope Note
This was completed as academic coursework in a simulated environment. Nexora Dynamics, its personnel, systems, and incident are fictional scenario elements. The repository does not represent professional incident-response employment or a real client engagement.

## Attribution Note
The original coursework considered possible threat-actor attribution. This portfolio version emphasizes observable tactics, techniques, and procedures instead. The scenario evidence does not support definitive attribution to a specific real-world threat actor.
