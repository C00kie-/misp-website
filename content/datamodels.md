---
layout: page
title: MISP data models - MISP core format - MISP taxonomies
permalink: /datamodels/
toc: true
---

MISP is not only a software but also a series of data models created by the MISP community. MISP includes a simple and practical information sharing format expressed in JSON that can be used with MISP software or by any other software. The MISP formats are now standards handled by the [MISP standard body](https://www.misp-standard.org).

## MISP Core Format

The MISP core format is a simple JSON format used by MISP and other tools to exchange events and attributes. The JSON schema 2.4 is described on the MISP core software and many sample files are available in the OSINT feed.

The MISP format is described as Internet-Draft in [misp-rfc](https://github.com/MISP/MISP-rfc). The MISP format are described to support the developer or organisation willing to build your own tool supporting the MISP format (as import or export). The standard is built from practical use-cases and the implementation references within the MISP project. The standard is quickly evolving following the MISP implementation.

### MISP default attributes and categories

### Attribute Categories vs. Types

|Category| Antivirus detection | Artifacts dropped | Attribution | External analysis | Financial fraud | Internal reference |
| --- |:---:|:---:|:---:|:---:|:---:|:---:|
|AS| | | | X | | |
|aba-rtn| | | | | X | |
|anonymised| X | X | X | X | X | X |
|attachment| X | X | | X | | |
|authentihash| | X | | | | |
|azure-application-id| | | | | | |
|bank-account-nr| | | | | X | |
|bic| | | | | X | |
|bin| | | | | X | |
|boolean| | | | | | |
|bro| | | | X | | |
|btc| | | | | X | |
|campaign-id| | | X | | | |
|campaign-name| | | X | | | |
|cc-number| | | | | X | |
|cdhash| | X | | | | |
|chrome-extension-id| | | | | | |
|comment| X | X | X | X | X | X |
|community-id| | | | X | | |
|cookie| | X | | | | |
|cortex| | | | X | | |
|counter| | | | | | |
|country-of-residence| | | | | | |
|cpe| | | | X | | |
|dash| | | | | X | |
|date-of-birth| | | | | | |
|datetime| | | | | | |
|dkim| | | | | | |
|dkim-signature| | | | | | |
|dns-soa-email| | | X | | | |
|domain| | | | X | | |
|domain&#124;ip| | | | X | | |
|email| | | X | | | |
|email-attachment| | | | | | |
|email-body| | | | | | |
|email-dst| | | | | | |
|email-dst-display-name| | | | | | |
|email-header| | | | | | |
|email-message-id| | | | | | |
|email-mime-boundary| | | | | | |
|email-reply-to| | | | | | |
|email-src| | | | | | |
|email-src-display-name| | | | | | |
|email-subject| | | | | | |
|email-thread-index| | | | | | |
|email-x-mailer| | | | | | |
|eppn| | | | | | |
|favicon-mmh3| | | | | | |
|filename| | X | | X | | |
|filename-pattern| | X | | X | | |
|filename&#124;authentihash| | X | | | | |
|filename&#124;impfuzzy| | X | | | | |
|filename&#124;imphash| | X | | | | |
|filename&#124;md5| | X | | X | | |
|filename&#124;pehash| | X | | | | |
|filename&#124;sha1| | X | | X | | |
|filename&#124;sha224| | X | | | | |
|filename&#124;sha256| | X | | X | | |
|filename&#124;sha3-224| | X | | X | | |
|filename&#124;sha3-256| | X | | X | | |
|filename&#124;sha3-384| | X | | X | | |
|filename&#124;sha3-512| | X | | X | | |
|filename&#124;sha384| | X | | | | |
|filename&#124;sha512| | X | | | | |
|filename&#124;sha512/224| | X | | | | |
|filename&#124;sha512/256| | X | | | | |
|filename&#124;ssdeep| | X | | | | |
|filename&#124;tlsh| | X | | | | |
|filename&#124;vhash| | X | | | | |
|first-name| | | | | | |
|float| | | | | | |
|frequent-flyer-number| | | | | | |
|full-name| | | | | | |
|gender| | | | | | |
|gene| | X | | | | |
|git-commit-id| | | | | | X |
|github-organisation| | | | | | |
|github-repository| | | | X | | |
|github-username| | | | | | |
|hassh-md5| | | | X | | |
|hasshserver-md5| | | | X | | |
|hex| X | X | | | X | X |
|hostname| | | | X | | |
|hostname&#124;port| | | | | | |
|http-method| | | | | | |
|iban| | | | | X | |
|identity-card-number| | | | | | |
|impfuzzy| | X | | | | |
|imphash| | X | | | | |
|ip-dst| | | | X | | |
|ip-dst&#124;port| | | | X | | |
|ip-src| | | | X | | |
|ip-src&#124;port| | | | X | | |
|issue-date-of-the-visa| | | | | | |
|ja3-fingerprint-md5| | | | X | | |
|jabber-id| | | | | | |
|jarm-fingerprint| | | | X | | |
|kusto-query| | X | | | | |
|last-name| | | | | | |
|link| X | | | X | | X |
|mac-address| | | | X | | |
|mac-eui-64| | | | X | | |
|malware-sample| | X | | X | | |
|malware-type| | | | | | |
|md5| | X | | X | | |
|middle-name| | | | | | |
|mime-type| | X | | | | |
|mobile-application-id| | | | | | |
|mutex| | X | | | | |
|named pipe| | X | | | | |
|nationality| | | | | | |
|other| X | X | X | X | X | X |
|passenger-name-record-locator-number| | | | | | |
|passport-country| | | | | | |
|passport-expiration| | | | | | |
|passport-number| | | | | | |
|pattern-in-file| | X | | X | | |
|pattern-in-memory| | X | | X | | |
|pattern-in-traffic| | | | X | | |
|payment-details| | | | | | |
|pdb| | X | | | | |
|pehash| | | | | | |
|pgp-private-key| | X | | | | |
|pgp-public-key| | X | | | | |
|phone-number| | | | | X | |
|place-of-birth| | | | | | |
|place-port-of-clearance| | | | | | |
|place-port-of-onward-foreign-destination| | | | | | |
|place-port-of-original-embarkation| | | | | | |
|port| | | | | | |
|primary-residence| | | | | | |
|process-state| | X | | | | |
|prtn| | | | | X | |
|redress-number| | | | | | |
|regkey| | X | | X | | |
|regkey&#124;value| | X | | X | | |
|sha1| | X | | X | | |
|sha224| | X | | | | |
|sha256| | X | | X | | |
|sha3-224| | X | | X | | |
|sha3-256| | X | | X | | |
|sha3-384| | X | | X | | |
|sha3-512| | X | | X | | |
|sha384| | X | | | | |
|sha512| | X | | | | |
|sha512/224| | X | | | | |
|sha512/256| | X | | | | |
|sigma| | X | | | | |
|size-in-bytes| | | | | | |
|snort| | | | X | | |
|special-service-request| | | | | | |
|ssdeep| | X | | | | |
|ssh-fingerprint| | | | | | |
|stix2-pattern| | X | | | | |
|target-email| | | | | | |
|target-external| | | | | | |
|target-location| | | | | | |
|target-machine| | | | | | |
|target-org| | | | | | |
|target-user| | | | | | |
|telfhash| | X | | | | |
|text| X | X | X | X | X | X |
|threat-actor| | | X | | | |
|tlsh| | | | | | |
|travel-details| | | | | | |
|twitter-id| | | | | | |
|uri| | | | | | |
|url| | | | X | | |
|user-agent| | | | X | | |
|vhash| | X | | | | |
|visa-number| | | | | | |
|vulnerability| | | | X | | |
|weakness| | | | X | | |
|whois-creation-date| | | X | | | |
|whois-registrant-email| | | X | | | |
|whois-registrant-name| | | X | | | |
|whois-registrant-org| | | X | | | |
|whois-registrant-phone| | | X | | | |
|whois-registrar| | | X | | | |
|windows-scheduled-task| | X | | | | |
|windows-service-displayname| | X | | | | |
|windows-service-name| | X | | | | |
|x509-fingerprint-md5| | X | X | X | | |
|x509-fingerprint-sha1| | X | X | X | | |
|x509-fingerprint-sha256| | X | X | X | | |
|xmr| | | | | X | |
|yara| | X | | | | |
|zeek| | | | X | | |

|Category| Network activity | Other | Payload delivery | Payload installation | Payload type | Persistence mechanism |
| --- |:---:|:---:|:---:|:---:|:---:|:---:|
|AS| X | | X | | | |
|aba-rtn| | | | | | |
|anonymised| X | X | X | X | X | X |
|attachment| X | | X | X | | |
|authentihash| | | X | X | | |
|azure-application-id| | | X | X | | |
|bank-account-nr| | | | | | |
|bic| | | | | | |
|bin| | | | | | |
|boolean| | X | | | | |
|bro| X | | | | | |
|btc| | | | | | |
|campaign-id| | | | | | |
|campaign-name| | | | | | |
|cc-number| | | | | | |
|cdhash| | | X | X | | |
|chrome-extension-id| | | X | X | | |
|comment| X | X | X | X | X | X |
|community-id| X | | | | | |
|cookie| X | | | | | |
|cortex| | | | | | |
|counter| | X | | | | |
|country-of-residence| | | | | | |
|cpe| | X | X | X | | |
|dash| | | | | | |
|date-of-birth| | | | | | |
|datetime| | X | | | | |
|dkim| X | | | | | |
|dkim-signature| X | | | | | |
|dns-soa-email| | | | | | |
|domain| X | | X | | | |
|domain&#124;ip| X | | | | | |
|email| X | | X | | | |
|email-attachment| | | X | | | |
|email-body| | | X | | | |
|email-dst| X | | X | | | |
|email-dst-display-name| | | X | | | |
|email-header| | | X | | | |
|email-message-id| | | X | | | |
|email-mime-boundary| | | X | | | |
|email-reply-to| | | X | | | |
|email-src| X | | X | | | |
|email-src-display-name| | | X | | | |
|email-subject| X | | X | | | |
|email-thread-index| | | X | | | |
|email-x-mailer| | | X | | | |
|eppn| X | | | | | |
|favicon-mmh3| X | | | | | |
|filename| | | X | X | | X |
|filename-pattern| X | | X | X | | |
|filename&#124;authentihash| | | X | X | | |
|filename&#124;impfuzzy| | | X | X | | |
|filename&#124;imphash| | | X | X | | |
|filename&#124;md5| | | X | X | | |
|filename&#124;pehash| | | X | X | | |
|filename&#124;sha1| | | X | X | | |
|filename&#124;sha224| | | X | X | | |
|filename&#124;sha256| | | X | X | | |
|filename&#124;sha3-224| | | X | X | | |
|filename&#124;sha3-256| | | X | X | | |
|filename&#124;sha3-384| | | X | X | | |
|filename&#124;sha3-512| | | X | X | | |
|filename&#124;sha384| | | X | X | | |
|filename&#124;sha512| | | X | X | | |
|filename&#124;sha512/224| | | X | X | | |
|filename&#124;sha512/256| | | X | X | | |
|filename&#124;ssdeep| | | X | X | | |
|filename&#124;tlsh| | | X | X | | |
|filename&#124;vhash| | | X | X | | |
|first-name| | | | | | |
|float| | X | | | | |
|frequent-flyer-number| | | | | | |
|full-name| | | | | | |
|gender| | | | | | |
|gene| | | | | | |
|git-commit-id| | | | | | |
|github-organisation| | | | | | |
|github-repository| | | | | | |
|github-username| | | | | | |
|hassh-md5| X | | X | | | |
|hasshserver-md5| X | | X | | | |
|hex| X | X | X | X | | X |
|hostname| X | | X | | | |
|hostname&#124;port| X | | X | | | |
|http-method| X | | | | | |
|iban| | | | | | |
|identity-card-number| | | | | | |
|impfuzzy| | | X | X | | |
|imphash| | | X | X | | |
|ip-dst| X | | X | | | |
|ip-dst&#124;port| X | | X | | | |
|ip-src| X | | X | | | |
|ip-src&#124;port| X | | X | | | |
|issue-date-of-the-visa| | | | | | |
|ja3-fingerprint-md5| X | | X | | | |
|jabber-id| | | | | | |
|jarm-fingerprint| X | | X | | | |
|kusto-query| | | | | | |
|last-name| | | | | | |
|link| | | X | | | |
|mac-address| X | | X | | | |
|mac-eui-64| X | | X | | | |
|malware-sample| | | X | X | | |
|malware-type| | | X | X | | |
|md5| | | X | X | | |
|middle-name| | | | | | |
|mime-type| | | X | X | | |
|mobile-application-id| | | X | X | | |
|mutex| | | | | | |
|named pipe| | | | | | |
|nationality| | | | | | |
|other| X | X | X | X | X | X |
|passenger-name-record-locator-number| | | | | | |
|passport-country| | | | | | |
|passport-expiration| | | | | | |
|passport-number| | | | | | |
|pattern-in-file| X | | X | X | | |
|pattern-in-memory| | | | X | | |
|pattern-in-traffic| X | | X | X | | |
|payment-details| | | | | | |
|pdb| | | | | | |
|pehash| | | X | X | | |
|pgp-private-key| | X | | | | |
|pgp-public-key| | X | | | | |
|phone-number| | X | | | | |
|place-of-birth| | | | | | |
|place-port-of-clearance| | | | | | |
|place-port-of-onward-foreign-destination| | | | | | |
|place-port-of-original-embarkation| | | | | | |
|port| X | X | | | | |
|primary-residence| | | | | | |
|process-state| | | | | | |
|prtn| | | | | | |
|redress-number| | | | | | |
|regkey| | | | | | X |
|regkey&#124;value| | | | | | X |
|sha1| | | X | X | | |
|sha224| | | X | X | | |
|sha256| | | X | X | | |
|sha3-224| | | X | X | | |
|sha3-256| | | X | X | | |
|sha3-384| | | X | X | | |
|sha3-512| | | X | X | | |
|sha384| | | X | X | | |
|sha512| | | X | X | | |
|sha512/224| | | X | X | | |
|sha512/256| | | X | X | | |
|sigma| | | X | X | | |
|size-in-bytes| | X | | | | |
|snort| X | | | | | |
|special-service-request| | | | | | |
|ssdeep| | | X | X | | |
|ssh-fingerprint| X | | | | | |
|stix2-pattern| X | | X | X | | |
|target-email| | | | | | |
|target-external| | | | | | |
|target-location| | | | | | |
|target-machine| | | | | | |
|target-org| | | | | | |
|target-user| | | | | | |
|telfhash| | | X | X | | |
|text| X | X | X | X | X | X |
|threat-actor| | | | | | |
|tlsh| | | X | X | | |
|travel-details| | | | | | |
|twitter-id| | | | | | |
|uri| X | | | | | |
|url| X | | X | | | |
|user-agent| X | | X | | | |
|vhash| | | X | X | | |
|visa-number| | | | | | |
|vulnerability| | | X | X | | |
|weakness| | | X | X | | |
|whois-creation-date| | | | | | |
|whois-registrant-email| | | X | | | |
|whois-registrant-name| | | | | | |
|whois-registrant-org| | | | | | |
|whois-registrant-phone| | | | | | |
|whois-registrar| | | | | | |
|windows-scheduled-task| | | | | | |
|windows-service-displayname| | | | | | |
|windows-service-name| | | | | | |
|x509-fingerprint-md5| X | | X | X | | |
|x509-fingerprint-sha1| X | | X | X | | |
|x509-fingerprint-sha256| X | | X | X | | |
|xmr| | | | | | |
|yara| | | X | X | | |
|zeek| X | | | | | |

|Category| Person | Social network | Support Tool | Targeting data |
| --- |:---:|:---:|:---:|:---:|
|AS| | | | |
|aba-rtn| | | | |
|anonymised| X | X | X | X |
|attachment| | | X | |
|authentihash| | | | |
|azure-application-id| | | | |
|bank-account-nr| | | | |
|bic| | | | |
|bin| | | | |
|boolean| | | | |
|bro| | | | |
|btc| | | | |
|campaign-id| | | | |
|campaign-name| | | | |
|cc-number| | | | |
|cdhash| | | | |
|chrome-extension-id| | | | |
|comment| X | X | X | X |
|community-id| | | | |
|cookie| | | | |
|cortex| | | | |
|counter| | | | |
|country-of-residence| X | | | |
|cpe| | | | |
|dash| | | | |
|date-of-birth| X | | | |
|datetime| | | | |
|dkim| | | | |
|dkim-signature| | | | |
|dns-soa-email| | | | |
|domain| | | | |
|domain&#124;ip| | | | |
|email| X | X | | |
|email-attachment| | | | |
|email-body| | | | |
|email-dst| | X | | |
|email-dst-display-name| | | | |
|email-header| | | | |
|email-message-id| | | | |
|email-mime-boundary| | | | |
|email-reply-to| | | | |
|email-src| | X | | |
|email-src-display-name| | | | |
|email-subject| | | | |
|email-thread-index| | | | |
|email-x-mailer| | | | |
|eppn| | X | | |
|favicon-mmh3| | | | |
|filename| | | | |
|filename-pattern| | | | |
|filename&#124;authentihash| | | | |
|filename&#124;impfuzzy| | | | |
|filename&#124;imphash| | | | |
|filename&#124;md5| | | | |
|filename&#124;pehash| | | | |
|filename&#124;sha1| | | | |
|filename&#124;sha224| | | | |
|filename&#124;sha256| | | | |
|filename&#124;sha3-224| | | | |
|filename&#124;sha3-256| | | | |
|filename&#124;sha3-384| | | | |
|filename&#124;sha3-512| | | | |
|filename&#124;sha384| | | | |
|filename&#124;sha512| | | | |
|filename&#124;sha512/224| | | | |
|filename&#124;sha512/256| | | | |
|filename&#124;ssdeep| | | | |
|filename&#124;tlsh| | | | |
|filename&#124;vhash| | | | |
|first-name| X | | | |
|float| | | | |
|frequent-flyer-number| X | | | |
|full-name| X | | | |
|gender| X | | | |
|gene| | | | |
|git-commit-id| | | | |
|github-organisation| | X | | |
|github-repository| | X | | |
|github-username| | X | | |
|hassh-md5| | | | |
|hasshserver-md5| | | | |
|hex| | | X | |
|hostname| | | | |
|hostname&#124;port| | | | |
|http-method| | | | |
|iban| | | | |
|identity-card-number| X | | | |
|impfuzzy| | | | |
|imphash| | | | |
|ip-dst| | | | |
|ip-dst&#124;port| | | | |
|ip-src| | | | |
|ip-src&#124;port| | | | |
|issue-date-of-the-visa| X | | | |
|ja3-fingerprint-md5| | | | |
|jabber-id| | X | | |
|jarm-fingerprint| | | | |
|kusto-query| | | | |
|last-name| X | | | |
|link| | | X | |
|mac-address| | | | |
|mac-eui-64| | | | |
|malware-sample| | | | |
|malware-type| | | | |
|md5| | | | |
|middle-name| X | | | |
|mime-type| | | | |
|mobile-application-id| | | | |
|mutex| | | | |
|named pipe| | | | |
|nationality| X | | | |
|other| X | X | X | |
|passenger-name-record-locator-number| X | | | |
|passport-country| X | | | |
|passport-expiration| X | | | |
|passport-number| X | | | |
|pattern-in-file| | | | |
|pattern-in-memory| | | | |
|pattern-in-traffic| | | | |
|payment-details| X | | | |
|pdb| | | | |
|pehash| | | | |
|pgp-private-key| X | X | | |
|pgp-public-key| X | X | | |
|phone-number| X | | | |
|place-of-birth| X | | | |
|place-port-of-clearance| X | | | |
|place-port-of-onward-foreign-destination| X | | | |
|place-port-of-original-embarkation| X | | | |
|port| | | | |
|primary-residence| X | | | |
|process-state| | | | |
|prtn| | | | |
|redress-number| X | | | |
|regkey| | | | |
|regkey&#124;value| | | | |
|sha1| | | | |
|sha224| | | | |
|sha256| | | | |
|sha3-224| | | | |
|sha3-256| | | | |
|sha3-384| | | | |
|sha3-512| | | | |
|sha384| | | | |
|sha512| | | | |
|sha512/224| | | | |
|sha512/256| | | | |
|sigma| | | | |
|size-in-bytes| | | | |
|snort| | | | |
|special-service-request| X | | | |
|ssdeep| | | | |
|ssh-fingerprint| | | | |
|stix2-pattern| | | | |
|target-email| | | | X |
|target-external| | | | X |
|target-location| | | | X |
|target-machine| | | | X |
|target-org| | | | X |
|target-user| | | | X |
|telfhash| | | | |
|text| X | X | X | |
|threat-actor| | | | |
|tlsh| | | | |
|travel-details| X | | | |
|twitter-id| | X | | |
|uri| | | | |
|url| | | | |
|user-agent| | | | |
|vhash| | | | |
|visa-number| X | | | |
|vulnerability| | | | |
|weakness| | | | |
|whois-creation-date| | | | |
|whois-registrant-email| | X | | |
|whois-registrant-name| | | | |
|whois-registrant-org| | | | |
|whois-registrant-phone| | | | |
|whois-registrar| | | | |
|windows-scheduled-task| | | | |
|windows-service-displayname| | | | |
|windows-service-name| | | | |
|x509-fingerprint-md5| | | | |
|x509-fingerprint-sha1| | | | |
|x509-fingerprint-sha256| | | | |
|xmr| | | | |
|yara| | | | |
|zeek| | | | |


### Categories

*   **Antivirus detection**: All the info about how the malware is detected by the antivirus products
*   **Artifacts dropped**: Any artifact (files, registry keys etc.) dropped by the malware or other modifications to the system
*   **Attribution**: Identification of the group, organisation, or country behind the attack
*   **External analysis**: Any other result from additional analysis of the malware like tools output
*   **Financial fraud**: Financial Fraud indicators
*   **Internal reference**: Reference used by the publishing party (e.g. ticket number)
*   **Network activity**: Information about network traffic generated by the malware
*   **Other**: Attributes that are not part of any other category or are meant to be used as a component in MISP objects in the future
*   **Payload delivery**: Information about how the malware is delivered
*   **Payload installation**: Info on where the malware gets installed in the system
*   **Payload type**: Information about the final payload(s)
*   **Persistence mechanism**: Mechanisms used by the malware to start at boot
*   **Person**: A human being - natural person
*   **Social network**: Social networks and platforms
*   **Support Tool**: Tools supporting analysis or detection of the event
*   **Targeting data**: Internal Attack Targeting and Compromise Information

### Types

*   **AS**: Autonomous system
*   **aba-rtn**: ABA routing transit number
*   **anonymised**: Anonymised value - described with the anonymisation object via a relationship
*   **attachment**: Attachment with external information
*   **authentihash**: Authenticode executable signature hash
*   **azure-application-id**: Azure Application ID.
*   **bank-account-nr**: Bank account number without any routing number
*   **bic**: Bank Identifier Code Number also known as SWIFT-BIC, SWIFT code or ISO 9362 code
*   **bin**: Bank Identification Number
*   **boolean**: Boolean value - to be used in objects
*   **bro**: An NIDS rule in the Bro rule-format
*   **btc**: Bitcoin Address
*   **campaign-id**: Associated campaign ID
*   **campaign-name**: Associated campaign name
*   **cc-number**: Credit-Card Number
*   **cdhash**: An Apple Code Directory Hash, identifying a code-signed Mach-O executable file
*   **chrome-extension-id**: Chrome extension id
*   **comment**: Comment or description in a human language
*   **community-id**: A community ID flow hashing algorithm to map multiple traffic monitors into common flow id
*   **cookie**: HTTP cookie as often stored on the user web client. This can include authentication cookie or session cookie.
*   **cortex**: Cortex analysis result
*   **counter**: An integer counter, generally to be used in objects
*   **country-of-residence**: The country of residence of a natural person
*   **cpe**: Common Platform Enumeration - structured naming scheme for information technology systems, software, and packages.
*   **dash**: Dash Address
*   **date-of-birth**: Date of birth of a natural person (in YYYY-MM-DD format)
*   **datetime**: Datetime in the ISO 8601 format
*   **dkim**: DKIM public key
*   **dkim-signature**: DKIM signature
*   **dns-soa-email**: RFC 1035 mandates that DNS zones should have a SOA (Statement Of Authority) record that contains an email address where a PoC for the domain could be contacted. This can sometimes be used for attribution/linkage between different domains even if protected by whois privacy
*   **domain**: A domain name used in the malware
*   **domain&#124;ip**: A domain name and its IP address (as found in DNS lookup) separated by a &#124;
*   **email**: An email address
*   **email-attachment**: File name of the email attachment.
*   **email-body**: Email body
*   **email-dst**: The destination email address. Used to describe the recipient when describing an e-mail.
*   **email-dst-display-name**: Email destination display name
*   **email-header**: Email header
*   **email-message-id**: The email message ID
*   **email-mime-boundary**: The email mime boundary separating parts in a multipart email
*   **email-reply-to**: Email reply to header
*   **email-src**: The source email address. Used to describe the sender when describing an e-mail.
*   **email-src-display-name**: Email source display name
*   **email-subject**: The subject of the email
*   **email-thread-index**: The email thread index header
*   **email-x-mailer**: Email x-mailer header
*   **eppn**: eduPersonPrincipalName - eppn - the NetId of the person for the purposes of inter-institutional authentication. Should be stored in the form of user@univ.edu, where univ.edu is the name of the local security domain.
*   **favicon-mmh3**: favicon-mmh3 is the murmur3 hash of a favicon as used in Shodan.
*   **filename**: Filename
*   **filename-pattern**: A pattern in the name of a file
*   **filename&#124;authentihash**: A filename and Authenticode executable signature hash
*   **filename&#124;impfuzzy**: Import fuzzy hash - a fuzzy hash created based on the imports in the sample.
*   **filename&#124;imphash**: Import hash - a hash created based on the imports in the sample.
*   **filename&#124;md5**: A filename and an MD5 hash separated by a &#124;
*   **filename&#124;pehash**: A filename and a peHash separated by a &#124;
*   **filename&#124;sha1**: A filename and an SHA1 hash separated by a &#124;
*   **filename&#124;sha224**: A filename and a SHA-224 hash separated by a &#124;
*   **filename&#124;sha256**: A filename and an SHA256 hash separated by a &#124;
*   **filename&#124;sha3-224**: A filename and an SHA3-224 hash separated by a &#124;
*   **filename&#124;sha3-256**: A filename and an SHA3-256 hash separated by a &#124;
*   **filename&#124;sha3-384**: A filename and an SHA3-384 hash separated by a &#124;
*   **filename&#124;sha3-512**: A filename and an SHA3-512 hash separated by a &#124;
*   **filename&#124;sha384**: A filename and a SHA-384 hash separated by a &#124;
*   **filename&#124;sha512**: A filename and a SHA-512 hash separated by a &#124;
*   **filename&#124;sha512/224**: A filename and a SHa-512/224 hash separated by a &#124;
*   **filename&#124;sha512/256**: A filename and a SHA-512/256 hash separated by a &#124;
*   **filename&#124;ssdeep**: A checksum in ssdeep format
*   **filename&#124;tlsh**: A filename and a Trend Micro Locality Sensitive Hash separated by a &#124;
*   **filename&#124;vhash**: A filename and a VirusTotal hash separated by a &#124;
*   **first-name**: First name of a natural person
*   **float**: A floating point value.
*   **frequent-flyer-number**: The frequent flyer number of a passenger
*   **full-name**: Full name of a natural person
*   **gender**: The gender of a natural person (Male, Female, Other, Prefer not to say)
*   **gene**: GENE - Go Evtx sigNature Engine
*   **git-commit-id**: A Git commit ID.
*   **github-organisation**: A GitHub organisation
*   **github-repository**: A Github repository
*   **github-username**: A GitHub user name
*   **hassh-md5**: hassh is a network fingerprinting standard which can be used to identify specific Client SSH implementations. The fingerprints can be easily stored, searched and shared in the form of an MD5 fingerprint.
*   **hasshserver-md5**: hasshServer is a network fingerprinting standard which can be used to identify specific Server SSH implementations. The fingerprints can be easily stored, searched and shared in the form of an MD5 fingerprint.
*   **hex**: A value in hexadecimal format
*   **hostname**: A full host/dnsname of an attacker
*   **hostname&#124;port**: Hostname and port number separated by a &#124;
*   **http-method**: HTTP method used by the malware (e.g. POST, GET, ...).
*   **iban**: International Bank Account Number
*   **identity-card-number**: Identity card number
*   **impfuzzy**: A fuzzy hash of import table of Portable Executable format
*   **imphash**: Import hash - a hash created based on the imports in the sample.
*   **ip-dst**: A destination IP address of the attacker or C&C server
*   **ip-dst&#124;port**: IP destination and port number separated by a &#124;
*   **ip-src**: A source IP address of the attacker
*   **ip-src&#124;port**: IP source and port number separated by a &#124;
*   **issue-date-of-the-visa**: The date on which the visa was issued
*   **ja3-fingerprint-md5**: JA3 is a method for creating SSL/TLS client fingerprints that should be easy to produce on any platform and can be easily shared for threat intelligence.
*   **jabber-id**: Jabber ID
*   **jarm-fingerprint**: JARM is a method for creating SSL/TLS server fingerprints.
*   **kusto-query**: Kusto query - Kusto from Microsoft Azure is a service for storing and running interactive analytics over Big Data.
*   **last-name**: Last name of a natural person
*   **link**: Link to an external information
*   **mac-address**: MAC address
*   **mac-eui-64**: MAC EUI-64 address
*   **malware-sample**: Attachment containing encrypted malware sample
*   **malware-type**: 
*   **md5**: A checksum in MD5 format
*   **middle-name**: Middle name of a natural person
*   **mime-type**: A media type (also MIME type and content type) is a two-part identifier for file formats and format contents transmitted on the Internet
*   **mobile-application-id**: The application id of a mobile application
*   **mutex**: Mutex, use the format \BaseNamedObjects\<Mutex>
*   **named pipe**: Named pipe, use the format \.\pipe\<PipeName>
*   **nationality**: The nationality of a natural person
*   **other**: Other attribute
*   **passenger-name-record-locator-number**: The Passenger Name Record Locator is a key under which the reservation for a trip is stored in the system. The PNR contains, among other data, the name, flight segments and address of the passenger. It is defined by a combination of five or six letters and numbers.
*   **passport-country**: The country in which the passport was issued
*   **passport-expiration**: The expiration date of a passport
*   **passport-number**: The passport number of a natural person
*   **pattern-in-file**: Pattern in file that identifies the malware
*   **pattern-in-memory**: Pattern in memory dump that identifies the malware
*   **pattern-in-traffic**: Pattern in network traffic that identifies the malware
*   **payment-details**: Payment details
*   **pdb**: Microsoft Program database (PDB) path information
*   **pehash**: peHash - a hash calculated based of certain pieces of a PE executable file
*   **pgp-private-key**: A PGP private key
*   **pgp-public-key**: A PGP public key
*   **phone-number**: Telephone Number
*   **place-of-birth**: Place of birth of a natural person
*   **place-port-of-clearance**: The port of clearance
*   **place-port-of-onward-foreign-destination**: A Port where the passenger is transiting to
*   **place-port-of-original-embarkation**: The original port of embarkation
*   **port**: Port number
*   **primary-residence**: The primary residence of a natural person
*   **process-state**: State of a process
*   **prtn**: Premium-Rate Telephone Number
*   **redress-number**: The Redress Control Number is the record identifier for people who apply for redress through the DHS Travel Redress Inquiry Program (DHS TRIP). DHS TRIP is for travelers who have been repeatedly identified for additional screening and who want to file an inquiry to have erroneous information corrected in DHS systems
*   **regkey**: Registry key or value
*   **regkey&#124;value**: Registry value + data separated by &#124;
*   **sha1**: A checksum in SHA1 format
*   **sha224**: A checksum in SHA-224 format
*   **sha256**: A checksum in SHA256 format
*   **sha3-224**: A checksum in SHA3-224 format
*   **sha3-256**: A checksum in SHA3-256 format
*   **sha3-384**: A checksum in SHA3-384 format
*   **sha3-512**: A checksum in SHA3-512 format
*   **sha384**: A checksum in SHA-384 format
*   **sha512**: A checksum in SHA-512 format
*   **sha512/224**: A checksum in the SHA-512/224 format
*   **sha512/256**: A checksum in the SHA-512/256 format
*   **sigma**: Sigma - Generic Signature Format for SIEM Systems
*   **size-in-bytes**: Size expressed in bytes
*   **snort**: An IDS rule in Snort rule-format
*   **special-service-request**: A Special Service Request is a function to an airline to provide a particular facility for A Passenger or passengers. 
*   **ssdeep**: A checksum in ssdeep format
*   **ssh-fingerprint**: A fingerprint of SSH key material
*   **stix2-pattern**: STIX 2 pattern
*   **target-email**: Attack Targets Email(s)
*   **target-external**: External Target Organizations Affected by this Attack
*   **target-location**: Attack Targets Physical Location(s)
*   **target-machine**: Attack Targets Machine Name(s)
*   **target-org**: Attack Targets Department or Organization(s)
*   **target-user**: Attack Targets Username(s)
*   **telfhash**: telfhash is symbol hash for ELF files, just like imphash is imports hash for PE files.
*   **text**: Name, ID or a reference
*   **threat-actor**: A string identifying the threat actor
*   **tlsh**: A checksum in the Trend Micro Locality Sensitive Hash format
*   **travel-details**: Travel details
*   **twitter-id**: Twitter ID
*   **uri**: Uniform Resource Identifier
*   **url**: Uniform Resource Locator
*   **user-agent**: The user-agent used by the malware in the HTTP request.
*   **vhash**: A VirusTotal checksum
*   **visa-number**: Visa number
*   **vulnerability**: A reference to the vulnerability used in the exploit
*   **weakness**: A reference to the weakness (CWE) used in the exploit
*   **whois-creation-date**: The date of domain's creation, obtained from the WHOIS information.
*   **whois-registrant-email**: The e-mail of a domain's registrant, obtained from the WHOIS information.
*   **whois-registrant-name**: The name of a domain's registrant, obtained from the WHOIS information.
*   **whois-registrant-org**: The org of a domain's registrant, obtained from the WHOIS information.
*   **whois-registrant-phone**: The phone number of a domain's registrant, obtained from the WHOIS information.
*   **whois-registrar**: The registrar of the domain, obtained from the WHOIS information.
*   **windows-scheduled-task**: A scheduled task in windows
*   **windows-service-displayname**: A windows service's displayname, not to be confused with the windows-service-name. This is the name that applications will generally display as the service's name in applications.
*   **windows-service-name**: A windows service name. This is the name used internally by windows. Not to be confused with the windows-service-displayname.
*   **x509-fingerprint-md5**: X509 fingerprint in MD5 format
*   **x509-fingerprint-sha1**: X509 fingerprint in SHA-1 format
*   **x509-fingerprint-sha256**: X509 fingerprint in SHA-256 format
*   **xmr**: Monero Address
*   **yara**: YARA signature
*   **zeek**: An NIDS rule in the Zeek rule-format

## MISP objects

MISP objects are in addition to MISP attributes to allow advanced combinations of attributes. The creation of these objects
and their associated attributes are based on real cyber security use-cases and existing practices in information sharing.
MISP objects are standardised under a simple templating format and are automatically available in MISP. A series of relationships
are also defined along with the objects which can be used to create relationships between objects.

The objects available can be [browsed via the web site](/objects.html) or downloaded as [PDF](/objects.pdf) or directly via the MISP software.

## MISP Taxonomies

Along with the core format, [MISP taxonomies](https://www.github.com/MISP/misp-taxonomies/) provide a set of already defined classifications modeling estimative language, CSIRTs/CERTs classifications, national classifications or threat model classification. The fixed taxonomies provide a practical method to tag efficiently events and attributes within a set of MISP instances where taxonomies can be easily cherry-picked or extended to meet the local requirements of an organization or a specific sharing community. When using MISP, the MISP taxonomies are available and can be freely used based on the community practises.

The taxonomies can be [browsed via the web site](/taxonomies.html) or downloaded as [PDF](/taxonomies.pdf) or via the MISP software.

### CERT-XLM

[CERT-XLM](https://github.com/MISP/misp-taxonomies/tree/main/CERT-XLM) :
CERT-XLM Security Incident Classification. [Overview](https://www.misp-project.org/taxonomies.html#_cert_xlm)

### DFRLab-dichotomies-of-disinformation

[DFRLab-dichotomies-of-disinformation](https://github.com/MISP/misp-taxonomies/tree/main/DFRLab-dichotomies-of-disinformation) :
DFRLab Dichotomies of Disinformation. [Overview](https://www.misp-project.org/taxonomies.html#_dfrlab_dichotomies_of_disinformation)

### DML

[DML](https://github.com/MISP/misp-taxonomies/tree/main/DML) :
The Detection Maturity Level (DML) model is a capability maturity model for referencing ones maturity in detecting cyber attacks.  It's designed for organizations who perform intel-driven detection and response and who put an emphasis on having a mature detection program. [Overview](https://www.misp-project.org/taxonomies.html#_dml)

### GrayZone

[GrayZone](https://github.com/MISP/misp-taxonomies/tree/main/GrayZone) :
Gray Zone of Active defense includes all elements which lay between reactive defense elements and offensive operations. It does fill the gray spot between them. Taxo may be used for active defense planning or modeling. [Overview](https://www.misp-project.org/taxonomies.html#_grayzone)

### PAP

[PAP](https://github.com/MISP/misp-taxonomies/tree/main/PAP) :
The Permissible Actions Protocol - or short: PAP - was designed to indicate how the received information can be used. [Overview](https://www.misp-project.org/taxonomies.html#_pap)

### access-method

[access-method](https://github.com/MISP/misp-taxonomies/tree/main/access-method) :
The access method used to remotely access a system. [Overview](https://www.misp-project.org/taxonomies.html#_access_method)

### accessnow

[accessnow](https://github.com/MISP/misp-taxonomies/tree/main/accessnow) :
Access Now classification to classify an issue (such as security, human rights, youth rights). [Overview](https://www.misp-project.org/taxonomies.html#_accessnow)

### acs-marking

[acs-marking](https://github.com/MISP/misp-taxonomies/tree/main/acs-marking) :
The Access Control Specification (ACS) marking type defines the object types required to implement automated access control systems based on the relevant policies governing sharing between participants. [Overview](https://www.misp-project.org/taxonomies.html#_acs_marking)

### action-taken

[action-taken](https://github.com/MISP/misp-taxonomies/tree/main/action-taken) :
Action taken in the case of a security incident (CSIRT perspective). [Overview](https://www.misp-project.org/taxonomies.html#_action_taken)

### admiralty-scale

[admiralty-scale](https://github.com/MISP/misp-taxonomies/tree/main/admiralty-scale) :
The Admiralty Scale or Ranking (also called the NATO System) is used to rank the reliability of a source and the credibility of an information. Reference based on FM 2-22.3 (FM 34-52) HUMAN INTELLIGENCE COLLECTOR OPERATIONS and NATO documents. [Overview](https://www.misp-project.org/taxonomies.html#_admiralty_scale)

### adversary

[adversary](https://github.com/MISP/misp-taxonomies/tree/main/adversary) :
An overview and description of the adversary infrastructure [Overview](https://www.misp-project.org/taxonomies.html#_adversary)

### ais-marking

[ais-marking](https://github.com/MISP/misp-taxonomies/tree/main/ais-marking) :
The AIS Marking Schema implementation is maintained by the National Cybersecurity and Communication Integration Center (NCCIC) of the U.S. Department of Homeland Security (DHS) [Overview](https://www.misp-project.org/taxonomies.html#_ais_marking)

### analyst-assessment

[analyst-assessment](https://github.com/MISP/misp-taxonomies/tree/main/analyst-assessment) :
A series of assessment predicates describing the analyst capabilities to perform analysis. These assessment can be assigned by the analyst him/herself or by another party evaluating the analyst. [Overview](https://www.misp-project.org/taxonomies.html#_analyst_assessment)

### approved-category-of-action

[approved-category-of-action](https://github.com/MISP/misp-taxonomies/tree/main/approved-category-of-action) :
A pre-approved category of action for indicators being shared with partners (MIMIC). [Overview](https://www.misp-project.org/taxonomies.html#_approved_category_of_action)

### artificial-satellites

[artificial-satellites](https://github.com/MISP/misp-taxonomies/tree/main/artificial-satellites) :
This taxonomy was designed to describe artificial satellites [Overview](https://www.misp-project.org/taxonomies.html#_artificial_satellites)

### aviation

[aviation](https://github.com/MISP/misp-taxonomies/tree/main/aviation) :
A taxonomy describing security threats or incidents against the aviation sector. [Overview](https://www.misp-project.org/taxonomies.html#_aviation)

### binary-class

[binary-class](https://github.com/MISP/misp-taxonomies/tree/main/binary-class) :
Custom taxonomy for types of binary file. [Overview](https://www.misp-project.org/taxonomies.html#_binary_class)

### cccs

[cccs](https://github.com/MISP/misp-taxonomies/tree/main/cccs) :
Internal taxonomy for CCCS. [Overview](https://www.misp-project.org/taxonomies.html#_cccs)

### circl

[circl](https://github.com/MISP/misp-taxonomies/tree/main/circl) :
CIRCL Taxonomy - Schemes of Classification in Incident Response and Detection. [Overview](https://www.misp-project.org/taxonomies.html#_circl)

### cnsd

[cnsd](https://github.com/MISP/misp-taxonomies/tree/main/cnsd) :
La presente taxonomia es la primera versión disponible para el Centro Nacional de Seguridad Digital del Perú. [Overview](https://www.misp-project.org/taxonomies.html#_cnsd)

### coa

[coa](https://github.com/MISP/misp-taxonomies/tree/main/coa) :
Course of action taken within organization to discover, detect, deny, disrupt, degrade, deceive and/or destroy an attack. [Overview](https://www.misp-project.org/taxonomies.html#_coa)

### collaborative-intelligence

[collaborative-intelligence](https://github.com/MISP/misp-taxonomies/tree/main/collaborative-intelligence) :
Collaborative intelligence support language is a common language to support analysts to perform their analysis to get crowdsourced support when using threat intelligence sharing platform like MISP. The objective of this language is to advance collaborative analysis and to share earlier than later. [Overview](https://www.misp-project.org/taxonomies.html#_collaborative_intelligence)

### common-taxonomy

[common-taxonomy](https://github.com/MISP/misp-taxonomies/tree/main/common-taxonomy) :
Common Taxonomy for Law enforcement and CSIRTs [Overview](https://www.misp-project.org/taxonomies.html#_common_taxonomy)

### copine-scale

[copine-scale](https://github.com/MISP/misp-taxonomies/tree/main/copine-scale) :
The COPINE Scale is a rating system created in Ireland and used in the United Kingdom to categorise the severity of images of child sex abuse. The scale was developed by staff at the COPINE (Combating Paedophile Information Networks in Europe) project. The COPINE Project was founded in 1997, and is based in the Department of Applied Psychology, University College Cork, Ireland. [Overview](https://www.misp-project.org/taxonomies.html#_copine_scale)

### course-of-action

[course-of-action](https://github.com/MISP/misp-taxonomies/tree/main/course-of-action) :
A Course Of Action analysis considers six potential courses of action for the development of a cyber security capability. [Overview](https://www.misp-project.org/taxonomies.html#_course_of_action)

### crowdsec

[crowdsec](https://github.com/MISP/misp-taxonomies/tree/main/crowdsec) :
Crowdsec IP address classifications and behaviors taxonomy. [Overview](https://www.misp-project.org/taxonomies.html#_crowdsec)

### cryptocurrency-threat

[cryptocurrency-threat](https://github.com/MISP/misp-taxonomies/tree/main/cryptocurrency-threat) :
Threats targetting cryptocurrency, based on CipherTrace report. [Overview](https://www.misp-project.org/taxonomies.html#_cryptocurrency_threat)

### csirt-americas

[csirt-americas](https://github.com/MISP/misp-taxonomies/tree/main/csirt-americas) :
Taxonomía CSIRT Américas. [Overview](https://www.misp-project.org/taxonomies.html#_csirt_americas)

### csirt_case_classification

[csirt_case_classification](https://github.com/MISP/misp-taxonomies/tree/main/csirt_case_classification) :
It is critical that the CSIRT provide consistent and timely response to the customer, and that sensitive information is handled appropriately.  This document provides the guidelines needed for CSIRT Incident Managers (IM) to classify the case category, criticality level, and sensitivity level for each CSIRT case.  This information will be entered into the Incident Tracking System (ITS) when a case is created.  Consistent case classification is required for the CSIRT to provide accurate reporting to management on a regular basis.  In addition, the classifications will provide CSIRT IM’s with proper case handling procedures and will form the basis of SLA’s between the CSIRT and other Company departments. [Overview](https://www.misp-project.org/taxonomies.html#_csirt_case_classification)

### cssa

[cssa](https://github.com/MISP/misp-taxonomies/tree/main/cssa) :
The CSSA agreed sharing taxonomy. [Overview](https://www.misp-project.org/taxonomies.html#_cssa)

### cti

[cti](https://github.com/MISP/misp-taxonomies/tree/main/cti) :
Cyber Threat Intelligence cycle to control workflow state of your process. [Overview](https://www.misp-project.org/taxonomies.html#_cti)

### current-event

[current-event](https://github.com/MISP/misp-taxonomies/tree/main/current-event) :
Current events - Schemes of Classification in Incident Response and Detection [Overview](https://www.misp-project.org/taxonomies.html#_current_event)

### cyber-threat-framework

[cyber-threat-framework](https://github.com/MISP/misp-taxonomies/tree/main/cyber-threat-framework) :
Cyber Threat Framework was developed by the US Government to enable consistent characterization and categorization of cyber threat events, and to identify trends or changes in the activities of cyber adversaries. https://www.dni.gov/index.php/cyber-threat-framework [Overview](https://www.misp-project.org/taxonomies.html#_cyber_threat_framework)

### cycat

[cycat](https://github.com/MISP/misp-taxonomies/tree/main/cycat) :
Taxonomy used by CyCAT, the Universal Cybersecurity Resource Catalogue, to categorize the namespaces it supports and uses. [Overview](https://www.misp-project.org/taxonomies.html#_cycat)

### cytomic-orion

[cytomic-orion](https://github.com/MISP/misp-taxonomies/tree/main/cytomic-orion) :
Taxonomy to describe desired actions for Cytomic Orion [Overview](https://www.misp-project.org/taxonomies.html#_cytomic_orion)

### dark-web

[dark-web](https://github.com/MISP/misp-taxonomies/tree/main/dark-web) :
Criminal motivation and content detection the dark web: A categorisation model for law enforcement. ref: Janis Dalins, Campbell Wilson, Mark Carman. Taxonomy updated by MISP Project and extended by the JRC (Joint Research Centre) of the European Commission. [Overview](https://www.misp-project.org/taxonomies.html#_dark_web)

### data-classification

[data-classification](https://github.com/MISP/misp-taxonomies/tree/main/data-classification) :
Data classification for data potentially at risk of exfiltration based on table 2.1 of Solving Cyber Risk book. [Overview](https://www.misp-project.org/taxonomies.html#_data_classification)

### dcso-sharing

[dcso-sharing](https://github.com/MISP/misp-taxonomies/tree/main/dcso-sharing) :
Taxonomy defined in the DCSO MISP Event Guide. It provides guidance for the creation and consumption of MISP events in a way that minimises the extra effort for the sending party, while enhancing the usefulness for receiving parties. [Overview](https://www.misp-project.org/taxonomies.html#_dcso_sharing)

### ddos

[ddos](https://github.com/MISP/misp-taxonomies/tree/main/ddos) :
Distributed Denial of Service - or short: DDoS - taxonomy supports the description of Denial of Service attacks and especially the types they belong too. [Overview](https://www.misp-project.org/taxonomies.html#_ddos)

### de-vs

[de-vs](https://github.com/MISP/misp-taxonomies/tree/main/de-vs) :
German (DE) Government classification markings (VS). [Overview](https://www.misp-project.org/taxonomies.html#_de_vs)

### death-possibilities

[death-possibilities](https://github.com/MISP/misp-taxonomies/tree/main/death-possibilities) :
Taxonomy of Death Possibilities [Overview](https://www.misp-project.org/taxonomies.html#_death_possibilities)

### deception

[deception](https://github.com/MISP/misp-taxonomies/tree/main/deception) :
Deception is an important component of information operations, valuable for both offense and defense.  [Overview](https://www.misp-project.org/taxonomies.html#_deception)

### detection-engineering

[detection-engineering](https://github.com/MISP/misp-taxonomies/tree/main/detection-engineering) :
Taxonomy related to detection engineering techniques [Overview](https://www.misp-project.org/taxonomies.html#_detection_engineering)

### dga

[dga](https://github.com/MISP/misp-taxonomies/tree/main/dga) :
A taxonomy to describe domain-generation algorithms often called DGA. Ref: A Comprehensive Measurement Study of Domain Generating Malware Daniel Plohmann and others. [Overview](https://www.misp-project.org/taxonomies.html#_dga)

### dhs-ciip-sectors

[dhs-ciip-sectors](https://github.com/MISP/misp-taxonomies/tree/main/dhs-ciip-sectors) :
DHS critical sectors as in https://www.dhs.gov/critical-infrastructure-sectors [Overview](https://www.misp-project.org/taxonomies.html#_dhs_ciip_sectors)

### diamond-model

[diamond-model](https://github.com/MISP/misp-taxonomies/tree/main/diamond-model) :
The Diamond Model for Intrusion Analysis establishes the basic atomic element of any intrusion activity, the event, composed of four core features: adversary, infrastructure, capability, and victim. [Overview](https://www.misp-project.org/taxonomies.html#_diamond_model)

### diamond-model-for-influence-operations

[diamond-model-for-influence-operations](https://github.com/MISP/misp-taxonomies/tree/main/diamond-model-for-influence-operations) :
The diamond model for influence operations analysis is a framework that leads analysts and researchers toward a comprehensive understanding of a malign influence campaign by addressing the socio-political, technical, and psychological aspects of the campaign. The diamond model for influence operations analysis consists of 5 components: 4 corners and a core element. The 4 corners are divided into 2 axes: influencer and audience on the socio-political axis, capabilities and infrastructure on the technical axis. Narrative makes up the core of the diamond. [Overview](https://www.misp-project.org/taxonomies.html#_diamond_model_for_influence_operations)

### dni-ism

[dni-ism](https://github.com/MISP/misp-taxonomies/tree/main/dni-ism) :
A subset of Information Security Marking Metadata ISM as required by Executive Order (EO) 13526. As described by DNI.gov as Data Encoding Specifications for Information Security Marking Metadata in Controlled Vocabulary Enumeration Values for ISM [Overview](https://www.misp-project.org/taxonomies.html#_dni_ism)

### domain-abuse

[domain-abuse](https://github.com/MISP/misp-taxonomies/tree/main/domain-abuse) :
Domain Name Abuse - taxonomy to tag domain names used for cybercrime. [Overview](https://www.misp-project.org/taxonomies.html#_domain_abuse)

### doping-substances

[doping-substances](https://github.com/MISP/misp-taxonomies/tree/main/doping-substances) :
This taxonomy aims to list doping substances [Overview](https://www.misp-project.org/taxonomies.html#_doping_substances)

### drugs

[drugs](https://github.com/MISP/misp-taxonomies/tree/main/drugs) :
A taxonomy based on the superclass and class of drugs. Based on https://www.drugbank.ca/releases/latest [Overview](https://www.misp-project.org/taxonomies.html#_drugs)

### economical-impact

[economical-impact](https://github.com/MISP/misp-taxonomies/tree/main/economical-impact) :
Economical impact is a taxonomy to describe the financial impact as positive or negative gain to the tagged information (e.g. data exfiltration loss, a positive gain for an adversary). [Overview](https://www.misp-project.org/taxonomies.html#_economical_impact)

### ecsirt

[ecsirt](https://github.com/MISP/misp-taxonomies/tree/main/ecsirt) :
Incident Classification by the ecsirt.net version mkVI of 31 March 2015 enriched with IntelMQ taxonomy-type mapping. [Overview](https://www.misp-project.org/taxonomies.html#_ecsirt)

### enisa

[enisa](https://github.com/MISP/misp-taxonomies/tree/main/enisa) :
The present threat taxonomy is an initial version that has been developed on the basis of available ENISA material. This material has been used as an ENISA-internal structuring aid for information collection and threat consolidation purposes. It emerged in the time period 2012-2015. [Overview](https://www.misp-project.org/taxonomies.html#_enisa)

### estimative-language

[estimative-language](https://github.com/MISP/misp-taxonomies/tree/main/estimative-language) :
Estimative language to describe quality and credibility of underlying sources, data, and methodologies based Intelligence Community Directive 203 (ICD 203) and JP 2-0, Joint Intelligence [Overview](https://www.misp-project.org/taxonomies.html#_estimative_language)

### eu-marketop-and-publicadmin

[eu-marketop-and-publicadmin](https://github.com/MISP/misp-taxonomies/tree/main/eu-marketop-and-publicadmin) :
Market operators and public administrations that must comply to some notifications requirements under EU NIS directive [Overview](https://www.misp-project.org/taxonomies.html#_eu_marketop_and_publicadmin)

### eu-nis-sector-and-subsectors

[eu-nis-sector-and-subsectors](https://github.com/MISP/misp-taxonomies/tree/main/eu-nis-sector-and-subsectors) :
Sectors, subsectors, and digital services as identified by the NIS Directive [Overview](https://www.misp-project.org/taxonomies.html#_eu_nis_sector_and_subsectors)

### euci

[euci](https://github.com/MISP/misp-taxonomies/tree/main/euci) :
EU classified information (EUCI) means any information or material designated by a EU security classification, the unauthorised disclosure of which could cause varying degrees of prejudice to the interests of the European Union or of one or more of the Member States. [Overview](https://www.misp-project.org/taxonomies.html#_euci)

### europol-event

[europol-event](https://github.com/MISP/misp-taxonomies/tree/main/europol-event) :
This taxonomy was designed to describe the type of events [Overview](https://www.misp-project.org/taxonomies.html#_europol_event)

### europol-incident

[europol-incident](https://github.com/MISP/misp-taxonomies/tree/main/europol-incident) :
This taxonomy was designed to describe the type of incidents by class. [Overview](https://www.misp-project.org/taxonomies.html#_europol_incident)

### event-assessment

[event-assessment](https://github.com/MISP/misp-taxonomies/tree/main/event-assessment) :
A series of assessment predicates describing the event assessment performed to make judgement(s) under a certain level of uncertainty. [Overview](https://www.misp-project.org/taxonomies.html#_event_assessment)

### event-classification

[event-classification](https://github.com/MISP/misp-taxonomies/tree/main/event-classification) :
Classification of events as seen in tools such as RT/IR, MISP and other [Overview](https://www.misp-project.org/taxonomies.html#_event_classification)

### exercise

[exercise](https://github.com/MISP/misp-taxonomies/tree/main/exercise) :
Exercise is a taxonomy to describe if the information is part of one or more cyber or crisis exercise. [Overview](https://www.misp-project.org/taxonomies.html#_exercise)

### extended-event

[extended-event](https://github.com/MISP/misp-taxonomies/tree/main/extended-event) :
Reasons why an event has been extended. This taxonomy must be used on the extended event. The competitive analysis aspect is from Psychology of Intelligence Analysis by Richard J. Heuer, Jr. ref:http://www.foo.be/docs/intelligence/PsychofIntelNew.pdf [Overview](https://www.misp-project.org/taxonomies.html#_extended_event)

### failure-mode-in-machine-learning

[failure-mode-in-machine-learning](https://github.com/MISP/misp-taxonomies/tree/main/failure-mode-in-machine-learning) :
The purpose of this taxonomy is to jointly tabulate both the of these failure modes in a single place. Intentional failures wherein the failure is caused by an active adversary attempting to subvert the system to attain her goals – either to misclassify the result, infer private training data, or to steal the underlying algorithm. Unintentional failures wherein the failure is because an ML system produces a formally correct but completely unsafe outcome. [Overview](https://www.misp-project.org/taxonomies.html#_failure_mode_in_machine_learning)

### false-positive

[false-positive](https://github.com/MISP/misp-taxonomies/tree/main/false-positive) :
This taxonomy aims to ballpark the expected amount of false positives. [Overview](https://www.misp-project.org/taxonomies.html#_false_positive)

### file-type

[file-type](https://github.com/MISP/misp-taxonomies/tree/main/file-type) :
List of known file types. [Overview](https://www.misp-project.org/taxonomies.html#_file_type)

### financial

[financial](https://github.com/MISP/misp-taxonomies/tree/main/financial) :
Financial taxonomy to describe financial services, infrastructure and financial scope. [Overview](https://www.misp-project.org/taxonomies.html#_financial)

### flesch-reading-ease

[flesch-reading-ease](https://github.com/MISP/misp-taxonomies/tree/main/flesch-reading-ease) :
Flesch Reading Ease is a revised system for determining the comprehension difficulty of written material. The scoring of the flesh score can have a maximum of 121.22 and there is no limit on how low a score can be (negative score are valid). [Overview](https://www.misp-project.org/taxonomies.html#_flesch_reading_ease)

### fpf

[fpf](https://github.com/MISP/misp-taxonomies/tree/main/fpf) :
The Future of Privacy Forum (FPF) [visual guide to practical de-identification](https://fpf.org/2016/04/25/a-visual-guide-to-practical-data-de-identification/) taxonomy is used to evaluate the degree of identifiability of personal data and the types of pseudonymous data, de-identified data and anonymous data. The work of FPF is licensed under a creative commons attribution 4.0 international license. [Overview](https://www.misp-project.org/taxonomies.html#_fpf)

### fr-classif

[fr-classif](https://github.com/MISP/misp-taxonomies/tree/main/fr-classif) :
French gov information classification system [Overview](https://www.misp-project.org/taxonomies.html#_fr_classif)

### gdpr

[gdpr](https://github.com/MISP/misp-taxonomies/tree/main/gdpr) :
Taxonomy related to the REGULATION (EU) 2016/679 OF THE EUROPEAN PARLIAMENT AND OF THE COUNCIL on the protection of natural persons with regard to the processing of personal data and on the free movement of such data, and repealing Directive 95/46/EC (General Data Protection Regulation) [Overview](https://www.misp-project.org/taxonomies.html#_gdpr)

### gea-nz-activities

[gea-nz-activities](https://github.com/MISP/misp-taxonomies/tree/main/gea-nz-activities) :
Information needed to track or monitor moments, periods or events that occur over time. This type of information is focused on occurrences that must be tracked for business reasons or represent a specific point in the evolution of ‘The Business’. [Overview](https://www.misp-project.org/taxonomies.html#_gea_nz_activities)

### gea-nz-entities

[gea-nz-entities](https://github.com/MISP/misp-taxonomies/tree/main/gea-nz-entities) :
Information relating to instances of entities or things. [Overview](https://www.misp-project.org/taxonomies.html#_gea_nz_entities)

### gea-nz-motivators

[gea-nz-motivators](https://github.com/MISP/misp-taxonomies/tree/main/gea-nz-motivators) :
Information relating to authority or governance. [Overview](https://www.misp-project.org/taxonomies.html#_gea_nz_motivators)

### gsma-attack-category

[gsma-attack-category](https://github.com/MISP/misp-taxonomies/tree/main/gsma-attack-category) :
Taxonomy used by GSMA for their information sharing program with telco describing the attack categories [Overview](https://www.misp-project.org/taxonomies.html#_gsma_attack_category)

### gsma-fraud

[gsma-fraud](https://github.com/MISP/misp-taxonomies/tree/main/gsma-fraud) :
Taxonomy used by GSMA for their information sharing program with telco describing the various aspects of fraud [Overview](https://www.misp-project.org/taxonomies.html#_gsma_fraud)

### gsma-network-technology

[gsma-network-technology](https://github.com/MISP/misp-taxonomies/tree/main/gsma-network-technology) :
Taxonomy used by GSMA for their information sharing program with telco describing the types of infrastructure. WiP [Overview](https://www.misp-project.org/taxonomies.html#_gsma_network_technology)

### honeypot-basic

[honeypot-basic](https://github.com/MISP/misp-taxonomies/tree/main/honeypot-basic) :
Updated (CIRCL, Seamus Dowling and EURECOM) from Christian Seifert, Ian Welch, Peter Komisarczuk, ‘Taxonomy of Honeypots’, Technical Report CS-TR-06/12, VICTORIA UNIVERSITY OF WELLINGTON, School of Mathematical and Computing Sciences, June 2006, http://www.mcs.vuw.ac.nz/comp/Publications/archive/CS-TR-06/CS-TR-06-12.pdf [Overview](https://www.misp-project.org/taxonomies.html#_honeypot_basic)

### ics

[ics](https://github.com/MISP/misp-taxonomies/tree/main/ics) :
FIRST.ORG CTI SIG - MISP Proposal for ICS/OT Threat Attribution (IOC) Project [Overview](https://www.misp-project.org/taxonomies.html#_ics)

### iep

[iep](https://github.com/MISP/misp-taxonomies/tree/main/iep) :
Forum of Incident Response and Security Teams (FIRST) Information Exchange Policy (IEP) framework [Overview](https://www.misp-project.org/taxonomies.html#_iep)

### iep2-policy

[iep2-policy](https://github.com/MISP/misp-taxonomies/tree/main/iep2-policy) :
Forum of Incident Response and Security Teams (FIRST) Information Exchange Policy (IEP) v2.0 Policy [Overview](https://www.misp-project.org/taxonomies.html#_iep2_policy)

### iep2-reference

[iep2-reference](https://github.com/MISP/misp-taxonomies/tree/main/iep2-reference) :
Forum of Incident Response and Security Teams (FIRST) Information Exchange Policy (IEP) v2.0 Reference [Overview](https://www.misp-project.org/taxonomies.html#_iep2_reference)

### ifx-vetting

[ifx-vetting](https://github.com/MISP/misp-taxonomies/tree/main/ifx-vetting) :
The IFX taxonomy is used to categorise information (MISP events and attributes) to aid in the intelligence vetting process [Overview](https://www.misp-project.org/taxonomies.html#_ifx_vetting)

### incident-disposition

[incident-disposition](https://github.com/MISP/misp-taxonomies/tree/main/incident-disposition) :
How an incident is classified in its process to be resolved. The taxonomy is inspired from NASA Incident Response and Management Handbook. https://www.nasa.gov/pdf/589502main_ITS-HBK-2810.09-02%20%5bNASA%20Information%20Security%20Incident%20Management%5d.pdf#page=9 [Overview](https://www.misp-project.org/taxonomies.html#_incident_disposition)

### infoleak

[infoleak](https://github.com/MISP/misp-taxonomies/tree/main/infoleak) :
A taxonomy describing information leaks and especially information classified as being potentially leaked. The taxonomy is based on the work by CIRCL on the AIL framework. The taxonomy aim is to be used at large to improve classification of leaked information. [Overview](https://www.misp-project.org/taxonomies.html#_infoleak)

### information-origin

[information-origin](https://github.com/MISP/misp-taxonomies/tree/main/information-origin) :
Taxonomy for tagging information by its origin: human-generated or AI-generated. [Overview](https://www.misp-project.org/taxonomies.html#_information_origin)

### information-security-data-source

[information-security-data-source](https://github.com/MISP/misp-taxonomies/tree/main/information-security-data-source) :
Taxonomy to classify the information security data sources. [Overview](https://www.misp-project.org/taxonomies.html#_information_security_data_source)

### information-security-indicators

[information-security-indicators](https://github.com/MISP/misp-taxonomies/tree/main/information-security-indicators) :
A full set of operational indicators for organizations to use to benchmark their security posture. [Overview](https://www.misp-project.org/taxonomies.html#_information_security_indicators)

### interactive-cyber-training-audience

[interactive-cyber-training-audience](https://github.com/MISP/misp-taxonomies/tree/main/interactive-cyber-training-audience) :
Describes the target of cyber training and education. [Overview](https://www.misp-project.org/taxonomies.html#_interactive_cyber_training_audience)

### interactive-cyber-training-technical-setup

[interactive-cyber-training-technical-setup](https://github.com/MISP/misp-taxonomies/tree/main/interactive-cyber-training-technical-setup) :
The technical setup consists of environment structure, deployment, and orchestration. [Overview](https://www.misp-project.org/taxonomies.html#_interactive_cyber_training_technical_setup)

### interactive-cyber-training-training-environment

[interactive-cyber-training-training-environment](https://github.com/MISP/misp-taxonomies/tree/main/interactive-cyber-training-training-environment) :
The training environment details the environment around the training, consisting of training type and scenario. [Overview](https://www.misp-project.org/taxonomies.html#_interactive_cyber_training_training_environment)

### interactive-cyber-training-training-setup

[interactive-cyber-training-training-setup](https://github.com/MISP/misp-taxonomies/tree/main/interactive-cyber-training-training-setup) :
The training setup further describes the training itself with the scoring, roles, the training mode as well as the customization level. [Overview](https://www.misp-project.org/taxonomies.html#_interactive_cyber_training_training_setup)

### interception-method

[interception-method](https://github.com/MISP/misp-taxonomies/tree/main/interception-method) :
The interception method used to intercept traffic. [Overview](https://www.misp-project.org/taxonomies.html#_interception_method)

### ioc

[ioc](https://github.com/MISP/misp-taxonomies/tree/main/ioc) :
An IOC classification to facilitate automation of malicious and non malicious artifacts [Overview](https://www.misp-project.org/taxonomies.html#_ioc)

### iot

[iot](https://github.com/MISP/misp-taxonomies/tree/main/iot) :
Internet of Things taxonomy, based on IOT UK report https://iotuk.org.uk/wp-content/uploads/2017/01/IOT-Taxonomy-Report.pdf [Overview](https://www.misp-project.org/taxonomies.html#_iot)

### kill-chain

[kill-chain](https://github.com/MISP/misp-taxonomies/tree/main/kill-chain) :
The Cyber Kill Chain, a phase-based model developed by Lockheed Martin, aims to help categorise and identify the stage of an attack. [Overview](https://www.misp-project.org/taxonomies.html#_kill_chain)

### maec-delivery-vectors

[maec-delivery-vectors](https://github.com/MISP/misp-taxonomies/tree/main/maec-delivery-vectors) :
Vectors used to deliver malware based on MAEC 5.0 [Overview](https://www.misp-project.org/taxonomies.html#_maec_delivery_vectors)

### maec-malware-behavior

[maec-malware-behavior](https://github.com/MISP/misp-taxonomies/tree/main/maec-malware-behavior) :
Malware behaviours based on MAEC 5.0 [Overview](https://www.misp-project.org/taxonomies.html#_maec_malware_behavior)

### maec-malware-capabilities

[maec-malware-capabilities](https://github.com/MISP/misp-taxonomies/tree/main/maec-malware-capabilities) :
Malware Capabilities based on MAEC 5.0 [Overview](https://www.misp-project.org/taxonomies.html#_maec_malware_capabilities)

### maec-malware-obfuscation-methods

[maec-malware-obfuscation-methods](https://github.com/MISP/misp-taxonomies/tree/main/maec-malware-obfuscation-methods) :
Obfuscation methods used by malware based on MAEC 5.0 [Overview](https://www.misp-project.org/taxonomies.html#_maec_malware_obfuscation_methods)

### malware_classification

[malware_classification](https://github.com/MISP/misp-taxonomies/tree/main/malware_classification) :
Classification based on different categories. Based on https://www.sans.org/reading-room/whitepapers/incident/malware-101-viruses-32848 [Overview](https://www.misp-project.org/taxonomies.html#_malware_classification)

### misinformation-website-label

[misinformation-website-label](https://github.com/MISP/misp-taxonomies/tree/main/misinformation-website-label) :
classification for the identification of type of misinformation among websites. Source:False, Misleading, Clickbait-y, and/or Satirical News Sources by Melissa Zimdars 2019 [Overview](https://www.misp-project.org/taxonomies.html#_misinformation_website_label)

### misp

[misp](https://github.com/MISP/misp-taxonomies/tree/main/misp) :
MISP taxonomy to infer with MISP behavior or operation. [Overview](https://www.misp-project.org/taxonomies.html#_misp)

### misp-workflow

[misp-workflow](https://github.com/MISP/misp-taxonomies/tree/main/misp-workflow) :
MISP workflow taxonomy to support result of workflow execution. [Overview](https://www.misp-project.org/taxonomies.html#_misp_workflow)

### monarc-threat

[monarc-threat](https://github.com/MISP/misp-taxonomies/tree/main/monarc-threat) :
MONARC Threats Taxonomy [Overview](https://www.misp-project.org/taxonomies.html#_monarc_threat)

### ms-caro-malware

[ms-caro-malware](https://github.com/MISP/misp-taxonomies/tree/main/ms-caro-malware) :
Malware Type and Platform classification based on Microsoft's implementation of the Computer Antivirus Research Organization (CARO) Naming Scheme and Malware Terminology. Based on https://www.microsoft.com/en-us/security/portal/mmpc/shared/malwarenaming.aspx, https://www.microsoft.com/security/portal/mmpc/shared/glossary.aspx, https://www.microsoft.com/security/portal/mmpc/shared/objectivecriteria.aspx, and http://www.caro.org/definitions/index.html. Malware families are extracted from Microsoft SIRs since 2008 based on https://www.microsoft.com/security/sir/archive/default.aspx and https://www.microsoft.com/en-us/security/portal/threat/threats.aspx. Note that SIRs do NOT include all Microsoft malware families. [Overview](https://www.misp-project.org/taxonomies.html#_ms_caro_malware)

### ms-caro-malware-full

[ms-caro-malware-full](https://github.com/MISP/misp-taxonomies/tree/main/ms-caro-malware-full) :
Malware Type and Platform classification based on Microsoft's implementation of the Computer Antivirus Research Organization (CARO) Naming Scheme and Malware Terminology. Based on https://www.microsoft.com/en-us/security/portal/mmpc/shared/malwarenaming.aspx, https://www.microsoft.com/security/portal/mmpc/shared/glossary.aspx, https://www.microsoft.com/security/portal/mmpc/shared/objectivecriteria.aspx, and http://www.caro.org/definitions/index.html. Malware families are extracted from Microsoft SIRs since 2008 based on https://www.microsoft.com/security/sir/archive/default.aspx and https://www.microsoft.com/en-us/security/portal/threat/threats.aspx. Note that SIRs do NOT include all Microsoft malware families. [Overview](https://www.misp-project.org/taxonomies.html#_ms_caro_malware_full)

### mwdb

[mwdb](https://github.com/MISP/misp-taxonomies/tree/main/mwdb) :
Malware Database (mwdb) Taxonomy - Tags used across the platform [Overview](https://www.misp-project.org/taxonomies.html#_mwdb)

### nato

[nato](https://github.com/MISP/misp-taxonomies/tree/main/nato) :
NATO classification markings. [Overview](https://www.misp-project.org/taxonomies.html#_nato)

### nis

[nis](https://github.com/MISP/misp-taxonomies/tree/main/nis) :
The taxonomy is meant for large scale cybersecurity incidents, as mentioned in the Commission Recommendation of 13 September 2017, also known as the blueprint. It has two core parts: The nature of the incident, i.e. the underlying cause, that triggered the incident, and the impact of the incident, i.e. the impact on services, in which sector(s) of economy and society. [Overview](https://www.misp-project.org/taxonomies.html#_nis)

### nis2

[nis2](https://github.com/MISP/misp-taxonomies/tree/main/nis2) :
The taxonomy is meant for large scale cybersecurity incidents, as mentioned in the Commission Recommendation of 13 May 2022, also known as the provisional agreement. It has two core parts: The nature of the incident, i.e. the underlying cause, that triggered the incident, and the impact of the incident, i.e. the impact on services, in which sector(s) of economy and society. [Overview](https://www.misp-project.org/taxonomies.html#_nis2)

### open_threat

[open_threat](https://github.com/MISP/misp-taxonomies/tree/main/open_threat) :
Open Threat Taxonomy v1.1 base on James Tarala of SANS http://www.auditscripts.com/resources/open_threat_taxonomy_v1.1a.pdf, https://files.sans.org/summit/Threat_Hunting_Incident_Response_Summit_2016/PDFs/Using-Open-Tools-to-Convert-Threat-Intelligence-into-Practical-Defenses-James-Tarala-SANS-Institute.pdf, https://www.youtube.com/watch?v=5rdGOOFC_yE, and https://www.rsaconference.com/writable/presentations/file_upload/str-r04_using-an-open-source-threat-model-for-prioritized-defense-final.pdf [Overview](https://www.misp-project.org/taxonomies.html#_open_threat)

### organizational-cyber-harm

[organizational-cyber-harm](https://github.com/MISP/misp-taxonomies/tree/main/organizational-cyber-harm) :
A taxonomy to classify organizational cyber harms based on categories like physical, economic, psychological, reputational, and social/societal impacts. [Overview](https://www.misp-project.org/taxonomies.html#_organizational_cyber_harm)

### osint

[osint](https://github.com/MISP/misp-taxonomies/tree/main/osint) :
Open Source Intelligence - Classification (MISP taxonomies) [Overview](https://www.misp-project.org/taxonomies.html#_osint)

### pandemic

[pandemic](https://github.com/MISP/misp-taxonomies/tree/main/pandemic) :
Pandemic [Overview](https://www.misp-project.org/taxonomies.html#_pandemic)

### passivetotal

[passivetotal](https://github.com/MISP/misp-taxonomies/tree/main/passivetotal) :
Tags from RiskIQ's PassiveTotal service [Overview](https://www.misp-project.org/taxonomies.html#_passivetotal)

### pentest

[pentest](https://github.com/MISP/misp-taxonomies/tree/main/pentest) :
Penetration test (pentest) classification. [Overview](https://www.misp-project.org/taxonomies.html#_pentest)

### pfc

[pfc](https://github.com/MISP/misp-taxonomies/tree/main/pfc) :
Le Protocole des feux de circulation (PFC) est basé sur le standard « Traffic Light Protocol (TLP) » conçu par le FIRST. Il a pour objectif d’informer sur les limites autorisées pour la diffusion des informations. Il est classé selon des codes de couleurs. [Overview](https://www.misp-project.org/taxonomies.html#_pfc)

### phishing

[phishing](https://github.com/MISP/misp-taxonomies/tree/main/phishing) :
Taxonomy to classify phishing attacks including techniques, collection mechanisms and analysis status. [Overview](https://www.misp-project.org/taxonomies.html#_phishing)

### poison-taxonomy

[poison-taxonomy](https://github.com/MISP/misp-taxonomies/tree/main/poison-taxonomy) :
Non-exhaustive taxonomy of natural poison [Overview](https://www.misp-project.org/taxonomies.html#_poison_taxonomy)

### political-spectrum

[political-spectrum](https://github.com/MISP/misp-taxonomies/tree/main/political-spectrum) :
A political spectrum is a system to characterize and classify different political positions in relation to one another. [Overview](https://www.misp-project.org/taxonomies.html#_political_spectrum)

### priority-level

[priority-level](https://github.com/MISP/misp-taxonomies/tree/main/priority-level) :
After an incident is scored, it is assigned a priority level. The six levels listed below are aligned with NCCIC, DHS, and the CISS to help provide a common lexicon when discussing incidents. This priority assignment drives NCCIC urgency, pre-approved incident response offerings, reporting requirements, and recommendations for leadership escalation. Generally, incident priority distribution should follow a similar pattern to the graph below. Based on https://www.cisa.gov/news-events/news/cisa-national-cyber-incident-scoring-system-nciss. [Overview](https://www.misp-project.org/taxonomies.html#_priority_level)

### pyoti

[pyoti](https://github.com/MISP/misp-taxonomies/tree/main/pyoti) :
PyOTI automated enrichment schemes for point in time classification of indicators. [Overview](https://www.misp-project.org/taxonomies.html#_pyoti)

### ransomware

[ransomware](https://github.com/MISP/misp-taxonomies/tree/main/ransomware) :
Ransomware is used to define ransomware types and the elements that compose them. [Overview](https://www.misp-project.org/taxonomies.html#_ransomware)

### ransomware-roles

[ransomware-roles](https://github.com/MISP/misp-taxonomies/tree/main/ransomware-roles) :
The seven roles seen in most ransomware incidents. [Overview](https://www.misp-project.org/taxonomies.html#_ransomware_roles)

### retention

[retention](https://github.com/MISP/misp-taxonomies/tree/main/retention) :
Add a retenion time to events to automatically remove the IDS-flag on ip-dst or ip-src attributes. We calculate the time elapsed based on the date of the event. Supported time units are: d(ays), w(eeks), m(onths), y(ears). The numerical_value is just for sorting in the web-interface and is not used for calculations. [Overview](https://www.misp-project.org/taxonomies.html#_retention)

### rsit

[rsit](https://github.com/MISP/misp-taxonomies/tree/main/rsit) :
Reference Security Incident Classification Taxonomy [Overview](https://www.misp-project.org/taxonomies.html#_rsit)

### rt_event_status

[rt_event_status](https://github.com/MISP/misp-taxonomies/tree/main/rt_event_status) :
Status of events used in Request Tracker. [Overview](https://www.misp-project.org/taxonomies.html#_rt_event_status)

### runtime-packer

[runtime-packer](https://github.com/MISP/misp-taxonomies/tree/main/runtime-packer) :
Runtime or software packer used to combine compressed or encrypted data with the decompression or decryption code. This code can add additional obfuscations mechanisms including polymorphic-packer or other obfuscation techniques. This taxonomy lists all the known or official packer used for legitimate use or for packing malicious binaries. [Overview](https://www.misp-project.org/taxonomies.html#_runtime_packer)

### scrippsco2-fgc

[scrippsco2-fgc](https://github.com/MISP/misp-taxonomies/tree/main/scrippsco2-fgc) :
Flags describing the sample [Overview](https://www.misp-project.org/taxonomies.html#_scrippsco2_fgc)

### scrippsco2-fgi

[scrippsco2-fgi](https://github.com/MISP/misp-taxonomies/tree/main/scrippsco2-fgi) :
Flags describing the sample for isotopic data (C14, O18) [Overview](https://www.misp-project.org/taxonomies.html#_scrippsco2_fgi)

### scrippsco2-sampling-stations

[scrippsco2-sampling-stations](https://github.com/MISP/misp-taxonomies/tree/main/scrippsco2-sampling-stations) :
Sampling stations of the Scripps CO2 Program [Overview](https://www.misp-project.org/taxonomies.html#_scrippsco2_sampling_stations)

### sentinel-threattype

[sentinel-threattype](https://github.com/MISP/misp-taxonomies/tree/main/sentinel-threattype) :
Sentinel indicator threat types. [Overview](https://www.misp-project.org/taxonomies.html#_sentinel_threattype)

### smart-airports-threats

[smart-airports-threats](https://github.com/MISP/misp-taxonomies/tree/main/smart-airports-threats) :
Threat taxonomy in the scope of securing smart airports by ENISA. https://www.enisa.europa.eu/publications/securing-smart-airports [Overview](https://www.misp-project.org/taxonomies.html#_smart_airports_threats)

### social-engineering-attack-vectors

[social-engineering-attack-vectors](https://github.com/MISP/misp-taxonomies/tree/main/social-engineering-attack-vectors) :
Attack vectors used in social engineering as described in 'A Taxonomy of Social Engineering Defense Mechanisms' by Dalal Alharthi and others. [Overview](https://www.misp-project.org/taxonomies.html#_social_engineering_attack_vectors)

### srbcert

[srbcert](https://github.com/MISP/misp-taxonomies/tree/main/srbcert) :
SRB-CERT Taxonomy - Schemes of Classification in Incident Response and Detection [Overview](https://www.misp-project.org/taxonomies.html#_srbcert)

### state-responsibility

[state-responsibility](https://github.com/MISP/misp-taxonomies/tree/main/state-responsibility) :
A spectrum of state responsibility to more directly tie the goals of attribution to the needs of policymakers. [Overview](https://www.misp-project.org/taxonomies.html#_state_responsibility)

### stealth_malware

[stealth_malware](https://github.com/MISP/misp-taxonomies/tree/main/stealth_malware) :
Classification based on malware stealth techniques. Described in https://vxheaven.org/lib/pdf/Introducing%20Stealth%20Malware%20Taxonomy.pdf [Overview](https://www.misp-project.org/taxonomies.html#_stealth_malware)

### stix-ttp

[stix-ttp](https://github.com/MISP/misp-taxonomies/tree/main/stix-ttp) :
TTPs are representations of the behavior or modus operandi of cyber adversaries. [Overview](https://www.misp-project.org/taxonomies.html#_stix_ttp)

### targeted-threat-index

[targeted-threat-index](https://github.com/MISP/misp-taxonomies/tree/main/targeted-threat-index) :
The Targeted Threat Index is a metric for assigning an overall threat ranking score to email messages that deliver malware to a victim’s computer. The TTI metric was first introduced at SecTor 2013 by Seth Hardy as part of the talk “RATastrophe: Monitoring a Malware Menagerie” along with Katie Kleemola and Greg Wiseman. [Overview](https://www.misp-project.org/taxonomies.html#_targeted_threat_index)

### thales_group

[thales_group](https://github.com/MISP/misp-taxonomies/tree/main/thales_group) :
Thales Group Taxonomy - was designed with the aim of enabling desired sharing and preventing unwanted sharing between Thales Group security communities. [Overview](https://www.misp-project.org/taxonomies.html#_thales_group)

### threatmatch

[threatmatch](https://github.com/MISP/misp-taxonomies/tree/main/threatmatch) :
The ThreatMatch Sectors, Incident types, Malware types and Alert types are applicable for any ThreatMatch instances and should be used for all CIISI and TIBER Projects. [Overview](https://www.misp-project.org/taxonomies.html#_threatmatch)

### threats-to-dns

[threats-to-dns](https://github.com/MISP/misp-taxonomies/tree/main/threats-to-dns) :
An overview of some of the known attacks related to DNS as described by Torabi, S., Boukhtouta, A., Assi, C., & Debbabi, M. (2018) in Detecting Internet Abuse by Analyzing Passive DNS Traffic: A Survey of Implemented Systems. IEEE Communications Surveys & Tutorials, 1–1. doi:10.1109/comst.2018.2849614 [Overview](https://www.misp-project.org/taxonomies.html#_threats_to_dns)

### tlp

[tlp](https://github.com/MISP/misp-taxonomies/tree/main/tlp) :
The Traffic Light Protocol (TLP) (v2.0) was created to facilitate greater sharing of potentially sensitive information and more effective collaboration. Information sharing happens from an information source, towards one or more recipients. TLP is a set of four standard labels (a fifth label is included in amber to limit the diffusion) used to indicate the sharing boundaries to be applied by the recipients. Only labels listed in this standard are considered valid by FIRST. This taxonomy includes additional labels for backward compatibility which are no more validated by FIRST SIG. [Overview](https://www.misp-project.org/taxonomies.html#_tlp)

### tor

[tor](https://github.com/MISP/misp-taxonomies/tree/main/tor) :
Taxonomy to describe Tor network infrastructure [Overview](https://www.misp-project.org/taxonomies.html#_tor)

### trust

[trust](https://github.com/MISP/misp-taxonomies/tree/main/trust) :
The Indicator of Trust provides insight about data on what can be trusted and known as a good actor. Similar to a whitelist but on steroids, reusing features one would use with Indicators of Compromise, but to filter out what is known to be good. [Overview](https://www.misp-project.org/taxonomies.html#_trust)

### type

[type](https://github.com/MISP/misp-taxonomies/tree/main/type) :
Taxonomy to describe different types of intelligence gathering discipline which can be described the origin of intelligence. [Overview](https://www.misp-project.org/taxonomies.html#_type)

### unified-kill-chain

[unified-kill-chain](https://github.com/MISP/misp-taxonomies/tree/main/unified-kill-chain) :
The Unified Kill Chain is a refinement to the Kill Chain. [Overview](https://www.misp-project.org/taxonomies.html#_unified_kill_chain)

### unified-ransomware-kill-chain

[unified-ransomware-kill-chain](https://github.com/MISP/misp-taxonomies/tree/main/unified-ransomware-kill-chain) :
The Unified Ransomware Kill Chain, a intelligence driven model developed by Oleg Skulkin, aims to track every single phase of a ransomware attack. [Overview](https://www.misp-project.org/taxonomies.html#_unified_ransomware_kill_chain)

### use-case-applicability

[use-case-applicability](https://github.com/MISP/misp-taxonomies/tree/main/use-case-applicability) :
The Use Case Applicability categories reflect standard resolution categories, to clearly display alerting rule configuration problems. [Overview](https://www.misp-project.org/taxonomies.html#_use_case_applicability)

### veris

[veris](https://github.com/MISP/misp-taxonomies/tree/main/veris) :
Vocabulary for Event Recording and Incident Sharing (VERIS) [Overview](https://www.misp-project.org/taxonomies.html#_veris)

### vmray

[vmray](https://github.com/MISP/misp-taxonomies/tree/main/vmray) :
VMRay taxonomies to map VMRay Thread Identifier scores and artifacts. [Overview](https://www.misp-project.org/taxonomies.html#_vmray)

### vocabulaire-des-probabilites-estimatives

[vocabulaire-des-probabilites-estimatives](https://github.com/MISP/misp-taxonomies/tree/main/vocabulaire-des-probabilites-estimatives) :
Ce vocabulaire attribue des valeurs en pourcentage à certains énoncés de probabilité [Overview](https://www.misp-project.org/taxonomies.html#_vocabulaire_des_probabilites_estimatives)

### vulnerability

[vulnerability](https://github.com/MISP/misp-taxonomies/tree/main/vulnerability) :
A taxonomy for describing vulnerabilities (software, hardware, or social) on different scales or with additional available information. [Overview](https://www.misp-project.org/taxonomies.html#_vulnerability)

### workflow

[workflow](https://github.com/MISP/misp-taxonomies/tree/main/workflow) :
Workflow support language is a common language to support intelligence analysts to perform their analysis on data and information. [Overview](https://www.misp-project.org/taxonomies.html#_workflow)

### workflow

[workflow](https://github.com/MISP/misp-taxonomies/tree/main/workflow) :
Workflow support language is a common language to support intelligence analysts to perform their analysis on data and information. [Overview](/taxonomies.html#_workflow)

## MISP Galaxy

MISP galaxy is a simple method to express a large object called cluster that can be attached to MISP events or attributes. A cluster can be composed of one or more elements. Elements are expressed as key-values. There are default vocabularies available in MISP galaxy but those can be overwritten, replaced or updated as you wish. Existing clusters and vocabularies can be used as-is or as a template. MISP distribution can be applied to each cluster to permit a limited or broader distribution scheme. Many MISP galaxy clusters are already available like Exploit-Kit, Microsoft Activity Group actor, Preventive Measure, 
Ransomware, TDS, Threat actor or Tool used by adversaries.

The galaxy can be [browsed via the web site](/galaxy.html) or downloaded as [PDF](/galaxy.pdf) or directly via the MISP software. There is also the website for the [misp-galaxy project](https://www.misp-galaxy.org).
