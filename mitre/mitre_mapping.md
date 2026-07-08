# MITRE ATT&CK Mapping

## Project

Windows Detection Engineering Lab

Author: Krishna Kumar

---

# Purpose

This document maps the Sigma detection rules developed during this project to the MITRE ATT&CK Framework.

The mapping helps analysts understand which attacker techniques are detected by each Sigma rule.

---

# Detection Mapping

| Sigma Rule | Sysmon Event ID | MITRE Technique | Technique ID | Tactic |
|------------|-----------------|-----------------|--------------|---------|
| PowerShell Execution Policy Bypass | Event ID 1 | PowerShell | T1059.001 | Execution |
| Encoded PowerShell Command | Event ID 1 | PowerShell | T1059.001 | Execution |
| CMD to PowerShell | Event ID 1 | Command and Scripting Interpreter | T1059 | Execution |
| PowerShell Network Connection | Event ID 3 | Application Layer Protocol | T1071 | Command and Control |
| PowerShell File Creation | Event ID 11 | Data Staged | T1074 | Collection |
| Registry Persistence | Event ID 13 | Registry Run Keys / Startup Folder | T1547.001 | Persistence |
| Mimikatz Detection | Event ID 1 | OS Credential Dumping | T1003 | Credential Access |

---

# Event Coverage

## Event ID 1
Process Creation

Purpose:
Detect process execution and suspicious command-line arguments.

Rules:
- PowerShell Execution Policy
- Encoded PowerShell
- CMD to PowerShell
- Mimikatz

---

## Event ID 3
Network Connection

Purpose:
Detect outbound network communication initiated by suspicious processes.

Rules:
- PowerShell Network Connection

---

## Event ID 11
File Creation

Purpose:
Detect files created by suspicious processes.

Rules:
- PowerShell File Creation

---

## Event ID 13
Registry Modification

Purpose:
Detect registry modifications that may indicate persistence or configuration changes.

Rules:
- Registry Persistence

---

# ATT&CK Tactics Covered

- Execution
- Persistence
- Credential Access
- Collection
- Command and Control

---

# Summary

This project demonstrates detection coverage for multiple stages of the MITRE ATT&CK framework using Sysmon telemetry and Sigma rules.

The implemented detections focus on identifying suspicious PowerShell execution, process creation, network communication, file creation, registry modification, and credential dumping activities.

Additional ATT&CK techniques can be added as the detection library expands.





One Small Correction

Earlier, I used Data Staged (T1074) for the file creation example. On reflection, that's not the best mapping for a generic "PowerShell created a file" detection.

A more accurate approach is:

Keep PowerShell Execution mapped to T1059.001.
Keep Registry Persistence mapped to T1547.001 when the registry modification is specifically for persistence.
Keep Mimikatz mapped to T1003.
For generic file creation, avoid assigning a specific ATT&CK technique unless the file creation is tied to a known attacker behavior (for example, dropping a payload or staging data). In professional detection engineering, it's better to avoid overly specific mappings when the evidence doesn't justify them.

That's another important lesson: MITRE mappings should reflect the behavior you're actually detecting, not just the event type.
