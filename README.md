# Security Testing Labs

This repository documents hands-on security testing labs performed in a controlled, isolated environment to practice safe scoping, network discovery, service enumeration, and security tooling analysis.

## Scope & Ethics
- All testing was conducted in a local, isolated lab network.
- Targets were intentionally vulnerable or owned test systems.
- No testing was performed against external or unauthorized systems.

## Tools Used
- Kali Linux
- Nmap
- OpenVAS / Greenbone (setup + feed troubleshooting)
- VirtualBox (isolated networking)

## Lab Modules
- `network-discovery/` — host discovery + service enumeration with Nmap
- `tooling-limitations/` — tooling constraints + what was done to validate results
- `methodology/` — repeatable testing workflow used during the lab

## How to Use This Repo
Start in `network-discovery/overview.md`, then review the discovery and enumeration notes and screenshots.
