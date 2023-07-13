<img src="/Levels/twt-logo.png" height="100">
There's never a quiet month in cyber security, but over the past month at least it's felt like it was happening to other people (the Trusts seemed to be unaffected by the MOVEit breach, and with one of the largest botnets largely dormant phishing attacks are down).  However there are a couple of things Wildlife Trusts should be aware of, set out below. As always, if you have any questions comment on the post or send me an email.

# Urgent Security Notice for SonicWall GMS/Analytics
Yesterday (12th July) SonicWall issued an [Urgent Security Notice](https://www.sonicwall.com/support/product-notification/urgent-security-notice-sonicwall-gms-analytics-impacted-by-suite-of-vulnerabilities/230710150218060/) for SonicWall GMS/Analytics, their Global Management System for managing multiple SonicWall or Dell X-Series devices (only likely in the larger Trusts with multiple SonicWall devices).

This is a suite of vulnerabilities including four which are Critical, the highest risk rating. There's currently no evidence of exploitation of this in the wild, but I expect that to change. The gap between patches being released and reverse engineered by criminals to make an exploit is measured in days rather than weeks (in 2020 Mandiant reported that 12% of exploits were developed within a week of the patch and 27% developed within a month).

**Recommendation**: If you have use SonicWall GSM/Analytics apply the vendor updates as soon as possible, even if the system is not accessible from the public internet.

# Threat briefing service
I've just launched a Technical Information Security Alert service for technical staff to help them prioritise mitigations.  There are so many vulnerabilities published every month ([this graph](https://www.first.org/epss/figures/cve_pub_year_to_date-1.png) is quite depressing) that keeping up with them is difficult, and and patching is time consuming and potentially risky.  It saves a lot of time and effort if you can prioritise what's most important, and let the rest be picked up by automatic updates.  I already pull together multiple open source and private information feeds and can provide an informed recommendation for Trusts based on known threats, vulnerabilities, trends and analysis.

I'm also planning to do higher level quarterly briefings for Managers and annual briefings for Executives and Trustees, so they're informed about current and potential future information security risks.  Whilst many vendors produce similar reports these briefings will be untainted by commercial interests, and won't try to sell you anything!

# Risk Trends
Cyber security commentators are calling out a trend over the last year or so for specific types of product to be targeted by cyber-crime groups with widespread impact.  Below are prominent examples just from 2023 (though the trend has been apparent since before the pandemic). Ironically these are all security products (either firewalls/routers designed to separate your internal network with the wider internet or secure file transfer software).

## Routers
CVE-2023-28771 (Zyxel firewalls) OS command injection used by the Mirai botnet
CVE-2023-1389 (TP-Link routers) OS command injection used by the Mirai botnet
## File transfer software
CVE-2023-0669 (Fortra Goanywhere Managed File Transfer) used by the Cl0p ransomware group
CVE-2023-34362 (Progress MOVEit Transfer) an SQL Injection vulnerability used by the Cl0p ransomware group
## Firewall/Remote Access
CVE-2023-2868 (Barracuda Email Security Gateways) used by Chinese espionage groups
CVE-2022-41328 (Fortinet FortiOS firewalls) used by Chinese espionage groups

These are all vulnerabilities which allow an attacker to take total control of the system, over the internet, without a password.  These are sometimes referred to as a 'one click exploit' or 'one click hack', and are typically a result of making programming mistakes which most undergraduates are taught about year 2 of their degree.

# End of support for Windows Server 2012 and Windows Server 2012 R2 Oct 10, 2023

# Barts Health NHS Trust breach
highlights importance of protecting access to staff PII

