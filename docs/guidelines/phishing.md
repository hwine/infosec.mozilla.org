---
layout: default
resource: true
categories: [Guidelines]
title: Phishing
description: A fraudulent practice of sending emails (or other communications) purporting to be from reputable companies in order to induce individuals to reveal personal information, such as passwords and credit card numbers.
---

*The goal of this document is to help users figure out if they are being phished and escalate accordingly.*

If at any point you believe you are being targeted in a phishing campaign, it's important to raise those concerns with your [security team](/#contact).

# Background

Phishing is an attack used to elicit an action from you that you would otherwise not do (click a link, login, pay a bill, click an attachment, etc.) that has a negative affect on you, your computers, your business, or others (often compromising an account, a computer, or eliciting payment for services not rendered).

# Intuition

Your own intuition is probably your best asset for easily detecting phishing attacks.  If an email seems out of place, unsolicited or asks you to take a weird action, stop and consider whether you are in a phishing scenario.  The below information will be helpful in supporting those "weird feels" with evidence that would validate those concerns.

# Email Headers

Email headers are a great way to deduce the true origin of a given email.  As noted above, emails often contain a format section which is forgable by an attacker to make it seem as though an email came from a different source.  If you're using Gmail, you can follow the following steps to view the full email headers.

1. Open the email in Gmail
2. Open the drop down menu (three vertical dots, next to the reply button)
3. Select 'Show original'

When viewing the full headers, it's important to understand who actually sent a given email.  As noted above, formatting content within emails can be tampered with to make an email seem as though it's from someone else.

One of the more common techniques with phishing emails is to abuse the From: field content. This often looks like...

```
From: Pat Smith (psmith@example.com) <abadguy@evil.com>
To: You <you@example.com>
Subject: An Example Subject
```

# Links

HTML documents can contain links to email addresses (such as `mailto:hello@example.com`). These links can be misleading, much like a link on any webpage.  It's important to hover over any links provided in emails before clicking them to ensure they take you to the correct domain.  This hover action will present you with a preview of the URL in the bottom of your email client.

A common tactic for detecting malicious URLs in email is simply making sure the link is to the right domain. Phishing attacks will often leverage common looking domains with one character subsituted in the hopes of getting you to trust them.

A legitimate link for mozilla.org would look like this when hovered...

`https://mozilla.org/`

However, an attacker may replace the `l` with a numerical 1 to try and trick you...

`https://mozi11a.org/`

One way to avoid falling for such attacks, is simply not to click links provided in email.  If an email is asking that you click a link to login to a website, consider visiting the website directly using a bookmark.  Another technique is to make use of a password manager that supports an auto-fill feature that binds to the site address.  A password manager with an auto-fill feature will often require the website to match exactly before submitting credentials and this can sometimes act as a red flag if the auto-fill feature does not work.

If you observe this or some other behavior that suggests you've received a phishing email and have been coerced into clicking a malicious link, it's important to raise it with your security team for further review and attach the email headers (see above) and provide the phishing URL for further review.

# Attachments

Phishing emails often contain attachments in the hope that you will click and run them and compromise your workstation.  If you need to open an email attachment, make sure that you can confirm that the sender of that email is truely the sender and not a spoofed email made to look as if it was a trusted sender.  This can often be determined by examing the email headers (more details above) and generally whether that email was out of the blue from someone you rarely talk to or is outside the norm.

There are a number of malicious attachment types that are more dangerous than others, which include:

- PDF Documents (very powerful, can have embedded malicious content)
- MS Word/Excel Document (very powerful, especially in cases where Macros need to be enabled)
- Bash/.exe Files (extremely dangerous)

If you observe this or some other behavior that suggests someone is sending you unsolicited dangerous attachment types raise it with your [security team](/#contact) for further review and attach the email headers (see above) and provide the example attachment for further review.

# Password Manager Behavior

Phishing emails often attempt to have you enter credentials in a lookalike site with a similar domain name. The human eye may have a hard time telling the difference, but a password manager will refuse to autofill your credentials because it won't recognize the fraudulent domain. By using a password manager, you make your passwords more secure _and_ reduce your risk of being phished.

## References/Additional Reading

- [Phishing and Malware Protection in Firefox](https://support.mozilla.org/en-US/kb/how-does-phishing-and-malware-protection-work)
- [Report a Bad Site to Google Safe Browsing](https://safebrowsing.google.com/safebrowsing/report_phish/)
- [Report a Bad Site to StopBadWare.org](https://www.stopbadware.org/report-badware)
- [Anti-Phishing Working Group](https://www.apwg.org/)
- [Phishing Wikipedia](https://en.wikipedia.org/wiki/Phishing)
- [WebAuthn](https://duo.com/blog/web-authentication-what-it-is-and-what-it-means-for-passwords)


