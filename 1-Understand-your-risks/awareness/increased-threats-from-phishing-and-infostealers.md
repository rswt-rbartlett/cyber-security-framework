<img src="/Levels/twt-logo.png" height="100">

# Increased threats from phishing and infostealer malware
Two threats have significantly increased over the past few days, and I strongly recommend all IT teams take steps to detect and prevent those, and make your colleagues aware of them too.

# Phishing
At RSWT we've seen a significant increase in phishing attacks, mostly using .htm or .html attachments which when opened present a fake Microsoft login page, designed to trick staff into giving away their credentials. We've also received alerts of a number of 'typo-squatting' campaigns, where attackers register lookalike domains for popular domains (e.g.youtube.ngo, youtube.ong and youtubse.cloud).  These are typically used in phishing attacks and used to host malware.  In addition to Youtube, there have also been recent alerts for Barclays, Fedex, Salesforce and DocuSign.

**Recommendation**: review your anti-phishing defences and consider blocking attachments commonly used by attackers, if necessary whitelisting domains known to send legitimate .htm/html file attachments.

# Infostealer malware
There has been a recent surge in malicious downloads being promoted via Google Ads.  Attackers are impersonating the websites of frequently downloaded software (like OBS Studio, Notepad++, 7-Zip, WinRAR and VLC player), promoting those sites using Google Adwords and using them to distribute malware. Many of the attacks distribute a particular type of malware called an Infostealer, which collects credentials, credit card details, information about cryptocurrency wallets and logs keystrokes.  This method of compromise was used in recent high impact attacks like the one on [Circle CI](https://circleci.com/blog/jan-4-2023-incident-report/) in December.

**Recommendation**: consider the use of an ad-blocker for all staff systems (as [recommended](https://www.ic3.gov/Media/Y2022/PSA221221) by the FBI), uBlock Origin is very effective and works on Edge, Chrome and Firefox.  You could also use a DNS based ad/malware blocking service like OpenDNS or NextDNS.  Also ensure your antivirus is updating on all systems and someone is responding to any alerts raised.