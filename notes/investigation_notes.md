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



# Investigation Notes

## Investigation Workflow

Alert

↓

Collect Evidence

↓

Validate

↓

Correlate

↓

Classify

↓

Respond

↓

Document

---

## Evidence Sources

Sysmon

Windows Logs

PowerShell Logs

DNS

Firewall

Proxy

EDR

---

## Investigation Questions

What happened?

When did it happen?

Who executed it?

Which process started it?

What command was used?

Was there network communication?

Were files created?

Was the registry modified?

Was persistence established?

---

## Event Correlation

Process

↓

Network

↓

File

↓

Registry

↓

Timeline

↓

Incident

---

## Severity Guide

Low

Expected activity

Medium

Suspicious behavior

High

Multiple suspicious actions

Critical

Confirmed compromise

Credential theft

Malware

Ransomware

---

## Investigation Checklist

□ Review Process Creation

□ Review Network Events

□ Review File Creation

□ Review Registry Changes

□ Review Parent Process

□ Review User

□ Review Command Line

□ Review Destination IP

□ Review Timeline

□ Review Related Events

---

## Golden Rules

Never assume.

Correlate evidence.

Document every finding.

Escalate only when justified.

Evidence drives conclusions—not assumptions.
