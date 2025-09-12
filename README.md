# Independent Security Research Findings for MDM (Mosyle Manager) controlled Apple MacBooks

## Overview
This repository contains a list of many hypothetical and theoretical vulnerabilities and exploits that could be discovered by independent research in a controlled and locked-down environment.
The main purpose of this is to help learn more about potential cyberthreats, attack vectors, and also some defense knowledge. These changes are hypothetical and theoretical and could be exploited on computers controlled and operated by the Diocese of Charlotte and CCHS

---

## Project: Analyzing Security in Controlled Environments

## Summary
A well-tested assesment of a managed MacOS that is controlled by MDM (Mosyle Manager) and is supposed to shield against potential mis-use and threatening or harmful content.
Two exploits could be found using MacOS's Terminal and another method which I will soon describe.

## Findings

## 1: Theoretical Basic External Drive Bypass
-Risk Level: Critical

-Description and Summary: MDM does limit the use of certain unsigned and downloaded applications by prohibting and password locking the application folder to administrator access.
However, using a very simple technique, you are able to effecitvely bypass this altogether. Setting up an external disk drive, you are able to launch a application from the external
drive without any interruptions.

-How?: Pre-compiled apps can run directly from a disk drive, no files touched on the main system at all.

-Result?: Full access to unsigned apps and software without authorization.

## 2: Theoretical Symlink Terminal Bypass Command
-Risk Level: High

-Description and Summary: Apps that are not pre-compiled and do need to run off the main system drive can still be launched. This is where the symlink command comes into play.
Symlink is able to mimic a drive to think the file is there but it's actually on a different drive. Think of it as a shortcut.

-How?: Terminal commands are rarely logged and easily usable, somebody with simple knowledge can use this with more malicious intent.

-Result?: Access to unsigned apps and software that can be used on the main system drive. Disabling WiFi makes this method completely untraceable.

## Programmable Microcontroller Emulation
-Risk Level: Critical

-Description and Summary: Using custom programmable microcontrollers such as Raspberry Pis can mimic keystrokes, open terminal, run commands, and download and execute various scripts.

-How?: Inserting it via USB-C and executing your custom made executions.

-Result: Full command executions without any interruptions bypassing all software restrictions.

## The Classic Linux Dual Boot
-Risk Level: Critical

-Description and Summary: Linux is an open-source Operating System. Linux is considered one of the most portable and compatible OS's to date and there are mant versions called Distros, short for distribution. Dual Booting with Linux is very possible.

-How?: Install a Linux Distro from the internet via your own personal computer. Export the Linux OS onto your USB Drive(preferably a 32GB Drive, Linux is lightweight). Restart the Macbook and hold Option (⌥) key as soon as the start-up chime happens. This will launch Startup Manager, which is very accessible even on controlled Macs due to it being a low-level firmware function. Install Linux through the External Drive and you have successfully bypassed every safeguard on the Mac.

-Result?: MacOS safeguards completey bypassed. DiLL Kernel Extensions, CCHS Policies, DNS Rerouting, VPN Blocks, completey removed. You are running your own OS, and a better one at that. Full access to everything, games could be exploited by loading Android Emulators allow further control. 0 forensic traces as this is a start-up level bypass. Mosyle only runs once the OS has been launched. This is entirely firmware based exploit, completey untraceable unless it was physically witnessed.

## Proposed Mitigation Strategy
-Restrict any binary from removable hardware or media using the MDM.

-Lock down the Terminal or implement a solution that limits certain commands.

-Lock down external booting via a Firmware Password.

## Disclaimer
**IMPORTANT** This research is purely theoretical and for educational purposes only. No malicious intent is involved with this theory and is purely for the education of other IT officials in the
industry. The author **does not condone, encourage, or participate** in the unauthorized testing of any computer systems. Always obtain explicit, written permission before testing any network or system that you do not own.

© 2025 - Pete Research | Security Enthusiast
