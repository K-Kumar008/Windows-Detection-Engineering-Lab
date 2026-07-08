# Sysmon Event IDs

## Overview

Sysmon (System Monitor) is a Windows system service and driver that logs detailed system activity into the Windows Event Log.

The logs are stored under:

Applications and Services Logs
└── Microsoft
    └── Windows
        └── Sysmon
            └── Operational

---

## Event ID 1 - Process Creation

Description:
Logs every process that starts.

Important Fields:
- Image
- CommandLine
- ParentImage
- ParentCommandLine
- User
- ProcessId
- ProcessGuid

Use Cases:
- Detect PowerShell
- Detect CMD
- Detect LOLBins
- Detect Mimikatz

---

## Event ID 3 - Network Connection

Description:
Logs outbound network connections.

Important Fields:
- Image
- SourceIP
- DestinationIP
- DestinationHostname
- DestinationPort
- Protocol
- User

Use Cases:
- Detect malware communication
- Detect C2 traffic
- Detect suspicious outbound connections

---

## Event ID 11 - File Creation

Description:
Logs file creation.

Important Fields:
- Image
- TargetFilename
- CreationUtcTime
- User

Use Cases:
- Malware dropping files
- Suspicious scripts
- Payload creation

---

## Event ID 13 - Registry Value Set

Description:
Logs registry modifications.

Important Fields:
- Image
- TargetObject
- Details
- User

Use Cases:
- Persistence
- Registry tampering
- Malware configuration

---

## Investigation Tips

Never investigate one event alone.

Always correlate:

Process
↓

Network
↓

File

↓

Registry

This gives the complete attack story.
