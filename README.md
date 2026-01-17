# Security Testing Labs

Hands-on security testing documentation covering network discovery, web application security, and tooling limitations using intentionally vulnerable lab environments.

This repository demonstrates practical security engineering skills, including traffic interception, authentication testing, service enumeration, and structured reporting aligned with industry standards.

---

## Scope & Ethics

All testing documented in this repository was performed in **isolated lab environments** using **intentionally vulnerable applications** such as OWASP Juice Shop.

- No external or unauthorized systems were tested
- No real user data was accessed
- Activities are strictly educational and defensive in nature

---

## Repository Structure

security-testing-labs/
├── methodology/
├── network-discovery/
├── web-application-testing/
│ ├── authentication/
│ │ ├── evidence/
│ │ └── testcase-02-authentication-interception.md
│ ├── authorization-testing.md
│ ├── findings-summary.md
│ └── overview.md
├── tooling-limitations/
└── README.md

---

## Key Areas Covered

### 🔎 Network Discovery
- Host discovery and service enumeration using Nmap
- Documentation of exposed services and attack surface considerations

### 🌐 Web Application Security Testing
- Proxy-based traffic interception with Burp Suite
- Authentication request inspection and response analysis
- Evidence-backed test cases with screenshots and observations

### 🧰 Tooling & Limitations
- Practical constraints encountered during scanning and interception
- Environment and configuration considerations

---

## Example Test Case

**Test Case 02 — Authentication Request Interception**

- Captures `POST /rest/user/login` via Burp Suite
- Observes `401 Unauthorized` responses for invalid credentials
- Demonstrates visibility into sensitive authentication flows

See:
web-application-testing/authentication/testcase-02-authentication-interception.md

---

## Career Direction

This repository reflects a focus on **Security Engineering and Security Testing**, emphasizing:

- Understanding how applications behave under attack
- Validating security controls through observation and evidence
- Communicating findings clearly and professionally

---

## Disclaimer

This repository is intended for **educational and defensive security purposes only**.

Do not attempt to replicate these techniques on systems you do not own or have explicit permission to test.
