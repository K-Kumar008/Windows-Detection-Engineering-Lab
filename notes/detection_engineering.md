# Detection Engineering Notes

## What is Detection Engineering?

Detection Engineering is the process of designing, testing, improving, and maintaining detections that identify malicious behavior.

---

## Goal

Detect attackers

Minimize false positives

Reduce false negatives

Improve SOC visibility

---

## Detection Lifecycle

Collect Logs

↓

Understand Attack

↓

Write Detection

↓

Test

↓

Tune

↓

Deploy

↓

Monitor

↓

Improve

---

## Data Sources

Sysmon

Windows Security Logs

PowerShell Logs

DNS Logs

Firewall Logs

Proxy Logs

EDR

---

## Detection Logic

Weak Detection

Image = powershell.exe

↓

Better Detection

Image

+

CommandLine

↓

Best Detection

Image

+

CommandLine

+

ParentImage

+

Network Activity

+

Registry Changes

---

## Detection Confidence

Low

Single Indicator

Medium

Two Indicators

High

Multiple Correlated Indicators

---

## False Positives

Expected legitimate behavior that triggers a rule.

Examples

- Administrators
- Automation
- Software deployment
- Backup software

---

## False Negatives

Malicious activity that is NOT detected.

Reasons

Poor rule

Missing logs

Disabled Sysmon

Incomplete visibility

---

## Good Detection Rule

Purpose

Evidence

Logic

False Positives

Severity

MITRE Mapping

Investigation Steps
