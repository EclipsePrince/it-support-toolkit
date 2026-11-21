## Windows Troubleshooting

## Overview

Windows troubleshooting involves identifying, diagnosing and resolving problems affecting Windows computers and their operating systems.

IT Support Technicians use built-in Windows utilities, command-line tools and administrative features to investigate hardware, software, network and performance issues.

This document covers common Windows troubleshooting scenarios and diagnostic procedures.

## Slow Computer Performance

Problem

A Windows computer is running slowly or responding slowly to user commands.

Possible causes:

- High CPU utilisation.
- High memory consumption.
- Too many startup applications.
- Insufficient disk space.
- Background processes.
- Malware or unwanted software.

Diagnostic tools:

Task Manager:

taskmgr

Check system information:

systeminfo

Check running processes:

tasklist

Troubleshooting procedure:

1. Open Task Manager.
2. Inspect CPU, memory and disk utilisation.
3. Identify applications consuming excessive resources.
4. Investigate unnecessary startup applications.
5. Check available storage space.
6. Restart the computer if appropriate.
7. Verify whether performance improves.

## Network Connectivity Problems

Problem

A Windows computer cannot connect to the internet or network resources.

Possible causes:

- Disconnected network cable.
- Wi-Fi connectivity problems.
- Incorrect IP configuration.
- DNS resolution failure.
- Default gateway problems.

Diagnostic commands:

Display network configuration:

ipconfig /all

Test connectivity:

ping 8.8.8.8

Test DNS resolution:

nslookup google.com

Display network routes:

route print

Clear DNS cache:

ipconfig /flushdns

Renew IP configuration:

ipconfig /release
ipconfig /renew

Troubleshooting procedure:

1. Check the physical network connection or Wi-Fi status.
2. Inspect IP configuration.
3. Verify the default gateway.
4. Ping the default gateway.
5. Ping an external IP address.
6. Test DNS resolution.
7. Apply the appropriate corrective action.
8. Confirm that connectivity has been restored.

## Windows Printer Problems

Problem

A user cannot print documents.

Possible causes:

- Printer disconnected.
- Incorrect printer selection.
- Outdated printer driver.
- Print queue problems.
- Print Spooler service issues.

Diagnostic tools:

Open the printer settings:

control printers

Open the Services management console:

services.msc

Troubleshooting procedure:

1. Check whether the printer is powered on.
2. Verify its USB or network connection.
3. Confirm that the correct printer is selected.
4. Check the print queue.
5. Inspect the Print Spooler service.
6. Verify printer drivers.
7. Print a test page.

## Windows Login Problems

Problem

A user cannot sign in to Windows.

Possible causes:

- Incorrect password.
- Account locked or disabled.
- Network connectivity problems.
- Domain authentication issues.
- Corrupted user profile.

Diagnostic tools:

Check the computer's hostname:

hostname

Display logged-in users:

query user

Open Event Viewer:

eventvwr.msc

Troubleshooting procedure:

1. Confirm the username and account being used.
2. Check keyboard layout and Caps Lock.
3. Determine whether the computer has network connectivity.
4. Check whether the issue affects one user or multiple users.
5. Review relevant authentication errors.
6. Escalate domain account or access-control issues when necessary.

Never request or record a user's password.

## Windows System Information

Problem

A technician needs to identify hardware or operating system information.

Diagnostic commands:

Display Windows system information:

systeminfo

Open System Information:

msinfo32

Display disk information:

wmic logicaldisk get caption,size,freespace

Note: WMIC is deprecated in modern Windows versions. PowerShell alternatives should be preferred.

Troubleshooting procedure:

1. Identify the Windows version.
2. Check system architecture.
3. Identify installed memory.
4. Inspect storage capacity.
5. Record relevant hardware information.

## Windows Services Problems

Problem

A Windows service is not functioning correctly.

Diagnostic tools:

Open Services:

services.msc

Display running services:

sc query state= all

Check a specific service:

sc query Spooler

Troubleshooting procedure:

1. Identify the affected service.
2. Check its current status.
3. Inspect related error messages.
4. Review service dependencies.
5. Investigate configuration issues.
6. Restart the service only when appropriate.
7. Verify that the service is functioning.

## Windows System File Problems

Problem

Windows displays system errors, crashes or unexpected behaviour.

Diagnostic commands:

System File Checker:

sfc /scannow

Deployment Image Servicing and Management:

DISM /Online /Cleanup-Image /RestoreHealth

Troubleshooting procedure:

1. Identify the reported system problem.
2. Run System File Checker from an elevated terminal.
3. Review the scan results.
4. If necessary, run the DISM repair command.
5. Restart the computer if required.
6. Verify whether the problem has been resolved.

These commands can modify Windows system files. Use them on an appropriate test machine or with authorisation.

## Windows Troubleshooting Methodology

A structured troubleshooting approach helps technicians resolve problems efficiently.

1. Identify the reported issue.
2. Gather information from the user.
3. Determine the scope of the problem.
4. Identify possible causes.
5. Perform diagnostic tests.
6. Apply the appropriate solution.
7. Verify system functionality.
8. Document the incident and resolution.

## Practical Exercises

Complete the following exercises on a Windows computer:

1. Open Task Manager and inspect resource utilisation.
2. Display system information using systeminfo.
3. Display network configuration using ipconfig /all.
4. Test network connectivity using ping.
5. Investigate DNS resolution using nslookup.
6. Open Windows Services.
7. Inspect running processes using tasklist.
8. Open Event Viewer and inspect available system logs.

Record the commands, results and observations.

## Learning Outcomes

After completing this section, I should be able to:

- Diagnose common Windows performance problems.
- Investigate network connectivity issues.
- Troubleshoot printer problems.
- Investigate Windows login issues.
- Identify system information and hardware details.
- Inspect Windows services.
- Use built-in Windows repair utilities.
- Apply a structured IT troubleshooting methodology.

---

Project: IT Support Toolkit

Category: Windows Administration

Lab: Windows Troubleshooting

Status: Documentation in progress
