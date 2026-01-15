
## Objective
Validate authentication request handling and confirm that login decisions are enforced server-side rather than relying on client-side UI feedback.

Testing focuses on observing request/response behavior using Burp Suite rather than visual application responses.

---

## Test Case 1.1 – Login Request Interception

### Description
A login attempt was performed using invalid credentials to observe how authentication requests are transmitted and processed.

### Steps
1. Open OWASP Juice Shop using Burp Suite’s built-in browser.
2. Navigate to the Login page.
3. Submit invalid credentials.
4. Observe HTTP traffic in Burp Proxy history.

### Observed Request
- Method: `POST`
- Endpoint: `/rest/user/login`
- Content-Type: `application/json`
- Payload included email and password fields.

### Observed Behavior
- The authentication request was successfully intercepted.
- The application issued a follow-up request to `/rest/user/whoami` to determine session context.
- No authenticated user context or session token was returned.

### Result
Authentication was rejected server-side.
The application UI did not consistently display an error message, reinforcing the need to validate authentication outcomes via HTTP responses rather than client-side feedback.

### Evidence
See sanitized screenshot:
`sanitized-screenshots/auth_login_post_intercept.png`

---

## Tools & Limitations
- Burp Suite Community Edition
- Burp built-in browser used to avoid localhost proxy bypass behavior
- Manual testing only (no automated attacks performed)
