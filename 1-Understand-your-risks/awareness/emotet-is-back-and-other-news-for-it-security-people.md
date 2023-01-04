<img src="/Levels/twt-logo.png" height="100">

# Emotet is back
After being shut down in 2021 when a multinational law enforcement operation took control of the servers, Emotet is back again.  Expect to see more XLS malware either as direct .XLS attachments (Note: NOT .xlsx files, they're using a legacy file extension), or as password protected zip files. Bleeping Computer has a good [commentary and technical write-up](https://www.bleepingcomputer.com/news/security/emotet-botnet-starts-blasting-malware-again-after-4-month-break/).

**Recommendation**: Block .xls and password protected zip files and encourage colleagues to use OneDrive or Google Drive file sharing options rather than sending files via email.

# OpenSSL bug wasn't a big deal
There was quite a lot of noise about the OpenSSL vulnerability which was initially rated as Critical but then downrated to High.  Marcus Hutchings (the security researcher famous for stopping the NHS WannaCry attack) has done a good [write up](https://www.malwaretech.com/2022/11/everything-you-need-to-know-about-the-openssl-3-0-7-patch.html).

**Recommendation**: read the write-up and check the NCSC-NL list of vulnerable/not-vulnerable/fixed products at https://github.com/NCSC-NL/OpenSSL-2022/blob/main/software/README.md

# Draytek router exploit
There's an remote commend execution exploit for Draytek routers being sold on the dark web.  Draytek have provided a [list of vulnerable devices](https://www.draytek.com/about/security-advisory/draytek-router-unauthenticated-remote-code-execution-vulnerability-%28cve-2022-32548%29/).

**Recommendation**: patch your routers!