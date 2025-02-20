---
title: "Adaptive authentication"
description: "Guides lead a user through a specific task they want to accomplish, often with a sequence of steps."
summary: ""
date: 2024-02-17T16:04:48+02:00
lastmod: 2024-02-17T16:04:48+02:00
draft: false
weight: 810
toc: true
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---

Credentials—such as passwords, passphrases, passkeys, and security keys—stand between sensitive data and those who want to exploit it. A single weak or mishandled credential can expose systems to theft or misuse. Protecting credentials means protecting what matters most.

## Our identity providers and single sign-on (SSO)

{{< callout context="note" title="MFA is enabled by default" icon="outline/check-circle" >}}
- All identity providers have multi-factor authentication (MFA) enabled by default to reduce the threat of compromised credentials.  
- All newly acquired services must support single sign-on (SSO) and approved MFA methods.
{{< /callout >}}

Single sign-on (SSO) allows one set of credentials to access multiple systems, reducing the juggling of multiple logins.

- **Apple**: Internal systems  
- **Google**: Client-facing systems  
- **GitHub**: Developer tools and workflows

## Credential requirements

{{< callout context="danger" title="Never share or write down credentials" icon="outline/alert-octagon" >}}
Avoid revealing a credential over phone, email, chat, SMS or in writing as it may lead to a breach. **Always use the password manager sharing features**.
{{< /callout >}}

{{< details "General requirements" open >}}
- **Sharing or writting down credentials** Avoid revealing credentials over phone, email, chat, SMS or in writing as it may lead to a breach. **Always use the password manager sharing features**.
- **Transmission** Never store or send plaintext credentials
- **Credential expiration** Change only if compromised 
- **No reuse**: Block the last 20 passwords, or the highest number possible close to 20  
- **No hints or security questions** They are guessable, public, and easy to bypass  
- **Support for Character Sets** All ASCII & Unicode supported   
- **Credential visibility** Allow toggling credential visibility while typing to reduce errors  
- **Strength meters** Provide real-time feedback to encourage stronger credentials  
- **Rejection feedback** Explain why a credential is rejected to prevent confusion and improve security
{{< /details >}}

{{< callout context="danger" title="If you need to use hints or security questions" icon="outline/alert-octagon" >}}
If required, generate passphrase answers and store them in the password manager. The same applies to data such as birthdates.  
{{< /callout >}}

{{< callout context="note" title="Sharing externally" icon="outline/info-circle" >}}
Items can be shared with anyone, but recipients must verify their email address before viewing the item. Links expire after the item is viewed one time, with a maximum link lifespan of 1 day (default expiration is 1 hour).
{{< /callout >}}

### Passkeys

{{< callout context="tip" title="Why Passkeys matter" icon="outline/rocket" >}}
- Passkeys replace passwords with biometrics or device-based authentication, offering a more streamlined and secure login experience.
- Choose passkeys over passphrases over passwords. **Always** choose the more secure methods.
{{< /callout >}}

Passkeys are strongly recommended over passphrases and passwords. Do not store them on personal or company devices or browsers. Keep them in the approved password manager or on a physical security key.

{{< callout context="note" title="Check system compatibility" icon="outline/info-circle" >}}
See the [passkeys directory](https://passkeys.directory/) for services that allow passkeys and steps to enable them.
{{< /callout >}}

### Passwords, PINs and passphrases

{{< details "Passphrase requirements" >}}
**Passphrases** Preferred over passwords; must be at least 5 words
{{< /details >}}

{{< details "Password requirements" >}}     
- **Alphanumeric length**: 20–100 characters can optionally include letters, numbers, symbols, or emojis  
- **Alphanumeric focus** Emphasize length rather than forcing special characters
- **Non-typed passwords** If not manually entered, they must be at least 65 characters
- **Legacy services** Older services may have outdated password requirements that can't be controlled. These services may enforce rules such as numbers, special characters or shorter maximum lengths.
{{< /details >}}

{{< details "Pin-code requirements" >}}
**Avoid PINs**; if necessary, they must be at least 8 characters
{{< /details >}}

{{< details "Crypographic requirements" >}}  
**Salting & Hashing** Never store or send plaintext passwords. Use hashing with salting before storage. Passwords must not be retrievable from the server or anywhere a password is handled before being secured. Use zero-knowledge protocols or zeroization to prevent exposure. For further details, see the [cryptographic policy](#crypto-policy).  
{{< /details >}} 

## Multi-factor authentication (MFA) 

{{< callout context="tip" title="Why MFA matters" icon="outline/rocket" >}}
- MFA adds an extra layer of protection, reducing the chance of unauthorized access if a password is compromised.  
{{< /callout >}}

### MFA methods

#### Security keys (small USB-type devices)

Security keys require physical interaction to sign in. Each individual receives one primary key and one backup key—keep the primary key accessible and store the backup in a locked drawer or cabinet to gain access to systems and services in an emergency.  

- [Yubico YubiKey C Bio FIDO Edition](https://www.yubico.com/gb/product/yubikey-bio-series/yubikey-c-bio/)  
- [Yubico YubiKey 5C NFC](https://www.yubico.com/gb/product/yubikey-5-series/yubikey-5c-nfc/)

{{< callout context="tip" title="Did you know?" icon="outline/rocket" >}}
Security keys are preferred over App-based one-time passcodes.
{{< /callout >}}

#### App-based MFA 

Use only [Ente Auth](https://ente.io/auth/) for generating one-time codes. Ente Auth is deployed to any bring-your-own-device (BYOD) or company phone, as explained in the [Mobile device policy](#centralized-security-with-the-password-manager).

#### Prohibited MFA 
  {{< callout context="danger" title="Avoid SMS or phone call-based MFA" icon="outline/alert-octagon" >}}
  Text messages or voice calls are vulnerable to interception and do not meet required security standards.
  {{< /callout >}}

#### Biometric authentication
Only Apple (Face ID, Touch ID), Google (Android Biometric), and Yubico (biometric-enabled security keys) are approved for biometric authentication because data is processed on the device itself. This approach:
- Keeps biometric details local, improving privacy  
- Speeds up daily access  
- Reduces the risk of data interception

{{< callout context="caution" title="Keep factors separate" icon="outline/alert-triangle" >}}
Storing a password or passphrase with its MFA factor (passkey or one-time code) in one place weakens multi-factor protection. Keeping them apart helps maintain stronger security.
{{< /callout >}}

## Password manager deployment
{{< details "What is the approved password manager?" open >}}
[1Password](https://1password.com/) app, cli and browser extension is installed by default on managed devices for credential storage and management.
{{< /details >}}
  
{{< callout context="caution" title="Password management on personal devices" icon="outline/alert-triangle" >}}
If you use a personal device for work, installation of the password manager and the browser-based identity threat detection and response (ITDR) plugin is required.
{{< /callout >}}

{{< details "Shared vault restrictions" >}}
- Printing
- Exporting or
- Deleting items, preventing offline copies or accidental removals. 

This is verified with the password managers reporting feature.
{{< /details >}} 

{{< details "Functions" >}}  
  - Generates unique passwords or passphrases  
  - Creates temporary credentials  
  - Alerts for weak or reused credentials
  - Uses role-based access controls (RBAC) for controlled sharing
  {{< /details >}}

{{< details "Detection features" >}}  
  - Compromised websites  
  - Vulnerable passwords (those found in known data breaches)  
  - Unsecured websites (sites not using HTTPS, which encrypts data in transit)  
{{< /details >}}

## Backup plans: recovery codes
- **Usage** Recovery codes are needed if neither security keys nor an MFA app is available.
- **Storage** Print codes and keep them secured. Storing them digitally increases exposure.
- **lost access** Use a backup security key, printed recovery codes, or a recovery key (if provided).


{{< callout context="tip" title="How to store printed recovery codes" icon="outline/rocket" >}}
Keep printed recovery codes in a locked drawer to ensure they are accessible when needed without digital vulnerabilities.
{{< /callout >}}

## Creating and managing temporary credentials
- Must be unique, random, and—if possible—protected with MFA.
- Must be generated by the approved password manager.

## Idle sessions and default accounts
- **Lock-out** After 10 minutes of inactivity, a login session will prompt re-authentication to prevent misuse of an unattended device.
- **Default credentials** During initial setup, disable or change any default system accounts or passwords on first login.

## Handling failed logins, account suspension, and lockouts
- Ten unsuccessful login attempts will lock the account.  
- An administrator must unlock it **manually**.  
- After an account has been suspended for **90 days**, it is automatically deleted.

## Compromised credentials: immediate steps
1. Reset credentials through the system’s recovery process.  
2. Notify security based on the [incident response plans](#incident-response-plans).  
3. Watch for unusual account behavior.  

## Tracking resets and credentials 
  - **Lost MFA** If passwords are forgotten, MFA is inaccessible, or a security key is lost, file a ticket in the [Access Requests Project](#access-requests-project). 
  - **Label tickets** All resets are logged and tagged with the label 'reset'
  
{{< callout context="note" title="How to confirm someones identity" icon="outline/info-circle" >}}
A video call is mandatory before resetting credentials to confirm someones identity. Requiring a video call ensures that only the rightful owner can regain access, protecting accounts from unauthorized resets.
{{< /callout >}}
  

## Shared accounts and non-human identities
- Used only for non-human identities (such as automated scripts or software services).  
- Each non-human identity must use MFA and have a designated owner.  
- Tracked in the [non-human identity registry](#non-human-identity-registry).

## Admin accounts and privilege separation
- Use a dedicated admin account to safeguard elevated privileges.  
- The account’s password must differ from the user’s standard account.  
- Admin accounts must follow the same MFA rules.  

{{< callout context="tip" title="Separate admin accounts from standard accounts" icon="outline/rocket" >}}
Separating admin accounts ensures that high-level access remains secure even if a standard account is compromised.
{{< /callout >}}

## Credential managment for Developers
- **Secrets manager** Keep credentials, tokens, and keys in a keystore, not on-device, to minimize exposure if lost or stolen.  
- **Expiring tokens** Tokens must expire within **90 days**, minimizing harm if any token is leaked. For further details, see the [SDL policy](#sdl-policy).  

{{< callout context="tip" title="Use short-lived tokens for added security" icon="outline/rocket" >}}
Short-lived tokens reduce the window of opportunity for unauthorized use if a token is compromised. 
{{< /callout >}}

## Visibility through logging and monitoring

{{< callout context="note" title="MFA and login activity are monitored" icon="outline/shield-check" >}}
A browser-based identity threat detection and response (ITDR) system monitors all logins. Activities are checked against the [logging and monitoring policy](#logging-and-monitoring-policy), and any unusual events receive extra scrutiny.
{{< /callout >}}

## Incident response plans for urgent situations
Refer to the [incident response plans](#incident-response-plans) if you suspect provider-level issues or compromised credentials. Timely reporting can minimize harm and protect everyone’s data.

## Key takeaways for lasting security
- **Passkeys over passphrases over passwords** Always prefer more secure methods to reduce explotation.
  
- **One password manager** Centralize all credentials with 1Password, simplifying management and quick revocation.
  
- **Protect backups** Keep backup security keys locked and avoid saving recovery codes digitally.
  
- **Act promptly** Use incident response procedures if anything seems compromised.
  
- **Separate admin credentials** Use different passwords for admin accounts to contain potential damage.
  
- **Session re-authentication** After 10 minutes, re-authenticate to keep services safe if you step away.
  
- **Audit trails** Lockouts, resets, and shared accounts are tracked for clear oversight.
  
- **No default accounts** Change or remove defaults as soon as systems are set up.
  
- **Review backups** Periodically confirm backup keys and recovery codes remain accessible and up to date.
