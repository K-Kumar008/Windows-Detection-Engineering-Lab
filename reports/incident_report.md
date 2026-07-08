# SOC Incident Investigation Report

## Executive Summary

A sequence of PowerShell-related activities was observed on a Windows 11 virtual machine.

The investigation identified:

- Process creation
- Network communication
- File creation
- Registry modification

The activity was classified as **High Severity** because multiple suspicious behaviors occurred in sequence. However, the available evidence did not confirm malicious activity.

---

## Timeline

1. Explorer launched CMD.
2. CMD launched PowerShell.
3. PowerShell executed with ExecutionPolicy Bypass.
4. PowerShell connected to an external IP over HTTPS.
5. PowerShell created a file.
6. PowerShell modified the registry.

---

## Evidence Collected

### Event ID 1
Process Creation

### Event ID 3
Network Connection

### Event ID 11
File Creation

### Event ID 13
Registry Modification

---

## Analysis

The observed activity resembles several attacker techniques commonly seen during post-exploitation.

No evidence confirmed malware execution.

Further investigation would be required.

---

## Severity

High

---

## Recommended Actions

- Review EDR telemetry
- Review DNS logs
- Review Proxy logs
- Review Firewall logs
- Review PowerShell command line
- Investigate destination IP
- Escalate if additional malicious evidence is identified

---

## Conclusion

The investigation identified multiple suspicious events that warrant further investigation. The available evidence was insufficient to confirm a compromise.
                                                                                                                                                                   
