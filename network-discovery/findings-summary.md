# Network Discovery & Service Enumeration – Findings Summary

## Executive Summary
A scoped network discovery and service enumeration exercise was conducted within an isolated lab environment using intentionally vulnerable systems. The assessment identified multiple exposed network services, resulting in a broad attack surface consistent with legacy or misconfigured hosts.

## Scope
- Testing was limited to a local, isolated lab subnet.
- No external or unauthorized systems were scanned.
- Target systems were intentionally vulnerable test VMs.

## Key Findings

### 1. Broad Attack Surface
- Numerous open TCP ports were identified.
- Exposed services increase the likelihood of exploitation through service-specific vulnerabilities or weak authentication.

### 2. Presence of Insecure or Legacy Protocols
- Cleartext protocols (e.g., Telnet) were observed.
- Such protocols may expose credentials and session data to interception.

### 3. Administrative and Remote Access Services Exposed
- Remote access and management services were accessible from the network.
- These services are commonly targeted for credential attacks, brute force attempts, and lateral movement.

## Risk Context
Systems exposing many services—especially legacy or administrative ones—present elevated risk if deployed in production environments without compensating controls.

## Recommendations
- Disable unnecessary services to reduce attack surface.
- Replace insecure protocols with encrypted alternatives.
- Restrict administrative access through network segmentation and access controls.
- Enforce strong authentication and remove default or weak credentials.

## Evidence
- Host discovery: `nmap-host-discovery.md`
- Service enumeration: `nmap-service-enumeration.md`
- Sanitized screenshots: `sanitized-screenshots/`

