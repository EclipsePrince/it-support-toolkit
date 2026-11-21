## Linux User Management

## Overview

Linux user management involves creating, modifying, monitoring and deleting user accounts and managing group memberships.

User management is an important part of Linux system administration because it helps control access to system resources and maintain security.

This document covers essential Linux user and group management commands.

## Identifying Users

Display the current user

whoami

Displays the username of the currently logged-in user.

Display user and group IDs

id

Displays the current user's UID, primary GID and supplementary groups.

Display logged-in users

who

Displays users currently logged into the system.

View user account information

cat /etc/passwd

Displays the system's local user account database.

Each entry contains information such as username, UID, GID, home directory and login shell.

Security note: Do not confuse "/etc/passwd" with "/etc/shadow". Password hashes are normally stored in "/etc/shadow", which has restricted access.

## Creating User Accounts

Create a new user

sudo useradd username

Creates a new user account.

Create a user with a home directory

sudo useradd -m username

Creates a user and generates a home directory.

Set a user's password

sudo passwd username

Allows an administrator to set or change the account password.

Example

sudo useradd -m labuser
sudo passwd labuser

Creates a user called labuser and sets a password.

## Modifying User Accounts

Change a username

sudo usermod -l newname oldname

Changes an existing username.

Add a user to a supplementary group

sudo usermod -aG groupname username

Adds a user to an additional group.

The "-aG" options append the user to the specified supplementary group without replacing existing supplementary group memberships.

Lock a user account

sudo passwd -l username

Locks password authentication for the account.

Unlock a user account

sudo passwd -u username

Unlocks password authentication for the account.

## Deleting User Accounts

Delete a user

sudo userdel username

Deletes a user account.

Delete a user and their home directory

sudo userdel -r username

Deletes the account and removes its associated home directory and mail spool where applicable.

Important: Always verify the account and its files before deleting a user.

## Linux Group Management

Groups allow administrators to manage permissions for multiple users.

Display groups

groups

Displays the groups associated with the current user.

Display a specific user's groups

groups username

Displays group memberships for a specified user.

Create a group

sudo groupadd developers

Creates a group called developers.

Add a user to a group

sudo usermod -aG developers labuser

Adds labuser to the developers group.

Delete a group

sudo groupdel developers

Deletes the specified group.

## User Account Security

Good user management practices include:

- Use strong, unique passwords.
- Avoid sharing administrator accounts.
- Follow the principle of least privilege.
- Review user accounts regularly.
- Remove accounts that are no longer required.
- Avoid granting unnecessary administrative privileges.
- Use sudo for controlled administrative operations.

## Practical Exercises

Complete these exercises in a controlled Linux environment:

1. Identify the current username.
2. Display the current user's UID and GID.
3. Display the available user accounts.
4. Display your current group memberships.
5. Create a test user named labuser.
6. Create a group named it-support.
7. Add labuser to the it-support group.
8. Verify the user's group membership.
9. Remove the test user after completing the exercise.

## Important NetHunter Considerations

Kali NetHunter Rootless runs within a restricted environment on Android.

Some administrative commands may be unavailable or restricted because the environment does not have full root access to the Android host.

Before attempting user-management operations, verify your environment and privileges.

Useful commands:

whoami
id
command -v sudo
command -v useradd
command -v groupadd

Do not attempt to modify Android system accounts from the NetHunter container.

## Learning Outcomes

After completing this section, I should be able to:

- Identify Linux users and groups.
- Understand UID and GID.
- Create and manage Linux user accounts.
- Modify user group memberships.
- Explain basic account security.
- Understand administrative privileges.

---

Project: IT Support Toolkit

Category: Linux Administration

Lab: 02 – User Management

Status: Documentation in progress
