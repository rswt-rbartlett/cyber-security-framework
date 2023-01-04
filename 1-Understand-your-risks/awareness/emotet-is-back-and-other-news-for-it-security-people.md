# Emotet is back
- After being shut down in 2021 when a multinational law enforcement operation took control of the servers, Emotet is back again.  Expect to more XLS malware either as direct .XLS attachments (Note: NOT .xlsx files, they're using a legacy file extension), or as password protected zip files. See https://www.bleepingcomputer.com/news/security/emotet-botnet-starts-blasting-malware-again-after-4-month-break/ for commentary and technical write-up.

**Recommendation**: Block .xls and password protected zip files and encourage colleagues to use OneDrive or Google Drive file sharing options rather than sending files via email.

# Openssl bug wasn't a big deal
There was quite a lot of noise about the OpenSSL vulnerability which was initially rated as Critical but then downrated to High.  See https://www.malwaretech.com/2022/11/everything-you-need-to-know-about-the-openssl-3-0-7-patch.html for a write up.

**Recommendation**: read the write-up and check the NCSC-NL list of vulnerable/not-vulnerable/fixed products at https://github.com/NCSC-NL/OpenSSL-2022/blob/main/software/README.md

# Draytek router exploit
There's an remote commend execution exploit for Draytek routers being sold on the dark web.  See https://www.draytek.com/about/security-advisory/draytek-router-unauthenticated-remote-code-execution-vulnerability-%28cve-2022-32548%29/ for list of vulnerable devices.

**Recommendation**: patch your routers!