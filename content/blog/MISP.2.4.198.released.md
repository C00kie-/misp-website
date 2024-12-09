---
title: MISP 2.4.198 released with many bugs fixed, security fixes and improvements. 
date: 2024-09-17
layout: post
tags: ["MISP", "Threat Intelligence", "release" ]
banner: /img/blog/object-collapse.png
---

# MISP v2.4.198 (2024-09-13)

Based on a set of fixes including a security fix, we are pleased to announce the immediate availability of MISP 2.4.198. You can find a list of the detailed changes along with new features further below. As with any security release, we highly encourage everyone to update their  instance as soon as possible.

## New

- **[attribute type]** `dom-hash` is a structural fingerprint of HTML's Document Object Model. [Alexandre Dulaunoy]

  `dom-hash` is a structural fingerprint of the HTML's Document Object Model (DOM) originally developed by CERT.PL.

  The fingerprint is calculated by extracting all the tag names (ignoring the content itself as well as attributes of the HTML Page). The tag names are concatenated with a pipe value `|`, hashed using the SHA-256 algorithm, and truncated to the first 32 characters.

  Software such as LookyLoo[1] has implemented the algorithm, which can be used in MISP to share and correlate information about similar web pages (e.g., phishing pages).

  [1] https://github.com/Lookyloo/lookyloo/commit/466a3c56148f2ddb911620fd24e4f0c9d602a6a3

## Changes

- **[version]** bump. [iglocska]
- **[PyMISP]** Bump. [Raphaël Vinot]
- **[internal]** Simplified `cake.php` and load dispatcher from absolute path. [Jakub Onderka]
- **[internal]** Server sync debug message when pushing events. [Jakub Onderka]
- **[PyMISP]** Updated to the latest version. [Alexandre Dulaunoy]
- **[ui]** Better description for server settings. [Jakub Onderka]

## Fixes

- **[event-report:edit]** Take first Attribute value from an object if unable to get the priority value. [Sami Mokaddem]
- **[security]** Ensure proper sanitization of sensitive fields in user-login-profiles. [Sami Mokaddem]

  Prevents other org-admins (from the same org) from viewing sensitive fields of other org-admins when they confirm their login session.
  
  - [CVE-2024-45509](https://vulnerability.circl.lu/vuln/cve-2024-45509) as been assigned for this vulnerability.
  - Reported by Sharad Kumar Dahal of Green Tick Nepal Pvt. Ltd

- **[users:view_login_history]** Column not found error when not being a site-admin. [Sami Mokaddem]

  Ensured the user's Role is included in the result.

- **[users:index]** Redact autkey visibility to other org-admins in the same organization. [Sami Mokaddem]

  - Since by design, org admins can already change the password of other org-admins (from the same org), this is considered a fix.

- **[security]** ACL ignored on GUI attribute search. [iglocska]
  
  - CVE allocation is pending.
  - Reported by KZ-CERT, the National CERT Team of Kazakhstan.

- **[attribute search]** Fixes for invalid returns on `deleted = [0,1]`, fixes #9866. [iglocska]

  - Object-level deleted field check blocked the inclusion of non-object attributes.

- **[feed]** Old path replaced with official MISP website path. [Alexandre Dulaunoy]
- **[baseurl]** Preference changed to `MISP.baseurl`, fixes #9895. [iglocska]

  - `external_baseurl` no longer used as a preferred source.
    - Now intended to be informational only for sharing groups.

- **[internal]** Throw exception in `GpgTool` if `GnuPG.homedir` is empty. [Jakub Onderka]
- **[internal]** Throw exception in `EncryptedValue` invalid state. [Jakub Onderka]

## Other

- Merged branch `develop` into `2.4`. [iglocska]
- Merged branch `develop` from `github.com:MISP/MISP` into `develop`. [iglocska]
- Merged branch `2.4` into `develop`. [Alexandre Dulaunoy]
- Merged branch `fix/authkey-visibility` into `develop`. [Sami Mokaddem]
- Merged pull request #9903 from JakubOnderka/shell-dispatcher. [Jakub Onderka]

  - **[internal]** Simplified `cake.php` and loaded dispatcher from absolute path.

- Merged branch `2.4` into `develop`. [iglocska]
- Merged pull request #9685 from JakubOnderka/push-server-sync-debug. [Jakub Onderka]

  - **[internal]** Server sync debug message when pushing events.

- Merged branch `2.4` into `develop`. [iglocska]
- Merged pull request #9890 from JakubOnderka/log-unpublished. [Jakub Onderka]

  - **[ui]** Better description for server settings.

- Merged pull request #9896 from JakubOnderka/encrypt-exception. [Jakub Onderka]

  - Encrypt exception fix.

For a complete list of updates, please refer to the [changelog pages](https://www.misp-project.org/Changelog.txt). Many thanks to all the diligent contributors that ensure that MISP keeps improving rapidly!

