<img src="/Levels/twt-logo.png" height="100">

# Phishing attacks using QR codes and via Microsoft Teams chat

This week I'm flagging something to keep you (or your IT team/Managed Service Provider) up at night, which is recent developments in the techniques used by cyber-criminals to steal credentials (aka 'phishing attacks').  There's also a couple of vulnerabilities to note and a warning about payroll diversion (a fraud technique recently used to target a Trust in the federation).

## QR code phishing emails

If you have effective technical defences against phishing (i.e. those outlined in the Wildlife Trust Cyber Security [Framework](https://github.com/rswt-rbartlett/cyber-security-framework/blob/main/2-Implement-appropriate-mitigations/Step-05-Architecture-and-Configuration.md#implement-additional-phishing-protection)) you would have been able to block the majority of phishing emails.

Unfortunately cyber-criminal groups have worked out a new technique to bypass current detection methods by using QR codes. These are embedded in emails which imitate legitimate emails related to authentication, account control or Multi-Factor Authentication. If the QR code image is scanned by a smartphone it will direct the victim to what appears to be a login page which will then steal the victims credentials.

This is effective for two reasons;

1. Because the device which is scanning the image will typically be a smartphone with a smaller screen than a computer or laptop display it's harder for staff to spot the indicators that the page is fake (mainly the URL).
2. They are almost impossible to detect because the email contains no links, and often very little or no text, and the account they're sent from will only recently have been compromised.

### Advice for everyone

Look out for emails containing QR codes.  Unless you've been advised by your IT team or Managed Service Provider that such emails will be sent out, treat them with suspicion, and if in doubt check with IT.

### Advice for technical staff

Male sure your colleagues are aware of this risk, what to look out for, and make clear whether you will use QR codes as part of your account or access management.  If you have Microsoft Sentinel I can provide an Analytics Rule you can use to trigger an incident which has been effective her at RSWT, or I can provide advice on the logic behind that rule which could be used in other systems.

## Phishing via Microsoft Teams

In the last month there have been articles from [Truesec](https://www.truesec.com/hub/blog/darkgate-loader-delivered-via-teams) and then [Microsoft](https://www.microsoft.com/en-us/security/blog/2023/09/12/malware-distributor-storm-0324-facilitates-ransomware-access/) about cyber-criminal groups using Microsoft Teams chat to deliver malware and phishing.

This is a new delivery method and one which most organisations are unprepared for. I'd assumed that attacks were not widespread but the next day I was alerted to an attack on a Scottish public sector body using this exact methodology, which indicates the technique is already in widespread use.

### Advice for everyone

Be wary of any unsolicited or unusual Microsoft Teams chat messages, and certainly any chat messages from outside your Trust. By default any chat messages you receive from outside your Trust should appear with the warning below (the first time you chat to that person).

### Advice for technical staff

The protections against phishing in Teams are primitive, with the choices being allow-all, allow specific domains, block specific domains or no external collaboration (see the Microsoft article on [managing external access in Teams](https://learn.microsoft.com/en-us/microsoftteams/trusted-organizations-external-meetings-chat?tabs=organization-settings)). At RSWT we have developed an allow list of 150 domains including all Trusts in the federation plus the key partners, but each Trust will have their own partners and suppliers, so this list should only be used as a baseline to build on.  I can share the details of how this allow-list was developed which could help you or your managed service provider set this up.  We are not implementing this allow-list method yet as there's a strong risk it will be disruptive to collaboration, but we are keeping it ready in case we find ourselves being targeted by this technique.

## Vulnerabilities and Payroll Diversion Fraud

Two other things of note from the last couple of weeks are the WebP vulnerability which affects all web browsers.  This is actively being exploited 'in the wild', so IT Teams or Managed Service Providers should prioritise patching this vulnerability.  The relevant links from the browser vendors are;

- Google Chrome https://chromereleases.googleblog.com/2023/09/stable-channel-update-for-desktop_11.html
- Microsoft Edge https://msrc.microsoft.com/update-guide/vulnerability/CVE-2023-4863
- Mozilla Firefox https://www.mozilla.org/en-US/security/advisories/mfsa2023-40/

Finally, there was an incident at a Trust in the federation where an attempted payroll diversion fraud was fortunately spotted before any money was transferred. Two defences any Trust should be able to employ are;

1. Detection and quarantine of emails which pretend to be from a member of staff (e.g. [phishing protections](https://github.com/rswt-rbartlett/cyber-security-framework/blob/main/2-Implement-appropriate-mitigations/Step-05-Architecture-and-Configuration.md#implement-additional-phishing-protection) in Microsoft 365)
2. Verification (ideally face to face or verbal) with the employee that they submitted the request and the details are correct.