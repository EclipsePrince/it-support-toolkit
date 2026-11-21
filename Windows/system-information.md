## Windows System Information

## Overview

System information gathering is an essential IT Support task used to identify hardware specifications, operating system details, software configurations and system performance.

Technicians use built-in Windows utilities and command-line tools to collect information when diagnosing technical issues or preparing systems for maintenance.

## Operating System Information

Display Windows version

winver

Opens the Windows version information window.

Display detailed system information

systeminfo

Displays information including:

- Operating system name and version.
- System manufacturer.
- System model.
- Processor information.
- Installed RAM.
- BIOS version.
- Network configuration.

Open System Information

msinfo32

Opens the graphical System Information utility.

## Hardware Information

Display processor information

PowerShell:

Get-CimInstance Win32_Processor | Select-Object Name, NumberOfCores, NumberOfLogicalProcessors

Displays processor name, physical cores and logical processors.

Display installed memory

Get-CimInstance Win32_PhysicalMemory | Select-Object Manufacturer, Capacity, Speed

Displays installed memory modules and their specifications.

Display computer manufacturer and model

Get-CimInstance Win32_ComputerSystem | Select-Object Manufacturer, Model

Identifies the computer manufacturer and model.

Display BIOS information

Get-CimInstance Win32_BIOS | Select-Object Manufacturer, SMBIOSBIOSVersion, ReleaseDate

Displays BIOS manufacturer, version and release date.

## Storage Information

Display available disk drives

Get-PSDrive -PSProvider FileSystem

Displays available filesystem drives and their storage information.

Display physical disks

Get-PhysicalDisk

Displays physical disk information where supported.

Display logical disk information

Get-CimInstance Win32_LogicalDisk | Select-Object DeviceID, Size, FreeSpace

Displays drive letters, total storage and available storage.

## Network Information

Display IP configuration

ipconfig /all

Displays network adapter configuration, IP addresses, DNS servers and other network information.

Display network adapters

PowerShell:

Get-NetAdapter

Displays network adapters and their connection status.

Display network connections

netstat -ano

Displays active network connections, listening ports and associated process IDs.

## Process and Service Information

Display running processes

Get-Process

Displays running processes.

Display running services

Get-Service | Where-Object {$_.Status -eq "Running"}

Lists services currently running.

Display system uptime

(Get-Date) - (Get-CimInstance Win32_OperatingSystem).LastBootUpTime

Calculates the time elapsed since the operating system last started.

## Windows Administrative Utilities

Utility| Command| Purpose
Task Manager| taskmgr| Monitor processes and resources
System Information| msinfo32| Inspect hardware and software
Device Manager| devmgmt.msc| Manage hardware devices
Disk Management| diskmgmt.msc| Manage disks and partitions
Services| services.msc| Manage Windows services
Event Viewer| eventvwr.msc| Investigate system logs
Resource Monitor| resmon| Monitor resource utilisation

## Practical Exercises

Complete these exercises on a Windows computer:

1. Identify the installed Windows version.
2. Display detailed system information.
3. Identify the processor model.
4. Check installed RAM.
5. Identify the computer manufacturer and model.
6. Inspect available disk space.
7. Display network adapters.
8. Inspect running processes.
9. Identify running services.
10. Calculate system uptime.

Record the results and explain what each command reveals.

## Learning Outcomes

After completing this section, I should be able to:

- Identify Windows operating system details.
- Inspect hardware specifications.
- Gather storage information.
- Identify network adapters and configurations.
- Inspect running processes and services.
- Use Windows administrative utilities.
- Collect system information for IT Support investigations.

---

Project: IT Support Toolkit

Category: Windows Administration

Lab: System Information

Status: Documentation in progress
