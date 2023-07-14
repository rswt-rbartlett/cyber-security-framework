<img src="/Levels/twt-logo.png" height="100">

When assessing the security of a proposed new system, or a system which is new to me, these are the questions I ask.  The answers then give me an idea of the level of risk of the application.

## What type of data will it store and process?
If it includes only public data the risk is lower, if it includes confidential (internal only) or strictly confidential (personal and sensitive personal information) then the risk is higher, because the consequences of a breach could include significant financial penalties.

## What is the attack surface of the system?
The attack surface is what an attacker use, including network ports, services and management interfaces.  Well architected systems have a very small attack surface, with only the vital interfaces and services exposed, and management interfaces and optional features disabled, hidden or restricted by default.

## How are system users authenticated and authorised?
If the system will hold confidential or strictly confidential information then users identity should be verified by strong authentication (for example Multi-Factor or Certificate authentication). Authorisation to access data within the system should be based on Role Based Access Control (RBAC) where permission to access data is based on the role or group membership of the users, rather than direct assignment of permissions to individuals.

## Is the system well written and maintained?
The size of the team maintaining the product is not necessarily an indicator of quality. Very large vendors have vulnerabilities in their code, and open-source projects maintained by one person may have less, or none.  The security of the product is a consequence of the skills of those writing code, testing code, and the effectiveness of their security assurance processes. To assess whether the product is well written and maintained you can break this down into a few questions:

1. Does the author or vendor follow secure coding practices?
2. Do they conduct vulnerability scans and penetration tests on their product?
3. Do they do code reviews to identify security bugs?
4. If vulnerabilities have been found in their product previously, have they issued patches promptly?
5. If they use open source or free libraries are those libraries also well maintained?

## Does the system exhibit any security anti-patterns?
These are some common bad practices which are indicative of a system developer not understanding or prioritising security.

1. **Excessive privileges**. This is where the system requires the service account or the account of the person using the system to be Local, Domain or Global Administrator. This means they couldn't be bothered to work out what permissions were needed, so they demand everything.
2. **Doesn't play with antivirus**. You have to disable anti-virus to get it to work, or exclude the entire program directory. This probably means they don't follow platform vendor development best practice guidelines, and the program works in a way which anti-virus will detect as malicious. Sometimes excluding a specific directory which has a lot of read/write transactions to prevent impacting performance is reasonable, but not everything.
3. **Archaic password policies**. Forcing users to reset their password every x days (best practice is only to reset passwords if they are believed to be compromised).