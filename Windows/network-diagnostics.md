## Windows Network Diagnostics

## Overview

Network diagnostics involve identifying, investigating and resolving connectivity problems affecting computers and network resources.

IT Support Technicians use Windows command-line utilities and PowerShell commands to investigate IP configuration, DNS resolution, network connectivity and routing.

This document covers essential Windows networking commands and practical troubleshooting procedures.

## Understanding Network Fundamentals

IP Address

An Internet Protocol (IP) address identifies a device on an IP network.

Example:

192.168.1.100

Subnet Mask

A subnet mask determines which portion of an IP address identifies the network and which portion identifies the host.

Example:

255.255.255.0

Default Gateway

A default gateway allows a computer to communicate with devices outside its local network.

Example:

192.168.1.1

DNS

Domain Name System (DNS) translates domain names into IP addresses.

Example:

google.com

DHCP

Dynamic Host Configuration Protocol (DHCP) automatically assigns network configuration to devices.

## IP Configuration

Display IP configuration

ipconfig

Displays basic IP configuration.

Display detailed IP configuration

ipconfig /all

Displays:

- IP addresses.
- Subnet masks.
- Default gateways.
- DNS servers.
- DHCP status.
- MAC addresses.

Release IP configuration

ipconfig /release

Releases DHCP-assigned IPv4 configuration for applicable adapters.

Renew IP configuration

ipconfig /renew

Requests new DHCP configuration.

Flush DNS cache

ipconfig /flushdns

Clears the local DNS resolver cache.

## Connectivity Testing

Test connectivity to an IP address

ping 8.8.8.8

Tests whether the destination responds to ICMP echo requests.

Test connectivity to a domain

ping google.com

Tests connectivity using a hostname, which also involves name resolution.

Test the default gateway

ping 192.168.1.1

Replace the example address with the actual default gateway.

Interpret ping results

Result| Possible meaning
Reply from| Destination responded
Request timed out| No response received within the timeout
Destination host unreachable| A routing or connectivity problem may exist
Could not find host| Name resolution may have failed

A failed ping does not always mean a destination is unavailable because firewalls may block ICMP traffic.

## DNS Diagnostics

Resolve a domain name

nslookup google.com

Displays DNS resolution information.

Query a specific DNS server

nslookup google.com 8.8.8.8

Requests DNS resolution using the specified DNS server.

Display DNS cache

ipconfig /displaydns

Displays cached DNS resolver records.

Troubleshooting approach

1. Confirm general network connectivity.
2. Test connectivity to an external IP address.
3. Test domain name resolution.
4. Inspect the configured DNS servers.
5. Flush the DNS cache if appropriate.
6. Verify that name resolution works.

## Network Route Diagnostics

Display the routing table

route print

Displays the computer's IPv4 and IPv6 routing tables.

Trace the route to a destination

tracert google.com

Displays the network hops between the computer and destination.

Test a network path

pathping google.com

Combines route tracing with network packet-loss analysis.

## Network Connection Monitoring

Display active network connections

netstat -ano

Displays active connections, listening ports and process IDs.

Display network adapters

PowerShell:

Get-NetAdapter

Displays network adapters and their operational status.

Display IP configuration using PowerShell

Get-NetIPConfiguration

Displays network interface configuration, IP addresses and gateways.

Test a TCP connection

Test-NetConnection google.com -Port 443

Tests connectivity to the destination using TCP port 443.

## Common Network Troubleshooting Scenarios

Scenario 1: No internet connectivity

Possible causes:

- Disconnected network connection.
- Incorrect IP configuration.
- Gateway failure.
- DNS issues.

Diagnostic procedure:

1. Check network adapter status.
2. Run "ipconfig /all".
3. Ping the default gateway.
4. Ping an external IP address.
5. Test DNS resolution.
6. Identify the failing network layer.

Scenario 2: One computer cannot access the internet

Possible causes:

- Incorrect network settings.
- Adapter problems.
- DHCP issues.
- DNS configuration errors.

Diagnostic procedure:

1. Determine whether other computers have connectivity.
2. Inspect the affected computer's IP configuration.
3. Check its default gateway and DNS servers.
4. Test local and external connectivity.
5. Compare its configuration with a working computer.
6. Apply the appropriate correction.

Scenario 3: Internet works but websites do not load

Possible causes:

- DNS resolution failure.
- Browser configuration problems.
- Proxy configuration.
- Website-specific problems.

Diagnostic procedure:

1. Test external IP connectivity.
2. Run "nslookup" on the affected domain.
3. Inspect DNS configuration.
4. Check browser and proxy settings.
5. Test another website.
6. Verify whether the issue has been resolved.

## Practical Exercises

Complete the following exercises on a Windows computer:

1. Display the computer's IP configuration.
2. Identify the default gateway.
3. Identify the DNS servers.
4. Test connectivity to the default gateway.
5. Test connectivity to 8.8.8.8.
6. Resolve google.com using nslookup.
7. Display the routing table.
8. Trace the route to google.com.
9. Display active network connections.
10. Test TCP connectivity on port 443.

Record actual command outputs and observations.

## Learning Outcomes

After completing this section, I should be able to:

- Understand basic IP addressing.
- Inspect DHCP and DNS configuration.
- Diagnose network connectivity problems.
- Test connectivity using ping.
- Investigate DNS resolution failures.
- Inspect routing information.
- Monitor active network connections.
- Troubleshoot common Windows networking incidents.

---

Project: IT Support Toolkit

Category: Windows Administration

Lab: Network Diagnostics

Status: Documentation in progress
