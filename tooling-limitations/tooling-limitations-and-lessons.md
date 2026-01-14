# Tooling Limitations & Lessons Learned

## Tooling Limitations

### Network Isolation Constraints
- Testing was conducted within a host-only / isolated lab network.
- Lack of DNS services resulted in reverse DNS warnings during Nmap scans.
- These limitations reflect realistic constraints often encountered in segmented enterprise environments.

### Vulnerability Scanning Tooling
- Greenbone/OpenVAS feed synchronization required stable internet connectivity and proper service sequencing.
- Scanner configuration and feed availability directly impacted scan readiness and completeness.
- Tool behavior reinforced the importance of validating scanner state before initiating assessments.

### Automated Scan Coverage
- Automated tools identify potential exposure but do not replace manual validation.
- Service presence alone does not confirm exploitability without further testing and context.

## Lessons Learned

### Importance of Scope Control
- Strict subnet scoping prevents accidental scanning of unauthorized systems.
- Clear scope definition mirrors professional penetration testing and red team engagements.

### Documentation Matters as Much as Detection
- Sanitized evidence and structured write-ups are critical for communicating risk.
- Clear reporting enables stakeholders to understand impact without technical overload.

### Tool Reliability ≠ Security Insight
- Tools assist discovery, but analyst interpretation determines value.
- Understanding why a service is risky matters more than simply detecting it.

### Enterprise Relevance
- Real-world environments often contain legacy services, misconfigurations, and operational constraints.
- Effective security testing balances technical findings with business and operational context.
