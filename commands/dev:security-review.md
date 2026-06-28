---
description: Perform a focused security review and remediation plan
---

# Security Review

Perform a comprehensive security review of the target code and provide specific remediation steps with code examples for each security issue identified.

## Inputs

- Optional PR, branch, commit range, file path, service, or security focus: `$ARGUMENTS`

## Steps

1. **Scope the review**
   - Use `$ARGUMENTS` to identify the PR, branch, commit range, file path, service, or security focus.
   - If no target is provided, review the current repository changes using git status and diff.
   - Identify trust boundaries, external inputs, privileged operations, and sensitive data flows.
2. **Authentication & authorization**
   - Verify proper authentication mechanisms.
   - Check authorization controls and permission systems.
   - Review session management and token handling.
   - Ensure secure password policies and storage where applicable.
3. **Input validation & sanitization**
   - Identify SQL, command, template, path traversal, and injection vulnerabilities.
   - Check for XSS and CSRF attack vectors.
   - Validate user inputs, API parameters, request bodies, and uploaded files.
   - Review file upload, parsing, and processing security.
4. **Data protection**
   - Ensure sensitive data is encrypted at rest and in transit where required.
   - Check for data exposure in logs, errors, traces, analytics, and API responses.
   - Review secrets management and avoid hardcoded credentials.
   - Verify least-privilege access to sensitive data.
5. **Infrastructure and dependency security**
   - Review dependency security and known vulnerability exposure when tooling exists.
   - Check HTTPS configuration and certificate validation when relevant.
   - Analyze CORS policies, cookies, security headers, and cache behavior.
   - Review environment variable and configuration security.
6. **Report findings**
   - Prioritize findings by severity and exploitability.
   - Include affected paths, concrete evidence, impact, and remediation steps.
   - Provide code examples for fixes when they are useful and safe.
   - If no issues are found, state the scope reviewed and residual risks.

## Security Review Checklist

- [ ] Review scope and trust boundaries identified
- [ ] Proper authentication mechanisms verified
- [ ] Authorization controls and permission systems checked
- [ ] Session management and token handling reviewed
- [ ] Password policies and storage reviewed where applicable
- [ ] SQL, command, path traversal, and injection risks checked
- [ ] XSS and CSRF attack vectors checked
- [ ] User inputs, API parameters, and uploaded files validated
- [ ] Sensitive data exposure in logs/errors/responses checked
- [ ] Secrets management reviewed
- [ ] Dependency security reviewed when tooling exists
- [ ] CORS policies, cookies, and security headers analyzed when relevant

## Output

Return a concise security review with severity-labeled findings. For each finding include: affected path, evidence, risk, remediation, and verification step. Do not report speculative issues without evidence from the reviewed code or configuration.
