# Sysmon Installation Notes

## Operating System

Windows 11 Virtual Machine

---

## Download Source

Microsoft Sysinternals

---

## Files Used

- Sysmon.exe
- Sysmon64.exe
- sysmonconfig.xml

---

## Installation Process

1. Download Sysmon from Microsoft Sysinternals.
2. Extract the ZIP archive.
3. Copy the Sysmon configuration file (sysmonconfig.xml) into the Sysmon folder.
4. Open Command Prompt as Administrator.
5. Navigate to the Sysmon directory.
6. Install Sysmon using the configuration file.
7. Verify successful installation.
8. Open Event Viewer.
9. Confirm that Sysmon events are being generated.

---

## Verification

Event Viewer

Applications and Services Logs

Microsoft

Windows

Sysmon

Operational

The following Event IDs were successfully observed:

- Event ID 1
- Event ID 3
- Event ID 11
- Event ID 13

---

## Commands Used

Installation

Sysmon64.exe -accepteula -i sysmonconfig.xml

Configuration Update

Sysmon64.exe -c sysmonconfig.xml

Uninstall

Sysmon64.exe -u

---

## Notes

Sysmon runs as a Windows service.

The generated telemetry is used for:

- Detection Engineering
- Threat Hunting
- Incident Response
- Digital Forensics

---

## Lessons Learned

Sysmon provides significantly more detailed telemetry than default Windows Security logs.

Combining Sysmon with Sigma rules enables detection of suspicious behaviors instead of relying only on malware signatures.
