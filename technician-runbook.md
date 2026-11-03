# Technician Runbook: Compromised Google Account

Use this runbook when a client's Google account (personal Gmail or Google Workspace) has been phished, shows unknown sign-ins, or is sending mail the client didn't write.

**Time needed:** 60–90 minutes per account · **Tools:** a clean device, the client present, their phone

---

## 0. Before you start

- [ ] Work from a device you trust, not the one the client used when they were phished.
- [ ] Have the client sign in and type their own passwords. Never write down or store a client's passwords or backup codes.
- [ ] Ask: what happened, when, which accounts, and whether any money was taken.
- [ ] Note whether the account is **personal Gmail** or **Workspace**. For a Workspace account, contact the organization's admin before making changes.

## 1. Regain control

- [ ] If locked out, use [Google Account Recovery](https://accounts.google.com/signin/recovery) from a device and location the client normally uses.
- [ ] Change the password to a new passphrase of 14+ characters that has never been used before.
- [ ] **Security > Your devices > Sign out** on every device the client doesn't recognize, or sign out everywhere.
- [ ] **Security > Recent security activity**: screenshot anything unusual (time, location, device) for the client's records.

## 2. Remove attacker persistence

Attackers often leave ways back in. Check each of these:

| Where | What to look for | Action |
| --- | --- | --- |
| Security > How you sign in | Unknown recovery phone or email | Remove and replace with the client's |
| Security > 2-Step Verification | Unknown phones, authenticator apps or security keys | Remove |
| Security > Third-party apps with account access | Apps the client doesn't recognize, including email extractors | Remove access |
| Security > App passwords | Any app password the client didn't create | Delete |
| Gmail > Settings > Filters and Blocked Addresses | Filters that delete, archive or forward mail | Delete |
| Gmail > Settings > Forwarding and POP/IMAP | Forwarding addresses; IMAP on when the client doesn't need it | Remove forwarding; turn off IMAP if not needed |
| Gmail > Settings > Accounts | Delegates under "Grant access"; unknown "Send mail as" addresses | Remove |
| Gmail > Sent and Trash | Messages the attacker sent | Note recipients so the client can warn them |
| Google Pay (pay.google.com) | Unknown payment methods or purchases | Remove; report to the card issuer |

**Workspace only:** ask the admin to review the user's sign-in logs, OAuth app grants and mail routing in the Admin console, and to require 2SV.

## 3. Harden the account

- [ ] Set up **passkeys** on the client's phone and computer.
- [ ] Turn on 2SV with Google prompts, and remove text messages as a method where possible.
- [ ] Print **backup codes** for the client to keep at home.
- [ ] Turn on **Enhanced Safe Browsing** (Security > Enhanced Safe Browsing).
- [ ] Run the **Security Checkup** (myaccount.google.com/security-checkup) until everything shows green.

## 4. Protect the client beyond Google

- [ ] **Cards:** review statements for unknown charges, especially gift cards. Have the client call the issuer to dispute charges and replace the card.
- [ ] **Password reuse:** change the password on every other account that shared the compromised one, starting with banking and email.
- [ ] **Credit freeze:** recommend freezing at Equifax, Experian and TransUnion.
- [ ] **Identity theft:** if fraud occurred, file at [IdentityTheft.gov](https://www.identitytheft.gov).
- [ ] **Browser:** delete saved passwords and cards from Chrome and move them to a password manager.
- [ ] **Devices:** install updates and run a malware scan on the device used when the client was phished.
- [ ] **Mobile carrier:** add a port-out / SIM lock PIN.

## 5. Contacts and education

- [ ] Have the client warn contacts not to open recent messages from them.
- [ ] Walk the client through the phishing email they fell for: the sender, the link, and the fake page's URL.
- [ ] Teach the one-line rule: **if an email asks you to sign in, don't use its link. Open the site yourself.**
- [ ] Give the client the one-page **Quick Guide** PDF.

## 6. Close out

- [ ] Record what you found and what you changed (date, account, findings, actions).
- [ ] Book a follow-up in 1–2 weeks to recheck sign-in activity and third-party apps.
- [ ] Recommend a quarterly Security Checkup.

---

## Common attack pattern: the "invitation" phish

1. The attacker sends a fake invitation (birthday, event, shared document) from a stolen account the victim trusts.
2. The link opens a look-alike Google sign-in page on a different domain.
3. The victim enters their password and 2SV code, and the attacker signs in immediately.
4. The attacker buys gift cards with saved or linked cards, since those are hard to trace.
5. The attacker harvests the victim's contacts and repeats the process from the victim's account.

**What breaks this chain:** passkeys (they can't be typed into a fake page), checking the URL before signing in, and not keeping cards saved in the browser.
