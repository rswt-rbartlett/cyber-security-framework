<img src="/Levels/twt-logo.png" height="100">

# Thread hijacking
Thread hijacking is a growing threat, it's proving a very effective method for attackers, and you should make sure you have effective defences against that, and that your colleagues know what to look for and what to do.

# Context
Thread hijacking is when attackers reply to an email stolen from organisations we communicate with in a previous breach. To the recipient the email looks legitimate because it's part of a conversation they were having with a supplier, funder or other partner organisation, but the attachment contains a virus.  The from address is sometimes faked, but sometimes the email will come from a real email address of a contact known to the recipient.  These emails are almost impossible to detect.

Thread hijacking has been used recently to spread IcedID, Bumblebee and Qakbot malware, all of which can lead to ransomware.

# Recommendations
- [ ] Implement DMARC for your email domain (the NCSC MailCheck service is helpful for this) which makes it harder for someone to spoof your domain.
- [ ] Implement anti-phishing mail protection for your email service
  - [ ] for Microsoft Exchange Online see https://docs.microsoft.com/en-us/microsoft-365/security/office-365-security/configure-anti-phishing-policies-eop?view=o365-worldwide and configure at https://security.microsoft.com/antiphishing
  - [ ] for Google Workspace see https://support.google.com/a/answer/9157861?hl=en-GB and configure at https://admin.google.com/).
- [ ] Inform your colleagues and make sure they understand the threat.  Use an example email to show what they can look for, stress the importance of being cautious when receiving an email with attachments unexpectedly, even if the sender is legitimate.
- [ ] Make sure your end user devices and email clients are patched and up to date, some cyber-crime groups are still exploiting Outlook vulnerabilities from 2017 and 2019 to deliver malware.

# What we're doing
- [ ] I'm continuing to monitor our quarantine and various threat intelligence sources (including Twitter!) for new and emerging threats.
- [ ] We're reviewing our anti-phishing protections to improve the protection for RSWT staff.
- [ ] I'll be putting a warning on our All Staff chat on Teams about threat hijacking to help them understand and recognise the threat.
- [ ] Significant new and emerging threats will be published in a Cyber Security Briefing here on Wildnet.
- [ ] A new 'Current threats and recommended mitigation' paper is being prepared which will also be posted to Wildnet.  This paper is designed to guide technical staff in implementing a baseline of security controls, and where necessary convince senior management and trustees to support those measures.

# In the news
Recent victims of ransomware include [Macmillan Publishing](https://www.itpro.co.uk/security/368401/macmillan-publishers-apparent-cyber-attack-systems-offline) (25th June), [Wiltshire Farm Foods](https://www.bbc.co.uk/news/uk-england-wiltshire-61949394), (26th June) and [Clarion](https://www.bbc.co.uk/news/uk-england-wiltshire-61949394) (26th June).

The UK Government has set out its approach to protecting and promoting the UK’s interests in cyberspace in the [National Cyber Strategy 2022](https://www.gov.uk/government/publications/uk-national-cyber-strategy-2022).

The first episode of a cyber drama "[The Undeclared War](https://www.channel4.com/programmes/the-undeclared-war)" is on Channel 4.  A cyber security expert who had a sneak peek said it was quite true to life, in technical terms at least.
