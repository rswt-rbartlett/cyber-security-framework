<img src="/Levels/twt-logo.png" height="100">

# Cyber threats and recommended mitigations
In response to some discussions I've had over the last three months I've put together a two page briefing report (attached) for all Trusts which sets out;

1. The threat landscape (what's going on 'out there')
2. A risk summary (what could happen and the potential impact)
3. Recommended mitigation (what your Trust should do about it)

The mitigation is very much a baseline which all Trusts should be able to reach, even if they require some support to get there.  In the event of a breach the Information Commissioners Office will consider the steps an organisation took (and didn't take) when deciding whether to levy a fine or just issue a judgement.  Failure to implement the most basic of technical controls significantly increases the risk of a fine (which on top of all the other costs of a breach would have a significant financial and reputational impact).

This briefing has been issued to ensure there is awareness of the risks and the appropriate mitigations from the top down in any Trust.

# Threat landscape

As the barriers to entry continue to shrink the number of individuals engaged in cyber-crime is growing, leading to a corresponding increase in attacks on organisations world-wide.

The incentives to engage in cyber-crime are very high, with individuals earning huge sums (a Canadian recently charged for involvement with the NetWalker gang had earned £22.2m[^1] from ransomware).

Disincentives are low, mainly because most groups operate from 'hostile nation states' (like Russia) where arrest is unlikely and custodial sentences even less so. Intelligence agencies and industry analysts believe ransomware gangs in these countries are either tolerated or actively supported by local authorities.

Most attacks target unpatched vulnerabilities[^2], or use phishing emails, virus infected emails or password guessing to gain access to networks[^3].

The trends for 2022 so far are not good, with Eset seeing a 20% increase in threat detections Jan-Apr compared to the previous period{^4].

The UK National Cyber Security Centre (part of GCHQ) has issued warnings of a heightened threat in the wake of the war in Ukraine, with multiple cyber-crime groups pledging support for the Russian state and threatening to conduct malicious operations in retaliation against countries providing support to Ukraine (which includes the UK). In addition, two cyber-crime groups have been observed using a new programming language (Rust) to improve their ransomware software which is now harder to detect and can infect more systems.

# Risk summary

The three most likely risks for Trusts are the same as equivalent sized businesses, the difference being the smaller budgets available to charities to combat the threats they face.

1. **Ransomware**. An attacker gains credentials through a phishing attack or virus infection and uses those to remotely access the victim network, steal and encrypt all data and then demand a payment to decrypt the data and prevent its release on the internet.
2. **Cyber Extortion**. The same as ransomware but the attacker doesn't encrypt the data, they just steal it and demand money to prevent its release on the internet.
3. **Business Email Compromise**. An attacker uses a well-crafted email, a compromised account at a supplier, or a valid account within the victim organisation to trick a member of staff into transferring funds to a bank account under their control.

## Impact of ransomware

The impact of ransomware is the greatest, with significant disruption whilst servers are reinstalled, and data restored from backup. If those backups are not effectively protected attackers will encrypt them, preventing the organisation from restoring their data. In this scenario, unless the victim pays, they may have to start completely from scratch, which could cause some organisations to shut down, as the cost of recovery would be too high.

Organisations hit by ransomware attacks have faced significant disruption to operations for weeks or even months, and full recovery could take years[^5].

The reputational damage from attackers accessing personally identifiable information is significant, which could lead to a reduction in supporter income.

Financial costs include paying specialist cyber security incident response companies to evict the attackers, identify the entry point and close any loopholes, the cost of rebuilding the environment and restoring data, and the potential for regulatory financial penalties (2%-4% of annual turnover) is significant[^6].

## Impact of Cyber Extortion and Business Email Compromise

Cyber Extortion attacks will have a similar impact, with no cost to rebuild but similar costs in incident response and forensics, regulatory fines, loss of supporter income, and potential reputational damage.

Business Email Compromise has a lower cost but is potentially an increasing threat as ransomware gangs start to adopt it as a new income stream.

# Recommended mitigation

This advice is based on the most recent NCSC alert[^7] which describes these steps as “immediate actions for all organisations” and is **strongly recommended** for all Trusts.

1. Prioritise patching of known exploited vulnerabilities,
2. Enforce multi-factor authentication (MFA),
3. Monitor remote desktop protocol (RDP), and
4. Provide end-user awareness and training.

Steps 1 and 2 should have no additional capital cost and should be seen as the most basic cyber-hygiene that any organisation should be able to achieve. This position is based on Article 32 of the GDPR (which is incorporated in the Data Protection Act 2018) clearly states that organisations should;

> “Taking into account the state of the art … the controller and the processor shall implement appropriate technical and organisational measures to ensure a level of security appropriate to the risk”. 

In a recent action[^6] the Information Commissioners Office demonstrated a willingness to impose financial penalties for failure to comply with Article 32 when they fined a law firm £98,000 on the grounds that they *“failed to process personal data in a manner that ensured appropriate security of the personal data, including protection against unauthorised or unlawful processing and against accidental loss, destruction or damage, using appropriate technical or organisational measures”.*

It is understood that some Trusts may struggle to plan and resource these activities, and the Strategic Lead is available to support any Trust in implementing steps 1-4 above, and any additional steps they need to take to secure their systems and data.  To support Trusts IT teams or Third Parties a [briefing](./technical-resources-for-implementing-recommended-mitigations.md) provides some technical background on:
- :wrench: How to hit the minimum baseline technical controls, and
- :heavy_check_mark: How to validate that the implemented controls were effective.

[^1]: https://www.bbc.co.uk/news/technology-61981923 
[^2]: https://nakedsecurity.sophos.com/2022/06/07/know-your-enemy-learn-how-cybercrime-adversaries-get-in/ 
[^3]: https://news.sophos.com/en-us/2022/06/07/active-adversary-playbook-2022/ 
[^4]: https://www.welivesecurity.com/wp-content/uploads/2022/06/eset_threat_report_t12022.pdf
[^5]: https://www.bbc.co.uk/news/uk-scotland-57578762 
[^6]: https://ico.org.uk/action-weve-taken/enforcement/tuckers-solicitors-llp-mpn/ 
[^7]: https://www.ncsc.gov.uk/news/uk-joins-international-partners-to-issue-advice-on-latest-russian-cyber-threat-