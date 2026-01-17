# Test Case 02 – Authentication Request Interception (Burp Suite)

## Objective
Observe and analyze authentication requests sent by the OWASP Juice Shop application in order to understand how credentials are transmitted and how the application responds to invalid login attempts.

## Scope
- Application: OWASP Juice Shop
- Target: Authentication endpoint (`/rest/user/login`)
- Tooling: Burp Suite Community Edition
- Environment: Isolated local lab network

## Preconditions
- OWASP Juice Shop is running and accessible.
- Browser traffic is configured to proxy through Burp Suite.
- Burp Proxy interception is enabled.
- Testing is limited to an intentionally vulnerable lab application.

## Test Steps

1. Launch Burp Suite and confirm the proxy listener is running on `127.0.0.1:8080`.
2. Open the **Burp Browser**.
3. Navigate to the Juice Shop login page:
http://<target_ip>:3000/#/login

4. Enter invalid credentials into the login form.
5. Submit the login request.
6. Observe the intercepted HTTP `POST` request in Burp Proxy → HTTP history.

## Observations

- The application submits credentials via a `POST` request to:


/rest/user/login

- Credentials are transmitted in JSON format:
```json
{
  "email": "test@test.com",
  "password": "test123"
}
```

- The server responds with:

  HTTP/1.1 401 Unauthorized


- Error message indicates invalid credentials without exposing sensitive internal details.

## Security Implications

- Authentication requests are clearly identifiable and interceptable.

- Brute-force protections, rate limiting, and account lockout controls should be evaluated.

- This endpoint represents a common target for credential-based attacks.

## Evidence

### HTTP History showing Juice Shop endpoints
![Burp HTTP history showing Juice Shop endpoints](authentication/evidence/burp-http-history-juice-shop-endpoints.png)

### Login request captured (POST /rest/user/login → 401 Unauthorized)
![Intercepted login POST returning 401 Unauthorized](authentication/evidence/testcase-02-login-post-401-intercept.png)

## Result

Authentication traffic was successfully intercepted and analyzed using Burp Suite, confirming visibility into credential handling and server-side authentication responses.
