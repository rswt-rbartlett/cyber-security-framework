<img src="/Levels/twt-logo.png" height="100">

# Implement appropriate mitigations
# Step 8. Data security

## Know what you're protecting
The first step in protecting your data is knowing what data you have, and where it is.  You should already have a record all your personal data in your [Information Asset Register](https://ico.org.uk/for-organisations/accountability-framework/records-management-and-security/#Register) as part of compliance with the UK General Data Protection Regulation (GDPR). To that you need to add your financial, legal and other sensitive or valuable information.  There is no reason why you should not add those non-personal information assets to your register, which means all the information is in one place.  Follow the GPDR principles of data minimisation, the more data you have the more work you have to do to secure it.

## Protect data with encryption
Data should be protected with encryption to prevent unauthorised access or modification in transit (for example when uploading a file to a cloud service) and at rest (when saved on a cloud service, server or your laptop).  If you store data unencrypted and suffer a security breach the Information Commissioners Office is far more likely to levy a fine.  If you encrypt data at rest if someone gains access to the encrypted data it will be impossible to read, and no personal data will be leaked.

> **Note**: All encryption should meet the current US Federal Information Processing Standards (FIPS) 140[^1] standard at the time of reading.  This standard (currently FIPS 140-2 and 140-3 are both valid) is recognised internationally and there is no UK equivalent which supercedes it.

### Encryption in transit
Ensure your servers (if you have any) and cloud services (including Microsoft 365, Google and other web services) protect data in transit using modern encryption technology ('modern' meaning currently in active development and supported by a vendor or community).

To ensure on-premises Microsoft servers and applications only support secure encryption protocols you can employ the [Microsoft Security Baselines](/2-Implement-appropriate-mitigations/Step-5-Architecture-and-configuration.md#reduce-attack-surface). Cloud based services typically only support modern encryption but you should check with the suppliers that this is the case and there are no exceptions.

Whilst you cannot check a web service for FIPS compliance you can check what encryption a service supports using the [Qualys SSL Server Test](https://www.ssllabs.com/ssltest/).  This will give any website a rating from A-F, you should expect an A rating for any service you use.  An explanation of those tests is explained at https://github.com/ssllabs/research/wiki/SSL-Server-Rating-Guide.

For non-web based services (e.g. access to file servers and other storage devices on your own network) you can check whether the services will use insecure encryption using a vulnerability scanner like Nessus Pro, which has a plugin to check for SMB v1 support (which is easily broken and should be disabled on all file servers).  You could also include this in the scope of a [vulnerability scan from RSWT](./Step-6-Vulnerability-management.md#scan-for-vulnerabilities) or a [penetration test](./Step-6-Vulnerability-management.md#conduct-penetration-testing) from a third party.

### Encryption at rest
Ensure your data is protected 'at rest' wherever it is stored.  This includes:
- on end user devices (computers, laptops, tablets and smartphones), 
- on servers (either hosted on your premises, at your IT provider or virtual servers in the cloud), and
- in cloud services and applications (e.g. Microsoft 365, Google Workspace, Amazon S3 etc.)

#### End user device encryption
Most modern devices purchased in the last five years will support encryption by default, though in some cases you will need to turn it on.  See below information about encryption for the most common platforms:
- [Microsoft Windows 10/11](https://support.microsoft.com/en-us/windows/turn-on-device-encryption-0c453637-bc88-5f74-5105-741561aae838)
- [Mac OS](https://support.apple.com/en-gb/HT204837)
- Android devices
	- [Google Pixel and Nexus](https://support.google.com/nexus/answer/2844831?hl=en)
	- [Samsung Galaxy devices protected by Samsung Knox](https://docs.samsungknox.com/admin/whitepaper/kpe/DualDAR.htm) [^2]
- [iOS and iPadOS](https://support.apple.com/en-gb/guide/security/sece3bee0835/web) [^3]

#### Server encryption
- [Microsoft Windows Server](https://learn.microsoft.com/en-us/windows/security/information-protection/bitlocker/bitlocker-how-to-deploy-on-windows-server)
- [Ubuntu Server](https://ubuntu.com/core/docs/uc20/full-disk-encryption)

#### Cloud services and applications
- Cloud services
	- [Microsoft 365](https://learn.microsoft.com/en-us/microsoft-365/compliance/encryption?view=o365-worldwide)
	- [Google Workspace](https://support.google.com/googlecloud/answer/6056693#zippy=%2Cdoes-google-encrypt-my-data-at-rest-within-google-workspace)
- Software as a Service
	- [Breathe HR](https://www.breathehr.com/en-gb/hr-software/security-reliability/security-and-reliability#data-security)
	- [XLedger](https://xledger.com/uk/xledger-security/)
	- Charity CRM, previously ThankQ.  Contact the [Strategic Lead for Information Security](mailto:rbartlett@wildlifetrusts.org) for detailed information.

## Backup your data
The availability and integrity of data cannot be assured without a backup that is held somewhere safe. If you suffer from a ransomware incident (the most likely and most serious security incident) being able to restore all your data quickly from a known working copy is critical.  There are four important steps to implementing data backup, set out below.

1. Decide what to backup.  Use your [record of data assets](../1-Understand-your-risks/Step-3-Asset-management.md#data-assets) to identify where your data is and include that in your backups.  If you want to restore a server which you are responsible for you should backup both the data and the application and operating system files.
2. Decide how frequently to backup your data.  This is important because the frequency of backup determines how much data you could lose.  For example, if you backup every night, if you had a ransomware incident at 5pm the next day, you would lose one day of work.  Your tolerance for data loss determines what is called your Recovery Point Objective, or RPO.
3. Decide how quickly you want to restore your data, which will determine how your backups are configured.  This is called your Recovery Time Objective or RTO.
4. Protect your backup from attackers.  Cyber criminals will try to encrypt backups to increase the pressure on victims to pay to have their stolen or encrypted data returned.  Make sure your backup is held outside your network, somewhere where it cannot be modified or destroyed. This is called immutability of backup.  A good test is whether you can modify your backup; if you can, so can an attacker. 

## Sanitise devices before disposal
Data breaches are sometimes caused by old hardware which still contained organisational data.  When hardware is broken or no longer required,  **before** you dispose of it you should ensure all data has been completely destroyed.  Just deleting the data is not sufficient, you should use a proper data destruction tool, examples of which are below:
- [Microsoft SDelete](https://learn.microsoft.com/en-us/sysinternals/downloads/sdelete) which will securely delete files and directories on Windows and Windows Server.
- [Parted Magic](https://partedmagic.com/store/) which can completely wipe disks including SSD

[^1]: To see if your product meets this standard search for it at https://csrc.nist.gov/Projects/cryptographic-module-validation-program/validated-modules/Search
[^2]: Certain Android devices from Huawei, Vivo, and OPPO can't be encrypted.  Please check the vendor documentation for your devices.
[^3]: Once you enable a passcode on your iPhone or iPad it enables encryption by default.

## Return to [Step 7. Identity and access management](./Step-07-Identity-and-Access-Management.md) or continue to [Step 9. Logging and monitoring](/3-Prepare-for-incidents/Step-09-Logging-and-monitoring.md)