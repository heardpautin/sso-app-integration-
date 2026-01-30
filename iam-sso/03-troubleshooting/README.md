# SSO Troubleshooting – Common Failures & Diagnostics

## Purpose
This document outlines common SSO failures and how IAM teams typically diagnose and resolve them.

It reflects **real-world IAM operational troubleshooting**, not textbook theory.

---

## Common SSO Failure Scenarios

### 1. User Cannot Access Application
**Possible Causes**
- User not assigned to the application
- Group or role missing
- Incorrect license

**Checks**
- Application user assignments
- Group membership
- Access reviews / entitlement records

---

### 2. Authentication Succeeds but Access Is Denied
**Possible Causes**
- Token missing required claims
- Role mapping mismatch
- Application-side authorization failure

**Checks**
- Token claims configuration
- Application role mappings
- Application logs

---

### 3. MFA or Conditional Access Blocking Access
**Possible Causes**
- Conditional Access policy applies unexpectedly
- Location or device requirements not met

**Checks**
- Sign-in logs
- Conditional Access policy evaluation
- Authentication details

---

### 4. Infinite Redirect or Login Loop
**Possible Causes**
- Incorrect redirect URI
- Token validation failure
- Session cookie issues

**Checks**
- Redirect URI configuration
- Token audience and issuer
- Browser session data

---

### 5. Access Works for Some Users but Not Others
**Possible Causes**
- Group overage
- Role assignment inconsistencies
- Nested group limitations

**Checks**
- Group size and nesting
- Claims filtering
- User-specific sign-in logs

---

## Troubleshooting Data Sources
- IdP sign-in logs
- Audit logs
- Application logs
- Access review evidence

---

## Operational Principle
SSO troubleshooting is rarely about **authentication alone** — it is usually a combination of:
- Identity
- Authorization
- Policy
- Application behavior

Understanding where the failure occurs in the flow is the key to fast resolution.
