<img src="/Levels/twt-logo.png" height="100">

I hope everyone had a relaxing Christmas break and is ready for 2023.  There have been a couple high profile breaches over the last few weeks so I've included those in the briefing below.  Alongside that is information on the current threat level (which remains high I'm afraid) and good news of some potential free money for Cyber Essentials for smaller Trusts!

# Lastpass Breach

At the end of November LastPass (the password manager app) announced in a [blog post](https://blog.lastpass.com/2022/12/notice-of-recent-security-incident/) that they'd suffered a security breach, which appeared to be a consequence of an earlier breach in August.  They've been rather stingy with the details, and their press releases might lead you to conclude everything is OK.  However other commentators have given a more balanced assessment, two useful insights being from [Graham Cluley](https://grahamcluley.com/lostpass-after-the-lastpass-hack-heres-what-you-need-to-know/) (blogger, podcaster, ex Sophos) and [Jeremi Gosney](https://infosec.exchange/@epixoip/109570449317277575) (password cracking expert).  The key takeaway is the risk to LastPass users is a factor of the length of your password the number of iterations of the PBKDF2 algorithm were used to salt and hash the password (which is lower the longer you've had your LastPass account). 

**Recommendation**: If you use LastPass for work purposes review the two articles linked above, and consider alternative password managers (I use and would recommend [1Password](https://1password.com)  others I trust have recommended [Bitwarden](https://bitwarden.com).  As always, [contact me](mailto:rbartlett@wildlifetrusts.org) if I you need help or advice.

# Guardian Ransomware Attack

Staff at the Guardian newspaper have been working remotely after a ransomware attack on 20th December.  Kevin Beaumont has a [thread](https://infosec.exchange/@epixoip/109570449317277575) on this, noting that their two data-centres were both still offline almost two weeks later.  Their offices are closed until January 23rd which is over a month since the original attack, and a good example of the devastation and disruption of a ransomware attack.  The most typical entry points for ransomware are phished user accounts + remote access with no MFA, or unpatched systems visible on the internet (typically routers, firewalls, storage devices and Microsoft Exchange servers).  

**Recommendation**: If you have remote access or cloud services without MFA or unpatched systems visible on the internet please prioritise [implementing MFA](https://github.com/rswt-rbartlett/cyber-security-framework/blob/main/2-Implement-appropriate-mitigations/Step-07-Identity-and-Access-Management.md#implement-multi-factor-authentication-mfa-for-all-remote-access) and [patching internet facing systems](https://github.com/rswt-rbartlett/cyber-security-framework/blob/main/2-Implement-appropriate-mitigations/Step-06-Vulnerability-Management.md#step-6-vulnerability-management) above any other security work (and arguabley above all other IT work).  To mitigate against the attacker who gets inside your network, protect the administrative accounts in your environment by following the guidance in the [Cyber Security Framework](https://github.com/rswt-rbartlett/cyber-security-framework/blob/main/2-Implement-appropriate-mitigations/Step-07-Identity-and-Access-Management.md#separate-admin-accounts-and-protect-them).  

# Current Threat Levels

## Ransomware and cyber extortion

The threat of ransomware and cyber extortion is still the top risk, based on the impact on victim organisations and the volume of attacks.  Ransomware described by the National Cyber Security Centre (NCSC) as:

> "one of the most significant cyber security threats facing businesses and organisations in the UK".

The Microsoft Digital Defence Report 2022 said:

> "Human operated ransomware is most prevalent, as one-third of targets are successfully compromised by criminals using these attacks and 5% of those are ransomed".

Whilst that might look scary, effective defence is clearly possible as two-thirds of targets are not compromised, so you want to put yourself in that group!

**Recommendation**: The most likely entry points for attackers are described above in the Guardian section, please follow that guidance and contact me if you need assistance.  

## Other threats

Other threats include phishing, which is often a prelude to ransomware but can also lead to the theft of personal data and extortion to prevent its release.  Hacking of social media accounts to financially extort victims for access to their accounts is also on the rise.

**Recommendation**: Follow the guidance in the Cyber Security Framework to [implement MFA](https://github.com/rswt-rbartlett/cyber-security-framework/blob/main/2-Implement-appropriate-mitigations/Step-07-Identity-and-Access-Management.md#implement-multi-factor-authentication-mfa-for-all-remote-access) and [additional phishing protections](https://github.com/rswt-rbartlett/cyber-security-framework/blob/main/2-Implement-appropriate-mitigations/Step-05-Architecture-and-Configuration.md#implement-additional-phishing-protection), check that all social media accounts have MFA enabled wherever possible, and that those with access to Trust social media accounts are [aware](https://github.com/rswt-rbartlett/cyber-security-framework/blob/main/1-Understand-your-risks/Step-02-Engagement-and-Training.md#security-awareness) of the risks of phishing and malware. 

# Financial Support To Achieve Cyber Essentials

The NCSC announced their [Funded Cyber Essentials Programme](https://www.ncsc.gov.uk/information/funded-cyber-essentials-programme) just before the break, and any Wildlife Trust up to 49 staff may be eligable, if you meet the criteria you you'll receive hands-on support from a Certifying Body (CB) at no cost (though any software or hardware you need to purchase would still need funding).