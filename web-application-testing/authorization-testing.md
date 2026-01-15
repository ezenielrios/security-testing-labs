# Authorization Testing

## Objective
Evaluate server-side authorization enforcement and role-based access controls for protected application endpoints.

Testing focuses on validating access decisions at the HTTP protocol level rather than relying on client-side behavior.

---

## Test Case 2.1 – Unauthenticated Access to Administrative Endpoint
_Status: Completed_

This test evaluates whether administrative endpoints are accessible without authentication.

(Details documented after execution.)

---

## Test Case 2.2 – Authenticated User Access to Administrative Endpoint
_Status: Pending_

This test evaluates whether a non-administrative authenticated user can access administrative endpoints.

(Details to be documented after execution.)

---

## Test Case 2.3 – Forced Browsing of Restricted Endpoints
_Status: Pending_

This test evaluates whether protected endpoints can be accessed directly via URL manipulation or request replay.

(Details to be documented after execution.)

---

## Tools & Limitations
- Burp Suite Community Edition
- Manual request analysis only
- Testing performed in a controlled local lab environment (OWASP Juice Shop)
