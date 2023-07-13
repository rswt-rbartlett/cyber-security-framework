<img src="/Levels/twt-logo.png" height="100">

# Urgent Security Notice for SonicWall GMS/Analytics
Yesterday (12th July) SonicWall issued an Urgent Security Notice for SonicWall GMS/Analytics and as I know Yorkshire has SonicWall firewalls I just wanted to make sure you were aware.  This is a suite of vulnerabilities including four which are Critical (e.g. CVE-2023-34124 Web Service Authentication Bypass and CVE-2023-34134 Password Hash Read via Web Service).

There's currently no evidence of exploitation of this in the wild, but I expect that to change. The gap between patches being released and reverse engineered by criminals to make an exploit is measured in days rather than weeks (in 2020 Mandiant reported that 12% of exploits were developed within a week of the patch and 27% developed within a month).
**Recommendation**: If you have Zyxel devices in any of your offices make sure they're up to date. If your staff use an affected Zyxel device at home, urge them to update as soon as possible.  Patches can be found at the Zyxel [download library](https://www.zyxel.com/global/en/support/download?model=).

