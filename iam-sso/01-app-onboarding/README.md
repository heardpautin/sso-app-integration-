
# SSO Application Onboarding – IAM Operations

## Purpose
This folder documents the **end-to-end SSO application onboarding process** used in IAM operations.
It is designed as a practical, repeatable reference for implementing and supporting SSO using
Microsoft Entra ID (Azure AD).

This documentation focuses on **process, decision points, and failure patterns** — not vendor marketing
or environment-specific details.

---

## What This Covers
- How applications are evaluated for SSO readiness
- Standard onboarding steps for SAML / OIDC applications
- Common failure scenarios and how IAM teams troubleshoot them
- Clear handoffs between IAM, application owners, and vendors

---

## What This Is NOT
- Not a policy document
- Not access review documentation
- Not environment-specific production configs
- Not tied to any employer or organization

---

## File Guide
- `01-sso-overview.md` – How SSO works at a practical IAM level
- `02-app-onboarding-checklist.md` – Step-by-step onboarding control checklist
- `03-common-sso-failures.md` – Real-world failure modes and fixes

---

## Intended Audience
- IAM Analysts
- Security Engineers (IAM-focused)
- Application Owners (technical)
- Audit & Risk partners (process understanding)

---

## Tools Referenced
- Microsoft Entra ID (Enterprise Applications)
- SAML 2.0 / OIDC concepts
- Conditional Access (contextual, not deep-dive)

---

## Outcome
After completing this module, an IAM analyst should be able to:
- Confidently onboard an app to SSO
- Troubleshoot failed sign-ins
- Explain SSO decisions to technical and non-technical stakeholders
