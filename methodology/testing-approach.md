# Testing Approach (Repeatable Workflow)

## 1) Pre-checks (Safety)
- Confirm scope is limited to an isolated lab subnet.
- Use host-only / internal networking for testing.
- Enable NAT only when updating tools/feeds, then disable NAT again.

## 2) Host Discovery
Goal: identify live hosts before scanning ports.

Example:
```bash
nmap -sn 192.168.56.0/24
```

#### **Service Enumeration**

Example:
```bash
nmap -T4 -F <target_ip>
```


