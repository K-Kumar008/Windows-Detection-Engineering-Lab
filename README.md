# Windows-Detection-Engineering-Lab
Detection Engineering Lab using Kali Linux, Windows 11, Sysmon and Sigma.

> A hands-on Detection Engineering and SOC Analyst lab built from scratch using Kali Linux and Windows 11.

---

# Project Overview

This project demonstrates the design and implementation of a Windows Detection Engineering Lab using Kali Linux as the analyst workstation and a Windows 11 Virtual Machine as the target system.

The objective of the lab was to understand how Windows telemetry is generated, how Sysmon records security events, and how Sigma rules can be developed to detect suspicious attacker behavior.

Throughout this project, Windows attack simulations were performed in a controlled virtual environment, security logs were collected and analyzed, Sigma detection rules were developed, and SOC-style incident investigations were completed.

---

# Project Objectives

- Build a Windows Detection Engineering Lab
- Learn Sysmon architecture and configuration
- Analyze Windows Event Logs
- Understand important Sysmon Event IDs
- Develop Sigma detection rules
- Investigate attack chains
- Correlate multiple security events
- Reduce false positives
- Improve SOC investigation skills
- Understand Detection Engineering concepts

---

# Lab Environment

## Analyst Machine

- Operating System: Kali Linux 2026.1
- Python 3.13
- Sigma CLI
- Virtual Environment (venv)

## Target Machine

- Windows 11
- Sysmon
- Event Viewer
- PowerShell

## Virtualization

- Oracle VirtualBox

---

# Project Architecture

```
                  Internet
                       │
          ┌────────────────────┐
          │   Kali Linux VM    │
          │  Detection Analyst │
          └────────────────────┘
                       │
                Virtual Network
                       │
          ┌────────────────────┐
          │   Windows 11 VM    │
          │   Sysmon Enabled   │
          └────────────────────┘
```

---

# Technologies Used

- Kali Linux
- Windows 11
- Sysmon
- Sigma CLI
- Python
- YAML
- Event Viewer
- PowerShell
- VirtualBox

---

# Windows Events Studied

| Event ID | Description |
|----------|-------------|
| 1 | Process Creation |
| 3 | Network Connection |
| 11 | File Creation |
| 13 | Registry Modification |

---

# Sigma Rules Developed

- Detect PowerShell ExecutionPolicy Bypass
- Detect Encoded PowerShell Commands
- Detect CMD launching PowerShell
- Detect PowerShell Network Connections
- Detect PowerShell File Creation
- Detect Registry Modification
- Detect Mimikatz Execution

---

# Attack Simulations Performed

The following activities were performed inside the Windows virtual machine to generate Windows telemetry:

- Command Prompt execution
- PowerShell execution
- PowerShell ExecutionPolicy Bypass
- PowerShell EncodedCommand
- PowerShell network communication
- File creation
- Registry modification

These activities were analyzed using Sysmon Event Logs and correlated during the investigation process.

---

# Detection Engineering Workflow

The project followed the following workflow:

```
Generate Activity
        │
        ▼
Windows Event Generated
        │
        ▼
Sysmon Records Event
        │
        ▼
Event Viewer Analysis
        │
        ▼
Develop Sigma Rule
        │
        ▼
Validate Detection
        │
        ▼
SOC Investigation
        │
        ▼
Incident Report
```

---

# Detection Engineering Concepts Learned

- Process Creation Monitoring
- Parent and Child Process Relationships
- Command Line Analysis
- PowerShell Detection
- Registry Monitoring
- Network Monitoring
- Event Correlation
- Detection Logic
- False Positive Analysis
- Alert Severity Classification
- SOC Investigation Workflow

---

# MITRE ATT&CK Techniques Covered

| Technique | Description |
|------------|-------------|
| T1059.001 | PowerShell |
| T1059.003 | Windows Command Shell |
| T1105 | Ingress Tool Transfer / File Download |
| T1112 | Modify Registry |

---

# Skills Demonstrated

## Detection Engineering

- Sigma Rule Development
- Detection Logic Design
- Rule Validation
- False Positive Analysis

## Windows Security

- Sysmon Configuration
- Event Viewer Analysis
- Windows Telemetry
- PowerShell Investigation

## SOC Operations

- Incident Investigation
- Timeline Reconstruction
- Event Correlation
- Severity Classification
- Threat Analysis

---

# Reports Included

- Incident Investigation Report
- Detection Engineering Report
- Final Project Report
- Lessons Learned
- MITRE ATT&CK Mapping

---

# Project Structure

```
cred/
│
├── README.md
├── logs/
├── reports/
├── rules/
├── screenshots/
├── diagrams/
├── mitre/
├── notes/
├── tools/
└── venv/
```

---

# Lessons Learned

This project significantly improved my understanding of Windows Detection Engineering.

During the project I learned:

- How Windows generates security telemetry
- How Sysmon captures detailed system activity
- How Sigma rules detect attacker behavior
- How to investigate Windows security events
- How to correlate multiple events into an attack timeline
- How to classify incidents using evidence instead of assumptions
- How to document investigations in a professional manner

---

# Future Improvements

The following enhancements are planned:

- Integrate Sysmon with Splunk
- Integrate Microsoft Sentinel
- Expand Sigma rule coverage
- Simulate additional ATT&CK techniques
- Automate detection validation
- Build threat hunting playbooks

---

# Project Outcome

By completing this project, I successfully built a Windows Detection Engineering Lab capable of:

- Generating Windows telemetry
- Monitoring Sysmon events
- Developing Sigma detection rules
- Investigating suspicious activity
- Producing SOC-style incident reports

This project strengthened my practical knowledge of Detection Engineering, Windows Security Monitoring, and Security Operations Center (SOC) workflows.

---

# Author

**Krishna Kumar**

Cybersecurity Enthusiast | SOC Analyst (Aspiring) | Detection Engineering Learner
