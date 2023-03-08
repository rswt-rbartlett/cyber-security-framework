<img src="/Levels/twt-logo.png" height="100">

# Prepare for incidents
# Step 10. Incident management
Unfortunately it is almost inevitable that you will experience some sort of security incident at some point.  The scale of the incident will range from one compromised user account or one infected laptop all the way up to a ransomware attack which compromises most of your systems.  How you respond to security incidents can significantly reduce the duration and extent of a breach.  To support Trusts in responding effectively to incidents, below are some useful resources.

> **Note**: This guidance assumes that you or your IT provider has configured your systems so you will be aware when an incident is ongoing, see [Step 9](./Step-09-Logging-and-monitoring.md).

## Develop an Incident Response Plan
All Trusts should have an incident response plan, not necessarily a technical plan (unless you have your own internal IT team) but you should develope a plan which addresses the following questions:
1. Who is responsible for triaging events (deciding if it is an incident, and if so what type of incident and severity)?
2. Who is in the wider Incident Response Team?  This should include the following:
	1. Senior Management
	2. Data Protection, 
	3. Legal and Insurance, 
	4. Human Resources, 
	5. Internal Communications, 
	6. External Communications including Media, 
	7. IT and/or third party IT provider, and 
	8. Your Insurer.
3. How will you communicate with all of those above even if your IT systems are offline?
4. Who else should you consider communicating with during an incident (e.g. people whose data is affected, other Trusts who might be at risk, suppliers, funders, regulatory bodies like the Information Commissioner's Office or law enforcement).
5. How will you escalate an incident if it becomes serious?
6. What other support might you need to invoke (e.g. a Technical Incident Response provider, which if you have Cyber Insurance may be part of your cover package)?

All of this detail could go into any existing Business Continuity Plan you have, it doesn't have to be a different process or document.

As part of your plan you should have post-incident review, where you consider whether there is anything to learn from either the incident or your response to it, so you identify any improvements and implement those.

To help you create your process a template based on the RSWT Incident Response Process is [here](./cyber-incident-response-process.md).

> **IMPORTANT: You should keep an up to date copy of your incident response plan somewhere safe which is not dependent on your IT systems.  For example paper copies at the homes of those staff who are in the wider Incident Response Team, and a copy held in your IT provider's environment.**

## Test your Incident Response plan
The first time you invoke your incident response plan will be a high stress scenario, which is a bad time to read it for the first time, and an even worse time to find ommissions, mistakes or mistaken assumptions.  Therefore it's vital that you test your incident response plan to make sure it works, and everyone understands their role.

This does not need to be a full facilitated business continuity exercise, a simple desktop exercise should be enough to check whether it will work.  To help you the National Cyber Security Centre have provided an online tool called [Exercise in a box](https://www.ncsc.gov.uk/information/exercise-in-a-box) which has a number of scenarios you could test.

> The intention is for RSWT to produce a template for a desktop exercise for Trusts to test their incident response process, based on one of the NCSC exercises but designed specifically for Trusts of different sizes.

## Tools for IT
If you have IT staff who will be responsible for triaging or responding to an incident it is important that they take appropriate precautions when handling potentially malicious content, and don't inadvertently make the situation worse.  Below are some tools that can be used to analyse suspect emails, websites or programs (malware).

- [Windows Sandbox](https://learn.microsoft.com/en-us/windows/security/threat-protection/windows-sandbox/windows-sandbox-overview). This is a lightweight desktop environment to safely run applications in isolation. Software installed inside the Windows Sandbox environment remains "sandboxed" and runs separately from the host machine.  If you close the Sandbox everything within it is deleted.  You can copy suspect executable, emails or URL's into the environment, inspect and/or run them, and any impact will be confined to the sandbox.
- [Virustotal](https://www.virustotal.com/gui/home/upload).  This is an environment you can upload files, URLs and other potential suspicious elements to and it will analyse those using multiple anti-virus engines and compare them to other information security sources.  **Note**: Anything you upload here is public and can be viewed by anyone so be sure a document contains no personal or other confidential information before uploading it.
- [Hybrid Analysis](https://www.hybrid-analysis.com/). A free malware analysis service for the community that detects and analyzes unknown threats, powered by CrowdStrike Falcon® Sandbox.
- [ANY.RUN](https://any.run). A cloud-based sandbox with full interactive access (so you can imitate a human interacting with the malware) which is not possible with the two services above.

## Return to [Step 9. Logging and monitoring](./Step-09-Logging-and-monitoring.md)