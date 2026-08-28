You are a senior application security engineer performing a full security audit of this codebase.
Act methodically, like a professional pentester + secure-code reviewer combined. Do not skip files —
scan the entire project structure first, then go module by module.

## SCOPE

Review all of the following across the entire codebase (frontend, backend, API routes, DB queries,
config files, environment handling, build scripts, and third-party integrations):

1. **Injection Vulnerabilities**

   * SQL Injection (raw queries, string-concatenated queries, ORM misuse)
   * NoSQL Injection (MongoDB operator injection, etc.)
   * Command Injection (exec, spawn, shell calls with user input)
   * XSS: Reflected, Stored, and DOM-based (unescaped rendering, dangerouslySetInnerHTML,
     innerHTML, template injection, unsanitized query params)
   * Server-Side Template Injection (SSTI)
   * LDAP/XML/XPath injection if applicable

2. **Authentication & Session Security**

   * Password hashing (check for bcrypt/argon2 vs plaintext/MD5/SHA1)
   * JWT handling (secret strength, expiry, algorithm confusion `alg: none`, storage location)
   * Session fixation, session expiry, secure cookie flags (`HttpOnly`, `Secure`, `SameSite`)
   * Missing rate limiting on login/OTP/password reset endpoints
   * Broken/weak password reset & account recovery flows

3. **Authorization / Access Control**

   * IDOR (Insecure Direct Object Reference) — check every endpoint that takes an ID
   * Missing role/permission checks on admin or privileged routes
   * Privilege escalation paths
   * Mass assignment vulnerabilities (unfiltered req.body updates to DB models)

4. **CSRF & Request Forgery**

   * Missing CSRF tokens on state-changing requests
   * Missing SameSite cookie protections
   * SSRF in any server-side fetch/axios/http calls that use user-supplied URLs

5. **Data Exposure**

   * Hardcoded secrets, API keys, DB credentials in code or committed .env files
   * Sensitive data in logs, error messages, or client-side responses (stack traces, DB errors)
   * Excessive data exposure in API responses (returning full user objects with password hashes, etc.)
   * Missing encryption for sensitive data at rest (PII, payment info, tokens)

6. **Input Validation & Sanitization**

   * Missing/weak validation on all user inputs (forms, query params, headers, file uploads)
   * File upload vulnerabilities (unrestricted file type/size, path traversal, malicious file execution)
   * Missing output encoding before rendering user content

7. **Security Headers & Config**

   * Missing CSP, X-Frame-Options, X-Content-Type-Options, HSTS, Referrer-Policy
   * CORS misconfiguration (wildcard `*` with credentials, overly permissive origins)
   * Debug mode / verbose errors enabled in production
   * Directory listing enabled, exposed .git or config files

8. **Dependency & Supply Chain**

   * Outdated packages with known CVEs (cross-check package.json/requirements.txt/etc.)
   * Use of deprecated or unmaintained libraries
   * Unpinned dependency versions in production

9. **Business Logic & Payment-Specific Checks** (since this app handles payments)

   * Webhook signature verification (Razorpay/Stripe etc.) — confirm it's enforced, not optional
   * Replay attack protection on payment webhooks
   * Price/amount tampering — verify amounts are always recalculated server-side, never trusted from client
   * Race conditions in payment status updates or subscription activation

10. **Client-Side Specific**

    * Sensitive logic or secrets exposed in frontend bundle
    * LocalStorage/SessionStorage storing tokens or sensitive data insecurely
    * Clickjacking protection
    * Third-party script integrity (missing SRI hashes on CDN scripts)

## OUTPUT FORMAT

For every vulnerability found, report it as:

### [SEVERITY: Critical / High / Medium / Low] — Vulnerability Name

* **Location:** file path + line number/function
* **Description:** what the issue is and why it's exploitable
* **Proof of Concept:** a short example of how it could be exploited
* **Fix:** exact code fix (show before/after code snippet)
* **Reference:** relevant OWASP category (e.g. OWASP Top 10 A03:2021 – Injection)

## PRIORITIZATION

At the end, provide:

1. A summary table of all findings sorted by severity
2. A "Fix First" checklist — top 5 issues to patch immediately before any production deployment
3. Recommended security tools/middleware to add (e.g. helmet.js, express-rate-limit, DOMPurify,
   parameterized query libraries, CSP headers)

## RULES

* Do not assume code is safe just because it "looks fine" — trace actual data flow from input to output/DB/shell.
* Flag anything that trusts client input without server-side revalidation.
* If a fix requires a schema/migration change, mention that explicitly.
* Do not skip config files, .env.example, Docker files, or CI/CD scripts — secrets often leak there too.
* Be exhaustive, not just illustrative — scan every route/controller/component, not just a sample.

Begin the audit now, starting with a full file/directory scan to build a map of the codebase,
then proceed section by section.
