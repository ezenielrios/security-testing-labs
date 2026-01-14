# Nmap Service Enumeration

## Objective
Enumerate open ports and identify exposed network services on the selected target host within the isolated lab environment.

## Commands Used

Fast scan of common ports:
```bash
nmap -T4 -F <target_ip>
```
Service and version detection:
```bash
nmap -sV <target_ip>
```

(When appropriate) full TCP port scan:
```bash
nmap -p- -T4 <target_ip>
```
##Observations

Service enumeration revealed multiple exposed services commonly associated with remote access, file sharing, and application hosting.

##Examples of services observed:

-Remote access services (e.g., SSH, Telnet)

-Web services (HTTP)

-File sharing / RPC services (SMB, RPC)

-Database services (e.g., MySQL or PostgreSQL)

-Remote desktop / management services (e.g., VNC)

##Risk Context

A large number of exposed services increases the attack surface.

Legacy protocols (such as Telnet) may transmit data in cleartext.

Administrative and file-sharing services are frequent targets for credential-based attacks.

##Evidence

Sanitized screenshots of Nmap output are stored in:

sanitized-screenshots/
