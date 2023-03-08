<img src="/Levels/twt-logo.png" height="100">

# Block attachments to prevent ransomware infection

**Tl;dr blocking the file extensions used by cyber-criminals is a simple way to avoid ransomware attacks**

# Context
- We use Microsoft Defender for Office to protect us from threats in Exchange Online, SharePoint, Teams and OneDrive.  It's highly effective, but we have to assume one day something will get through.
- As a second layer of defence we block a number of file extensions which are commonly used to deliver malicious payloads (viruses and trojans) using [Transport rules](https://admin.exchange.microsoft.com/#/transportrules).
- The list of file attachments we block includes;
  - less commonly used file types which are never legitimate (.bat, .lnk, .iso, .xltm, .dotm), 
  - rarely used file types which in theory someone might legitimately send via email (.xlsm, .docm) and 
  - file types which are sometimes sent by email, but we block as a precaution (.htm, .html, .zip).
- Sometimes this blocks legitimate email, but not often, and we check quarantine daily which takes 5-10 minutes.
- We can add exceptions to these rules for specific IP ranges, but right now there's not enough support overhead to justify it.

# Ransomware from ISO files
The practice of blocking specific file attachments has been in place for some time at RSWT. I use free threat intelligence sources to inform whether we change them, and recently an [incident report](https://thedfirreport.com/2022/04/25/quantum-ransomware/) caused us to add .ISO files to the list.

The incident report paints a very scary picture, it took only 4 hours from the infected attachment being opened for ransomware to hit every computer and server on the domain.

Because here's no requirement for staff at RSWT to receive .ISO files by email blocking them is an easy way to block malicious attachments even if they aren't detected by email filtering software or desktop endpoint protection/anti-virus.

# Recommendations
- [ ] If you maintain your own email environment (Exchange, Exchange Online or Google) I'd recommend implementing rules to block those attachments cyber criminals use, and your colleagues don't.
- [ ] If you don't  maintain your email environment do contact your IT service provider and discuss attachment blocking as a way of reducing the risk of ransomware.