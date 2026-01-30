# SSO Application Integration – IAM Operations

## Purpose
This project documents the operational process for onboarding and managing applications using Single Sign-On (SSO) in Microsoft Entra ID.

The goal is to demonstrate how IAM supports secure access while enabling business operations through a repeatable, auditable, and supportable process.

This repository focuses on **operations**, not architecture design.

---

## What This Project Covers
- Application onboarding for SSO
- Group-based access assignment
- Token-based authentication flow (high level)
- Common SSO failures and operational troubleshooting
- Evidence and audit considerations

---

## What This Project Does NOT Cover
- Network design
- Custom application development
- Identity federation architecture theory
- Conditional Access policy design (referenced only)

---

## High-Level SSO Flow
1. Application is onboarded into Entra ID
2. Authentication method is configured (SAML / OIDC / OAuth)
3. Users are assigned via security groups or roles
4. User authenticates through Entra ID
5. Entra issues a token containing required claims
6. Application grants or denies access based on claims

---

## Application Onboarding (Operational View)
Typical steps performed by IAM:
- Register or configure the application in Entra ID
- Define required attributes and claims
- Assign security groups to the application
- Validate sign-in behavior
- Document configuration and ownership

IAM does not usually develop the application — it enables secure access to it.

---

## Access Assignment Model
- Users are **not assigned directly**
- Access is granted through:
  - Security groups
  - Application roles
- This supports:
  - Least privilege
  - Easier access reviews
  - Faster onboarding and offboarding

---

## Common SSO Issues (Operational)
- User not in assigned group
- Incorrect claim mapping
- Expired or misconfigured certificate
- Application expects different identifier (email vs UPN)
- Token issued successfully but rejected by application

Troubleshooting typically starts with:
- Entra sign-in logs
- Application configuration
- Group membership validation

---

## Audit & Evidence
This process produces:
- Application ownership records
- Group-based access mappings
- Configuration documentation
- Sign-in and audit logs

These artifacts support:
- Access reviews
- Incident investigations
- Compliance and audit requests

---

## Why This Matters
SSO is not just a convenience feature — it is an **identity control point**.

When implemented correctly, it:
- Reduces credential sprawl
- Improves access governance
- Simplifies access reviews
- Strengthens security without blocking business

---

## Intended Audience
- IAM Analysts
- Security Operations
- Identity Governance teams
- Audit and Compliance partners


