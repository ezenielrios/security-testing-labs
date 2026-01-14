# Nmap Host Discovery

## Objective
Identify live hosts on the isolated lab subnet prior to conducting any targeted port or service enumeration.

## Command Used
```bash
nmap -sn <lab_subnet>/24
```
Results

Multiple live hosts were identified within the lab network.

Discovered hosts included:

Attacker VM

Target VM(s)

Virtual network gateway / host adapter

One target host was selected for follow-on service enumeration.

Notes

Reverse DNS warnings may appear in isolated lab environments without configured DNS.

Host discovery was strictly limited to the lab subnet.

Evidence

Sanitized Nmap output screenshots are stored in:

sanitized-screenshots/
