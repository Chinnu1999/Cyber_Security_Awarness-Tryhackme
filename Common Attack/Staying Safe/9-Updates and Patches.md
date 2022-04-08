![image](https://user-images.githubusercontent.com/94435318/162364801-6471da34-9ead-4c33-a168-dfa55c93bdfb.png)

# Common Attacks

With practical exercises see how common attacks occur, and improve your cyber hygiene to stay safer online.

----------------------------------------------------------------------------------------------------------

# 🟥 Task-9 Staying Safe - Updates and Patches

## ﻿Software Updates

Updates are an essential part of the software development lifecycle; they allow developers to add new features, fix bugs and otherwise simply alter aspects of the product. When vulnerabilities are discovered in software, the developers usually release special updates called patches that contain a fix for the vulnerability or otherwise "patch" the security issue.

For this reason, it is imperative that you update software whenever possible — especially for things like operating systems (e.g. Windows or macOS) where vulnerabilities can be particularly dangerous, as seen in the case study below.

Case Study: Eternal Blue (Click to read)

Eternal Blue is believed to have been discovered by the United States National Security Agency (the NSA) and was leaked to the general public in April 2017. The vulnerability affects an integral part of the Windows operating system and gives a remote attacker complete control over the target at the highest level of privileges. You can see this for yourself in the "Blue" room on TryHackMe.

Microsoft quickly released a patch (the infamous MS17-010) which was designed to remove the vulnerable component in the software; however, many administrators simply chose not to download it for one reason or another.

Why is this important? Eternal Blue was the transmission vector that the Wannacry ransomware (discussed in task 4) used to spread and infect new devices! Eternal Blue gave full access to a target remotely, making it a perfect vulnerability to exploit with a self-replicating virus. Despite a patch having been made available months before the appearance of Wannacry, the ransomware was still able to attack millions of unpatched systems, with devastating effects.

You can read more about Eternal Blue here.

Unfortunately, all software eventually loses support from its maintainers, becoming deprecated and no longer receiving updates (e.g. Windows 7) — this is referred to as the software being EOL (End Of Life). At this point, the software must be replaced as soon as possible. If replacing the software is not possible then the device should be segregated as far as is possible to prevent exploitation of the vulnerabilities that will inevitably be found and left unpatched.


## Antivirus Updates

Most antivirus software packages receive very frequent updates; this is because they largely work using a local database of known exploit signatures, which must be kept up-to-date.

In other words: when new malware is discovered, it gets sent around antivirus vendors who generate a "signature" that identifies this particular piece of malicious software. These signatures are then distributed to every device on the planet that uses the antivirus software, ensuring that your installed antivirus solution is kept up-to-date on all the latest (known) malware.

If antivirus software is not allowed to update it will still be able to catch some malware through other methods. However, the local signature database will quickly become outdated, resulting in malicious software potentially falling through the gaps. In short: if the antivirus wants to update, let it!

------------------------------------------------------------

Answer the questions below--------------------------------------------------------------------------
--

### (Optional) Complete the Blue room on TryHackMe to see the brutal effects of the Eternal Blue exploit in action against an unpatched machine for yourself!

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161687394-218a79b1-ce0d-49f2-8dfb-53600bdbed33.png">
</p>

-----------------------------------------------------------------
