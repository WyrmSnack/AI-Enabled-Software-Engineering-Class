# Security Checklist

Comprehensive security review checklist for web applications.

## Authentication & Authorization

- [ ] Passwords are hashed (bcrypt, argon2)
- [ ] No passwords in logs or error messages
- [ ] JWT tokens have expiration
- [ ] Tokens stored securely (httpOnly cookies preferred)
- [ ] Password complexity requirements enforced
- [ ] Account lockout after failed attempts
- [ ] Session management implemented
- [ ] Role-based access control (RBAC) if needed
- [ ] Authorization checks on all protected endpoints

## Input Validation

- [ ] All user inputs validated
- [ ] SQL injection prevented (use parameterized queries)
- [ ] XSS prevention (sanitize output)
- [ ] CSRF protection implemented
- [ ] File upload validation (type, size, content)
- [ ] Email validation
- [ ] URL validation
- [ ] Input length limits enforced

## API Security

- [ ] Rate limiting implemented
- [ ] API keys secured (not in code)
- [ ] CORS configured properly
- [ ] HTTPS enforced in production
- [ ] API versioning implemented
- [ ] Request size limits
- [ ] Authentication required for sensitive endpoints
- [ ] Error messages don't leak sensitive info

## Data Security

- [ ] Sensitive data encrypted at rest
- [ ] Sensitive data encrypted in transit (HTTPS)
- [ ] Database credentials in environment variables
- [ ] No secrets in code or version control
- [ ] PII handled according to regulations
- [ ] Data backup and recovery plan
- [ ] Database access restricted
- [ ] Regular security updates applied

## Dependency Security

- [ ] Dependencies up to date
- [ ] Known vulnerabilities checked (npm audit, pip-audit)
- [ ] Only necessary dependencies included
- [ ] Dependency versions pinned
- [ ] Security advisories monitored

## Error Handling

- [ ] Generic error messages to users
- [ ] Detailed errors logged securely
- [ ] No stack traces exposed
- [ ] No sensitive data in error messages
- [ ] Proper error logging

## Configuration

- [ ] Debug mode disabled in production
- [ ] Default passwords changed
- [ ] Unnecessary features disabled
- [ ] Security headers configured
- [ ] Environment variables for secrets
- [ ] Configuration files not in version control

## OWASP Top 10 (2021)

### A01:2021 – Broken Access Control
- [ ] Authorization checks on all endpoints
- [ ] User can't access others' data
- [ ] Privilege escalation prevented

### A02:2021 – Cryptographic Failures
- [ ] Sensitive data encrypted
- [ ] Strong encryption algorithms
- [ ] Keys managed securely

### A03:2021 – Injection
- [ ] SQL injection prevented
- [ ] NoSQL injection prevented
- [ ] Command injection prevented
- [ ] Input sanitized

### A04:2021 – Insecure Design
- [ ] Security considered in design
- [ ] Threat modeling done
- [ ] Security requirements defined

### A05:2021 – Security Misconfiguration
- [ ] Default configurations changed
- [ ] Unnecessary features disabled
- [ ] Security headers set
- [ ] Error handling secure

### A06:2021 – Vulnerable Components
- [ ] Dependencies up to date
- [ ] Vulnerabilities monitored
- [ ] Components verified

### A07:2021 – Authentication Failures
- [ ] Strong authentication
- [ ] Session management secure
- [ ] Password policies enforced

### A08:2021 – Software and Data Integrity
- [ ] CI/CD pipeline secure
- [ ] Dependencies verified
- [ ] Code integrity checked

### A09:2021 – Security Logging Failures
- [ ] Security events logged
- [ ] Logs monitored
- [ ] Incident response plan

### A10:2021 – Server-Side Request Forgery
- [ ] SSRF prevention
- [ ] URL validation
- [ ] Network access restricted

## OWASP API Security Top 10 (2023)

- [ ] API1: Broken Object Level Authorization
- [ ] API2: Broken Authentication
- [ ] API3: Broken Object Property Level Authorization
- [ ] API4: Unrestricted Resource Consumption
- [ ] API5: Broken Function Level Authorization
- [ ] API6: Unrestricted Access to Sensitive Business Flows
- [ ] API7: Server Side Request Forgery
- [ ] API8: Security Misconfiguration
- [ ] API9: Improper Inventory Management
- [ ] API10: Unsafe Consumption of APIs

## Code Review Checklist

- [ ] No hardcoded secrets
- [ ] Input validation present
- [ ] Error handling secure
- [ ] Authentication/authorization correct
- [ ] SQL injection prevented
- [ ] XSS prevented
- [ ] CSRF protection
- [ ] Rate limiting considered
- [ ] Logging appropriate (no sensitive data)

## Deployment Security

- [ ] Production environment secured
- [ ] Database access restricted
- [ ] Firewall rules configured
- [ ] SSL/TLS certificates valid
- [ ] Security monitoring enabled
- [ ] Backup and recovery tested
- [ ] Incident response plan ready

## Regular Maintenance

- [ ] Security updates applied regularly
- [ ] Dependencies updated
- [ ] Security audits performed
- [ ] Penetration testing done
- [ ] Security training completed
- [ ] Security policies reviewed

---

## Quick Security Review

Before deploying, ask:
1. Are all inputs validated?
2. Are all endpoints protected?
3. Are secrets in environment variables?
4. Is sensitive data encrypted?
5. Are dependencies up to date?
6. Is error handling secure?
7. Is logging secure?
8. Is HTTPS enforced?

---

## Resources

- [OWASP Top 10](https://owasp.org/www-project-top-ten/)
- [OWASP API Security](https://owasp.org/www-project-api-security/)
- [OWASP Cheat Sheets](https://cheatsheetseries.owasp.org/)
- [Security Best Practices](https://owasp.org/www-project-web-security-testing-guide/)

