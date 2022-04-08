![image](https://user-images.githubusercontent.com/94435318/162364801-6471da34-9ead-4c33-a168-dfa55c93bdfb.png)

# Common Attacks

With practical exercises see how common attacks occur, and improve your cyber hygiene to stay safer online.

----------------------------------------------------------------------------------------------------------

# 🟥 Task-5 Common Attacks - Passwords and Authentication

## Overview

For better or worse, passwords are an integral part of most authentication systems. We use passwords to protect everything, from our social media accounts to our banking applications. Unfortunately, despite their significant importance, it is still all-too-easy to create and use an insecure password, and even easier to take other actions that lower the overall security of the system. For example, even the most robust password in the world is useless if written on a whiteboard in full view of a web-camera — especially if the same password is used for more than one service.

This task will cover password security, as well as other measures you can take to strengthen your overall authentication security.


## What Makes A Strong Password?

<p align="center">
  <img src="![image](https://user-images.githubusercontent.com/94435318/162370878-7cc91e0b-bfc5-4c28-81a4-10bbc8d9d59a.png">
</p>

Advice on what constitutes a strong password has changed over time. In the past, people were advised to choose complex passwords that were easy to remember, for example:

@Ed1nburgh#1988-2000!

The password above is a collection of lowercase and uppercase characters, including symbols and numeric digits. It is over eight characters long (making it almost impossible to attack by brute-force with our current level of technology) and is created using knowledge that is unlikely to be held by anyone other than the owner of the password. Importantly, it also doesn't conform to normal patterns  (using unusual symbols, exchanging only some characters of l33t speak, and containing a date range as opposed to a single date), making it harder to guess. For all intents and purposes, this is a traditionally strong password. That said, the personal connection means that this password could potentially still be made weaker through social engineering or in-depth information gathering on a target.

Current best practices lean more towards length than complexity. For example:

Vim is _obviously_, indisputably the best text editor in existence!

By using a passphrase rather than a traditional password, the password is significantly longer whilst still retaining some of the more complex elements — despite not looking quite so obfuscated. This has the advantage of being easier to remember whilst still being incredibly difficult to brute-force.

Ideally, however, you should use long, completely random passwords. For example:

w41=V1)S7KIJGPN,dII>cHEh>FRVQsj3M^]CB

These take millions of years to crack and are objectively the most secure option available. The drawback is usability; however, this is largely mitigated by using a password manager, which will be discussed in the next task.

## What Makes A Weak Password?

People often go for simple passwords that mean something to them, often following one of a few "simple" patterns. For example, a commonly used pattern is a name/location, followed by a year, followed by an exclamation mark. For example:

Gareth2012!

This is enough to satisfy most password complexity requirements (lowercase and uppercase characters, over eight characters, contains numerical digits and a symbol); however, it is trivial to guess if an attacker knows that you have a son called Gareth who was born in 2012. This kind of password is inherently extremely insecure.

In short, any password that could easily be guessed by someone who knows you relatively well (this includes an attacker looking at your social media) is a bad idea!

Equally, short passwords (especially those that don't contain any non-alphanumeric characters) are weak against brute-force attacks. We will look at this in more depth later in the task.

Of equal importance to password strength is password reuse. You can have the strongest password in the world, but if you use it across numerous accounts and it gets leaked, an attacker can simply use the same strong password on all affected accounts. Equally, if you find out that your password has been exposed, you will have a lot of work to do changing all of your account passwords!

## Exposed Passwords

Unfortunately, not every service stores passwords securely (making it doubly important that you don't reuse passwords!).

### Background Information: Safe Password Storage (Click to read)

When you sign up for an online account, the provider must store a copy of your password in order to validate it the next time you sign in; but this poses a huge problem: how can the passwords be stored securely?

- Storing the passwords as plain text (e.g. the same way you submit them) isn't an option as every password will instantly be leaked if the database is ever hacked.
- Encrypting the passwords is an improvement, but not by much. If the passwords are stored encrypted, then they can also be decrypted — an attacker simply has to obtain the key, and they can turn every encrypted password back into plaintext. Encrypting passwords was part of what made the 2013 Adobe breach so serious.
- The industry-standard password storage method is referred to as password hashing. Password hashing (or simply "hashing") involves using complicated mathematical algorithms to take any input and turn it into a unique, fixed-length output in a way that is impossible to reverse. This means that when you sign up, your password will be hashed and stored in the database in a way that stops everyone (including server administrators) from being able to read it!
- When you try to sign in, the same algorithm is applied to the password that you supply: if the stored hash matches the hash of the password you are trying to log in with (remembering that the same input will always create the same unique output), then you are considered to have successfully authenticated.

Ideally, every service would hash user passwords with a secure algorithm. Even if the entire database were leaked, the attackers would still need to waste valuable time and computational power attempting to brute-force the (otherwise useless) hashes to find the plaintext passwords. This is why it is so important that passwords are long and preferably of a decent level of complexity: the longer the password and the larger the number of potential characters involved, the more power it takes to effectively guess the password input used to generate a hash.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162370968-67f7658f-83bb-4bde-b272-4521bd0b702d.png">
</p>

So, what happens if a service gets hacked and their database containing user account information gets leaked? As a best-case scenario, the service has used a secure hashing algorithm, and you have a strong password — in this case, your password is safe, but your email address or username may still be leaked publicly (so expect some spam emails).Decorative image of a broken chain

As a worst-case scenario, your plaintext password is either immediately available, or is easy for an attacker to find. If this happens then both your username and password are known to the attacker, allowing them to take over your account or perform "credential stuffing" attacks — using your stolen username and password pair against other services to see if you reused them elsewhere. These leaked databases containing credentials frequently appear on the dark web, which leads us to our final point in this section: data exposure notification services.

The largest and most well-known data exposure checker is called "Have I Been Pwned?". It exists as a free online service that scours data dumps and catalogues all of the information found, allowing users to enter their email addresses to see if they have been included in any breaches. Have I Been Pwned also allows you to add yourself to a notification list, meaning that you will receive an email notifying you if your email address appears in any data breaches.

Whilst not a perfect defence, notification services give you a vital early warning to change your passwords (hopefully) before you get hacked.

## Password Attacks

An attacker has a few options when it comes to attacking passwords and authentication systems. Some attacks are entirely local (i.e. working entirely on a device owned by the attacker without interacting with the target service at all), others are remote attacks involving the original server.

Local attacks require a stolen copy of the credentials in question. The attacker will take a file full of stolen usernames/emails and hashed passwords, then use software to effectively try to guess the input that created the hash either using randomly generated sequences of characters (slower but more thorough) or by using a pre-generated wordlist of possible passwords (faster but much more likely to miss things). Hybrid types are also very widely used; these are when an attacker takes an existing wordlist and mutates it to add new characters, symbols, or random elements. Local password attacks will be demonstrated in the interactive element for this task.

Remote attacks tend to be one of two categories; they either involve attempting to brute-force known usernames by sending requests to the server and seeing what it responds with, or they use known username and password pairs from previous breaches to see if they are valid on the target site — this is the aforementioned credential stuffing.

---------------------------------------------------------------------------------------------------------

Answer the questions below------------------------------------------------------------------------
-- 


Put yourself in the shoes of a malicious hacker. You have managed to dump the password database for an online service, but you still have to crack those hashes!

### 1. Click the green button at the start of the task to deploy the interactive hash brute-forcer!

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161687394-218a79b1-ce0d-49f2-8dfb-53600bdbed33.png">
</p>

Based on the content of the website, you have generated a list of likely passwords, which is as follows:

    TryH@ckMe
    TryHackMe123
    THM123456
    qwertyuiop123
    TryHackMe2021
    TryHackMe123!
    TryHackMe345
    TryHackM3!

### 2. Copy the list of passwords into the "Password List" field of the hash cracker, then click "Go"!

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161687394-218a79b1-ce0d-49f2-8dfb-53600bdbed33.png">
</p>

Look at the "Current Word / Hash" section of the hash cracker.

Notice that for each word in the list you entered, the cracker is creating an MD5 hash of the word then comparing it to the Target Hash. If the two hashes match then the password has been found!

The hash cracker should find the password that matches the target hash very quickly.

### 3. What is the password?

- Answer: TryHackMe123!

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162371695-95468476-1e82-4bb2-abf1-cebb7b32ede8.png">
  <img src="https://user-images.githubusercontent.com/94435318/162371737-b3a557d4-2d96-401a-92d8-dc3ee89f9ed0.png">
</p>

This is a very simple, browser-based example; however, in reality local hash cracking with a wordlist isn't any more complex from a high-level perspective — it's the same technique, but with a lot more potential passwords!

Hopefully this example illustrates why it is so important to choose a strong password — even if the passwords are hashed appropriately.

### 4. In the next task we will look at some of the common account protection measures, as well as how to generate secure passwords.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161687394-218a79b1-ce0d-49f2-8dfb-53600bdbed33.png">
</p>

