<img src="/Levels/twt-logo.png" height="100">

# IN AN EMERGENCY (MEDIUM OR HIGH IMPACT INCIDENT)
![Process to follow in an emergency](./media/in-an-emergency.png)

**In a medium or high impact incident all technical response activities will be led by the Cyber Insurance Incident Response Team. See Section 5 for more details.**

The Incident Manager (by default the Strategic Lead Information Security) co-ordinates communications, escalations and any reporting issues, pulling the whole response together.

# Introduction

This document sets out the process for managing and responding to information security incidents within RSWT, as per the IT Information Security Policy version 1.0.

## Invocation

Multiple information security **events** occur every day, and not every event is an **incident**.

A security incident is when a sequence of events has/will lead to the disclosure, modification or loss of data.

The most likely events are;

1.  Anti-virus alerts
2.  Staff reporting unusual behaviour on an account.
3.  A third party reporting suspicious emails or other activity from our network.
4.  National Cyber Security Centre (NCSC) Early Warning Service notification.
5.  Absolute Networks reporting a suspect incident.

## Recording

Once a security incident is declared it should be recorded in Jitbit,
and as the incident progresses all information gathered, decisions made,
actions taken, data captured (or missing) should be recorded within
Jitbit.

> ***Note:** If an incident has already got to the point where Jitbit is no longer believed to be a secure environment (i.e. the attackers have Active Directory administration rights) the incident would be a major or critical incident, and escalated to a third party (see Escalation section below).*

## Key Contacts

Communication is vital throughout any security incident. The table below lays out the important people who may need to be involved, and an alternative contact if they are not available. This is the RSWT Cyber Security Incident Response Team.

For any internal contacts who need to be reached for a rapid response (including out of hours) a mobile phone number is required. This is to avoid communicating over potentially compromised or disrupted communication channels.

| Role | Internal Contact | Phone |
| ---- | ---------------- | ----- |
| Incident Manager. _Oversee, communicate, engage support, escalate, notify_. | Jane Smith Operations Manager | 07725 999999 |
| Senior Management. _Escalation of serious incidents_. |   |   | 
| Data Protection. _Provide advice on Data Protection issues including ICO notification_. |  |  |
| Incident Response. _Technical incident response resource_.  |  |  |
| Legal & Insurance. _Provide advice on insurance, liability and other legal matters_.  |  |  |
| HR. _Liaison for staff disciplinary or wellbeing matters_.   |  |  |
| Internal Communications. _Communication within RSWT and TWT_.   |  |  |
| External Relations. _Communication with the media, the public_.  |  |  |
| Cyber Insurance Provider. _Incident Management, IT Forensics, Legal, PR services._  |  |  |

*Table 1 - Key Contacts*

## Management

From invocation to review the Incident Manager will;

- Oversee the technical incident response (RSWT or Insurer IR team),
- Co-ordinate communication with Key Contacts,
- Trigger escalation, and
- Initiate any reporting and notification required including regulatory, law enforcement, customers and other stakeholders.

## Communication

During an incident the following stakeholders may need to be informed about the incident or the consequences of the incident;

- RSWT staff
- Anyone whose data has been disclosed
- Wildlife Trusts
- Suppliers (particularly cloud service providers)
- Funders (especially where our contract requires us to notify them of   an incident)
- Regulatory bodies (the Information Comissioners Office)
- Law enforcement (Action Fraud)

Communication with these stakeholders will be undertaken by the appropriate Key Contact.

## Process

Following is a flowchart showing the Incident Response Process from beginning to end, including the key communication points and regulatory requirements.

![Incident Response Process Flowchart](./media/process-flowchart.png)

# Triage

The first stage of an incident is triage, where the Incident Manager and Technical Incident Response Team determine the type and severity of the incident, which determines what happens next.

Triage needs to be quick, so you are only looking to gather as much information as is required to identify the type and take an *initial assessment* of the severity (this will probably change as the response progresses). If there is a suspected data breach report/record it as a suspected breach and then validate it in the next stage.

**Incident type** would typically be one or more of the following attacks;

- Phishing (including spear phishing, whale phishing, vishing etc.)
- Malware infection (including ransomware)
- Denial of Service
- Insider (malicious or accidental incident caused by a member of staff)

**Incident severity** follows the RSWT Risk Framework of Low, Medium or High, see examples below.

| Descriptor | 1 (Low) | 2 (Medium) | 3 (High) |
| ---------- | ------- | ---------- | -------- |
| Example | Compromised non-privileged account, loss of non PII data, outage of a one or two non-critical systems. | Compromised privileged account, loss of PII (<500 persons) or other valuable or sensitive data, short term (1-10 days) outage on multiple systems or one critical system. | Large scale loss of PII (500+ persons) or other sensitive or valuable data judged to be a significant breach of DPA, extended loss (10+ days) of multiple critical systems. |

*Table 2 - Incident Severity*

Having determined the type and severity of the incident during the triage process you can then determine whether to escalate, and how to respond.

## Escalation

An incident can be escalated (or de-escalated) at any time. Escalation determines who is **responsible** for making decisions during the incident, who is the most senior person **informed** about the incident whilst it is active, and which team is running the **technical incident response**.

For Medium and High Impact incidents where an insurance claim is more likely the Cyber Insurance Incident Response Provider will run the response (with support from RSWT ICT).

| Descriptor | 1 (Low) | 2 (Medium) | 3 (High) |
| ---------- | ------- | ---------- | -------- |
| Responsible | Head of IT | Director of Business Services | Deputy Chief Executive |
| Informed | Director Business Services | Chief Executive | Chief Executive |
| Incident Response | RSWT ICT | Cyber Insurance Incident Response Provider | Cyber Insurance Incident Response Provider |

*Table 3 - Escalation Matrix*

# RSWT Technical Incident Response
*Redacted*

# Third party Incident Response

In the event of a medium impact incident involving PII or any high impact incident you call the 24/7 hotline (see IN AN EMERGENCY and Key Contacts) and you will get a callback from their incident response team. Their initial questions (which you should have answers for) will be;

1.  Date, time and location of the incident
2.  The evidence that triggered the incident (e.g. M365 Security Alerts, staff or third party report, systems going offline).
3.  The known impact (e.g. data accessed or lost, systems in scope).
4.  Current status (is the incident ongoing, or ‘live’, or has it ceased).

Once the external incident response team is engaged they will direct all technical incident response actions, with the RSWT ICT team acting under their instructions, overseen by the Incident Manager. 

This Cyber Insurer Incident Response team may ask for access to interrogate RSWT systems directly, but it’s more likely they will direct RSWT staff to do so on their behalf. Therefore, familiarity with the concepts in sections 3.1 to 3.4 above would be useful.

# Post Incident Review

After an incident has been resolved and the recover stage is completed (or sufficiently progressed to begin review) there should be a documented review of the incident and the response to it.

## Incident Review

- Could anything has been done to prevent the incident?
- Could the incident have been detected earlier?
- Are there any trends from this and other incidents or events which   might inform security improvements?

## Response Review

- Was the response effective and timely?
- Were all the right people involved?
- Were those involved sufficiently informed and empowered to make   decisions?
- Was all the data required to respond promptly and effectively   available?
- Did the processes and communications work well?

The findings from these reviews should be recorded, with any risks identified recorded in the risk log, and any actions recorded in the minutes, assigned to a named individual with a deadline for implementation.

[^1]: <https://us-cert.cisa.gov/ncas/alerts/aa20-245a>

[^2]: <https://www.exterro.com/ftk-imager>
