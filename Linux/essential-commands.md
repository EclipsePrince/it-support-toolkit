Linux Essential Commands

## Overview

This document covers essential Linux commands used in system administration, IT Support and troubleshooting.

The objective is to understand how to navigate the Linux filesystem, inspect system information, manage files and monitor system resources.

## System Information

Check operating system information

uname -a

Displays kernel and system information.

Display Linux distribution information

cat /etc/os-release

Displays the Linux distribution name and version.

Check current username

whoami

Displays the username of the currently logged-in user.

Display system uptime

uptime

Displays how long the system has been running and system load averages.

## File and Directory Management

Display current directory

pwd

Shows the current working directory.

List directory contents

ls -la

Displays files and directories, including hidden files and permissions.

Create a directory

mkdir test-directory

Creates a new directory.

Create a file

touch test.txt

Creates an empty file if it does not already exist.

Copy a file

cp test.txt backup.txt

Creates a copy of a file.

Move or rename a file

mv test.txt renamed.txt

Moves or renames a file.

## User and Permission Management

Display logged-in users

who

Displays users currently logged into the system.

Display user identity and group information

id

Displays user ID, group ID and group memberships.

Check file permissions

ls -l

Displays file permissions and ownership.

Change file permissions

chmod 644 test.txt

Sets the file permissions to read/write for the owner and read-only for group and others.

## Process Management

Display running processes

ps aux

Displays currently running processes.

Monitor system processes

top

Provides a live view of running processes and resource usage.

Find a specific process

pgrep -a ssh

Searches for processes matching the name ssh.

## Disk and Memory Management

Check available disk space

df -h

Displays filesystem disk usage in a human-readable format.

Check directory storage usage

du -sh .

Displays the total storage used by the current directory.

Check memory usage

free -h

Displays RAM and swap memory information. Availability depends on the Linux environment.

## Practical Exercises

Complete these exercises to practise the commands.

1. Identify your Linux distribution.
2. Find your current username.
3. Display your current working directory.
4. Create a directory called "IT-Lab".
5. Create a file called "system-report.txt" inside that directory.
6. Display the file permissions.
7. Check available disk space.
8. Display running processes.

## Learning Outcomes

After completing these exercises, I should be able to:

- Navigate the Linux filesystem.
- Identify operating system information.
- Create and manage files and directories.
- Understand basic Linux file permissions.
- Inspect running processes.
- Check disk and memory usage.

---

Project: IT Support Toolkit
Category: Linux Fundamentals
Status: In Progress
