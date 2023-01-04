<img src="/Levels/twt-logo.png" height="100">

# Introduction

This document accompanies the “Cyber threats and recommended mitigations” paper previously posted, and provides some technical background on;

- :wrench: How to hit the minimum baseline technical controls, and
- :heavy_check_mark: How to validate that the implemented controls were effective.

It doesn’t identify all technical resources associated with the recommendation, to prevent this becoming a huge exercise I’ve had to assume a level of knowledge and experience of managing Microsoft on-premises systems and cloud services. I have added links to more specialised cyber security information. If you need more support to complete these mitigation steps let me know and I’ll do my best to help. All of the resources referenced below are free, however depending on the products you use some steps (e.g. MFA for VPN) may require a license upgrade or add-on.

# 1. Prioritise patching of known exploited vulnerabilities

1.1 Set all EUD to automatically download and install updates via Group Policy Objects (for domain joined computers), Local Policy (using LGPO) or Endpoint Manager/Intune (for Azure joined devices).
1.2 Manage Windows servers updates using WSUS (for on-premises infrastructure) and/or Azure Update Management (for on-premises and cloud hosts).
1.3 Sign up to NCSC ACD Early Warning (https://www.ncsc.gov.uk/section/active-cyber-defence/introduction) to monitor your perimeter, they will warn you of exposed ports and particularly vulnerable exposed services.
1.4 Get a vulnerability scan of your perimeter and internal network from RSWT Strategic Lead for Cyber and Data Security or implement your own (e.g. free Nessus Pro)

# 2. Enforce multi-factor authentication (MFA)
2.1. Enable MFA for all Azure/M365 accounts (this is free on Microsoft 365 Business Basic, Office 365 E1 and Microsoft 365 E3 and above, and on Google Workspace for non-profits).
2.2. Enable MFA for all Remote Access (particularly any Remote Desktop Gateway or VPN services, but more generally anything which allows access to your on-premises network).
2.3. Block Legacy Protocols in M365 to prevent MFA bypass (see https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/block-legacy-authentication). This will happen automatically starting October, but it's better to do it in a managed way and inform users in advance and help them switch to a modern authentication client, otherwise they'll be cut off from email.
2.4. Enable MFA on cloud services which store PII (e.g., HR and Payroll systems and CRM systems).
2.5. Check for users without MFA using LazyAdmin PowerShell script (see https://lazyadmin.nl/powershell/list-office365-mfa-status-powershell/) or MFASweep (see https://github.com/dafthack/MFASweep) WARNING the latter will probably trigger AV systems so run it on a virtual machine for that specific purpose.
2.6. Monitor Azure sign-in logs for single factor authentication (also one of the steps in 2.3 above)

# 3. Monitor remote desktop protocol (RDP)
3.1. Block RDP on any systems where it’s not required via local or group policy settings (Computer Configuration\Windows Settings\Security Settings\Local Policies\User Rights Assignment) or Windows Firewall Rules (Remote Desktop - User Mode (TCP-In) & (UDP-In))
3.2. Where RDP is required on a system, whitelist so only the required hosts can connect (also using Windows Firewall rules).
3.3. Don't allow RDP from outside your network, only through a VPN connection (ideally also secured using MFA)
3.4. Enforce account lockout to prevent brute force attacks (using local or group policy). 3.5. Audit RDP connection and logon/logoff events (see http://woshub.com/rdp-connection-logs-forensics-windows/ for which events to log and https://www.ncsc.gov.uk/information/logging-made-easy if you want to setup your own SIEM (using Windows Event Forwarding and Elastic Security).

# 4. Provide end-user awareness and training
4.1. Require all new staff to complete cyber security training (if you don't have an existing provider use http://ncsc.gov.uk/training/v4/Top+tips/Web+package/content/index.html) and ask people to complete a refresher if they are victim of a cyber-attack.
4.2. When significant new threats emerge alert users and make sure they know what to do if they see something suspicious or think they have been compromised.