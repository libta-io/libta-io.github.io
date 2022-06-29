---
title: "Anonsurf for Anonymity"
header:
toc: true
toc_sticky: true
excerpt_separator:  <!--more-->
categories:
  - Hacking
tags:
  - Kali
  - Guides
  - Anonymity
  - VPN
  - Proxy
  - Helpful
  - Privacy
---

<!--more-->

## What is Anonsurf?

Anonsurf is one of the good anonymizing tools of Linux distribution. It helps us make our network tunnel secure. This tool uses TOR iptables to anonymize our network system. Anonsurf is a tool that will help you stay anonymous by routing every packet through TOR relay. When you use Anonsurf for ethical hacking, all the traffic from your system goes through a TOR proxy server due to which your IP address is changed.

## Installation of Anonsurf

First of all, you can make a separate directory for this tool for your convenience and git clone the following URL or you can simply run this command in the terminal:

**For a separate directory**:

```text
libta@kali:~/anonymity# mkdir Anonsurf && cd Anonsurf
```

**Clone the URL in your terminal**:
```text
libta@kali:~/anonymity/Anonsurf# git clone https://github.com/Und3rf10w/kali-anonsurf.git
Cloning into 'kali-anonsurf'...
remote: Enumrating objects:321, done.
remote: Total 321 (delta 0), reused 0 (delta 0), pack-reused 321
Receiving objects: 100% (321/321), 167.72 KiB | 439.08 KiB/s, done.
Resolving deltas: 100% (99/99), done.
```

**Now change the directory and go to the kali-anonsurf run the installer script:**
```text
libta@kali:~/anonymity/Anonsurf/# cd kali-anonsurf
```
```text
libta@kali:~/anonymity/Anonsurf/kali-anonsurf# sudo ./installer.sh
--2022-06-19 17:46:46-- https://geti2p.net/_static/i2p-debian-repo.key.asc
Resolving geti2p.net (geti2p.net)... 2a02:180:2:c1:81:7:7:63, 81.7.7.63
Connecting to geti2p.net (geti2p) |2a02:180:2:c1:81:7:7:63|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 18019 (18K) [text/plan]
Saving to: '/tmp/i2p-debian-repo.key.asc'

/tmp/i2p-debian-repo.key 100%[=======================>] 17.60K 72.1KB/s in 0.2 s

2022-06-19 17:46:46 (72.1 KB/s) - '/tmp/i2p-debian-repo.key.asc' saved [18019/18019]
```

## Usages

**Now run this command for anonsurf start:**
```text
libta@kali:~/anonymity/Anonsurf/kali-anonsurf# sudo anonsurf
Usage:
 anonsurf {start|stop|restart|change|status}

 start - Start system-wide anonymous
          tunneling under TOR proxy through iptables
 stop - Reset original iptables settings
          and return to clear navigation
 restart - Combines "stop" and "start" options
 change - Changes identity restarting TOR 
 status - Check if AnonSurf is working properly
----[ I2P related features ]----
 starti2p - Start i2p services
 stopi2p - Stop i2p services
```

**To start this tool just simply run this command, a pop-up will show on your screen:**
```text
libta@kali:~/anonymity/Anonsurf/kali-anonsurf# anonsurf start
```

**If this tool isn’t running and you are running the stop command a pop up will show as shown in figure:**
```text
libta@kali:~/anonymity/Anonsurf/kali-anonsurf# anonsurf stop
```

**You can restart it again if you face any problem during the task:**
```text
libta@kali:~/anonymity/Anonsurf/kali-anonsurf# anonsurf restart
```

**To changes identity:**

This tool connects our system with the tor browser and if we want to change or IP address then we can use this command, in the following images you can see our system is connected with tor or not.
```text
libta@kali:~/anonymity/Anonsurf/kali-anonsurf# anonsurf change
```

**You can check what is current IP address is after connecting with tor network:**
```text
libta@kali:~/anonymity/Anonsurf/kali-anonsurf# anonsurf myip
```

**Change status or check the status:**
```text
libta@kali:~/anonymity/Anonsurf/kali-anonsurf# anonsurf status
```

Thanks for reading!
