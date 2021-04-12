
# Cring ransomware

The ransomware targets, in particular industrial companies. The attackers use CVE-2018-13379 in Fortinet VPNs to enter the internal network. The threat actor then uses the Mimikatz tool to retrieve administrator credentials.
The attackers then use the Cobaltstrike framework and Powershell for lateral movement. They spread the Cring ransomware.
The ransom demanded is between $100k and $500k.
The victims are mainly located in European countries.

#### OSINT Research :

The ransom notes that were published gives the attackers' email contacts:
- ethernalnightmare@tutanota.com
- poolhackers@tutanota.com
- qkhooks0708@protonmail.com (created on 2020-09-09 at 09:14:01)

This last email address is used for a Twitter account that could not be identified.

In the Kaspersky analysis, it is cited that a threat actor published on November 24, 2020 a list of 6.7Gb containing Fortinet VPNs vulnerable to CVE-2018-13379 (the same vulnerability used by the actors behind Cring).
The alias used to distribute the data is `arendee2018` and `pumpedkicks` (New pseudo : `mont4na`). On the forum we can observe that this actor changed his nickname on August 3, 2020, his former nickname was `usb2007`.
This alias is used by several people, so the search was made for users with the same interests. The username `usb2007` is used on the forums `xda-developers.com`. The user with this nickname indicates that he resides in Pakistan. The nickname is also used on Ebay by a person residing in Germany, and on Pinterest by a person residing in Russia.

#### Sources :

- https://id-ransomware.blogspot.com/2021/01/cring-ransomware.html
- https://pastebin.com/PN2a5mBC
- https://twitter.com/swisscom_csirt/status/1354052879158571008
- https://malpedia.caad.fkie.fraunhofer.de/details/win.cring

#### File hashes :

| Actor who share the IOCs | Type | MD5 | SHA256 | First submission on VT | Link |
| - | - | - | - | - | - |
| [ICS-CERT Kaspersky](https://ics-cert.kaspersky.com/media/Kaspersky-ICS-CERT-Vulnerability-in-Fortigate-VPN-servers-is-exploited-in-Cring-ransomware-attacks-En.pdf) | Cring executable | c5d712f82d5d37bb284acd4468ab3533 |  f7d270ca0f2b4d21830787431f881cd004b2eb102cc3048c6b4d69cb775511c8 |   2020-12-22 03:54:26 | [Virustotal](https://www.virustotal.com/gui/file/f7d270ca0f2b4d21830787431f881cd004b2eb102cc3048c6b4d69cb775511c8) |
| [ICS-CERT Kaspersky](https://ics-cert.kaspersky.com/media/Kaspersky-ICS-CERT-Vulnerability-in-Fortigate-VPN-servers-is-exploited-in-Cring-ransomware-attacks-En.pdf) | Cring executable | 317098d8e21fa4e52c1162fb24ba10ae  |   |   |   |
| [ICS-CERT Kaspersky](https://ics-cert.kaspersky.com/media/Kaspersky-ICS-CERT-Vulnerability-in-Fortigate-VPN-servers-is-exploited-in-Cring-ransomware-attacks-En.pdf) | Downloader script | 44d5c28b36807c69104969f5fed6f63f |   |   |   |
| [SwissCom](https://twitter.com/swisscom_csirt/status/1354052879158571008) | Cring executable | 8d1650e5e02cd1934d21ce57f6f1af34 |  77399701a436c1646f86487fdcae133dd30bc5be  | 2020-12-10 04:24:18 | [Virustotal](https://www.virustotal.com/gui/file/3f14e4691b7429b25ec2950db6677df3a9b278e17f6df067d29aba129a5a7d18/detection) |
| [SwissCom](https://twitter.com/swisscom_csirt/status/1354052879158571008) | Cobaltstrike | 8d156725c6ce172b59a8d3c92434c352 |  0b9aa3787d62268f14d7533e93e7baa8dbdc7beaf6b53aa54e722950a5e40b13  |  2020-12-10 04:22:35  | [Virustotal](https://www.virustotal.com/gui/file/0b9aa3787d62268f14d7533e93e7baa8dbdc7beaf6b53aa54e722950a5e40b13/details) |
| [SwissCom](https://twitter.com/swisscom_csirt/status/1354052879158571008) | Mimikatz | 38217fa569df8f93434959c1c798b29d |   1a41c18bbdef02b4e182705c2c9e4471010db7e77c40ed752197f48a8cf150ba   |  2020-12-10 04:25:27  | [Virustotal](https://www.virustotal.com/gui/file/1a41c18bbdef02b4e182705c2c9e4471010db7e77c40ed752197f48a8cf150ba/details) |
| [SwissCom](https://twitter.com/swisscom_csirt/status/1354052879158571008) | Cring executable | d8415a528df5eefcb3ed6f1a79746f40 |  21c04b9ed17c4f831b64a659bc530502f6931865cf7ad1db45b78629ec809e7e  |  2020-12-08 08:57:53  | [Virustotal](https://www.virustotal.com/gui/file/21c04b9ed17c4f831b64a659bc530502f6931865cf7ad1db45b78629ec809e7e/details) |

#### URLs :
- www.mircoupdate.https443.net

#### IP addresses :
- 129.227.156.216
- 129.227.156.214
- 198.12.112.204
- 45.67.231.128
- 45.142.213.40

A set of YARA rules is available [here](https://github.com/reversinglabs/reversinglabs-yara-rules/blob/develop/yara/ransomware/Win32.Ransomware.Cring.yara)
