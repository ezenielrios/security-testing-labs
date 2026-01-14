# Nmap Service Enumeration

## Objective
Enumerate open ports and identify exposed network services on the selected target host within an isolated lab environment.

## Command Used
```bash
nmap -o <sanitized_output> <target_ip>
```
## Results

The scan identified a large number of open TCP ports, indicating extensive service exposure.

Observed open services included (non-exhaustive):

- FTP (21/tcp)

- SSH (22/tcp)

- Telnet (23/tcp)

- SMTP (25/tcp)

- DNS (53/tcp)

- HTTP (80/tcp)

- RPC services (111/tcp)

- SMB / NetBIOS (139/tcp, 445/tcp)

- Remote command execution services (512–514/tcp)

- NFS (2049/tcp)

- Database services (MySQL 3306/tcp, PostgreSQL 5432/tcp)

- VNC (5900/tcp)

- IRC (6667/tcp)

The presence of multiple administrative, legacy, and network services significantly increases the attack surface.

## Notes

- Reverse DNS warnings were observed, which is common in isolated lab environments without configured DNS.

- The target system appears intentionally vulnerable and exposes numerous services by design.

## Evidence

## Evidence

![Sanitized Nmap Service Enumeration Output](sanitized-screenshots/kali-linux-2025.4nmapScans.sanitized.png)

*Figure 1: Sanitized Nmap output showing exposed network services on the target host within an isolated lab environment.*

