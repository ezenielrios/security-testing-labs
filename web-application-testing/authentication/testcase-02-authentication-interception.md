# Test Case 2 — Burp Suite Authentication Request Interception (Login POST)

## Objective
Validate that HTTP traffic from the browser is successfully routed through Burp Suite and capture the authentication request made by OWASP Juice Shop during a login attempt.

## Lab Context (Scope & Ethics)
- Testing performed in an isolated lab environment using intentionally vulnerable targets.
- No external or unauthorized systems were tested.

## Tools Used
- Burp Suite Community Edition (Proxy + HTTP History)
- Burp Browser (preconfigured proxy browser)
- OWASP Juice Shop

## Target
- OWASP Juice Shop (local lab instance)
- Example URL: `http://127.0.0.1:3000` or `http://192.168.56.103:3000`

## Procedure (Steps)
1. Launch Burp Suite and confirm the proxy listener is running on `127.0.0.1:8080`.
2. Open **Burp Browser** from Burp (Proxy → Open browser).
3. Navigate to the Juice Shop login page: `http://<target_ip>:3000/#/login`.
4. Generate traffic by browsing the application and attempting a login.
5. In **Proxy → HTTP history**, confirm multiple Juice Shop endpoints are captured.
6. Filter for the login request and select:
   - `POST /rest/user/login`
7. Review the request and response to confirm the authentication flow is visible in Burp.

## Results / Observations
- Burp successfully captured Juice Shop traffic in HTTP history.
- The login request was observed as:
  - `POST /rest/user/login`
- The response returned **401 Unauthorized**, confirming the authentication endpoint behavior for invalid credentials.

## Security Notes
- Capturing authentication requests confirms proxy visibility of sensitive flows (credentials, tokens, session cookies).
- A 401 response validates server-side enforcement for invalid login attempts.

## Evidence
### HTTP History showing Juice Shop endpoints
![Burp HTTP history showing Juice Shop endpoints](sanitized-screenshots/burp-http-history-juice-shop-endpoints.png)

### Login request captured (POST /rest/user/login → 401 Unauthorized)
![Intercepted login POST returning 401 Unauthorized](sanitized-screenshots/testcase-02-login-post-401-intercept.png)
