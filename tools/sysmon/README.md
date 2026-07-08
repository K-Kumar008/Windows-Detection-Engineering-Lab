# Sysmon Tool

## Overview

Sysmon (System Monitor) is a Windows system service and device driver from Microsoft Sysinternals.

It provides detailed logging of system activity, allowing defenders to monitor process execution, network connections, file creation, registry modifications, and other security-relevant events.

Unlike standard Windows Event Logs, Sysmon generates rich telemetry that is useful for threat detection, incident response, and threat hunting.

---

## Purpose in This Project

Sysmon was installed on the Windows 11 Virtual Machine to generate telemetry for security analysis.

The generated events were analyzed using Event Viewer and used to develop Sigma detection rules.

---

## Important Event IDs Used

| Event ID | Description |
|----------|-------------|
| 1 | Process Creation |
| 3 | Network Connection |
| 11 | File Creation |
| 13 | Registry Modification |

---

## Project Workflow

Windows 11

↓

Sysmon collects telemetry

↓

Windows Event Viewer

↓

Security Analysis

↓

Sigma Rule Development

↓

SOC Investigation

---

## Configuration

The Sysmon configuration file used in this project is:

sysmonconfig.xml

This configuration determines which events Sysmon records.

---

## Skills Learned

- Sysmon installation
- Windows telemetry collection
- Windows Event Viewer analysis
- Detection Engineering
- SOC Investigation
- Sigma Rule Development
