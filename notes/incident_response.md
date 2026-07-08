# Incident Response Notes

## What is Incident Response?

Incident Response (IR) is the structured process of identifying, analyzing, containing, eradicating, and recovering from cybersecurity incidents.

---

## Incident Response Lifecycle

Preparation

↓

Identification

↓

Containment

↓

Eradication

↓

Recovery

↓

Lessons Learned

---

## Preparation

Examples

- Logging
- Sysmon
- EDR
- SIEM
- Playbooks
- Backups

---

## Identification

Goal

Determine whether suspicious activity is an actual security incident.

Evidence

- Sysmon
- Windows Logs
- Firewall
- DNS
- Proxy
- EDR

---

## Containment

Goal

Prevent the attack from spreading.

Examples

- Isolate endpoint
- Disable user account
- Block IP
- Block domain

---

## Eradication

Goal

Remove the attacker's presence.

Examples

- Delete malware
- Remove persistence
- Patch vulnerability
- Reset credentials

---

## Recovery

Goal

Return systems to normal operation.

Examples

- Restore files
- Monitor system
- Reconnect endpoint
- Verify security

---

## Lessons Learned

Questions

How did the attack happen?

Why was it successful?

Can we improve detection?

Can we improve response?

---

## SOC Analyst Responsibilities

Collect evidence

Analyze logs

Determine severity

Escalate if necessary

Document findings

Recommend actions

---

## Golden Rule

Never destroy evidence.

Always preserve logs before taking action.
