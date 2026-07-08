# Threat Hunting Notes

## What is Threat Hunting?

Threat Hunting is the proactive search for malicious activity that has not yet generated an alert.

---

## Reactive vs Proactive

SOC Alert

↓

Investigate

(Incident Response)

---

Threat Hunting

↓

Search for hidden threats

(Proactive)

---

## Threat Hunting Process

Create Hypothesis

↓

Search Logs

↓

Correlate Events

↓

Validate Findings

↓

Document Results

---

## Example Hypothesis

An attacker may be abusing PowerShell.

Search

Image = powershell.exe

↓

CommandLine

↓

ParentImage

↓

Network

↓

Registry

---

## Common Hunt Questions

Who executed PowerShell?

What process started it?

Did it create files?

Did it connect to the Internet?

Did it modify the registry?

Did it establish persistence?

---

## Useful Data Sources

Sysmon

Windows Logs

PowerShell Logs

DNS

Firewall

Proxy

EDR

---

## Hunting Mindset

Do not wait for alerts.

Assume attackers may already be present.

Look for unusual behavior instead of signatures.

---

## Example Hunt

Hypothesis

PowerShell is being abused.

Evidence

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

Conclusion
