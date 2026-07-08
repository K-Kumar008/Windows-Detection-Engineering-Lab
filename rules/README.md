# Sigma Rules Documentation

## Overview

This directory contains Sigma detection rules developed as part of the Windows Detection Engineering Lab.

The rules are designed to detect common attacker techniques using Windows Sysmon telemetry.

All rules were created for learning, testing, and demonstrating detection engineering concepts.

---

# Rule List

## 1. mimikatz.yml

**Purpose**

Detects execution of the Mimikatz credential dumping tool.

**Log Source**

- Sysmon Event ID 1
- Process Creation

**Detection**

Looks for process execution where the executable name contains `mimikatz.exe`.

**Severity**

High

**Reason**

Mimikatz is commonly used by attackers to dump Windows credentials from memory.

---

## 2. powershell_executionpolicy.yml

**Purpose**

Detects PowerShell launched with the `-ExecutionPolicy Bypass` argument.

**Log Source**

- Sysmon Event ID 1

**Detection**

Checks for:

- PowerShell executable
- Command line containing `ExecutionPolicy`
- Command line containing `Bypass`

**Severity**

Medium

**Reason**

ExecutionPolicy Bypass is frequently used by attackers to execute scripts without restriction, but it may also be used by administrators.

---

## 3. powershell_encoded.yml

**Purpose**

Detects PowerShell executed with an encoded command.

**Log Source**

- Sysmon Event ID 1

**Detection**

Looks for:

- PowerShell executable
- Command line containing `-EncodedCommand`

**Severity**

High

**Reason**

Encoded PowerShell commands are commonly used to hide malicious scripts and evade detection.

---

## 4. cmd_to_powershell.yml

**Purpose**

Detects PowerShell launched from Command Prompt.

**Log Source**

- Sysmon Event ID 1

**Detection**

Checks for:

- Image = powershell.exe
- ParentImage = cmd.exe

**Severity**

Medium

**Reason**

Although administrators may launch PowerShell from Command Prompt, attackers frequently use this process chain during post-exploitation.

---

## 5. powershell_network.yml

**Purpose**

Detects outbound network connections initiated by PowerShell.

**Log Source**

- Sysmon Event ID 3
- Network Connection

**Detection**

Looks for network activity where the process is PowerShell.

**Severity**

Medium

**Reason**

PowerShell communicating over the network may indicate downloading payloads, command-and-control communication, or data exfiltration. Additional investigation is required.

---

## 6. powershell_file_creation.yml

**Purpose**

Detects files created by PowerShell.

**Log Source**

- Sysmon Event ID 11
- File Creation

**Detection**

Monitors file creation events where PowerShell is the creating process.

**Severity**

Medium

**Reason**

PowerShell is frequently used to create scripts, drop malware, or write temporary files. Context determines whether the activity is malicious.

---

## 7. registry_persistence.yml

**Purpose**

Detects registry modifications performed by PowerShell.

**Log Source**

- Sysmon Event ID 13
- Registry Modification

**Detection**

Looks for registry changes initiated by PowerShell.

**Severity**

High

**Reason**

Registry modifications may indicate persistence, configuration changes, or malware installation. Legitimate administrative activity should be ruled out before escalation.

---

# Investigation Guidance

When any Sigma rule generates an alert:

1. Review the complete Sysmon event.
2. Verify the full command line.
3. Identify the parent process.
4. Determine which user executed the process.
5. Correlate related Event IDs.
6. Review EDR telemetry.
7. Review Windows Event Logs.
8. Review DNS, proxy, and firewall logs if network activity is involved.
9. Determine whether the activity is expected or suspicious.
10. Escalate only if additional evidence supports malicious activity.

---

# Lessons Learned

Through developing these Sigma rules, the following skills were practiced:

- Windows Event Analysis
- Sysmon Telemetry
- Sigma Rule Development
- Detection Engineering
- PowerShell Analysis
- Incident Investigation
- False Positive Analysis
- Event Correlation
- SOC Investigation Workflow

---

# Future Improvements

Future versions of these rules may include:

- Additional detection conditions
- Improved false positive filtering
- MITRE ATT&CK mappings
- More Windows Event IDs
- Detection for LOLBins
- Scheduled Task monitoring
- Service creation detection
- WMI detection
- Lateral movement detection
