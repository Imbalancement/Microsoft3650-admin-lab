# Microsoft 365 Admin Lab: Users, Password Resets, and MFA

## Overview

This lab documents hands-on Microsoft 365 and Microsoft Entra ID administration practice focused on common help desk workflows. The goal was to practice the type of tasks an entry-level help desk technician, IT support specialist, or MSP technician may perform when supporting Microsoft 365 users.

The lab focused on three core areas:

- User account management
- Password reset workflow
- MFA and authentication methods review

## Tools Used

- Microsoft 365 Admin Center
- Microsoft Entra Admin Center
- Microsoft 365 Business Standard lab tenant
- Test user account
- Browser private/incognito sign-in testing

## Lab Scenario

A test user account was created in Microsoft 365 to simulate a basic help desk support request. The workflow covered creating or reviewing the user account, checking MFA/authentication settings, resetting the password, and confirming the user-side password change prompt during first sign-in.

Example mock ticket:

> A user cannot sign in to Microsoft 365. The help desk needs to review the account, reset the password, require the user to change the password at first sign-in, and verify authentication options in Microsoft Entra ID.

---

## 1. Active Users Review

The first step was to open the Microsoft 365 Admin Center and navigate to **Users > Active users**. From this page, I reviewed the current user list and confirmed that the test user existed in the tenant.

This is a common starting point for help desk troubleshooting because it allows an admin to review user status, licensing, sign-in access, and available account actions.

![Microsoft 365 Active Users](images/01-active-users.png)

### Skills Practiced

- Navigating to **Users > Active users**
- Reviewing user accounts
- Identifying licensed and unlicensed users
- Locating admin actions such as reset password, MFA, delete user, and export users

### Help Desk Relevance

In a real support environment, this is where an IT technician may begin when handling account-related tickets such as:

- New user onboarding
- User cannot sign in
- License/access issue
- Account status review
- Password reset request

---

## 2. Microsoft Entra ID Authentication Methods Review

Next, I opened the test user in the Microsoft Entra Admin Center and reviewed the **Authentication methods** page. This area is used to review or manage how a user signs in, including MFA-related options.

![Microsoft Entra Authentication Methods](images/02-entra-authentication-methods.png)

### Skills Practiced

- Navigating to a user in Microsoft Entra ID
- Opening **Authentication methods**
- Reviewing usable and non-usable authentication methods
- Locating MFA support actions
- Identifying options such as:
  - Add authentication method
  - Reset password
  - Require re-register multifactor authentication
  - Revoke sessions

### Help Desk Relevance

This is useful for tickets such as:

- User got a new phone and cannot access Microsoft Authenticator
- User is stuck in an MFA loop
- User needs to re-register MFA
- User reports suspicious sign-in activity
- Admin needs to revoke sessions after a potential compromise

### Key Takeaway

Microsoft Entra ID is where identity and authentication troubleshooting often happens. For MFA issues, the admin should know where to review authentication methods, require re-registration, and revoke sessions.

---

## 3. Password Reset from Microsoft 365 Admin Center

The next step was to reset the test user's password from the Microsoft 365 Admin Center. The password reset blade allowed the admin to automatically generate a password and require the user to change it at first sign-in.

![Microsoft 365 Password Reset](images/03-password-reset-admin.png)

### Skills Practiced

- Selecting a user account
- Opening the **Reset password** action
- Automatically generating a temporary password
- Requiring password change at first sign-in
- Understanding that admins cannot view a user's current password

### Help Desk Relevance

Password resets are one of the most common help desk tasks. This workflow is used when a user forgets their password, cannot access Outlook/Teams, or needs a temporary password issued by IT.

### Important Security Note

Admins cannot view an existing Microsoft 365 password. They can only reset it, issue a temporary password, and require the user to create a new password during sign-in.

---

## 4. User-Side Account Homepage Verification

After the admin-side password reset workflow, I signed in as the test user to confirm the account could reach the Microsoft account homepage.

![Test User Account Homepage](images/04-user-account-homepage.png)

### Skills Practiced

- Testing sign-in as the affected user
- Verifying user-side account access
- Reviewing user self-service areas such as:
  - Security info
  - Devices
  - Change password
  - Sign-in/security options

### Help Desk Relevance

A good support workflow does not stop at clicking reset. The technician should verify the user experience when possible, especially in a lab. This helps connect the admin-side action to the user-side result.

---

## 5. Password Change Prompt Verification

After the password reset, the test user was prompted to update the password during sign-in. This confirmed that the **require password change at first sign-in** option worked as expected.

![Microsoft Password Change Prompt](images/05-password-change-prompt.png)

### Skills Practiced

- Confirming temporary password behavior
- Verifying first sign-in password change prompt
- Understanding the user experience after an admin password reset

### Help Desk Relevance

This validates the full password reset ticket lifecycle:

1. User reports sign-in issue
2. Admin resets password
3. Admin requires password change at first sign-in
4. User signs in with temporary password
5. User creates a new password

---

## Summary of What Was Practiced

This lab provided hands-on practice with the following Microsoft 365 and Entra ID administration tasks:

- Reviewed users in Microsoft 365 Admin Center
- Created/reviewed a test user account
- Reviewed licensing status
- Opened password reset workflow
- Generated a temporary password
- Required password change at first sign-in
- Reviewed Microsoft Entra authentication methods
- Located MFA re-registration and session revocation controls
- Verified the user-side sign-in/password update experience

## Interview Talking Point

> I built a Microsoft 365 lab tenant and practiced common help desk admin workflows, including user account review, password resets, requiring password changes at first sign-in, and reviewing MFA/authentication methods in Microsoft Entra ID.

## Resume Bullet

- Practiced Microsoft 365 and Microsoft Entra ID administration tasks including user account review, password resets, MFA authentication method review, session revocation options, and first sign-in password change verification.

## Lessons Learned

- Microsoft 365 Admin Center is used for common user management tasks such as account review, licensing, and password resets.
- Microsoft Entra Admin Center is used for identity-focused tasks such as authentication methods, MFA re-registration, and session revocation.
- Admins cannot view existing user passwords; they can only reset passwords and issue temporary credentials.
- Verifying the user-side experience is important because it confirms the admin action worked as intended.

## Next Steps

Future Microsoft 365 admin labs could include:

- Creating Microsoft 365 groups
- Assigning and removing product licenses
- Blocking and unblocking user sign-in
- Creating a shared mailbox
- Testing OneDrive and SharePoint permissions
- Creating Teams and managing membership
- Reviewing sign-in logs in Microsoft Entra ID
