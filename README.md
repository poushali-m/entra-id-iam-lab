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
-

---
*Built by Poushali Majumder | BSc Cyber Security, First Class Honours, UWL 2026*
