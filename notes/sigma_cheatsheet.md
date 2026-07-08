# Sigma Cheat Sheet

## What is Sigma?

Sigma is a generic detection rule format used to detect suspicious activity across different SIEM platforms.

---

## Basic Rule Structure

title:
id:
status:
description:
author:

logsource:

detection:

condition:

level:

---

## Common Operators

contains

endswith

startswith

equals

re

all

any

---

## Example

Image|endswith:
    - '\powershell.exe'

---

CommandLine|contains:
    - "-ExecutionPolicy"
    - "Bypass"

---

Condition Examples

condition: selection

condition: selection1 and selection2

condition: all of selection_*

condition: selection1 or selection2

---

Severity Levels

low

medium

high

critical

---

False Positives

Always document expected legitimate activity.

Examples:

- Administrators
- Automation
- Software deployment
- Scheduled tasks

---

Rule Checklist

✓ Title

✓ Description

✓ Detection

✓ Condition

✓ False Positives

✓ MITRE Tag

✓ Severity
