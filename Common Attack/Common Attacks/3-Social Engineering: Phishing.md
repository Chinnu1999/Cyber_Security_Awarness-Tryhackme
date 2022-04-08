
![image](https://user-images.githubusercontent.com/94435318/162364801-6471da34-9ead-4c33-a168-dfa55c93bdfb.png)

# Common Attacks

With practical exercises see how common attacks occur, and improve your cyber hygiene to stay safer online.

----------------------------------------------------------------------------------------------------------

# 🟥 Task-3 common Attacks - Social Engineering: Phishing

## Overview

Phishing is one of the most common cyber attack types employed by scammers and bad actors, targeting individuals and businesses indiscriminately. In many cases, phishing is the initial attack vector used to gain access to a company's infrastructure before performing further attacks against the corporate network. Whilst there are many automated tools now available to help combat phishing threats, phishing is still one of the most prolific attack vectors around.

## What is Phishing?

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162368885-23d79f72-c008-4288-a787-97b3495ba828.png">
</p>  

Phishing is a sub-section of social engineering. Whereas social engineering is a very general term used to describe any attack that takes advantage of a human rather than a computer system, phishing specifically describes attacks whereby a scammer or other attacker tricks a victim into opening a malicious webpage by sending them a text message, email, or another form of online correspondence. Traditionally, "phishing" simply referred to emails; however, in the days of instant messaging, text messages, and voice/video calling, the term has evolved to blanket these other categories. These other forms are sometimes referred to individually as "smishing" — phishing over SMS — and "vishing" — phishing over voice chat — respectively. These attacks are very widespread (indeed, the chances of you not having been on the receiving end of such an attack are slim!) and are frequently deployed on massive scales using lists of leaked or stolen phone numbers and email addresses.

Phishing messages usually deploy psychological trickery (for example, inducing a false sense of urgency to make victims act rashly) and nearly always involve getting a victim to click on a link to a web application owned by the attacker. The victim is then often asked to enter sensitive information — for example, login details or credit card information — at which point the malicious site stores the information and the attack is complete. Alternatively, the victim may inadvertently install malware from the malicious page, thus giving an attacker an entry point into their device and network.

There are three primary types of phishing attacks:

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162368941-3e8b7547-d090-4cda-9244-ee5494bc5183.png">
</p>

Be aware that you are much more likely to encounter a general phishing attack than a spearphishing or whaling attack in your day-to-day life. This may not be the case in your work life, however — especially if you are a high-ranking member of a company.

An example of a popular general phishing scenario (or "pretext") would be receiving an email purportedly from "Amazon", informing you that your account has been used to buy a very costly item (e.g. the latest iPad). You are then provided with a link to view your purchase history. The link looks like it goes to https://amazon.co.uk but will actually take you to an attacker-controlled web application (that looks identical to the Amazon login page), asking you to enter your Amazon credentials. When you enter your credentials, you get redirected to the real Amazon orders page, where you find that there are no unauthorised purchases... yet. The attacker will then use your duly provided credentials to actually order expensive items with your account.

This process is shown in the following diagram:

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162369106-30f17984-bd7a-4bc0-a3d7-a7f14df12afb.png">
</p>

1. The attacker sends out a malicious phishing email campaign
2. Prospective victims receive the emails — some of them open the email and click the link
3. The victims enter their credentials into the attacker's fake web page
4. The web page stores the credentials or sends them directly to the attacker
5. The attacker uses the credentials to access the site, thus taking over the victims' accounts

Phishing attacks work best when the malicious web page mimics an existing (usually well-known) web page. For this reason, attackers/scammers will usually use one of many freely available tools to simply clone an existing page, which can then be edited at their leisure.

The end goal of a phishing attack can vary significantly depending on who is performing the attack. For example, a low-level scammer may simply be after sensitive information (e.g., bank details), whereas a high-powered group of malicious hackers may be targeting a specific organisation with the intention of causing further damage.


## Identifying Phishing Attacks

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162369252-136b41e9-80a7-4376-b5e5-91f51e832e48.png">
</p>  

Many generic phishing attacks are relatively easy to spot; they frequently have poor grammar and often do not address their victims by name (instead leaving the greetings generic — e.g., "Dear customer"). That said, other instances can be extremely difficult to spot, with some attacks being thorough enough to fool cybersecurity professionals.

Regardless of the attack type, in many cases, the pretext will be plausible — for example: the Amazon scam listed above, or a (fake) message from your "bank" telling you that there has been unusual activity with your account and to please log in to review it. This is especially true for spearphishing or whaling attacks where the pretext will be very carefully tailored to the target.

Equally, the domain name for the malicious site will usually be similar (but never identical) to the domain name used by the legitimate website. As a real-world example from 2021, a group of scammers sent out a mass phishing campaign over SMS, mimicking the British Royal Mail service and using the domain name https://royalmai1.co.uk (as opposed to https://royalmail.co.uk). By exchanging the final "L" for the number one, the scammers were able to successfully register a domain name that looked almost identical to the domain name of their cloned website; this is a very common tactic.

Also, bear in mind that HTML emails (effectively any email that looks fancy and contains formatting/graphics) can also be used to mask the real domain name in use. For example, the text in the email may be "https://amazon.co.uk"; however, the link actually goes to "https://am4zon.co.uk". You can see this by hovering your mouse over the link in a desktop application — the real link should appear at the bottom of the screen as in this graphic:

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162369320-533aa7de-b545-4355-be18-7ee3e15774e4.png">
</p>  

You can try this for yourself with the link below!

https://tryhackme.com

In a similar vein, the "From" email address in an email-based phishing campaign will often be suspicious. Many generic mass phishing campaigns will simply use Gmail addresses — not bothering to use a domain name associated with the company they are spoofing. This is a dead giveaway that the email is suspicious.

The best way to identify a phishing email is simply to keep your eyes open and look for anything suspicious — all but the best will have a mistake somewhere.

## Staying Safe from Phishing Attacks

There are a variety of things that you can (and should!) do to keep yourself safe from phishing attacks:

- Delete unknown or untrusted emails without opening them. If you can see anything suspicious in the email, also report it as spam to your email provider, or forward it to your IT Security department if you received the email at work.
- Never open attachments from untrusted emails — this includes any attachments from a legitimate contact that you were not expecting.
- Do not click on embedded links in emails or messages. Where possible, navigate to the real website in your web browser and access the content that way. If you absolutely must click on the link, ensure that the domain name is correct and that the link points to where you think it does.
- Always make sure that your device and antivirus software are up-to-date.
- Avoid making your personal information (e.g. email address and phone number) public if possible. If you must publish personal details publicly, create a "burner" email address (a temporary address made for one purpose, then destroyed soon afterwards) for the occasion, then destroy it as soon as it is no longer required.

It's worth noting at this point that anyone can fall for a phishing attack — especially a complex one that has been made to look very realistic. If you accidentally fall for one, don't panic! Make sure that you change any affected passwords immediately, and contact IT Services if the attack happens at work.

----------------------------------------------------------------------------------------------------------

Answer the questions below---------------------------------------------------------------------------
--

### 1. Click the green "View Site" button at the top of this task if you haven't already done so.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161687394-218a79b1-ce0d-49f2-8dfb-53600bdbed33.png">
</p>

The static site will display a series of emails and text messages. You will be asked to identify which of these messages are genuine and which are phishing attempts. Once you have successfully identified all of the messages you will be presented with a flag to enter, here.

Good luck!

### 2. What is the flag?

- Answer: THM{I_CAUGHT_ALL_THE_PHISH}

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162369801-aeb63ee6-dca9-4d6e-8c80-4f992589df5d.png">
</p>

--------------------------------------------------------------------------------------------------------
