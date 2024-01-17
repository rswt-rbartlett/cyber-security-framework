<img src="/Levels/twt-logo.png" height="100">

# Implement appropriate mitigations
# Step 5. Architecture and configuration

The security of systems is largely a product of how they are configured (not some inherent property) so this is a vital consideration for Trusts of all size.  Below are the most important steps to consider, including known working solutions and recommended configurations.  It is important to note that these recommendations will change over time as both the technology and attackers tactics change, so it is important to review and update your configuration regularly.  To support Trusts, when there are important changes to this section all framework subscribers will be automatically notified so they can take appropriate steps.

## Reduce attack surface
Your 'attack surface' is what an attacker can see, either from the public internet, or from a compromised device inside your network.  Like most security decisions, reducing your attack surface is a balance between security and usability.  Beware implementing technical controls which make it too difficult for staff to do their job, as they will implement their own workarounds which will increase security risk.
### Implement boundary firewalls and internet gateways
> Compliance with the Cyber Essentials **Firewalls** requirements (questions A4.1, A4.1.1 & A4.5)
- All routers and firewalls should prevent any direct access to staff computers inside your network.
- For smaller offices the router provided by your ISP may be sufficient.
- Larger offices with more staff or services which need to be remotely accessible may need a firewall with more functionality and capacity.
- Check that your router/firewall allows you to control network traffic coming in and going out of your network, and allows you to protect any remote access with Multi-Factor Authentication.
- Ensure your firewall and routers are configured only to expose to the internet those services which are needed.

### Harden your servers and end user devices
- 'Hardening' is the term used to describe making a server or computer more secure by removing or disabling unwanted components.  **Caution: this should only be done by technically qualified staff**.
- An easy 'shortcut' to hardening Microsoft Windows and Windows Server systems is to apply Microsoft Windows Security Baselines, which can be done using:
	- The [Microsoft Security Compliance Toolkit](https://learn.microsoft.com/en-us/windows/security/threat-protection/windows-security-configuration-framework/security-compliance-toolkit-10) which can be downloaded from the [Microsoft Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=55319).
	- Microsoft Endpoint Manager Intune [MDM Security Baselines](https://learn.microsoft.com/en-us/mem/intune/protect/security-baseline-settings-mdm-all?pivots=mdm-november-2021)
	- These baseline configurations can be applied by your internal IT team, or you can ask your external IT provider to apply them on your behalf.
- An additional Microsoft solution to 'harden' a system is to employ [Attack Surface Reduction](https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/overview-attack-surface-reduction?view=o365-worldwide) in Windows Defender (which comes free with Windows 10 and 11).  If you deploy Defender for Endpoint you can employ more protective features.
- If you decide not to apply the Windows Security Baselines at a minimum you should configure Windows systems as follows:
  - Do not allow staff administrative access, or if they **must** have administrative access give them a separate account for that purpose and have them use a normal account for day to day activities.
  - Set a unique strong password on any accounts with administrative privileges (do not set the same Administrator passwords for all your PCs and laptops)
  - Disable remote access and only turn it on when needed, and disable it afterwards.
  - [Log,](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_logging_windows?view=powershell-7.2#enabling-script-block-logging) and if not already set (this is the default for Windows clients) [restrict](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_execution_policies?view=powershell-7.2#restricted) access to PowerShell (PowerShell is commonly used by ransomware groups).
  - Restrict access to other executables commonly used by attackers (e.g. the [Microsoft recommended block rules](https://learn.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-control/microsoft-recommended-block-rules)).
- For any publically accessible system where you are responsible for the platform/operating system (e.g. a router or firewall at your office or a web server you maintain) technically qualified staff should take the following approach:
  - Ensure only the services you need are accessible by stopping or disabling the services you don't need (e.g. mail or file transfer services) or blocking them using a firewall
  - Disable or change the password for any default accounts, especially for which passwords are publically documented (e.g. in vendor manuals on the internet).
  - Restrict access to any management interface (e.g. the management port for you office router) either by using access lists to restrict access to specific IP addresses, or disabling public access completely which would require the administrator to be in the office or connected via a Virtual Private Network (VPN) before they can manage the system.

## Make it harder to spoof your email domain

Attackers will try and trick user by changing the FROM: address in an email to match your email domain.  This is called 'spoofing'.  To make this harder deploy the following technologies on your mail service:
- DMARC (this tells a receiving mail server if your domain is protected by Sender Policy Framework (SPF) and/or DomainKeys Identified Mail (DKIM), and what to do if the message doesn't pass those checks). 
- SPF (checks that a mail claiming to come from a specific domain comes from an approved IP address for that domain)
- DKIM (checks that a mail claiming to come from a specific domain has a valid digital signature for that domain) 

The National Cyber Security Centre has put together a [guide for IT managers and systems administrators](https://www.ncsc.gov.uk/collection/email-security-and-anti-spoofing) which takes you through the steps to set this up.

Below are links to the vendor guides for setting up DMARC, SPF and DKIM
- [Microsoft Exchange Online](https://learn.microsoft.com/en-us/microsoft-365/security/office-365-security/use-dmarc-to-validate-email?view=o365-worldwide)
- [Google Workspace](https://support.google.com/a/answer/2466580?hl=en)
> **Note** There is no out of the box support for DMARC in Microsoft Exchange Server, and I strongly recommend moving to Microsoft 365 Exchange Online.

## Implement additional phishing protection

In addition to DMARC you should also implement specific anti-phishing controls in Exchange Online, I would recommend either:
- Implementing the 'Standard Protection' at https://security.microsoft.com/presetSecurityPolicies
	OR
- Implementing the following anti-phishing controls at https://security.microsoft.com/antiphishing
	- **Phishing threshold & protection**
	- Set Phishing email threshold to 3 (turn down to 2 if you get too many false positives)
	- Enable impersonation protection for all staff listed in your website (particularly Executives)
	- Enable impersonation protection for all domains
	- Enable mailbox intelligence
	- Enable Intelligence for impersonation protection
	- Enable spoof intelligence
	- **Actions**
	- If a message is detected as user impersonation Quarantine the message
	- If a message is detected as domain impersonation Quarantine the message
	- If Mailbox Intelligence detects an impersonated user Quarantine the message
	- If message is detected as spoof Quarantine the message
	- Turn on all the Safety tips & indicators

You should either monitor Quarantine and release 'false positive' (genuine messages blocked in error) yourself, or allow staff to release their own messages. What staff are allowed to release themselves is defined in the [Quarantine Policies](https://learn.microsoft.com/en-us/microsoft-365/security/office-365-security/quarantine-policies?view=o365-worldwide).

## Install effective endpoint protection 
> [!NOTE]
> The endpoint protection guidelines below enable compliance with the Cyber Essentials **Malware Protection** requirements

Endpoint Protection and Response (EDR) is critical to protecting from ransomware attacks. As attacker tactics have developed some anti-virus solutions have become less effective, proving relatively easy to bypass, and failing to detect when an attack is in progress.  For this reason, I recommend one of the following security solutions in order of preference.  These recommendations are based on a combination of feedback from Cyber Security Incident Response professionals and contacts in the Insurance sector.  They are not based on Gartner Magic Quadrant reports (though there is some correlation).

1. [Microsoft Defender for Endpoint](https://www.microsoft.com/en-gb/security/business/endpoint-security/microsoft-defender-endpoint) ([Plan 2](https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/defender-endpoint-plan-1-2?view=o365-worldwide) or as part of [Microsoft 365 Business Premium](https://www.microsoft.com/en-gb/microsoft-365/nonprofit/plans-and-pricing)).
2. [CrowdStrike Falcon Insight](https://www.crowdstrike.co.uk/products/endpoint-security/falcon-insight-edr/) 
3. [Sentinel One Singularity](https://www.sentinelone.com/surfaces/endpoint/)
4. [VMware Carbon Black](https://www.vmware.com/uk/products/carbon-black-cloud-endpoint.html)
5. [Sophos Intercept X with XDR](https://www.sophos.com/en-us/products/endpoint-antivirus)

This is not a statement that other endpoint protection products are not effective, but only that insurers believe they reduce the likelihood of a claim and Incident Response Analysts believe they are effective based on the incidents they have worked on.
> Whatever tool you use it is vital that **someone is monitoring events and alerts**, and that the product is configured as per the manufacturers recommendations. 

## Whitelist applications
A very strong defense against ransomware and any malicious software is to whitelist applications, which means only programs which you have already approved can run on the system.  This requires more up front investment in time to configure, and it can create an overhead to continually update and maintain the approved software list, but it can be extremely effective when other defenses have been breached.  This step is not recommended for Trusts unless they have the resource available to deploy it.

Whitelisting applications on Windows can be done for free using [Windows Defender Application Control](https://learn.microsoft.com/en-gb/windows/security/threat-protection/windows-defender-application-control/windows-defender-application-control), a native part of Windows 10 build 1909+, Windows 11 and Windows Server 2016 onwards.

## Return to [Step 4. Supply chain security](/1-Understand-your-risks/Step-04-Supply-Chain-Security.md) or continue to [Step 6. Vulnerability management](./Step-06-Vulnerability-Management.md)