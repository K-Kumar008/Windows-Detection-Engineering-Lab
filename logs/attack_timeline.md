# Attack Timeline

## Objective

Demonstrate how multiple Sysmon events can be correlated during a SOC investigation.

---

## Timeline

### Step 1
Explorer.exe launched Command Prompt.

Event ID:
1

---

### Step 2
Command Prompt launched PowerShell.

Event ID:
1

Command:
powershell.exe -ExecutionPolicy Bypass

---

### Step 3
PowerShell established an outbound HTTPS connection.

Event ID:
3

Destination Port:
443

---

### Step 4
PowerShell created a file on the system.

Event ID:
11

Target:
AttackLab.txt

---

### Step 5
PowerShell modified the Windows Registry.

Event ID:
13

Registry:
HKCU\Software\KrishnaLab

---

## Investigation Summary

The activity demonstrates a complete attack chain consisting of:

- Process Creation
- Command Execution
- Network Communication
- File Creation
- Registry Modification

These events should be correlated rather than investigated individually.

Severity:
High

Reason:
Multiple suspicious actions occurred in sequence. Although the behavior resembles attacker techniques, additional evidence would be required to confirm malicious activity.
