# Security Testing Labs

Hands-on security engineering labs focused on **network discovery**, **web application testing**, and **security tooling analysis** using intentionally vulnerable targets in a controlled lab environment.

This repository documents **how I test systems**, not just the tools I use.

---

## 🎯 Purpose

The goal of this repository is to demonstrate practical security engineering skills, including:

- Identifying exposed services and attack surface
- Intercepting and analyzing authentication flows
- Understanding session handling and authorization boundaries
- Documenting findings clearly and responsibly
- Recognizing tooling limitations and operational realities

All testing is performed **ethically** against **intentionally vulnerable applications** in isolated lab environments.

---

## 🧪 Lab Environment

- **Attacker:** Kali Linux
- **Targets:** 
  - Metasploitable2 
  - OWASP Juice Shop
- **Tools:** 
  - Nmap 
  - Burp Suite Community Edition 
  - Docker 
- **Network:** Isolated host-only / local lab networks

No production, external, or unauthorized systems were tested.

---

## 📂 Repository Structure

security-testing-labs/
├── methodology/
│ └── testing-approach.md
│
├── network-discovery/
│ ├── overview.md
│ ├── nmap-host-discovery.md
│ ├── nmap-service-enumeration.md
│ ├── findings-summary.md
│ └── sanitized-screenshots/
│
├── web-application-testing/
│ └── authentication/
│ ├── testcase-02-authentication-interception.md
│ ├── testcase-03-session-behavior.md
│ └── evidence/
│
├── tooling-limitations/
│ └── openvas-gvmd-limitations.md
│
└── README.md

Each section builds on the previous one, moving from **surface-level discovery** to **application-layer security testing**.

---

## 🔍 What’s Covered

### Network Discovery
- Host discovery and service enumeration
- Attack surface identification
- Risk-based observations and remediation context

### Web Application Testing
- Proxying traffic through Burp Suite
- Intercepting authentication requests
- Analyzing unauthorized vs authenticated behavior
- Observing API responses and session state handling

### Tooling & Limitations
- Practical challenges encountered during setup and use
- Why tools sometimes fail or behave unexpectedly
- Lessons learned from troubleshooting real environments

---

## 📸 Evidence Handling

- Screenshots are **sanitized**
- No credentials, tokens, or personal data are exposed
- Evidence supports findings without oversharing sensitive details

This mirrors real-world reporting standards.

---

## 🧠 Mindset & Approach

This repository emphasizes:

- Understanding **why** something behaves a certain way
- Validating assumptions with evidence
- Thinking like a defender while testing like an attacker
- Clear, structured documentation suitable for technical audiences

---

## 🚀 What’s Next

Planned expansions include:
- Authorization bypass testing
- Input validation and injection testing
- API misuse scenarios
- Mapping findings to OWASP ASVS and Top 10 controls

---

## ⚖️ Disclaimer

All activities documented here were conducted in controlled lab environments for educational and professional development purposes only.

---

If you’re reviewing this repository as part of an interview process, I’m happy to walk through **how each test was designed, executed, and interpreted**.
