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

Credentials—such as passwords, passphrases, passkeys, and security keys—stand between critical data and those who may attempt to exploit it. A single weak or mishandled credential can expose systems to theft or misuse. When we follow these guidelines, everyone contributes to protecting not only our environment but also each individual's sense of security and peace of mind.

## Our identity providers and single sign-on (SSO)

{{< callout context="note" title="MFA is enabled by default" icon="outline/check-circle" >}}
All identity provider accounts have multi-factor authentication (MFA) enabled to strengthen security.  
All newly acquired systems must support single sign-on (SSO) and approved MFA methods.
{{< /callout >}}

{{< details "What is SSO?" open >}}
Single sign-on (SSO) allows one set of credentials to access multiple systems, reducing the risk of juggling multiple logins.

- **Apple**: Internal systems  
- **Google**: Client-facing systems  
- **GitHub**: Developer tools and workflows  
{{< /details >}}

## MFA and passkeys: enhanced security steps

{{< callout context="tip" title="Why MFA and passkeys matter" icon="outline/rocket" >}}
- MFA adds an extra layer of protection, reducing the chance of unauthorized access if a password is compromised.  
- Passkeys replace passwords with biometrics or device-based authentication, offering a more streamlined and secure login experience.
{{< /callout >}}

### MFA rules
- **Preferred methods**  
  - **Security keys (small USB-type devices)**  
    - [Yubico YubiKey C Bio FIDO Edition](https://www.yubico.com/gb/product/yubikey-bio-series/yubikey-c-bio/)  
    - [Yubico YubiKey 5C NFC](https://www.yubico.com/gb/product/yubikey-5-series/yubikey-5c-nfc/)  
    These require physical interaction to sign in. Each individual receives one primary key and one backup key—keep the primary key accessible and store the backup in a locked drawer or cabinet to reduce misuse if one goes missing.  
    - Security keys are preferred over one-time passcodes.  

{{< callout context=“tip” title=“Keep a backup YubiKey for account access” icon=“outline/lock-closed” >}}
For example, if your YubiKey is lost, having a backup key ensures you can still access your accounts without delay.
{{< /callout >}}

  ### App-based MFA 

Use only [Ente Auth](https://ente.io/auth/) for generating one-time codes. Ente Auth is deployed to any bring-your-own-device (BYOD) or company phone, as explained in the [centralized security with the password manager](#centralized-security-with-the-password-manager).

### Prohibited  
  {{< callout context="danger" title="Avoid SMS or phone call-based MFA" icon="outline/alert-octagon" >}}
  Text messages or phone calls are vulnerable to interception and do not meet required security standards.
  {{< /callout >}}

### Biometric authentication
Only Apple (Face ID, Touch ID), Google (Android Biometric), and Yubico (biometric-enabled security keys) are approved for biometric authentication because data is processed on the device itself. This approach:
- Keeps biometric details local, improving privacy  
- Speeds up daily access  
- Reduces the risk of data interception  

### Passkeys
Passkeys are strongly recommended over passphrases. Do not store them on personal or company devices or browsers. Keep them in the approved password manager or on a physical security key.

{{< callout context="note" title="Check system compatibility" icon="outline/info-circle" >}}
See the [passkeys directory](https://passkeys.directory/) for systems that allow passkeys and steps to enable them.
{{< /callout >}}

{{< callout context="caution" title="Keep factors separate" icon="outline/alert-triangle" >}}
Storing a password or passphrase with its MFA factor (passkey, code, or security key) in one place weakens multi-factor protection. Keeping them apart helps maintain stronger security.
{{< /callout >}}

## Passwords and passphrases
Passphrases are preferred over traditional passwords. Use passwords only when passphrases are not an option.

- **Requirements**  
  - **Length**: 20–100 characters (letters, numbers, symbols, or emojis)  
  - **Alphanumeric focus**: Emphasize length rather than forcing special characters  
  - **No reuse**: The last 20 passwords cannot be repeated  
  - **No hints or security questions**  
    - If required, generate passphrase answers and store them in the password manager. The same applies to data such as birthdates.  
  - **Newly issued passwords**  
    Change them right after the first login  

{{< callout context=“caution” title=“Change default passwords immediately” icon=“outline/key” >}}
For instance, if you receive a new system password, update it immediately upon first use to secure your account.
{{< /callout >}}


{{< callout context="warning" title="Legacy system notes" icon="outline/alert-triangle" >}}
Some older or external systems have outdated password requirements that we cannot modify. They may enforce rules like special characters or shorter maximum lengths.
{{< /callout >}}

{{< callout context=“danger” title=“Never share or write down passwords” icon=“outline/shield-exclamation” >}}
Avoid revealing a password over phone, email, chat, or in writing as it may lead to a breach.
{{< /callout >}}

## Centralized security with the password manager
- **Approved tool** [1Password](https://1password.com/) is installed on managed devices for credential storage. If you use a personal device for work, installation is required. Only production builds of the password manager are permitted. Centralizing credentials makes auditing and revocation faster.

- **Shared vaults** Shared vaults in 1Password do not allow printing, exporting, or deleting items, preventing offline copies or accidental removals. 

- **Browser extension** Installed by default on managed devices

- **Functions**  
  - Generates unique passwords or passphrases  
  - Creates temporary credentials  
  - Alerts for weak or reused credentials  
  - **Detection of**  
    - Compromised websites  
    - Vulnerable passwords (those found in known data breaches)  
    - Unsecured websites (sites not using HTTPS, which encrypts data in transit)  
  - Uses role-based access controls (RBAC) for safe sharing  

{{< callout context=“note” title=“Secure item sharing with email verification” icon=“outline/mail-check” >}}
Items can be shared with anyone, but recipients must verify their email address before viewing the item. Links expire after the item is viewed one time, with a maximum link lifespan of 1 day (default expiration is 1 hour).
{{< /callout >}}

## Backup plans: recovery codes
- **Usage** Recovery codes are needed if neither security keys nor an MFA app is available.
  
- **Storage** Print codes and keep them secured. Storing them digitally increases exposure.  

{{< callout context=“tip” title=“How to store printed recovery codes” icon=“outline/document-duplicate” >}}
Keep printed recovery codes in a locked drawer to ensure they are accessible when needed without digital vulnerabilities.
{{< /callout >}}
  
{{< callout context=“tip” title=“Regain access to locked-out accounts” icon=“outline/refresh” >}}
Locked-out accounts Use a backup security key, printed recovery codes, or a recovery key (if provided).
{{< /callout >}}

## Creating and managing temporary credentials
- Must be unique, random, and—if possible—protected with MFA.
- Must be generated by the approved password manager.

## Idle sessions and default accounts
  After 10 minutes of inactivity, a login session will prompt re-authentication to prevent misuse of an unattended device.
  
- **Default credentials** During initial setup, disable or change any default system accounts or passwords right away.

## Handling failed logins, account suspension, and lockouts
- Ten unsuccessful login attempts will lock the account.  
- An administrator must unlock it manually.  
- After an account has been suspended for 90 days, it is automatically deleted.

## Compromised credentials: immediate steps
1. Reset credentials through the system’s recovery process.  
2. Notify security based on the [incident response plans](#incident-response-plans).  
3. Watch for unusual account behavior.  
   *If you notice unfamiliar login attempts, immediately follow these steps to secure your account.*

## Tracking resets and credentials 
  If passwords are forgotten, MFA is inaccessible, or a security key is lost, file a ticket in the [Access Requests Project](#access-requests-project). This ensures a recorded audit trail.  
  *Creating a ticket helps us track and respond to your requests efficiently.*
  
- **Verification**  
  A video call is mandatory before resetting credentials to confirm identity.  

{{< callout context=“note” title=“Secure account recovery with ownership verification” icon=“outline/shield-check” >}}
Requiring a video call ensures that only the rightful owner can regain access, protecting your account from unauthorized resets.
{{< /callout >}}
  
- **Tracking**  
  All resets are logged in the [Access Requests Project](#access-requests-project).

## Shared accounts and non-human identities
- Used only for non-human identities (such as automated scripts or software services).  
- Each non-human identity must use MFA and have a designated owner.  
- Tracked in the [non-human identity registry](#non-human-identity-registry).

## Admin profiles and privilege separation
- Use a dedicated admin profile to safeguard elevated privileges.  
- This profile’s password must differ from the user’s standard account.  
- Admin profiles follow the same MFA rules.  

{{< callout context=“tip” title=“Separate admin accounts from standard accounts” icon=“outline/user-cog” >}}
Separating admin accounts ensures that high-level access remains secure even if a standard account is compromised.
{{< /callout >}}

## Developers: secure API, SSH keys, and token management
- **Secrets manager** All credentials, tokens, and keys must not be stored on-device, limiting access and enabling quick updates.  
    
- **Expiring tokens** Tokens must expire within 90 days, minimizing harm if any token is leaked.  

{{< callout context=“tip” title=“Use short-lived tokens for added security” icon=“outline/clock” >}}
Short-lived tokens reduce the window of opportunity for unauthorized use if a token is compromised. For further details, see the [SDL policy](#sdl-policy).
{{< /callout >}}

## Visibility through logging and monitoring

{{< callout context="note" title="MFA and login activity are monitored" icon="outline/shield-check" >}}
A browser-based identity threat detection and response (ITDR) system monitors all logins. Activities are checked against the [logging and monitoring policy](#logging-and-monitoring-policy), and any unusual events receive extra scrutiny.
{{< /callout >}}

## Incident response plans for urgent situations
Refer to the [incident response plans](#incident-response-plans) if you suspect provider-level issues or compromised credentials. Timely reporting can minimize harm and protect everyone’s data.

## Key takeaways for lasting security
- **Passkeys over passphrases over passwords** Always prefer more secure methods to reduce vulnerabilities.
  
- **One password manager** Centralize all credentials with 1Password, simplifying management and quick revocation.
  
- **Protect backups** Keep backup security keys locked and avoid saving recovery codes digitally.
  
- **Act promptly** Use incident response procedures if anything seems compromised.
  
- **Separate admin credentials** Use different passwords for admin profiles to contain potential damage.
  
- **Session re-authentication** After 10 minutes, re-authenticate to keep systems safe if you step away.
  
- **Audit trails** Lockouts, resets, and shared accounts are tracked for clear oversight.
  
- **No default accounts** Change or remove defaults as soon as systems are set up.
  
- **Review backups** Periodically confirm backup keys and recovery codes remain accessible and up to date.
