---
title: "Update Kali Linux"
header:
toc: true
toc_sticky: true
excerpt_separator:  <!--more-->
categories:
  - Kali Linux
tags:
  - Kali
  - Guides
  - Helpful
---

<!--more-->

## Introduction

Today we will learn how to update and upgrade Kali Linux to the latest version. If you are using the default installation of Kali, you should check for new updates from time to time. If you need a new version of a tool or a security update, it can speed up your system.

To update Kali Linux, first of all, we need to check our repository file and the location of the file is /etc/apt/sources.list. The following code should be in the file.
```text
deb http://http.kali.org/kali kali-rolling main contrib non-free
deb-src http://http.kali.org/kali kali-rolling main contrib non-free
```
To verify this, we will type this command:
```text
┌──(libta㉿kali)-[~]
└─$ cat /etc/apt/sources.list
# See https://www.kali.org/docs/general-use/kali-linux-sources-list-repositories/
deb http://http.kali.org/kali kali-rolling main contrib non-free

# Additional line for source packages
# deb-src http://http.kali.org/kali kali-rolling main contrib non-free

deb http://http.kali.org/kali kali-rolling main non-free contrib
deb-src http://kali.download/kali kali-rolling main non-free contrib
```

## Update Kali Linux

Now we have to update our Kali Linux packages index list. Open your terminal and enter the following command:
```text
┌──(libta㉿kali)-[~]
└─$ sudo apt update  
```
If you want to display all packages which are scheduled for an update:
```text
┌──(libta㉿kali)-[~]
└─$ sudo apt list --upgradable
```
Now we can upgrade individual packages using sudo apt install PCKAGE_NAME or we can upgrade the entire system using this command:
```text
┌──(libta㉿kali)-[~]
└─$ sudo apt full-upgrade -y
```
If all went well, your Kali Linux system is now fully updated.
```text
┌──(libta㉿kali)-[~]
└─$ sudo apt update
[sudo] password for libta:
Hit:1 http://kali.download/kali kali-rolling InRelease
Reading package lists... Done
Building dependency tree... Done
All packages are up to date.
┌──(libta㉿kali)-[~]
└─$ sudo apt list --upgradable
Listing... Done
┌──(libta㉿kali)-[~]
└─$ sudo apt full-upgrade -y
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
Calculating upgrade... Done
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
```

## Uninstall packages that are no longer needed

Now, after the system updates, some of the packages may not be used anymore, and therefore not be needed anymore.

To remove all Kali Linux packages that are no longer needed, run the following command:
```text
┌──(libta㉿kali)-[~]
└─$ sudo apt autoremove
Reading package lists... Done
Building dependency tree... Done
Building state information... Done
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
```

Thanks for reading!