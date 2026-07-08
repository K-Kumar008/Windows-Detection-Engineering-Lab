# Windows Detection Engineering Lab

Author: Krishna Kumar

Platform:
Kali Linux 2026.1
Windows 11 Virtual Machine

Project Type:
Detection Engineering / SOC Lab

## Project Overview

The objective of this project was to build a Windows Detection Engineering lab using Kali Linux and Windows 11.

The project focused on collecting Windows telemetry using Sysmon, analyzing Windows event logs, developing Sigma detection rules, and performing SOC-style incident investigations.

The lab was designed to simulate common attacker behaviors while improving detection engineering and incident response skills.


## Objectives

• Learn Sysmon

• Understand Windows Event IDs

• Develop Sigma Rules

• Detect suspicious PowerShell activity

• Detect network connections

• Detect file creation

• Detect registry modifications

• Perform SOC investigations

• Improve detection engineering skills

## Lab Architecture

Draw it using Markdown.

               Internet
                    │
         ┌──────────────────┐
         │   Kali Linux VM  │
         │ Analyst Machine  │
         └──────────────────┘
                    │
            Virtual Network
                    │
         ┌──────────────────┐
         │ Windows 11 VM    │
         │ Sysmon Installed │
         └──────────────────┘
## Tools

Kali Linux

Windows 11

Python

Sigma CLI

Sysmon

Event Viewer

PowerShell

## Sysmon Events Studied

Create a table.

| Event ID | Description |
|----------|-------------|
| 1 | Process Creation |
| 3 | Network Connection |
| 11 | File Creation |
| 13 | Registry Modification |

## Detection Rules Developed

Another table.

| Rule | Purpose |
|------|---------|
| PowerShell ExecutionPolicy | Detect PowerShell Bypass |
| Encoded Command | Detect Encoded PowerShell |
| CMD → PowerShell | Detect suspicious parent process |
| Network Connection | Detect outbound connections |
| File Creation | Detect suspicious file creation |
| Registry Modification | Detect persistence attempts |
| Mimikatz | Detect credential dumping tool |


## Skills Demonstrated

Windows Log Analysis

Detection Engineering

Sigma Rule Development

Sysmon Configuration

Threat Detection

SOC Investigation

Event Correlation

PowerShell Analysis

Registry Analysis

Network Analysis

## Lessons Learned

This project improved my understanding of Windows telemetry and detection engineering.

I learned how Sysmon generates detailed process, network, file, and registry events.

I learned how Sigma rules detect attacker techniques while minimizing false positives.

I also learned the importance of correlating multiple events before classifying an incident and avoiding conclusions without sufficient evidence.


## Future Improvements

Deploy a SIEM platform

Integrate Sysmon with Splunk

Develop additional Sigma rules

Map detections to MITRE ATT&CK

Automate log analysis


# Windows Detection Engineering Lab

Author

Krishna Kumar

---

# Project Overview

This project demonstrates a Windows Detection Engineering lab developed using Kali Linux and a Windows 11 virtual machine.

The objective was to understand Windows telemetry, configure Sysmon, develop Sigma detection rules, investigate Windows events, and perform SOC-style incident analysis.

---

# Lab Environment

Analyst Machine

- Kali Linux 2026.1

Target Machine

- Windows 11

Virtualization

- Oracle VirtualBox

---

# Tools Used

- Sysmon
- Sigma CLI
- Python
- Event Viewer
- PowerShell

---

# Windows Events Investigated

- Event ID 1 – Process Creation
- Event ID 3 – Network Connection
- Event ID 11 – File Creation
- Event ID 13 – Registry Modification

---

# Detection Rules Developed

- PowerShell ExecutionPolicy Bypass
- Encoded PowerShell
- CMD to PowerShell
- PowerShell Network Activity
- File Creation Detection
- Registry Modification Detection
- Mimikatz Detection

---

# Skills Demonstrated

- Windows Log Analysis
- Detection Engineering
- Sigma Rule Development
- PowerShell Analysis
- Event Correlation
- Incident Investigation
- Threat Detection
- SOC Workflow

---

# Project Outcome

The project successfully demonstrated the use of Sysmon and Sigma for Windows threat detection and incident investigation.

The lab provided practical experience in analyzing Windows telemetry, developing detection logic, and performing evidence-based investigations.

---

# Future Improvements

- Integrate Splunk
- Integrate Microsoft Sentinel
- Deploy Sysmon to multiple endpoints
- Create additional Sigma rules
- Automate detection validation

Test against additional attack techniques

