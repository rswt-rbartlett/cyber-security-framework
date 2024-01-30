<img src="/Levels/twt-logo.png" height="100">

# cyber-security-framework
A Cyber Security Framework for The Wildlife Trusts

# Introduction
This framework sets out a standard for Cyber Security for The Wildlife Trusts to support the whole federation meeting legislative and regulatory requirements. It is written to be proportional, following the principle of [Article 32](https://www.legislation.gov.uk/eur/2016/679/article/32) of the UK GDPR to "implement appropriate technical and organisational measures", taking into account factors including risk and the costs of implementation.

The framework is based on the National Cyber Security Centre (NCSC) ['10 Steps to Cyber Security'](https://www.ncsc.gov.uk/collection/10-steps) and the steps apply to all Trusts, with the effort and skills required being proportional to the resource and size of the Trust. Each step is linked to the accompanying guidance, templates and technical resources which support Trusts in implementing the measures.

The framework will be reviewed at least every three years or where there are significant changes to legislation (UK GDPR) regulation (Charity Commission or Cyber Essentials) or guidance (the NCSC).

In addition to the standard set out below a [Maturity Model](/Levels/README.md#introduction) describes the measures Trusts should take in meeting this standard, dependent on the scope of their information systems and the resultant risks.  You can also browse the whole framework if you wish at [Contents](/Levels/Contents.md).

## Working with suppliers
The controls listed in this framework can be implemented by Trust staff, third party suppliers, or a combination of the two. In this vital that each Trust has a clear understanding of which party is responsible for the control, and where a supplier is responsible that is explicit in the agreement with them.  Otherwise it is possible for unshared assumptions on both sides to lead to critical responsibilities being missed, leading to increased risk or security breaches.

To support Trusts in reaching an understanding about who is responsible for each control an illustration [Shared Responsibility Model](/1-Understand-your-risks/shared-responsibility-model.md) has been developed to support conversations and decision making in this area.

# The Standard
Below are the 10 Steps to Cyber Security, with explicit statements of compliance for 6 of the 10 steps which Trusts satisfy as fundamental and essential security controls.

1. Risk management
2. Engagement and training
	1. Senior Management [visibly support](/1-Understand-your-risks/Step-02-Engagement-and-Training.md#top-down-support) Trust cyber risk controls and demonstrate good cyber hygiene 
	2. Appropriate steps are taken to [make staff aware](/1-Understand-your-risks/Step-02-Engagement-and-Training.md#security-awareness) of cyber risk and their part in managing those risks
3. Asset management
	1. An up to date record is kept of [Data](/1-Understand-your-risks/Step-03-Asset-Management.md#data-assets) and [Technology](/1-Understand-your-risks/Step-03-Asset-Management.md#technology-assets) Assets
4. Supply chain security
5. Architecture and configuration
	1. Trust email domains are [configured](/2-Implement-appropriate-mitigations/Step-05-Architecture-and-Configuration.md#make-it-harder-to-spoof-your-email-domain) to prevent spoofing
	2. Effective endpoint protection is [installed](/2-Implement-appropriate-mitigations/Step-05-Architecture-and-Configuration.md#install-effective-endpoint-protection) on all Trust end user devices
6. Vulnerability management
	1. All systems are [patched and updated](/2-Implement-appropriate-mitigations/Step-06-Vulnerability-Management.md#update-systems) periodically and testing validates that publicly accessible systems are [free of vulnerabilities](/2-Implement-appropriate-mitigations/Step-06-Vulnerability-Management.md#scan-for-vulnerabilities)
7. Identity and access management
	1. Access to personal data is [limited](/2-Implement-appropriate-mitigations/Step-07-Identity-and-Access-Management.md#decide-who-needs-access-to-what-and-how) to authorised staff only and regularly [reviewed](/2-Implement-appropriate-mitigations/Step-07-Identity-and-Access-Management.md#maintain-your-identities)
	2. Trusts use [multi-factor authentication](/2-Implement-appropriate-mitigations/Step-07-Identity-and-Access-Management.md#implement-multi-factor-authentication-mfa-for-all-remote-access) on all publicly accessible cloud services and remote access
	3. Trusts [restrict privileged access](/2-Implement-appropriate-mitigations/Step-07-Identity-and-Access-Management.md#separate-admin-accounts-and-protect-them) to those who need it and using a separate individually named account 
8. Data security
	1. Trusts ensure their systems [encrypt](/2-Implement-appropriate-mitigations/Step-08-Data-Security.md#protect-data-with-encryption) all personal data at rest and in transit
	2. Trusts [backup](/2-Implement-appropriate-mitigations/Step-08-Data-Security.md#backup-your-data) their data according to its value and sensitivity and protect that backup from attack.
9. Logging and monitoring
10. Incident management