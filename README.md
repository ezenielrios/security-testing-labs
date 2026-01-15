# Security Testing Labs

This repository documents hands-on security testing labs performed in a controlled, isolated environment to practice safe scoping, network discovery, service enumeration, and security tooling analysis.

## What This Repository Demonstrates
- Practical security testing workflows, not theoretical exercises
- Manual web application testing using Burp Suite (request/response analysis)
- Network discovery and enumeration using Nmap
- Vulnerability management tooling with OpenVAS/GVM, including setup and troubleshooting
- Emphasis on methodology, limitations, and realistic constraints



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
