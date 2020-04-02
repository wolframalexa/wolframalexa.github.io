---
layout: post
title: "Switch Your Email, Protect Your Privacy"
subtitle: A Comparison of Privacy-Focused Email for the Novice
categories:
  - Blog Posts
tags:
  - privacy
  - encryption
  - security
---

We all have data out there. You probably have a Facebook, Twitter, email account, in addition to publicly available records on the Internet. Lately, I’ve been thinking about the information I put out into the world, by giving my consent to different websites and internet companies. In return for providing me a way to share pictures of my lunch on Instagram and communicate with colleagues via email, We may click “accept terms and conditions” without actually reading them, but this doesn’t mean our data is actually secure – it’s no secret that companies like Facebook and Google collect the data you provide them. Ostensibly, this data is used to better the user experience, but users should also have the option to not provide certain types of data, like turning off location services ([although that may not always be respected](https://www.techrepublic.com/article/your-smartphone-can-be-tracked-even-if-gps-location-services-are-turned-off/)).

I know it’s easy to disregard your privacy, saying “I have nothing to hide,” but the reality is that many tech companies monetize the information you provide them: if you’re not paying, you’re the product. For me, safeguarding my privacy means being able to enjoy a full life without worrying that my texts or browsing habits will be sold. I can enjoy things without that weird moment where you get an Instagram ad for something you said aloud yesterday.

Email in particular is full of personal information. Think of all the things you put through your email – forgot password links, advertising emails from websites you shop from, personal communications. Gmail, the most widespread email provider, also gives you access to a calendar, YouTube, filesharing and hosting, among others, and when logged in on Chrome, Google can link your browsing history to your account as well. Suffice it to say – Google may know you better than you know yourself.

A cool resource I was referred to when thinking about alternatives to these products is [privacytools.io](https://www.privacytools.io/). Fair warning - this may be enough to turn you into a privacy evangelist and have your friends and family gifting you tinfoil hats – you have been warned. They suggest many different alternative, privacy-focused providers for things like email, search engines, or browsers.

It can certainly be a hassle to switch your primary email account. I had to update my email address for countless accounts, all with new passwords from a password manager (more on that in a future post?), and forward my old email. Sometimes I still forget what email I signed up for something with. However, the sheer amount of data you put through your email provider means that you want to be able to trust whoever’s administering it.

In this post, I want to take a look at a few of the most common privacy-focused email providers. I explore what encryption protocol they use, whether they’re open-source, cost, features, and something I’ll call “level of intensity”. Although it’s cool for an email provider to be open source, any one of the sites on this list are going to require you to trust them to some degree, particularly if you don’t have the knowledge to audit all of their code    . Otherwise, you might as well not use email at all. Level of intensity is a very subjective criteria, but my aim is to measure how much of a hassle it is to use any platform (i.e. could you convert your friends? Your geeky roommate? Your grandma?). The reality is that not everyone needs a super secure email client you can only access over Tor – you might just want to limit tracking and data leaks, and that’s good enough for you. I’m definitely a huge n00b in the world of online privacy, so please feel free to suggest or point out something I missed [here](https://www.alexajakob.com/about.html).

###
###

## Tutanota 

If you’ve checked out my contact page, you’ll notice this is what I use. Tutanota presents itself as an easy alternative for those looking to deGoogle: they’ve even made their own captcha instead of using Google’s “Are you a robot?” (I hope I’m not!), and are working on improving their encrypted calendar. That being said, I find they are lacking in features for free users.

**Encryption:** Tutanota uses its own implementation of the AES and RSA algorithms (link). This allows them to encrypt the body, attachments, subject lines, and names, leaving only times of emails and addresses unencrypted. Emails are end-to-end encrypted when they are sent within Tutanota, which is challenging if, like me, you have friends’ emails and newsletters that come from non-Tuta addresses. You can send your friend an invitation link to view the email securely with a password you’ve shared with them previously, however, but it does not use PGP, a widely-used encryption algorithm, unlike the rest of the providers on this list. Also worth noting: Tutanota is based in Germany, which makes it bound by the GDPR.

**Open-source?** [Yes!](https://github.com/tutao/tutanota) They are also accepting issues and PRs.

**Cost:** The free version has limited features, like search capability of only a month. Paying more gets you more storage, more aliases, and inbox rules (!). There are different membership levels, but Premium starts at 12 euro per year.

**Features:** Tutanota was the first to have a (limited) encrypted calendar, and they’re continuing to work on it. The features are quite limited if you don’t pay for the service (which is quite affordable at 12 euro/year) – you can only have one calendar, 1 GB of data, and search one month back. Even for paid users, Tutanota doesn’t have the option of tagging emails, something I miss from Gmail, although there are folders. For the privacy minded, you can set up two-factor authentication with an app or hardware token, like a Yubikey.

**Intensity or ease of use:** The interface is very simple and easy to use, and although the email service is privacy focused, I think a novice would find it fairly simple to navigate since there aren’t too many BIG PRIVACY WORDS. You could probably get your grandparents to use this with few issues.


## ProtonMail
ProtonMail is another very popular privacy-focused email service. It has 5 million accounts as of September 2018 (for comparison, Gmail hasteam 1.2 billion). They have a VPN service, ProtonVPN, and are also working on a calendar and have released the beta in late 2019. With their goal to help you “de-Google” your life, ProtonMail hopes to someday replace the G-Suite with their own products.

**Encryption:** ProtonMail uses PGP (pretty good privacy) and end-to-end encrypts your emails, which means that only the person on either end can read the message – not even ProtonMail has access. Much like Tutanota, you can send your friends who don’t use PGP a link to an encrypted email they can access with a password, but if your contacts have PGP set up with a service like Gmail or Hotmail, your messages will be end-to-end encrypted! Also, ProtonMail is based in Switzerland and bound by Swiss law, which has a reputation for being very privacy-friendly, even though it is not technically bound by the GDPR.

**Open-source?** Yes! Feel free to open an issue, send a pull request, or look at the code [here](https://github.com/ProtonMail).

**Cost:** ProtonMail is a freemium product, meaning that there are free accounts but the features are limited. The “plus” plan, at $5/month, gets you more storage, addresses, and messages.

**Features:** ProtonMail allows you to use both folders and tags as well as filters, which makes it easy to organize yourself. You can also use rich text formatting (like bolding and underlining) to compose emails. With the free accounts, you are limited to 150 messages per day, with each email to each recipient counting as a message, and 500 MB of storage, and different levels of monetary support increase that. ProtonMail supports 2FA with hardware (Yubikey) or codes.

**Intensity or ease of use:** Like Tutanota, ProtonMail is pretty simple to use. It is designed so that you don’t need to manage your own PGP keys or understand anything about the technical side of privacy. You could probably get your grandparents to use this also.

## CounterMail
Just from its website, it’s clear that CounterMail means business. If you really, really need your email to be as secure as possible, they’ve got your back.

**Encryption:** CounterMail uses OpenPGP to encrypt emails, which are stored on their servers in Sweden on CD-ROMS, not hard drives, which prevents data leaks and means that if someone tries to tamper with the server, your data will probably be lost. The company also doesn’t keep IP logs, so your emails can’t be traced back to you. Email headers are anonymous and the service does not use cookies (doesn’t trace your web browser). 

**Open-source?** Although CounterMail uses open source algorithms to encrypt your data, the service itself isn’t open source.

**Cost:** There are no free accounts available, although you may sign up for a one-week free trial. Premium accounts allow for more storage and your own domain for a fee. The longest term account, 24 months, is the cheapest – $3.29/month.

**Features:** There are folders, but no tags. CounterMail also offers its users a free encrypted calendar with their account. Although storage is somewhat limited, there is always the option to buy more. You can set up CounterMail’s USB-key option to log in with a hardware token. The decryption key is stored on the USB-key so even if someone steals your password, they won’t be able to log in without the physical key. Something I found interesting is that if you delete your account, that alias can be used again, which means that emails that were meant for you can go to someone else (oops!).

**Intensity or ease of use:** Personally, the all-black and basic HTML design of the website is off-putting and I don’t think it would be super welcoming for someone who’s not interested in privacy. Further, downloading the desktop client requires Java, and managing your PGP keys yourself in settings requires knowledge of how PGP encryption works, which is hard even though they have lots of support available for new users. I’d say using CounterMail is a time investment.

## HushMail
HushMail markets itself mostly to businesses with strict privacy requirements like healthcare and law practices, where HIPAA compliance is mandatory and there are reporting and archiving requirements surrounding any electronic communication. I’m fairly certain this is what my doctor’s office uses.

**Encryption:** HushMail uses OpenPGP, like CounterMail and ProtonMail, and will allow you to send end-to-end encrypted messages to non-users by sending them a link to the email on a secure web page where they will enter a password you’ve communicated to them. Hushmail also had multiple whitepapers on its website detailing its security practices and philosophy, which I found interesting to read and thought was transparent, even if they don’t betray many technical details. HushMail’s servers are in Vancouver, Canada, a country that has a pretty good reputation for respecting privacy, even though some are skeptical because of its closeness with the United States and [some history with giving user information to the federal government]( https://www.theregister.co.uk/2007/11/20/hushmail_update/) 

**Open-source?** No, the software is proprietary.

**Cost:** There is no free account, only a 2-week free trial, and yearly fees are about $50. That being said, you do get 10GB of storage, email aliases, and 2 secure web forms.

**Features:** Hushmail has secure forms, which no other provider on this list promises, which can be used for medical intake forms or feedback surveys. The user layout is simple and allows for sending emails with RTF. Two-factor authorization is available, but make sure you don’t lose your password, because like most services on this list, your information is only decrypted with the password, so losing it means losing all your data.

**Intensity or ease of use:** This seems pretty easy to use! However, the fact that there is no free account is detrimental to a more casual user, who wants privacy but cannot afford or isn’t willing to invest $50/year into it.

## 

As always, feel free to tell me what email you prefer by visiting my [contact page](https://www.alexajakob.com/about.html).
