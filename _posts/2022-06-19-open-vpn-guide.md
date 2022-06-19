---
title: "What is OpenVPN? How does OpenVPN work?"
header:
toc: true
toc_sticky: true
excerpt_separator:  <!--more-->
categories:
  - Guides
tags:
  - Privacy
  - Anonymity
  - VPN
  - Guides
---

<!--more-->

## Why use a VPN?

A VPN, or virtual private network, is an indispensable tool for accessing content and protecting your personal data on a public Wi-Fi network or on your home network. 

## What is OpenVPN?

OpenVPN is both a VPN protocol and software that uses VPN techniques to secure point-to-point and site-to-site connections. Currently, it is one of the most popular VPN protocols among VPN users.

Programmed by James Yonan and released in 2001, OpenVPN is one of the only open-source VPN protocols that also has its own open-source application (SoftEther being the other).

## How does OpenVPN work?

The OpenVPN protocol is responsible for handling client-server communications. Basically, it helps establish a secure "tunnel" between the VPN client and the VPN server.

When OpenVPN handles encryption and authentication, it uses the OpenSSL library quite extensively. In addition, OpenVPN can use UDP (User Datagram Protocol) or TCP (Transmission Control Protocol) to transmit data.

If you are not familiar with TCP and UDP, they are transport layer protocols, and are used to transmit data online. TCP is more stable since it offers error correction features (when a network packet is sent, TCP waits for confirmation before sending it again or sending a new packet). UDP does not perform error correction, which makes it a little less stable, but much faster.

OpenVPN works best over UDP (according to OpenVPN.net), which is why OpenVPN Access Server tries to establish UDP connections first. If these connections fail, only then does the server try to establish TCP connections. Most VPN providers also offer OpenVPN over UDP by default.

Because of the way it is programmed (it is a custom security protocol), the OpenVPN protocol can easily bypass HTTP and NAT.

Unlike most VPN protocols, OpenVPN is open-source. This means that its code is not owned by a single entity, and third parties can always inspect and continuously improve it.

## OpenVPN explained in depth - General technical details

- Typically, OpenVPN uses 256-bit OpenSSL encryption. To further strengthen the security of the connection, OpenVPN can use AES, Camellia, 3DES, CAST-128, or Blowfish algorithms.

- Although OpenVPN does not support L2TP, IPSec and PPTP, it uses its own custom protocol based on TLS and SSL.

- OpenVPN supports improved login and authentication processes with the use of third-party plugins and scripts.

- Clients can actually connect to servers beyond the OpenVPN server since it offers support for private subnet configuration.

- To protect users from buffer overflow vulnerabilities in TLS/SSL implementations, DoS attacks, port scanning and port flooding, OpenVPN relies on tls-auth for HMAC signature verification. OpenVPN is also programmed to remove privileges if necessary, and runs in a dedicated CRL environment.

- OpenVPN works in user space instead of kernel space.

## Is it safe to use OpenVPN?

Yes, in fact, OpenVPN is one of the most secure VPN protocols you can use right now. Most VPN providers and security experts recommend sticking to OpenVPN if you want to enjoy a private, unmonitored, hacker-free online experience.

## What is the speed of OpenVPN?

Speed isn't really OpenVPN's main strength, but you tend to get decent connection speeds if you have enough bandwidth. The reason why your speeds tend to drop quite often with OpenVPN is mainly due to its strong encryption. Of course, [other factors can come into play as well](https://www.reviews.org/vpn/will-a-vpn-slow-down-your-internet/#:~:text=Most%20likely%2C%20yes%3A%20a%20VPN,part%20in%20your%20internet%20speed).

Generally, you can get faster speeds if you use OpenVPN over UDP instead of TCP.

## How to use OpenVPN

OpenVPN isn't exactly the most user-friendly protocol on the market, and setting up a connection can be a bit daunting.

In this section, we will cover the Windows installation process as it was the most requested. The Android and iOS installation processes follow similar steps to the ones we'll cover here. Installing and using OpenVPN on Linux is quite complex, but [here is the main reason to do it](https://openvpn.net/vpn-server-resources/connecting-to-access-server-with-linux/) (you can also find [additional information here](https://openvpn.net/community-resources/how-to/)).

Now, before we move on, let's mention that in order to establish an OpenVPN connection, you will need a subscription to a VPN service. While you can set up your own OpenVPN server, it's extremely difficult, and most tutorials that are available online only cover Linux platforms.

Now that that's out of the way, here's what you need to know about using the OpenVPN protocol:

**First, get the configuration files**

To connect to your provider's servers, OpenVPN needs certain configuration files that define how a connection is made. As long as you choose a decent [VPN provider](https://www.techopedia.com/definition/30762/vpn-service-provider), you should be able to find all the configuration files you need on their download page.
  
**Install the OpenVPN client**

Once you have the configuration files, you need to install the OpenVPN client on your device. You can easily find the installers you need on the [OpenVPN.netdownload page](https://openvpn.net/community-downloads/). Simply run the installer, accept the default options, choose another installation destination folder if you wish, and continue the installation process.

When finished, your default text viewer may open a new file to display a guide with technical details. You can read it if you wish, but at this point it is also safe to close the file.

**Now import the VPN data**

To start OpenVPN, you need to launch the OpenVPN GUI application. It will add the service to your System Tray (the small taskbar in the lower right corner). Then copy all the downloaded OVPN files to the "Config" subfolder of the OpenVPN installation folder.

Now, if you click on the OpenVPN icon in your System Tray, you should be able to see the names of all the files you just copied. If it's easier for you, you can rename the files.

**Establish the connection**

To connect to a server, simply click on the OVPN files in the OpenVPN application. When prompted, enter your login credentials. If all goes well, you should see a log screen with status commands that will disappear when the connection is established.

You should receive a desktop notification that the connection has been successfully established. Also, if you look at the OpenVPN icon, you should see a green screen. When you hover over it, you will see a tooltip telling you the server name and your new IP address.

At this point, [you can try to test the connection](https://www.whatismyip.com/) to make sure that everything is in order.

To disconnect, simply click on the OpenVPN icon, choose the server you are connected to, and then click "Disconnect."
  
**Adjustment of parameters (basic and advanced)**

The OpenVPN application doesn't have many settings, but you can still play with some of them.

For example, you can go to "Settings" and make sure that OpenVPN launches automatically when you start your operating system. You can also get rid of the log screen that appears when you connect to a server by checking the "Silent connection" option. And be careful with the "Never" option as it disables desktop notifications.

In case you want to change your connections, you can open the OVPN files themselves (we recommend you do this with WordPad) to see what commands are assigned to them. If you are knowledgeable enough, you can change existing commands or add new ones. Here are some commands that might be of interest to those of you who are more experienced:

  * The "proto" command — This command allows you to switch between UDP and TCP. Simply add the name of the protocol after the command, like this: "proto udp."

  * The "remote" command — This is the line that tells OpenVPN the name of the server you want to use. It usually includes the port after the VPN server name. If you know other ports that your provider uses, you can switch between them here.

  * The "tun-mtu" command — This command represents the maximum value of the transmission unit. It is usually set around 1500, but you can try to change it to increase performance.

In addition, you can check the "doc" subfolder of your OpenVPN installation folder for more advanced documentation that can show you how to do other things (like setting up scripts for when your VPN disconnects, or blocking DNS leaks). [You can also check the Reference Manual](https://openvpn.net/community-resources/reference-manual-for-openvpn-2-4/) available at OpenVPN.net for more information.

## Advantages and disadvantages of OpenVPN

**Advantages**

  * OpenVPN is a very secure protocol, capable of using 256-bit encryption keys and high-end encryption algorithms.

  * The OpenVPN protocol can easily bypass any firewall it encounters.

  * Since OpenVPN can use TCP and UDP, it gives you more control over your connections.

  * OpenVPN works on a wide range of platforms. Some examples include Windows, macOS, iOS, Android, Linux, routers, FreeBSD, OpenBSD, NetBSD, and Solaris. OpenVPN supports [Perfect Forward Secrecy](https://www.techtarget.com/whatis/definition/perfect-forward-secrecy#:~:text=Perfect%20Forward%20Secrecy%20(PFS)%2C,unique%20session%20key%20is%20generated.).

**Disadvantages**

  * Manual configuration of the OpenVPN protocol can be quite difficult on some platforms.

  * Sometimes you may experience drops in connection speed due to strong encryption.

  * OpenVPN requires third-party applications to run.

## How does OpenVPN compare to other VPN protocols?

Currently, OpenVPN tends to outperform all other VPN protocols. The only one that manages to keep up with OpenVPN seems to be SoftEther, as you will soon see.

**OpenVPN versus SSTP**

SSTP and OpenVPN are quite similar as they both use SSL 3.0, and both VPN protocols can use port 443. They also offer a similar level of security, as both protocols can use 256-bit encryption and highly secure AES encryption.

However, OpenVPN is open-source, which means it is much more reliable than SSTP, which is exclusively owned by Microsoft — [a company that is known to collaborate with the NSA and the FBI](https://www.independent.co.uk/news edward-snowden-claims-microsoft-collaborated-with-nsa-and-fbi-to-allow-access-to-user-data-8705755.html).

Also, when it comes to firewalls, OpenVPN seems to be a bit more efficient than SSTP. How come? Well, here's a lesser known fact about SSTP — [according to Microsoft's claim](https://social.technet.microsoft.com/Forums/en-US/d0e7648e-5cfc-40d7-9030-e951d6f6e442/sstp-through-authenticated-web-http-proxy?forum=winserverNIS), the protocol doesn't really support authenticated web proxies. This means that the network administrator could theoretically detect SSTP headers and drop the connection if a non-authenticating proxy is used.

In terms of speed, SSTP is said to be faster than OpenVPN, but there is not much conclusive evidence. It's true that OpenVPN can be quite resource intensive, but that's usually when it uses the TCP port (the same one used by SSTP). However, OpenVPN can also use the UDP port, which offers much higher speeds.

When it comes to cross-platform compatibility, OpenVPN has the advantage since it works on many more platforms than SSTP, which is only available on Windows, Linux, Android and routers. Nevertheless, it should be noted that SSTP is natively integrated into Windows platforms, so it is easier to configure than OpenVPN.

Overall, OpenVPN and SSTP are a decent choice, but OpenVPN is simply more efficient. If you want to learn more about SSTP, [check out this article](https://www.techslang.com/definition/what-is-the-secure-socket-tunneling-protocol-sstp/).

**OpenVPN vs Wireguard**

OpenVPN uses the OpenSSL library to implement all kinds of cryptographic algorithms (the most popular being AES-256). WireGuard uses modern, fixed algorithms (you can't change them) to avoid configuration errors that lead to security holes. Overall, they both offer excellent security.

WireGuard is definitely faster than OpenVPN. Its code base is much lighter (about 4,000 lines vs. 70,000-600,000 lines) and uses processor cores more efficiently. In our tests, WireGuard was faster even when we used OpenVPN over UDP.

Want to know more about Wireguard? [Then read this article](https://cybernews.com/what-is-vpn/wireguard-protocol/).

**OpenVPN versus SoftEther**

It is safe to say that both OpenVPN and SoftEther are truly secure protocols. They are open-source, use military-grade encryption algorithms like AES, use 256-bit encryption, and also use SSL 3.0. The main difference between them is age — SoftEther is much newer than OpenVPN. For this reason, some people think that OpenVPN is much more reliable.

In terms of speed, SoftEther is faster than OpenVPN. In fact, [according to research from the University of Tsukuba](https://www.softether.org/1-features/4._Fast_Throughput_and_High_Ability) (the people behind SoftEther VPN, so not a 100% subjective source), the SoftEther protocol is supposed to be 13 times faster than the OpenVPN protocol.

Both protocols work on a decent number of platforms, but SoftEther seems to be a bit easier to set up than OpenVPN. However, you should know that even if you use a VPN provider that offers SoftEther connection, you'll still need to download additional software to make it work. With OpenVPN, this is optional.

Like OpenVPN, SoftEther can also run its own server, but the SoftEther server can also run the OpenVPN protocol, along with other protocols like IPSec, L2TP/IPSec, SSTP and SoftEther. The OpenVPN server can only run its own custom protocol.

All in all, SoftEther is a solid OpenVPN alternative. If — for some reason — you can't use OpenVPN, you should try SoftEther. If you want to know more, [follow this link](https://dataprot.net/guides/what-is-softether/).

**OpenVPN versus PPTP**

For starters, PPTP is significantly weaker than OpenVPN in terms of security. While OpenVPN can handle 256-bit encryption keys and encryptions like AES, PPTP can only use 128-bit keys via MPPE encryption. Unfortunately, MPPE encryption is very easy to exploit — here are just a few problems:

  * MPPE is vulnerable to bit-switching attacks.

  * MPPE cannot encrypt NCP (Network Control Protocol) PPP (Point-to-Point Protocol) packets.

  * Encryption usually does not check if the server is authentic.

  * The MPPE is vulnerable to the Reset-Request attack ([a form of man-in-the-middle attack](https://doubleoctopus.com/blog/enterprise-security/the-ultimate-guide-to-man-in-the-middle-mitm-attacks-and-how-to-prevent-them/))

Moreover, PPTP can use MS-CHAP-v1 ([which is not secure](https://www.schneier.com/wp-content/uploads/2016/02/paper-pptp.pdf)) or MS-CHAP-v2 ([again, not secure at all](https://web.archive.org/web/20160316174007/https://www.cloudcracker.com/blog/2012/07/29/cracking-ms-chap-v2/)) authentication. OpenVPN is much more secure since it can use better encryption for authentication, such as SHA-256, SHA-384 or SHA-512.

Moreover, PPTP is quite easy to block with a firewall. OpenVPN can't really be blocked by the network administrator since it uses the HTTPS port. Let's not forget that the [NSA can apparently crack PPTP traffic](https://www.darkreading.com/risk/nsa-surveillance-can-penetrate-vpns).

The only criteria that makes PPTP better than OpenVPN is its online speed and native availability on multiple platforms. Due to its low encryption, PPTP is very fast. And while OpenVPN is highly cross-platform compatible, it doesn't natively integrate on as many platforms as PPTP. However, it's worth mentioning that PPTP may no longer be natively available in future operating systems and devices.

If you want to know more about the PPTP protocol, [read this detailed article about it](https://dataprot.net/guides/what-is-pptp/).

**OpenVPN versus L2TP/IPSec**

Like PPTP, L2TP/IPSec is available natively on many platforms. So configuring it is much easier than configuring OpenVPN. However, if you use a VPN service, you won't notice any difference. On the other hand, L2TP/IPSec uses fewer ports than OpenVPN, and it does not use port 443. Thus, it is easier for the protocol to be blocked by a NAT firewall.

Although L2TP/IPSec is not entirely owned by Microsoft (since it was also developed by Cisco), it is still not as reliable as OpenVPN which is open-source. Also, it's important to note that Edward Snowden once claimed that L2TP was intentionally weakened by the NSA.

And speaking of security, you should know that L2TP alone offers 0 encryption. That's why it is always combined with IPSec. Also, even though OpenVPN over TCP can sometimes be resource intensive, L2TP/IPSec is also very resource intensive (depending on the power of your device) because it encapsulates data twice.

If you want to know more about L2TP/IPSec, [here is a useful link](https://www.techtarget.com/searchnetworking/definition/Layer-Two-Tunneling-Protocol-L2TP).

**OpenVPN versus IPSec**

IPSec is often associated with L2TP and IKEv2, but you may find VPN providers that offer access to this protocol on their own.

So what about the OpenVPN protocol? Well, both offer an equally decent level of security. However, you need to be more careful with IPSec when configuring it, as a small mistake can ruin the protection it offers. Also, since IPSec occupies kernel space (the space on the device reserved for the operating system), its security can be limited by the way it is configured by the vendor. This also makes IPSec less portable than OpenVPN, which uses user space (system memory allocated to applications).

IPSec is usually available natively on many platforms, while OpenVPN has to be configured manually on them. Of course, this is not a problem if you use a VPN service. Another thing to note is that IPSec traffic can sometimes be blocked by some firewalls, while OpenVPN UDP or TCP packets have no such problems.

As for speed and stability, both are pretty decent if you have enough bandwidth and a relatively powerful device. However, you should know that IPSec may take longer to negotiate the tunnel than OpenVPN.

Want to know more about IPSec? [Check out this article](https://www.techtarget.com/searchsecurity/definition/IPsec-Internet-Protocol-Security).

**OpenVPN versus IKEv2/IPSec**

OpenVPN and IKEv2 are both secure protocols, but it's worth noting that OpenVPN uses TLS/SSL to secure data at the Transport level, while IKEv2 secures data at the IP level. In general, it doesn't make much of a difference, but it's still good to know. And although IKEv2 was developed by Cisco with Microsoft, it's not such a big deal since there are open-source implementations of IKEv2.

OpenVPN offers more support when it comes to cross-platform compatibility, but IKEv2 is generally a favorite among mobile users because it is natively integrated into BlackBerry devices. Additionally, IKEv2 tends to offer better stability than OpenVPN because it can withstand network changes. What does this mean? That if, for example, you were to switch on the way from a WiFi connection to your data plan connection, IKEv2 could handle that without breaking the connection.

Also, be aware that IKEv2 tends to be faster than OpenVPN, but it's also easier to block than the OpenVPN protocol. Why? Because IKEv2 uses UDP port 500 and network administrators have an easier time targeting it than port 443, which is typically used by OpenVPN.

Overall, we'd say IKEv2 is a better choice than OpenVPN if you use your cell phone a lot — especially when traveling abroad. Otherwise, you should stick with OpenVPN.

In case you want to know more about IKEv2, [follow this link](https://nordvpn.com/fr/blog/ikev2ipsec/).

## So why use OpenVPN and when?

The main reason to use the OpenVPN protocol is that it is very secure, very stable and works across multiple platforms. Most security experts recommend always using OpenVPN for everything you do online — especially since it's a transparent option (due to its open-source nature).

As far as using OpenVPN goes, it's a suitable VPN protocol for securing your online connections — whether [you're gaming online, downloading](https://www.vpnmentor.com/blog/why-need-a-vpn-for-gaming/) torrents, or [if you're about to become a whistleblower](https://www.security.org/vpn/anonymity/). OpenVPN is also a good choice if you need to bypass a [firewall](https://hackercombat.com/difference-between-vpn-firewall-and-the-antivirus-software/#:~:text=While%20VPNs%20help%20bypass%20geo,restrictions%20the%20way%20VPNs%20do.) — whether it's to [unblock geo-blocked content](https://www.avast.com/c-geoblocking) or just to unblock websites at work or school.

## Conclusion - OpenVPN

OpenVPN is both an open-source VPN protocol and a VPN software that allows you to run secure VPN connections. Most VPN providers offer this protocol because it is very secure (it uses the OpenSSL library and 256-bit encryption) and it works on multiple platforms. OpenVPN is considered the best choice among VPN protocols, with only SoftEther being able to compete with it.

Generally, you should choose a VPN provider that gives access to OpenVPN connections, but also gives access to other VPN protocols.

Thanks for reading!
