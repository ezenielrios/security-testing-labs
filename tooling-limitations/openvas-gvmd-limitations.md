# OpenVAS / GVM Limitations

## Overview
OpenVAS (Greenbone Vulnerability Management) is a widely used vulnerability scanning platform designed to identify known vulnerabilities, misconfigurations, and outdated software across networked systems. While valuable for baseline assessments, OpenVAS has inherent limitations that must be understood to avoid false confidence in scan results.

This document outlines key constraints observed during lab usage and explains why OpenVAS should be combined with other testing methods.

---

## Key Limitations

### 1. Signature-Based Detection
OpenVAS relies primarily on vulnerability signatures (NVTs). As a result:
- Unknown or zero-day vulnerabilities are not detected
- Custom applications and logic flaws are typically missed
- Results are limited to what the signature database knows

---

### 2. False Positives and False Negatives
Scan results may include:
- False positives due to banner grabbing or incomplete service detection
- False negatives caused by network latency, filtered ports, or hardened configurations

Manual validation is required before treating findings as confirmed vulnerabilities.

---

### 3. Limited Application-Layer Context
OpenVAS performs poorly against modern web applications because it:
- Does not understand application workflows
- Cannot assess authentication logic or authorization controls
- Does not validate business logic flaws

Dedicated web testing tools (e.g., Burp Suite) are required for application-layer security testing.

---

### 4. Performance and Stability Constraints
During lab testing:
- Scans were resource-intensive
- Feed updates and service synchronization occasionally failed
- Large scans increased the likelihood of incomplete or stalled results

These factors make OpenVAS unsuitable for continuous or real-time security validation.

---

### 5. No Exploitation or Impact Verification
OpenVAS identifies potential vulnerabilities but:
- Does not exploit findings
- Does not confirm real-world impact
- Cannot assess exploitability or attack chaining

Human analysis is required to determine actual risk.

---

## Security Engineering Takeaway
OpenVAS is best used as:
- An initial discovery and hygiene tool
- A support mechanism for vulnerability management programs

It should always be paired with:
- Manual verification
- Network enumeration
- Web application testing
- Threat modeling and contextual analysis

Relying solely on automated scanning creates blind spots and increases organizational risk.

---

## Conclusion
OpenVAS is a useful component of a security toolkit, but it is not a complete security solution. Effective security engineering requires understanding tool limitations and applying layered testing approaches to accurately assess risk.
