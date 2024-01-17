<img src="/Levels/twt-logo.png" height="100">

# Implement appropriate mitigations
# Step 7. Identity and access management

## Decide who needs access to what, and how
> Cyber Essentials **User Access Control** requirements (question A7.4)

You will already have accounts which allow access to computers, email, files and applications.  You should develop a process which determimes:
1. Who gets an account, 
2. How you decide what they need access to, 
3. How to maintain that access, including how to revoke it when no longer needed.

### Role Based Access Control
- Access is most effectively maintained when it is based on role (known as 'Role Based Access Control', or RBAC).
- Define the different roles in your organisation in your directory:
	- [Active Directory Groups](https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/manage/understand-security-groups)
	- [Azure Active Directory groups](https://learn.microsoft.com/en-us/azure/active-directory/fundamentals/how-to-manage-groups)
	- [Microsoft 365 Groups, SharePoint and Teams](https://learn.microsoft.com/en-us/microsoft-365/solutions/groups-teams-access-governance?view=o365-worldwide)
	- [Google Workspace Organisational Units](https://support.google.com/a/topic/1227584)
	- [Google Configuration Group](https://support.google.com/a/answer/9224126)
- Access to files, a mailbox or an application are then enabled by membership of the group.
- Even if you only have one person in a group it is easier to assign permissions to the group than it is to assign it to a member of staff and have to assign them all again when they leave and are replaced. That way you assign the permissions once, and just remove the existing staff member and add their successor.

## Maintain your identities
> Cyber Essentials **User Access Control** requirements (questions A7.1-7.3)
- Have a starter/mover/leaver process.  This should be integrated with your existing HR processes.
	- Create a new named account for each member of staff, volunteer, Trustee or contractor and ensure they set a unique password.
	- Put the account in the group/s to provide access to the computers, files, email and applications to do fulfil their role.
	- If someone changes roles remove them from all groups and re-add them to the groups which reflect their new role.
	- When someone leaves remove them from all groups (which should revoke access to most services and data)
	- Disable the account or reset the password to revoke access.
- Review accounts annually
	- It is common for staff and other stakeholders to accumulate access they no longer need, which will increase the impact of any security incident involving their account.
	- Review access annually (a simple process of checking the membership of each group to ensure those members still need that access) and revoke any access no longer required.
	- **Note**: This is particularly important for those with a privileged access (e.g. those able to administer your IT systems or those with access to financial systems who can authorise payments or transfer funds).

## User friendly password policy
> Cyber Essentials **User Access Control** requirements (questions A7.10-7.12)

Credentials in the form of a username and password are still the most common method of granting staff access to files, data and systems.  Attacks on organisations often start with credentials either being stolen or guessed, because [contemporary password policies](https://www.ncsc.gov.uk/collection/passwords/updating-your-approach#tip5-password-collection) unintentionally led staff to create bad guessable passwords.  Update and improve your password policy (or create a new password policy) by following the guidelines below.
- Don't set password complexity requirement.  These lead to predictable letter/number substitution which attackers will use when trying to guess passwords.  It also makes it harder for staff to remember their password.
- Don't automatically expire passwords. This also leads to predictable password variants (e.g. adding a number of season/year at the end of the password) which attackers will also use when attacking accounts.
Password security is best achieved by a combination of:
- Setting a minimum password length (14 characters)
- Providing guidelines to help staff create memorable passwords of a suitable length
- Implement controls to defend against password guessing attacks, e.g.:
	- [Azure Active Directory Password Protection](https://learn.microsoft.com/en-gb/azure/active-directory/authentication/concept-password-ban-bad)
	- [Active Directory Account Lockout](https://learn.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2003/cc737614(v=ws.10)#configuring-account-lockout-for-local-users)

## Implement Multi-Factor Authentication (MFA) for all remote access
> Cyber Essentials **User Access Control** requirements (questions A7.10, 7.14, 7.17)
> Cyber Essentials **Secure Configuration** requirements (question A5.5)

Due to the ease with which account passwords can be guessed, stolen, intercepted or revealed in data breaches they are no longer an effective or appropriate control on their own, especially for sensitive data including personally identifiable information.  Therefore username and password should be supplemented by an additional factor in order to secure your identities, systems and data.
> [!IMPORTANT]
> If a system can be accessed from the internet (including cloud services like Outlook 365 or Gmail and services published from your network like VPN or Remote Desktop Gateway) you should require Multi-Factor Authentication (also known as '2-Step Verification') to access it.  This should be considered a **baseline minimum security requirement for all Trusts**.

Multi-factor authentication is not difficult or expensive to setup on modern systems including cloud based services, networking equipment or applications.  Below are instructions on how to setup MFA on commonly used cloud services and VPN systems.
- Cloud based services
	- [Microsoft Azure/365](https://learn.microsoft.com/en-us/azure/active-directory/authentication/concept-mfa-howitworks?culture=en-us&country=us)
	- [Google Workspace](https://support.google.com/a/answer/175197?hl=en)
- VPN systems
	- [Sophos Firewall](https://docs.sophos.com/nsg/sophos-firewall/18.5/Help/en-us/webhelp/onlinehelp/AdministratorHelp/Authentication/OneTimePassword/index.html#multi-factor-authentication-mfa-settings)
	- [Sonicwall Firewall](https://www.sonicwall.com/support/knowledge-base/how-do-i-configure-2fa-for-ssl-vpn-with-totp/190829123329169/)
	- [Draytek Vigor routers](https://www.draytek.com/support/knowledge-base/10730) **Note**: this is only supported on the Vigor3910 or Vigor2962 firmware version 4.3.2 or later.

When you require MFA is a balance of usability vs security.  If you require MFA at every sign-in this is extremely disruptive to the user (and is only recommended for highly privileged accounts).  If you only require MFA every 30 days then this may not reduce the risk of account compromise.  To reduce risk, require MFA if the login is:
- from an untrusted device or nrowser
- from an unusual location (e.g. a country your staff do not normally login from)
- more than *n* days since the last MFA/2SV prompt, where n is a balance between usability and security (I would say 7-14 days)
- risky based on threat intelligence indicators (for example from an IP Address from which logon attempts to multiple accounts has been detected)
- for a privileged account (e.g. a Global Administrator account)

## Separate admin accounts and protect them
> Cyber Essentials **User Access Control** requirements (questions A7.5, 7.6, 7.7, 7.9, 7.16)

The primary target for an attacker once they have gained access to a network is privileged accounts, accounts with the highest levels of access they can use to steal or encrypt data.  Those accounts should be afforded a greater level of protection than regular staff accounts and should be used with a great deal of caution.  Follow the guidelines below to reduce the risk of privileged accounts being compromised.
- Only use top level accounts when absolutely necessary. As far as possible delegate privileges needed more frequently to lower level (but still privileged) accounts, for example the named accounts described below.
- Have separate named accounts for admin and day to day use.  **Never** delegate administrative privileges to the accounts your IT team use every day (for email and web browsing for example).  Create each member of staff who needs privileged access a separate named account specifically for them, and have them only use it when that level of access is required.
- Enable MFA for all privileged accounts.  Every logon by a privileged account should be protected by MFA whenever possible.
- Review access regularly.  Staff may be allocated administrative rights temporarily, or may change roles, or systems may be decomissioned, so review which accounts have administrative access and revoke that access when no longer required.

## Return to [Step 6. Vulnerability management](./Step-06-Vulnerability-Management.md) or continue to [Step 8. Data security](./Step-08-Data-Security.md)