<img src="/Levels/twt-logo.png" height="100">

# Purpose

This policy sets out RSWT's approach to managing its information security objectives (see below). It addresses the governance and operation of IT security and sits above the Staff Information Security policy, which addresses staff conduct.

## Audience and scope

The audience for this policy is managers and technical staff responsible for delivering IT services to RSWT staff and volunteers.

# Information Security Objectives

- To ensure that our customers' data, and internal system security information, does not fall into the wrong hands, and that we fulfil our obligations with regards to the Data Protection Act and other applicable laws and regulations.
- To ensure that, in the event of a major security incident we can restore critical services and data promptly to reduce any disruption to RSWT.
- To establish responsibility and accountability for Information Security within our organisation.
- To be proportionate in the implementation of controls, respecting the expertise and professionalism of our staff, and ensuring security is an enabler to nature\'s recovery and not a barrier.
- To ensure our employees maintain an appropriate level of awareness, knowledge and skill to allow them to minimise the occurrence and severity of Information Security incidents.
- To review our information security policies annually to ensure they are effective and reflect both current good practice and applicable legislation/regulation.

# Information security roles and responsibilities

| Role | Title | Responsibility |
| ---- | ----- | -------------- |
| Senior Information Risk Owner (SIRO) | Head of Executive Office | Providing accountability and assurance to SLT that information governance policies, including data protection and information security policies are complied with.|
| Information Asset Owners | Directors and Heads | Has accountability and authority to manage the risk; approving the risk treatment plan and residual risk for the risks that they own.|
| Risk Assessor | Strategic Lead for Information Security | Assessing cyber security risk across RSWT and providing advice on appropriate mitigating measures.|
| Security Incident Management | Strategic Lead for Information Security | Co-ordinating RSWT technical response to a major or critical information security incident.|

# Information classification

The Information Classification section of the Staff Information Security Policy sets a framework for classifying and handling RSWT information based on its level of sensitivity, and its value to RSWT. Personally Identifiable Information (PII) must be managed and protected in accordance with RSWT Data Protection and Information Classification Policies.

# Communications security

## Network controls

RSWT operated wireless networks must be protected using modern authentication and encryption technology (\'modern\' meaning currently in active development and supported by a vendor or community). Encryption must meet the current FIPS 140[^1] standard at the time of reading.

All connections to RSWT systems should be protected using modern authentication and encryption technology including either multi-factor authentication where passwords are used, or strong authentication which meet contemporary FIPS 140 standards. Where that is not possible a security risk assessment should be carried out and the residual risk accepted by RSWT.

Network security events should be logged on network routers and firewalls on RSWT network, and on virtual network infrastructure in cloud hosted environments. Logs should be retained for 180 days.

Use of computers connected to RSWT network via wired, wireless or VPN connection must be authenticated, unless a security risk assessment is carried out and the residual risk accepted by RSWT.

## Unauthorised use

Attaching more than one device to any network port by use of network switches, firewalls, routers or wireless access points or any other means without permission from ICT should be prevented using technical controls.

Use of any software or hardware which causes disruption to the correct functioning of RSWT systems is prohibited under the Staff Information Security Policy. If such disruption does occur the offending device or software should be disconnected from RSWT network by ICT.

# Access control

Access to Public and Internal Only classified information is granted to all staff by default, to support effective communication and collaboration across RSWT.

Administrative or Privileged access and access to Strictly Confidential data is only granted to staff where it is explicitly required for their role. Such access should be added and removed to reflect changes in employment status, role and responsibility, and reviewed regularly to ensure compliance with these principles.

## Regular user access control

Role Based Access Control (RBAC) should be used wherever possible to assign access rights to users throughout the account lifecycle, where the role/s associated with the user determines the access they have.

Any access granted outside the RBAC groups should be reviewed regularly and wherever possible RBAC groups should be modified or created to incorporate that access and minimise exceptions.

All new staff accounts should be inactive until the user has been through an identity verification process, at which point the account can be activated, and the user must set their own unique password.

As the status of a user changes within the relevant information system accounts must be either:

1. Deactivated promptly if no longer required, and deleted after no
    more than six months, unless there is a business reason to retain
    it, or

2. The user's group membership must be cleared, and new group
    membership set according to the new role.

Owners of sensitive personal identifiable information assets should review the users who have access to those assets regularly.

## Privileged user access control

Staff, contractors or third-party employees who require privileged access for the technical administration of information systems must be provided with a separate named account for that purpose. Those accounts are only for use where privileged access is required, and not for any routine activity including email or instant messaging and web browsing.

Privileged access to systems should be reviewed annually.

Role Based Access Control (RBAC) is the default method of assigning privileged access rights based on the responsibilities of that member of staff.

Any privileged access granted outside the RBAC groups must be reviewed as part of the annual privileged account review, and wherever possible RBAC groups should be created or modified to incorporate that access to minimise exceptions.

Technical controls should enforce enhanced authentication measures (including but not limited to increased password length, multi-factor authentication and conditional access) for all privileged accounts.

Access to and administration of systems by privileged accounts must be logged.

## Access from personal devices

Access to RSWT data from personally owned devices (aka Bring Your Own Device, or BYOD) is permitted, but staff are required to comply with the Staff Information Security Policy when doing so.

Where systems allow, BYOD access to data should be constrained as follows;

1.  To devices with effective hardware backed credential storage

2.  To devices which are Trusted or Managed (depending on the
    sensitivity of the data)

3.  To Microsoft 365 applications (where the data resides within the
    Microsoft cloud services)

# Protection from malware

## Security awareness

The RSWT Staff Information Security Policy requires all staff to complete Data Protection and Information Security Training at the start of their employment, and every two years thereafter. This training includes information on how to stay safe online and avoid viruses.

## Controlling software installation and use

Staff should not have administrative access to desktops and laptops unless their role requires it. Where administrative access is required, it should be actively managed, proportionate to user need, wherever possible time limited, and subject to annual review.

## Malware detection

The Staff Information Security Policy requires that all personal computers which store or process RSWT information must be protected using up to date anti-virus software and updated frequently with the latest operating system and application patches and updates. RSWT computers must comply with the same requirement, and for those computers anti-virus and patching is managed by ICT to ensure compliance.

Email services used in RSWT have built-in malware protection to prevent the transmission of viruses contained in both inbound and outbound messages.

# Management of technical vulnerabilities

## Inventory of assets

All RSWT server and endpoint (desktop and laptop) assets and cloud-based services must be recorded within an IT asset inventory which should be maintained and regularly reviewed by the IT team to ensure it is accurate. For RSWT operated services which comprise multiple software components a Software Bill of Materials (SBOM) should be maintained and linked to from the asset inventory.

## Identifying vulnerabilities

Appropriate information resources to identify vulnerabilities should be maintained for all assets in the inventory and updated in line with changes to the inventory. This includes components within an asset in the linked SBOM.

The ICT team in collaboration with the Strategic Lead for Information Security are responsible for the identification and monitoring of vulnerabilities and advising RSWT on the level of risk presented and the appropriate corrective action. To that end, the ICT team will audit networks and systems to ensure compliance with this and other RSWT policies relating to information security and regulations. Audits will take the form of monthly automated vulnerability scanning of the internal and external network, quarterly internally resourced basic penetration testing and annual third-party penetration testing.

## Reacting to vulnerabilities

Once a vulnerability is identified (via third party notification, vulnerability scanning or penetration testing) it will be assessed by the ICT Team in collaboration with the Strategic Lead for Information Security. Wherever possible patches will always be applied within 30 days of release regardless of the severity.

High-risk or critical security updates for operating systems, firmware and applications must be installed as soon as possible, and within 14 days of release for all systems.

Medium to low-risk updates should applied automatically on a regular cycle, and ideally within 30 days.

If a patch cannot be applied the decision not to patch including the justification, alternate approach (mitigate, workaround or accept risk) and who made the decision will be documented in the risk register.

## Monitoring vulnerabilities

Monthly vulnerability scans are conducted of the internal network in Newark, the servers in Azure, and the cloud services for which RSWT is responsible for penetration testing.

Any vulnerabilities found are logged as a cyber security risk in the risk register and actions assigned to either mitigate the vulnerability or accept the risk. The risk of a High or Critical vulnerabilities on public facing services can only be accepted by a member of SLT, with the advice of the Strategic Lead for Information Security or the Head of ICT.

# Backup

All data should be backed up according to its value to RSWT, the cost of recreating the data, any financial costs or penalties which might be incurred due to data loss or corruption, and the risk of data loss or corruption.

The primary purpose of data backup is to allow RSWT to continue its activity after a data loss incident, by retrieving some or all the data lost, ideally from a point in time backup taken within the last 24 hours.

All backups should meet the following minimum requirements:

1. It has been designed to meet the recovery time and recovery point requirements of RSWT.
2. It is sufficiently resilient that failure of a single hardware component would not result in data loss.
3. It is held separately from the original data storage location such that it would be unaffected by hardware or software failure or physical/environmental incidents (e.g., fire or flood).
4. It is protected from unauthorised access through technical controls and as far as possible physical separation from the original data storage location (to prevent destruction in the event of a security incident, e.g. ransomware).
5. It is tested at least annually to ensure the data backed up could be used in the event of a data loss incident.

# Cryptographic controls

Business information should be protected wherever possible by modern encryption at rest and in transit, and always for information classified as Strictly Confidential (see Staff Information Security Policy Information Classification section). This includes data servers and on desktop computers and laptops.

Where it is not possible to provide this protection, this must be managed as an information security risk, and reviewed at least annually.

Backups should be encrypted to prevent unauthorised access or modification.

Wherever possible key management should be used to centrally provision and manage access to encryption keys and secrets, to prevent data loss in the event of key loss. Responsibility for cryptographic controls on servers, desktops and laptops should be clearly defined.

# Physical and environmental security

Areas where strictly confidential information is processed should be given an appropriate level of physical security and access control, at a minimum access control by key, card, or code. In these spaces delivery personnel and visitors must be supervised. Staff with authorisation to enter such areas are provided with information on the potential security risks and the measures used to control them.

# Supplier relationships

Responsibility for the management of supplier relationships should be clearly documented.

Cloud service providers and third-party software suppliers by default have no access to RSWT data, including administrative accounts on systems. Data is protected by access control and encryption, with the encryption keys being managed and controlled by RSWT. Non-Disclosure Agreements (NDAs) shall be used in all situations where access to Strictly Confidential information to a Cloud service provider or third-party software supplier is deemed necessary and appropriate.

Supplier access to systems should only be allowed when authorised by RSWT as part of a technical support call or planned maintenance activity, provided on the principle of least privilege, audited and logged. Where necessary, supplier access will be accompanied or observed in order to ensure compliance with RSWT policy.

# System acquisition and development

All systems or services acquired or developed should enable RSWT to meet the [Communications security](#communications-security), [Access control](#access-control), [Backup](#backup) and [Cryptographic controls](#cryptographic-controls) requirements of this policy.

All suppliers of products or services should be committed to the ‘secure by design’ principle. Any contract of supply must include security as a core requirement covered by the maintenance and support costs, and no extra charge must be levied to fix security flaws in the suppliers’ own products or services.

When acquiring or developing new systems it is important to identify the information security requirements of the system and manage those through design/implementation. The information security requirements will depend on the nature of the service and the value and sensitivity of the data it would store or process.

For lower risk systems or services, the requirements will be simple, and a set of security assurance questions may provide sufficient assurance. For systems processing or storing strictly confidential data or where the availability of the service is particularly important the requirements will be more complex. In this scenario the following steps are required;

-  Assessment of the proposed design, implementation, and configuration
    against the security requirements.

- Assessment of supplier information security policies and procedures
    and any relevant accreditation or certification.

- For cloud services (e.g., Software as a Service) assessment based on
    the NCSC Cloud Security Principles[^2] (using all 14 principles or
    the lightweight approach as determined by the sensitivity of the
    data being processed).

- For services developed by a third party for RSWT an assessment of
    the supplier's secure development methodology for inclusion of
    secure coding practices.

- Inclusion of information security requirements in the procurement
    requirements, and if required addressed directly in the contract.

# Information security incident management

RSWT has established an Incident Management procedure to ensure a quick, effective and orderly response to information security incidents. This procedure identifies the individual or team responsible for responding to information security incidents.

## Identifying security events

Information security events reported by service users or triggered by monitoring and management systems should be recorded. Those events should be assessed by staff with the appropriate skills and experience (or an appropriate third party), and decision made whether those events are classified as an information security incident

## Responding to security incidents

Information security incidents should be recorded as such and responded to according to the incident management procedure. Any knowledge gained from analysing and resolving those incidents should be recorded and used to reduce the likelihood or impact of future incidents.

Any evidence gathered during the incident response process should be appropriately recorded, and as far as possible original evidence should be preserved as per [ACPO guidelines](http://library.college.police.uk/docs/acpo/digital-evidence-2012.pdf) and [ISO/IEC 27037](https://www.iso.org/standard/44381.html).

The incident management procedure includes appropriate escalation, such as for internal escalation (including to the Senior Leadership Team, Media Relations), and for reporting to the relevant authorities (Action Fraud, and the East Midlands Cyber Protect Network).

[^1]: See
    <https://csrc.nist.gov/Projects/cryptographic-module-validation-program/validated-modules/Search>

[^2]: https://www.ncsc.gov.uk/collection/cloud/the-cloud-security-principles
