# Case Study: Recovering a Compromised Google Account and Securing a Household

**Role:** Freelance IT support · **Client:** Married couple, business clients (anonymized) · **Year:** 2026

## Summary

A client's Google account was taken over through a phishing email, and his wife's email addresses and passwords showed up in a dark web leak. I helped them investigate what the attacker had done, recover and lock down three Google accounts, and learn habits that stop the same attack from working again.

## Situation

- The husband's personal Gmail was compromised after he entered his credentials on a fake Google sign-in page. The link came from a phishing "birthday invitation" email.
- The attacker tried to buy gift cards with his credit card and ran an open-source email extractor against his account to harvest contacts.
- The wife was notified that some of her email addresses and passwords had leaked on the dark web.
- Both received heavy spam, some of it inappropriate.
- Data brokers were selling their personal information.
- Passwords and credit cards were saved in Chrome, and passwords were weak.

**Accounts in scope:** 3 (husband: personal Gmail; wife: personal Gmail and business Google Workspace)

## Approach

I worked in three phases: investigate and contain, harden, then educate.

### 1. Investigate and contain

- Reviewed recent sign-in activity and devices in Google Account > Security, which confirmed the unauthorized access.
- Traced the attack: analyzed the phishing email, followed the link to a look-alike Google sign-in page, and showed the client the URL that gave it away.
- Checked for attacker persistence: recovery phone and email, Gmail filters, forwarding and delegated access. None had been changed.
- Found that the attacker used an email extractor to harvest contacts, and had the client warn friends and family to expect phishing from his address.
- Confirmed the compromised password wasn't reused on any other account.

### 2. Harden

- Turned on 2-Step Verification and removed stale passkeys and saved passwords from their devices.
- Removed saved passwords and credit cards from Chrome to reduce exposure to info-stealing malware.
- Moved their credentials to Apple Passwords.
- Set up Aura for dark web monitoring, data broker removal and VPN.
- Recommended a credit freeze at Equifax, Experian and TransUnion.

### 3. Educate

- **Passwords:** length over complexity, a unique password per account, no personal details.
- **Phishing:** check the sender, hover over links, and verify the URL before signing in.
- **Spam:** built Gmail filters to move inappropriate messages out of the inbox.
- **How the attack works:** walked the husband through the full scheme. A stolen account sends mass invitations, a fake sign-in page captures credentials, the attacker commits gift card fraud, then repeats the process with the victim's contacts.

## Results

- Found the attacker's access and shut it off. No leftover filters, forwarding or recovery changes were found.
- The card issuer blocked the attempted gift card fraud, so no money was lost.
- Removed saved cards and passwords from the browser on their devices and moved credentials to a password manager.
- Put dark web and data broker monitoring in place for both clients.
- Both clients can now review their own account activity and spot phishing emails.

## Recommended next steps for the client

- Replace text-message 2SV with passkeys on all three accounts.
- Revoke any third-party app or IMAP access on the husband's account that he doesn't need.
- Change each password exposed in the wife's leak.
- Run an admin review of the Workspace account: sign-ins, connected apps and 2SV enforcement.
- Run Google's Security Checkup every quarter.

## Lessons learned

- **A password change isn't a full recovery.** Attackers often leave filters, forwarding or connected apps behind, so check for them every time.
- **Passkeys would have stopped this attack.** They can't be typed into a fake sign-in page.
- **Teaching matters as much as fixing.** Walking the client through how the attack worked is what prevents the next one.
- **Guidance should keep up with current practice.** I raised my password advice from an 8-character minimum to 14+ characters or a passphrase.

## Skills demonstrated

Incident response and account recovery · Google Account and Workspace security · Phishing analysis · Identity theft prevention · Password manager, 2SV and passkey setup · End-user security training · Technical documentation
