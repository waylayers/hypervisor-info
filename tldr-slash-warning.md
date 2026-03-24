# Warning from R.P.

This is a post from a member of the forum, R.P., which was shared by ResourcectoR into the discussion post for hypervisor.

---

Hi all,

Recently, a hypervisor developed by Makedev has been seeing traction as a potential solution to aid in Denuvo cracking. This is a huge step forward for analyses and tooling.

## What you need to know

So the goal is to crack Denuvo games, the Persona 5 Royal release seems it wont utilise a driver, but the plan is to use it in the future. This driver DOES come with significant security implications. I shall explain the technical requirements, and outline the security implications. If you test or install this be sure to disable it after usage. Let me explain some of the key concerns and why it shouldn't be left to stay active.

## The Technical Requirements - A Significant Tradeoff

The Makedev hypervisor is a kernel-level driver. This means it operates at the core of the operating system, granting it a high level of access.

Significant system modifications are required, disabling crucial Windows security features:
SVM Mode (BIOS), Test Signing Mode ( bcdedit), Secure Boot (BIOS ) , Windows Defender Memory Integrity/Credential Guard (VBS), & Hyper-V/Windows Hypervisor Platform.

Disabling these features significantly increases vulnerability to exploitation & malware. Open-source drivers, while transparent, present potential risks. Disabling security features like Secure Boot & VBS compromises the entire Windows security stack.

These drivers create significant security risks in your systems. It attracts users who are unaware of these risks, allowing malicious actors to analyze and exploit vulnerabilities. Proceed with extreme caution and only install if you fully understand the potential consequences.

Be warned.