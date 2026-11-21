## Linux Troubleshooting

## Overview

Linux troubleshooting is the process of identifying, diagnosing and resolving problems affecting a Linux operating system.

IT Support technicians use command-line utilities, system logs and diagnostic tools to investigate system performance, network connectivity, storage and service-related issues.

This document covers common Linux troubleshooting scenarios and diagnostic procedures.

## System Performance Troubleshooting

Problem: Linux system is running slowly

Possible causes:

- High CPU utilisation.
- Insufficient available memory.
- Too many running processes.
- Background applications consuming resources.

Diagnostic commands:

Check CPU and process utilisation:

top

Display running processes:

ps aux

Check memory usage:

free -h

Troubleshooting approach:

1. Identify processes consuming excessive resources.
2. Inspect CPU and memory utilisation.
3. Determine whether a particular process is causing the slowdown.
4. Investigate the process before taking action.
5. Escalate if the problem cannot be safely resolved.

## Disk Space Troubleshooting

Problem: Disk space is running low

Possible causes:

- Large log files.
- Accumulated temporary files.
- Unnecessary downloads.
- Applications generating excessive data.

Diagnostic commands:

Check filesystem usage:

df -h

Check directory storage:

du -sh *

Find large files within the current directory:

find . -type f -size +100M -print

Troubleshooting approach:

1. Identify the filesystem with limited space.
2. Investigate directories consuming storage.
3. Identify unusually large files.
4. Determine whether files can safely be archived or removed.
5. Verify available disk space after remediation.

Never delete system files or logs without understanding their purpose.

## Network Connectivity Troubleshooting

Problem: Linux system cannot access the internet

Possible causes:

- Network interface is disconnected.
- Incorrect IP configuration.
- DNS resolution failure.
- Gateway connectivity problems.

Diagnostic commands:

Display network interfaces:

ip addr

Display routing information:

ip route

Test connectivity to an IP address:

ping -c 4 1.1.1.1

Test domain name resolution:

getent hosts google.com

Troubleshooting approach:

1. Check whether a network interface is available.
2. Inspect the IP address configuration.
3. Verify the default gateway.
4. Test connectivity using an IP address.
5. Test DNS resolution using a domain name.
6. Identify whether the issue is related to connectivity or DNS.

Note: NetHunter Rootless uses Android's networking environment, so some network diagnostics may behave differently from a full Linux installation.

## Service Troubleshooting

Problem: A Linux service is not working

Possible causes:

- Service is stopped.
- Incorrect configuration.
- Missing dependencies.
- Insufficient permissions.

Diagnostic commands:

Check whether systemctl is available:

command -v systemctl

If supported, inspect a service:

systemctl status service-name

Check running processes:

ps aux

Inspect available logs:

journalctl -xe

Troubleshooting approach:

1. Identify the affected service.
2. Check its current status.
3. Review relevant error messages.
4. Investigate configuration and dependencies.
5. Apply an appropriate fix.
6. Verify that the service operates correctly.

Note: systemd and journalctl may not be available in a NetHunter Rootless environment.

## File Permission Troubleshooting

Problem: Permission denied error

Possible causes:

- Incorrect file permissions.
- Incorrect file ownership.
- Insufficient user privileges.

Diagnostic commands:

Inspect permissions:

ls -l filename

Identify current user:

whoami

Display user and group information:

id

Troubleshooting approach:

1. Identify the affected file or directory.
2. Inspect its permissions.
3. Check ownership.
4. Determine which permissions are required.
5. Apply the minimum necessary permission changes.
6. Verify access.

Avoid using chmod 777 as a general solution.

## Log File Investigation

System logs provide useful information when investigating Linux problems.

Display recent system messages

dmesg | tail -n 20

Display recent authentication log entries

Where the relevant log exists and access is permitted:

tail -n 20 /var/log/auth.log

Search logs for errors

grep -i error filename

Log locations and permissions depend on the Linux distribution and environment.

## Practical Troubleshooting Methodology

A structured troubleshooting process helps prevent unnecessary changes.

1. Identify the reported problem.
2. Gather relevant information.
3. Reproduce the issue where safe.
4. Identify possible causes.
5. Perform diagnostic tests.
6. Apply the appropriate solution.
7. Verify that the issue is resolved.
8. Document the findings and solution.

## Practical Exercises

1. Use top to inspect running processes.
2. Check available memory using free -h.
3. Inspect filesystem usage using df -h.
4. Display network interfaces using ip addr.
5. Test connectivity using ping.
6. Inspect file permissions using ls -l.
7. Investigate recent kernel messages using dmesg.

Record the commands, actual results and observations.

## Learning Outcomes

After completing this section, I should be able to:

- Identify common Linux system performance problems.
- Investigate disk-space issues.
- Diagnose basic network connectivity problems.
- Understand service-related errors.
- Investigate file permission problems.
- Read and interpret basic system logs.
- Follow a structured troubleshooting methodology.

---

Project: IT Support Toolkit

Category: Linux Administration

Lab: 03 – Linux Troubleshooting

Status: Documentation in progress
