# Findings and Root-Cause Analysis

## Primary Entry Vector
The scenario identifies spear phishing against a contractor as the initial access vector. A malicious macro-enabled document triggered PowerShell execution and unauthorized remote access.

## Systemic Weaknesses
### Cached Administrative Credentials
Administrative credentials were available on a contractor endpoint, allowing credential-dumping activity to accelerate privilege escalation.

### Weak Privilege Governance
The scenario describes inadequate role-based access control, no privileged-access-management system, and insufficient alerting for administrative-account changes.

### Inadequate Network Segmentation
RDP and SMB connectivity across weak internal boundaries enabled lateral movement after credentials were compromised.

### Insufficient Monitoring and Detection
Suspicious PowerShell execution, credential dumping, privilege escalation, and command-and-control activity were not detected quickly. The environment lacked centralized SIEM correlation.

### Patch and Vulnerability-Management Gaps
Weak configurations and incomplete patching/vulnerability-scanning practices increased the attack surface and complicated containment.

## Overall Conclusion
The incident was not caused by a single technical flaw. It was a defense-in-depth failure in which identity, endpoint, network, monitoring, and vulnerability-management weaknesses allowed an initial phishing compromise to develop into a broader intrusion.
