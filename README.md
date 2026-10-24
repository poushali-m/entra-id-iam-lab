# Entra ID IAM Lab

A hands-on home lab simulating real-world Identity and Access Management (IAM) workflows using Microsoft Entra ID (formerly Azure AD). Built to demonstrate practical IT support and cyber security skills including user provisioning, access control, and secure offboarding.

---

## Overview

This lab walks through the full Joiners, Movers, and Leavers (JML) lifecycle for a fictional employee (Alex Johnson) inside a personal Microsoft Entra ID tenant. It also covers administrator-initiated password resets, a common first-line IT support task.

**Tools used:** Microsoft Entra ID (Free tier), Azure Portal

---

## Task 1 - Joiner: New User Provisioning

- Created user account: alex.joiner@poushalisofficialgmail.onmicrosoft.com
- Set display name, job title (Junior Analyst), department (IT), company (Contoso)
- Assigned Security Reader role
- Created security group IT-Analysts and added Alex as a member

![User Created](01-user-created.png) ![User Profile](02-user-profile.png) ![Assigned Roles](03-assigned-roles.png) ![Security Reader](04-security-reader.png) ![IT Analysts Group](05-it-analysts-group.png) ![Authentication Methods](06-authentication-methods.png)

---

## Task 2 - Mover: Role and Department Change

- Updated job title to Senior Analyst
- Updated department to Security Operations
- Created new security group SOC-Analysts
- Added Alex to SOC-Analysts
- Removed Alex from IT-Analysts (old access revoked)

![SOC Analysts Group](08-soc-analysts-group.png) ![Removed from IT Analysts](09-removed-from-it-analysts.png)

---

## Task 3 - Leaver: Secure Offboarding

- Disabled Alex's account in Entra ID
- Removed Alex from all security groups
- Account retained in directory for audit purposes

![Account Disabled](10-account-disabled.png) ![Removed from SOC](11-removed-from-soc.png)

---

## Task 4 - Conditional Access (MFA Enforcement)

Navigated to Security > Conditional Access. Policy creation requires Microsoft Entra ID Premium P1, not available on the free tier.

In a production environment the policy would be configured as:

- Users: All users
- Cloud apps: All cloud apps
- Grant: Require multi-factor authentication

---

## Task 5 - Password Reset (Admin-Initiated)

A common first-line IT support task is resetting a user's password when they are locked out or have forgotten their credentials.

**Steps taken:**

- Created a test user account (test.user@poushalisofficialgmail.onmicrosoft.com) to simulate a live user account
- Navigated to Microsoft Entra ID > Users and opened the user profile
- Clicked **Reset password** from the user profile toolbar
- Entra ID generated a temporary password and confirmed: *"Password has been reset"*
- The temporary password would be securely communicated to the user
- On next sign-in, the user is forced to set a new permanent password before accessing any resources

![Test User Profile](13-test-user-profile.png) ![Reset Password Panel](14-reset-password-panel.png) ![Password Reset Confirmation](15-password-reset-confirmed.png)

> **Note:** The temporary password shown in the confirmation screen has been redacted in accordance with security best practices.

---

## Skills Demonstrated

- Microsoft Entra ID user and group management
- JML lifecycle (Joiners, Movers, Leavers)
- Role-Based Access Control (RBAC)
- Secure offboarding procedures
- Conditional Access policy design
- Admin-initiated password resets and secure credential handover
- IT support workflows: account creation, access changes, deprovisioning, password management

---

## Relevance to IT Support Roles

This lab directly mirrors tasks performed by first-line IT support and service desk teams:

- Creating and configuring new user accounts (Joiner)
- Updating access when employees change roles (Mover)
- Disabling accounts and revoking access on departure (Leaver)
- Enforcing security policies through Conditional Access (MFA)
- Resetting passwords and securely communicating temporary credentials to users

---

*Built by Poushali Majumder | BSc Cyber Security, First Class Honours, UWL 2026*
