# SOC Investigation Notes

## Investigation Workflow

Alert

↓

Collect Evidence

↓

Analyze

↓

Correlate Events

↓

Determine Severity

↓

Respond

↓

Close or Escalate

---

## Process Investigation

Image

ParentImage

CommandLine

User

---

## Network Investigation

Destination IP

Destination Hostname

Destination Port

Protocol

Reputation

---

## File Investigation

TargetFilename

Extension

Location

User

---

## Registry Investigation

TargetObject

Details

Persistence

---

## Severity Guide

Low

Expected administrative activity

---

Medium

Suspicious activity requiring investigation

---

High

Multiple suspicious behaviors observed

---

Critical

Confirmed compromise
Malware
Credential theft
Ransomware

---

Golden Rule

Never assume.

Always verify with evidence.

---

SOC Analyst Checklist

□ Review Sysmon

□ Review Security Logs

□ Review PowerShell Logs

□ Review EDR

□ Review Firewall

□ Review DNS

□ Review Proxy

□ Correlate Timeline

□ Decide Severity

□ Escalate if necessary
