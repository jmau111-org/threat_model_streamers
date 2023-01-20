#  Threat model for streamers

Threat model for the "new" hype and ways to protect 🧢

## What's a threat model?

[OWASP](https://owasp.org/www-community/Threat_Modeling) defines threat modeling as the act of "identifying, communicating, and understanding threats and mitigations within the context of protecting something of value."

In other words, it consists of taking the appropriate security measures according to your situation and your activities.

For example, security researchers do not have the same threat model as standard users, as their activities (e.g., online searches, exploiting bugs to demonstrate vulnerabilities) can be considered as particularly sensitive.

**Online streamers are primary targets** in 2023, especially the most popular ones, as they usually generate substantial revenues and have a large audience (hundred of thousands, perhaps millions of viewers/subscribers).

## Disclaimer

This very short guide is based on personal thoughts/researches and only provided for convenience. I'm not trying to speak with authority.

It's only a text-based document to keep things as simple as possible (no diagram, etc).

## Steps by steps

### What is a streamer exactly?

> A person who broadcasts his or herself in real time (referred to as streaming) while playing video games is known as a streamer. Those who want to stream their play may do so through online platforms such as Twitch and YouTube

> Many streamers attempt to make it a profession, dedicating full-time hours in hopes of receiving a steady pay check. Streamers make money from their viewers in the form of donations, subscriptions, sponsors, and advertising. As video game streaming has seen a large rise in popularity, it can be quite difficult to generate income as a streamer as the market is quite competitive.

[Source: computerhope](https://www.computerhope.com/jargon/s/streamer.htm)

### 7 things that can go wrong

* attackers might hack the account to delete published content, which could cut your revenues
* attackers might hack the account to spam or scam viewers, or spread malware
* attackers might disclose your personal info (PII) publicly, including your online habits but also your physical address, your friends, and family
* attackers might attempt to DoS your connection
* attackers might hack the account to attack your other businesses (streamers usually have multiple ways to monetize their audience)
* attackers might be politically driven and hack you to spread their messages (less probable but not impossible)
* attackers might target the entire platform (way less probable, but it already happened) instead of you specifically

### 7 techniques that could be used

Again, it's not exhaustive, but the following techniques seem probable:

* find and hack the email account associated with your stream
* phishing, spear phishing (more targeted phishing)
* use community forums and chats to send you tricked payloads
* more "direct" social engineering, like malicious phone calls
* technical exploit targeting the streaming platform or your personal websites, social platorms or eShop (e.g., merchandizing)
* if they manage to compromise your machine: ransomware (video files, other documents), RATs (Remote Access Trojans), reverse shells, 
* denial of service on your wireless connection if your location is known/leaked

### 7 robust protections

* use app-based/Yubikeys 2FA/MFA (double/multi-factor authentication) everywhere, including you and all your collaborators (SMS should be avoided unless it's the only one method available)
* use password managers to generate and autofill **long and random** passwords on your different accounts
* have a robust **and tested** backup strategies (may require a budget)
* use secured hardware (don't use cheap wireless accessories)
* use secure browsers with adblocker (may sound paradoxical for a streamer ^^) and [uBlock origin](https://ublockorigin.com/)
* keep your machine and applications up-to-date and use anti-malware solutions
* [other key points](#other-key-points)

### Other key points

* having a robust internet connection is not just good for your audience, maybe invest in a expensive plan that may include security options
* use a VPN permanently
* if possible, use a pseudo instead of your real name (but it will be hard to keep it private, especially if you become very popular)
* use a new email address **dedicated** to your stream
* prioritize robust platforms for your "merch" (e.g., Shopify, Squarespace)
* **secure payments** if you use alternative methods and even consider higher plans (professional/business offers) if you use Paypal
* secure all your uploads: remove EXIF data from documents, especially images, and don't expose family and friends if possible
* don't mention your physical location if possible (might be very hard if you are popular)
* take some privacy measures, as other online activities could potentially harm your reputation
* lie in your answers to the security questions (used to reset passwords)
* **don't feed the troll**: protect your mental health (e.g., regular pauses, moderation, holidays), as the social pressure can hack you "from inside"
