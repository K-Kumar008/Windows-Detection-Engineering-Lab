# PowerShell Notes

## Why Attackers Like PowerShell

- Installed by default
- Powerful scripting language
- Access to Windows APIs
- Network communication
- File management
- Registry modification

---

## Suspicious Arguments

ExecutionPolicy Bypass

EncodedCommand

NoProfile

WindowStyle Hidden

NonInteractive

DownloadString

Invoke-WebRequest

Invoke-Expression

---

## Important Sysmon Fields

Image

CommandLine

ParentImage

User

---

## Common Parent Processes

cmd.exe

explorer.exe

winword.exe

excel.exe

outlook.exe

---

## Investigation Questions

Who started PowerShell?

What arguments were used?

Did it create files?

Did it modify the registry?

Did it connect to the Internet?

Was it expected?
