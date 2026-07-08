# Detection Engineering Report

## Project Objective

The objective of this project was to build a Windows Detection Engineering lab using Sysmon and Sigma to detect common attacker techniques and improve incident investigation skills.

## Detection Rule 1

Title:
Detect PowerShell Execution Policy Bypass

## Purpose:

Detect PowerShell executions that bypass the Windows execution policy.

Attackers frequently use the ExecutionPolicy Bypass argument to execute scripts without being blocked by local policy settings.

## Log Source

Windows

Category:
Process Creation

Sysmon Event ID:1

## Detection Logic

The rule identifies process creation events where the executable is PowerShell and the command line contains the ExecutionPolicy Bypass argument.

Both conditions must be true before an alert is generated.


## Evidence Used

Image

CommandLine

ParentImage

User

## 
Image identifies the executable.

CommandLine identifies suspicious arguments.

ParentImage helps determine how PowerShell was launched.

User identifies the account responsible for the activity.


## MITRE ATT&CK

Technique: PowerShell

ID: T1059.001

## Expected False Positives

System administrators

Software deployment tools

Automation scripts

Enterprise management solutions

## "What should a SOC analyst do after this rule triggers?"
Investigation Steps

Review the full command line.

Identify the parent process.

Determine whether the execution was initiated by a legitimate administrator.

Review additional Sysmon events.

Review network activity.

Review EDR telemetry.


## Severity
High

# why 
Severity

Medium

The use of ExecutionPolicy Bypass is suspicious but not sufficient to confirm malicious activity.

Additional context is required before escalating the incident.


# "Tell me about one Sigma rule you wrote."
Instead of opening the YAML file, you can walk through:

The purpose.
The log source.
The detection logic.
The evidence.
The MITRE mapping.
The false positives.
The investigation steps.
The severity.

That demonstrates much deeper understanding than simply showing the rule.



## A Small Assignment

I don't want you to document all seven rules at once.

That would become repetitive.

Instead, I want you to fully document one rule—the PowerShell Execution Policy Bypass rule—using the structure above.

Once you've done that, we'll review it together. After that, the remaining rules will be much easier because you'll already know the format.










# Detection Engineering Report

## Project Objective

Develop Sigma detection rules capable of identifying suspicious Windows activities using Sysmon telemetry.

---

# Rule 1

## Detect PowerShell ExecutionPolicy Bypass

Purpose

Detect PowerShell launched using the ExecutionPolicy Bypass argument.

Log Source

- Windows
- Sysmon Event ID 1
- Process Creation

Detection Logic

- Image ends with powershell.exe
- CommandLine contains ExecutionPolicy
- CommandLine contains Bypass

Evidence Used

- Image
- CommandLine
- ParentImage
- User

MITRE ATT&CK

T1059.001 – PowerShell

False Positives

- System administrators
- Software deployment tools
- Automation scripts

Investigation Steps

- Review complete command line
- Identify parent process
- Review additional Sysmon events
- Check network activity
- Verify user activity

Severity

Medium

Reason

ExecutionPolicy Bypass is suspicious but may also be used by legitimate administrators.

---

# Rule 2

Detect Encoded PowerShell Commands

Purpose

Identify PowerShell executions using EncodedCommand.

MITRE

T1059.001

Severity

High

---

# Rule 3

Detect CMD Launching PowerShell

Purpose

Detect PowerShell started from Command Prompt.

Severity

Medium

---

# Rule 4

Detect PowerShell Network Connections

Purpose

Detect outbound network communication initiated by PowerShell.

Severity

High

---

# Rule 5

Detect PowerShell File Creation

Purpose

Detect files created by PowerShell.

Severity

Medium

---

# Rule 6

Detect Registry Modification

Purpose

Detect registry changes made by PowerShell.

Severity

Medium

---

# Rule 7

Detect Mimikatz Execution

Purpose

Detect execution of the Mimikatz credential dumping tool.

MITRE

T1003

Severity

High
