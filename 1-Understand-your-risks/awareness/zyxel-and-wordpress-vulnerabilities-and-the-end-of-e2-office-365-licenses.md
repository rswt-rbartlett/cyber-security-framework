<img src="/Levels/twt-logo.png" height="100">
It's been as busy as ever out there in the world of Cyber Security, here's my take on what you need to know to keep your Trusts systems and data safe.

# Zyxel vulnerability and the Mirai botnet
On 25th April Zyxel [announced](https://www.zyxel.com/global/en/support/security-advisories/zyxel-security-advisory-for-multiple-buffer-overflow-vulnerabilities-of-firewalls) a patch for a security vulnerabilities which would allow an attacker to take control of ATP, USG FLEX, VPN and Zywall/USG firewalls over the internet. This is a real threat, as the Mirai botnet is already using this vulnerability to take over Zyxel devices and add them to it's bot army.
**Recommendation**: If you have Zyxel devices in any of your offices make sure they're up to date. If your staff use an affected Zyxel device at home, urge them to update as soon as possible.  Patches can be found at the Zyxel [download library](https://www.zyxel.com/global/en/support/download?model=).

# WordPress Elementor vulnerabilities
On May 11th WPDeveloper released a patch for their [Essential Addons for Elementor](https://wordpress.org/plugins/essential-addons-for-elementor-lite/) plugin after Patchstack found a [vulnerability](https://patchstack.com/articles/critical-privilege-escalation-in-essential-addons-for-elementor-plugin-affecting-1-million-sites/) in the plugin which allowed an attacker to take control of the website. This is already being [actively exploited](https://www.bleepingcomputer.com/news/security/hackers-target-vulnerable-wordpress-elementor-plugin-after-poc-released/) by attackers to take over websites.
**Recommendation**: If you use WordPress for your main website or other project or other websites, please check whether you use Elementor (a page builder for WordPress), if you do check whether you're using this plugin, and update it asap.

# Microsoft ends Nonprofit O365 E2 Grant
From October 1st 2023 you will [no longer](https://partner.microsoft.com/en-gb/asset/collection/nonprofit-customer-change-to-o365-e2-grant#/) be able to renew the Office 365 E2 grant.  If you have any users licensed under E2 I would recommend transitioning to [Microsoft 365 Business Basic non-profit staff pricing](https://www.microsoft.com/en-gb/microsoft-365/nonprofit/plans-and-pricing?activetab=tab:primaryr1) (which is free for up to 300 seats), or you could transition to E3 licenses.

