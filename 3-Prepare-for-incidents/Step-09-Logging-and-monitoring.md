<img src="/Levels/twt-logo.png" height="100">

# Prepare for incidents
# Step 9. Logging and monitoring
Logging and monitoring logs makes it far more like you (or your IT provider) will detect an attack in process and be able to stop it.  Even if the attack is successful logs are vital during and after a security incident to understand how the attacker gained access, so that vulnerability can be address and further compromise prevented.  The short version of this is logging is not expensive, but monitoring logs is (as it involves someone or something looking at them and making decisions).  That may mean for some Trusts log monitoring would involve disproportionate expense, but all Trusts should be logging the right events.

## Log what matters 
At a minimum the following events should be logged on all systems you are responsible for, or which your IT provider manages on your behalf.
- Successful and Failed authentication (login) attempts on the following systems:
	- Your directory (Active Directory, Azure Active Directory, Google Workspace)
	- Your end user devices (Windows computers and laptops, Apple Mac and Macbooks)
	- Your servers and other infrastructure (firewall, router, network equipment)
	- Any other applications which do not use Single Sign-on with your directory (e.g. systems or applications with their own accounts)
- User administration actions (creating, modifying and deleting users, resetting passwords, changing permissions)
- Domain Name Service (DNS) resolution
- Outbound connections from your laptops, computers and servers (logged at your network firewall or on your devices)
- Emails sent and received
- Changes to endpoint protection (e.g. disabling endpoint protection or whitelisting applications or directories)

### Quick ways to log what matters
As this is a technically complex area which changes frequently below are some options for speeding up the process of configuring your systems to log what matters.
1. Microsoft Sysmon and either Olaf Hartong's [default configuration](https://raw.githubusercontent.com/olafhartong/sysmon-modular/master/sysmonconfig.xml), his [MDE augment configuration](https://raw.githubusercontent.com/olafhartong/sysmon-modular/master/sysmonconfig-mde-augment.xml)  or SwiftOnSecurity's [Sysmon config](https://github.com/SwiftOnSecurity/sysmon-config/blob/master/sysmonconfig-export.xml).
2. Apply the Baseline Recommendation or Stronger Recommendation from Microsoft's [Audit Policy Recommendation](https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/audit-policy-recommendations)
3. Apply the relevant [Microsoft Security Baseline](https://learn.microsoft.com/en-us/windows/security/threat-protection/windows-security-configuration-framework/windows-security-baselines).
> **Note**: it is recommended you test the security baseline before you apply it to live/production systems.

## Collect and protect logs
Having captured important security events in logs on your computers, servers and applications you need to protect them.  If an attacker gained access to your systems destroying evidence of their activity will be high on their priority list.  The logs are vulnerable in their original location, so whenever possible you should forward, send or in some other way copy the logs to another system which is well protected.  Once the logs are all held in one place you can also query them all at once, which makes Incident Response much quicker and easier.

There are many products on the market which claim to fulfil this requirement, but unfortunately many of those require that the devices you are collecting logs from are on your internal (office) network, or have a Virtual Private Network (VPN) connection open.  In a hybrid working this is frequently not the case and therefore many of these systems are no longer fit for purpose.  Below are two options for log aggregation, one free and one paid.

### Cybersecurity and Infrastructure Security Agency (CISA) Logging Made Easy (the free option)
The CISA has published a guide and configuration files to build a log aggregation tool based on free and open source software (originally released to the NCSC and then adopted by CISA).  It is non-trivial to configure and would require a skilled IT person to setup, and would also require sufficient computing resource to store and process the logs.  It is however free of any up front capital or ongoing subscription cost, and is highly effective.  You can find the the solution at [Github](https://github.com/cisagov/LME/blob/main/README.md).

### Azure Sentinel (the paid option)
This option is available to any Trust who has a Microsoft 365 or Azure subscription.  Details are at https://azure.microsoft.com/en-gb/products/microsoft-sentinel/, and you should approach your Cloud Solution Provider for pricing.
> **Note**: Data ingested into the Azure Monitor Log Analytics workspace can be retained free for 90 days, and ingestion of the following data sources is always free:
> - Azure Activity Logs
> - Office 365 Audit Logs (all SharePoint activity and Exchange admin activity)
> - Alerts from Microsoft Defender for Cloud, Microsoft 365 Defender, Microsoft Defender for Office 365, Microsoft Defender for Identity, Microsoft Defender for Endpoint and Microsoft Defender for Cloud Apps

RSWT are shortly embarking on an Azure Sentinel implementation and I will publish more cost information here once the system is running.

## Return to [Step 8. Data security](/2-Implement-appropriate-mitigations/Step-08-Data-Security.md) or continue to [Step 10. Incident management](./Step-10-Incident-management.md)