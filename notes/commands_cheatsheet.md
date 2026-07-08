# Command Cheat Sheet

## Linux Commands

### Current Directory

pwd

### List Files

ls

ls -l

ls -la

### Change Directory

cd directory_name

cd ..

cd ~

### Create Directory

mkdir reports

### Create File

touch test.txt

### Remove File

rm file.txt

### Remove Directory

rm -r folder

### Copy File

cp source destination

### Move File

mv source destination

### View File

cat filename

less filename

more filename

### Edit File

nano filename

### Search

find . -name "*.yml"

grep "PowerShell" filename

### Tree Structure

tree

---

## Python

Create Virtual Environment

python3 -m venv venv

Activate

source venv/bin/activate

Deactivate

deactivate

Install Package

pip install sigma-cli

Upgrade Pip

python -m pip install --upgrade pip

---

## Sigma CLI

Version

sigma version

Validate Rule

sigma check rules/example.yml

List Backends

sigma list targets

Convert Rule

sigma convert -t splunk rules/example.yml

Help

sigma --help

---

## Windows PowerShell

Launch PowerShell

powershell.exe

Execution Policy Bypass

powershell.exe -ExecutionPolicy Bypass

Encoded Command

powershell.exe -EncodedCommand <Base64>

---

## Event Viewer

Open

eventvwr.msc

Sysmon Logs

Applications and Services Logs

↓

Microsoft

↓

Windows

↓

Sysmon

↓

Operational

---

## Useful Sysmon Event IDs

1   Process Creation

3   Network Connection

11  File Creation

13  Registry Modification

---

## Interview Reminder

Do not memorize commands.

Understand:

- What they do
- Why they are used
- What evidence they generate
