<img src="/Levels/twt-logo.png" height="100">

# Microsoft onenote .one files to spread malware
Since January there has been a significant increase in cyber-crime gangs using .one files (Microsoft OneNote files) to distribute malware.  See [Hackers now use Microsoft OneNote attachments to spread malware](https://www.bleepingcomputer.com/news/security/hackers-now-use-microsoft-onenote-attachments-to-spread-malware/) and [OneNote Documents Increasingly Used to Deliver Malware ](https://www.proofpoint.com/us/blog/threat-insight/onenote-documents-increasingly-used-to-deliver-malware) for more details.

**Recommendation**: block .one file extensions in your email protection (either using [Exchange Transport Rules](https://admin.exchange.microsoft.com/#/transportrules), Microsoft 365 Defender [Anti-malware policies](https://security.microsoft.com/antimalwarev2) or whatever email filtering product you or your IT service provider uses).  Discourage users from sharing .one files, and promote the use of links rather than attachments for sharing information.

# Microsoft launching mfa number matching for all tenants
Starting February 27th, 2023 Microsoft will remove the admin controls and enforce the number match experience tenant-wide for all users of Microsoft Authenticator push notifications.  See [Use number matching in multifactor authentication (MFA) notifications](https://learn.microsoft.com/en-us/azure/active-directory/authentication/how-to-mfa-number-match) for more details.  The reason for this change is cyber-criminals are bypassing existing MFA controls by continually 'spamming' the victim by attempting to login repeatedly with valid credentials until the user hits 'Approve', or by relying on users approving sign-ins because they assume they are legitimate.  MFA number matching makes both attacks impossible because the user has to enter the number they see on the screen from their login attempt into the Authenticator dialog.

**Recommendation**: turn on MFA number matching now for a group of test users, and then roll out to all staff before 27th February to ensure any issues are resolved before it's enforced by Microsoft.

**Update**: 20th February, 2023 Microsoft deferred the roll-out of MFA number matching until 8th May 2023, but the recommendation to implement now still stands.