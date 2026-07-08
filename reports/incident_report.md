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
                                                                                                                                                                   
# SOC Incident Investigation Report

## Executive Summary

A sequence of PowerShell-related activities was observed on the Windows 11 virtual machine. The investigation focused on process creation, network communication, file creation, and registry modification recorded by Sysmon.

The observed behavior included PowerShell execution with the ExecutionPolicy Bypass argument, outbound network communication, file creation, and registry modification. While these activities resemble attacker behavior, the available evidence did not conclusively confirm malicious activity.

---

## Timeline

| Time | Activity |
|------|----------|
| Step 1 | Explorer.exe launched cmd.exe |
| Step 2 | cmd.exe launched powershell.exe |
| Step 3 | PowerShell executed with ExecutionPolicy Bypass |
| Step 4 | PowerShell established an outbound HTTPS connection |
| Step 5 | PowerShell created AttackLab.txt |
| Step 6 | PowerShell modified the Windows Registry |

---

## Evidence Collected

### Sysmon Event ID 1
- Process Creation
- Parent Process Analysis
- Command Line Analysis

### Sysmon Event ID 3
- Network Connection
- Destination IP
- Destination Port
- Protocol

### Sysmon Event ID 11
- File Creation
- Target Filename

### Sysmon Event ID 13
- Registry Modification
- Registry Path
- Registry Value

---

## Analysis

The sequence of events suggests PowerShell executed multiple actions after being launched through Command Prompt.

Observed behaviors included:

- Process execution
- External network communication
- File creation
- Registry modification

No malware or persistence mechanism was confirmed during the investigation. Additional evidence would be required before confirming malicious activity.

---

## Severity

**High**

Reason:

Multiple suspicious behaviors occurred during a single execution chain. However, the investigation did not identify sufficient evidence to classify the activity as a confirmed compromise.

---

## Recommendations

- Review EDR telemetry
- Review Windows Event Logs
- Review DNS logs
- Review Firewall logs
- Review Proxy logs
- Review PowerShell history
- Verify destination IP reputation
- Continue monitoring the endpoint

---

## Conclusion

This investigation demonstrated how Sysmon telemetry and Sigma detection rules can be used together to identify suspicious Windows activity while avoiding conclusions without sufficient evidence.
