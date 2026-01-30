# SSO Authentication Flow – Reference Guide

## Purpose
This document describes the end-to-end Single Sign-On (SSO) authentication flow from a user, identity provider (IdP), and application perspective.

It serves as a **reference for IAM operations**, troubleshooting, and interview walkthroughs — not as a configuration guide.

---

## High-Level SSO Flow

1. User attempts to access an application
2. Application redirects user to the Identity Provider (IdP)
3. User authenticates with the IdP
4. IdP issues a security token
5. Application validates the token
6. User is granted or denied access based on claims and assignments

---

## Step-by-Step Flow

### 1. Application Access Attempt
- User navigates to the application URL
- Application detects no active session

### 2. Redirect to Identity Provider
- Application redirects the user to the IdP (e.g., Entra ID)
- Redirect includes:
  - Application ID
  - Requested scopes
  - Redirect URI

### 3. User Authentication
- User authenticates using configured methods:
  - Password
  - MFA
  - Conditional Access (if applicable)

### 4. Token Issuance
- IdP generates a token (SAML assertion or OIDC token)
- Token contains claims such as:
  - User identifier
  - Group or role claims
  - Authentication context

### 5. Token Validation
- Application validates:
  - Signature
  - Issuer
  - Audience
  - Expiration

### 6. Authorization Decision
- Application maps claims to:
  - Roles
  - Groups
  - Permissions
- Access is granted or denied

---

## Key IAM Control Points
- User assignment to the application
- Group or role-based access
- Conditional Access enforcement
- Token claims configuration

---

## What This Document Is (and Is Not)

**This IS:**
- A conceptual flow reference
- An IAM troubleshooting aid
- Interview-ready explanation material

**This is NOT:**
- A setup tutorial
- A vendor-specific configuration guide
- A replacement for official documentation
