![image](https://user-images.githubusercontent.com/94435318/162364801-6471da34-9ead-4c33-a168-dfa55c93bdfb.png)

# Common Attacks

With practical exercises see how common attacks occur, and improve your cyber hygiene to stay safer online.

----------------------------------------------------------------------------------------------------------

# 🟥 Task-6 Staying Safe - Multi-Factor Authentication and Password Managers

﻿Overview

In the previous task, we looked at some of the common attacks made against passwords and authentication systems. We also looked at what makes a password weak or strong. This task will cover some of the extra steps that you can take to enhance your password security through the use of password managers and multi-factor authentication.


Multi-Factor Authentication

Multi-Factor Authentication (or MFA) is a term used to describe any authentication process where you need more than one thing to log in. The most common example of this is when you enter the password for an account, then get asked for a six-digit code that is sent to your phone and usually expires after fifteen minutes or so. This particular second authentication factor is referred to as a Time-based One Time Password (or TOTP) and is one of the most common second factors currently in use.

Background Information: Three Factors of Authentication (Click to Read)

There are three main factors that can be considered when implementing multi-factor authentication; these are:

- Something you have (e.g. a smart card, a TOTP, or a hardware authenticator such as a "YubiKey". You may also have experienced your bank asking you to insert your card into a card reader and enter your PIN code before allowing access to online banking services — this is the same principle)
- Something you know (e.g. a password)
- Something you are (i.e. biometric data such as a fingerprint or iris scan)

An ideal authentication uses all three of these — for example; it may require a password, a smart card, and a fingerprint before allowing the user access to the system.

Unfortunately, most individuals do not have access to a smart card reader, an expensive hardware authenticator (e.g. the aforementioned YubiKey) or a fingerprint scanner. They do have access to a smartphone which can be used to receive or access time-based one time passwords. As such, mobile-based MFA is amongst the most common multi-factor authentication methods implemented for personal use. Whilst not ideal, two factors are better than one.

You should always activate multi-factor authentication where available. Doing so means that an attacker must obtain more than one factor if they wish to compromise any of your accounts — for example, they must have both the password and your phone (or the ability to intercept your text messages). Many people see it as an "unnecessary hassle"; however, it is well worth it for the added security!

Unfortunately, SMS (text message) based TOTP authentication — despite being the most commonly used — is far from the most secure as there have been documented cases of attackers managing to reroute a victim's texts without undue difficulty[1].

So, if not SMS then what? Time-based one-time passwords are still the most accessible form of second-factor authentication for most users; fortunately, it's possible to generate them yourself!

Most services will provide you with an option to use an "Authenticator App" for MFA. When you select this option, you will be presented with a QR code as well as a "secret key" — either of which can be scanned or imported into an app such as Authy or Google Authenticator (Android | IOS). Once you have added your secret key for the application, these apps can generate TOTP codes entirely on your device without requiring any network connectivity or interceptable SMS.


## Password Managers and Generating Strong Passwords

As mentioned previously, the most secure passwords are simply long, completely random strings of characters, digits, and symbols. Unfortunately, these random passwords are very difficult to memorise — indeed, memorising a different 60-digit, randomly generated password for every online account is simply not feasible for most people.

Enter: Password Managers.

<p align="center">
<img width="125" alt="9b9eb96ff037c84f97d164ad45821ebd" src="https://user-images.githubusercontent.com/94435318/162372461-6a2aa082-cca6-4efb-a395-6fb5e13c8958.png">
</p>

At the most basic level, password managers provide a safe space to store your passwords. They store passwords in "vaults": encrypted storage either locally on your own device, or as an online service (which also usually allows you to access your passwords from any device). These vaults are accessed using a master password — the only password you need to remember —  or (more commonly in recent years) biometric data such as a fingerprint. Some password managers are free, whilst others require a paid subscription. That said, the features and usability provided by paid offerings often make them well worth the expense!

![5e5f7d9774935f71fd5546612b6db1c9](https://user-images.githubusercontent.com/94435318/162372482-7c272029-5966-4a68-9825-e0fd405bc620.png)

The more fully-featured password managers usually also include a range of additional capabilities, such as storing other types of data (e.g. images, files, etc.), auto-filling passwords automatically for other services, and secure password generation. Having these features available means that you can quickly and easily generate very strong passwords and store them automatically, then seamlessly have the password entered for you when you attempt to log into an app, all within the same application.

Password managers are the recommended way to handle authentication for your many accounts; however, it is worth remembering that the security of the whole structure can revolve around a single master password, so make sure that it's solid!

Some common password managers include:

- 1Password
- LastPass
- KeePass
- Bitwarden

There are many others available! Each password manager has its own advantages and disadvantages, so it is well worth doing some research to find the one that suits you best.

1. https://krebsonsecurity.com/2021/03/can-we-stop-pretending-sms-is-secure-now/

---------------------------------------------------------------------------

Answer the questions below------------------------------------------------------------------------
--

### Where you have the option, which should you use as a second authentication factor between SMS based TOTPs or Authenticator App based TOTPs (SMS or App)?

-Answer: APP

-------------------------------------------------------------------
