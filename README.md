# Task 1: Basic Network Scanning with Nmap

## Objective
Perform a network scan using Nmap to identify open ports and running
services on a target machine, and document what was found.

## Tools Used
- Nmap 7.99
- Target: my own Windows laptop (localhost)

## Steps
1. Installed Nmap from https://nmap.org/download.html (with Npcap included).
2. Opened Command Prompt and ran: nmap -sV -T4 localhost -oN nmap_scan_results.txt
3. Reviewed the results and documented each open port below.

## Results
See `nmap_scan_results.txt` for the raw output and `screenshot1.png` for
a screenshot of the scan running.

| Port | Service | What it means | Security significance |
|------|---------|----------------|------------------------|
| 135/tcp | MSRPC (Microsoft Windows RPC) | Used internally by Windows for programs to communicate with each other and other machines. | Should never be exposed to the public internet - it has historically been used in remote exploits. Fine on a private/local network. |
| 445/tcp | Microsoft-DS (SMB) | Windows file and printer sharing protocol. | A common attack target (e.g. WannaCry ransomware used this port). Should be blocked from external/internet access and only allowed on trusted local networks. |

## Key Takeaways
- Both open ports are normal for a Windows machine on a local network.
- Neither should be exposed to the internet directly; Windows Firewall
  should keep them restricted to the local network only.
- Regularly scanning your own machine helps you notice unexpected new
  open ports, which could indicate malware or misconfiguration.

## Legal / Ethical Note
This scan was performed only against my own machine (localhost).
Scanning systems without permission is illegal - always get explicit
authorization before scanning any device that isn't yours.

## Deliverables
- [x] nmap_scan_results.txt - raw scan output
- [x] screenshot1.png - screenshot of the scan running
- [x] README.md - this file