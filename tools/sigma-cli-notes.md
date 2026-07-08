# Sigma CLI Notes

## What is Sigma?

Sigma is an open standard used to describe security detection rules.

It allows detection logic to be written once and converted into queries for different SIEM platforms.

Examples:

- Splunk
- Microsoft Sentinel
- Elastic
- QRadar
- Graylog

---

## Why Sigma?

Instead of writing vendor-specific queries, Sigma provides a common rule format.

Benefits:

- Portable
- Easy to read
- Open source
- Community supported

---

## Sigma Rule Structure

Every Sigma rule generally contains:

title
id
status
description
author
logsource
detection
falsepositives
level
tags

---

## Commands Used During This Project

Check version

sigma version

---

Validate a rule

sigma check rules/<rule_name>.yml

Example

sigma check rules/mimikatz.yml

---

List available commands

sigma --help

---

## Rule Components

Title

Describes what the rule detects.

Example:

Detect PowerShell Execution Policy Bypass

---

Log Source

Specifies where the event comes from.

Example:

product: windows
category: process_creation

---

Detection

Contains the detection logic.

Example:

Image|endswith:
    - '\powershell.exe'

CommandLine|contains:
    - '-ExecutionPolicy'

Condition:

selection

or

all of selection_*

---

False Positives

Expected legitimate activities.

Examples:

- System administrators
- Automation scripts
- Software deployment tools

---

Severity Levels

Informational

Low

Medium

High

Critical

---

MITRE ATT&CK

Rules should be mapped to ATT&CK techniques whenever possible.

Example:

PowerShell

T1059.001

---

Best Practices

Use multiple fields.

Avoid relying only on Image.

Combine:

Image

CommandLine

ParentImage

User

TargetFilename

TargetObject

Reduce false positives.

Test every rule before using it.

Document every rule.

---

Project Rules Created

PowerShell Execution Policy

Encoded PowerShell

CMD → PowerShell

PowerShell Network Activity

PowerShell File Creation

Registry Persistence

Mimikatz Detection

---

Lessons Learned

Sigma is a detection language, not a SIEM.

Sigma detects behavior.

Detection quality improves by correlating multiple event fields.

Always consider false positives before assigning severity.

Detection engineering requires understanding attacker behavior, not only writing syntax.
