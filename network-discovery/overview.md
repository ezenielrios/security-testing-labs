# Network Discovery (Nmap)

## Purpose
This section documents scoped network discovery and service enumeration performed in an isolated lab environment. The goal was to identify live hosts and exposed services on intentionally vulnerable systems prior to deeper testing.

## Scope & Ethics
- All testing was conducted within a local, isolated VirtualBox lab network.
- Targets were intentionally vulnerable systems or owned test assets.
- No scanning was performed against external, production, or unauthorized networks.

## Lab Context
- Attacker system: Kali Linux virtual machine
- Target system(s): Vulnerable VM(s) on the same isolated subnet
- Network type: Host-only / internal networking

## Methodology Overview
1. Perform host discovery to identify live systems within the lab subnet.
2. Select a target host for further analysis.
3. Enumerate open ports and exposed services using Nmap.
4. Capture sanitized evidence and summarize findings.

## Evidence
Detailed results and evidence are documented in:
- `nmap-host-discovery.md`
- `nmap-service-enumeration.md`
- `findings-summary.md`
- `sanitized-screenshots/`

