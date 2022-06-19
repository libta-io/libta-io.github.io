---
title: "What is Encryption?"
header:
toc: true
toc_sticky: true
excerpt_separator:  <!--more-->
categories:
  - Guides
tags:
  - Guides
  - Encryption
  - Cryptography
  - Helpful
  - Privacy
  - Security
---

<!--more-->

## What is encryption?

Encryption is a way of scrambling data so that only authorized parties can understand the information. In technical terms, it is the process of converting human-readable plaintext to incomprehensible text, also known as ciphertext. In simpler terms, encryption takes readable data and alters it so that it appears random. Encryption requires the use of a [cryptographic key](https://www.cloudflare.com/learning/ssl/what-is-a-cryptographic-key/): a set of mathematical values that both the sender and the recipient of an encrypted message agree on.

![Lame](/assets/images/2022-06-19-6.png)
> Example of Data Encryption

Although encrypted data appears random, encryption proceeds in a logical, predictable way, allowing a party that receives the encrypted data and possesses the right key to decrypt the data, turning it back into plaintext. Truly secure encryption will use keys complex enough that a third party is highly unlikely to decrypt or break the ciphertext by [brute force](https://www.fortinet.com/resources/cyberglossary/brute-force-attack) — in other words, by guessing the key.

Data can be encrypted "at rest," when it is stored, or "in transit," while it is being transmitted somewhere else.

## What is a key in cryptography?

A cryptographic key is a string of characters used within an encryption algorithm for altering data so that it appears random. Like a physical key, it locks (encrypts) data so that only someone with the right key can unlock (decrypt) it.

## What are the different types of encryption?

The two main kinds of encryption are [symmetric encryption](https://www.cloudflare.com/learning/ssl/what-is-asymmetric-encryption/) and asymmetric encryption. Asymmetric encryption is also known as [public key encryption](https://www.cloudflare.com/learning/ssl/how-does-public-key-encryption-work/).

In symmetric encryption, there is only one key, and all communicating parties use the same (secret) key for both encryption and decryption. In asymmetric, or public key, encryption, there are two keys: one key is used for encryption, and a different key is used for decryption. The decryption key is kept private (hence the "private key" name), while the encryption key is shared publicly, for anyone to use (hence the "public key" name). Asymmetric encryption is a foundational technology for [TLS](https://www.internetsociety.org/deploy360/tls/basics/) (often called [SSL](https://www.websecurity.digicert.com/security-topics/what-is-ssl-tls-https)).

## Why is data encryption necessary?

**Privacy**: Encryption ensures that no one can read communications or data at rest except the intended recipient or the rightful data owner. This prevents attackers, ad networks, Internet service providers, and in some cases governments from intercepting and reading sensitive data.

**Security**: Encryption helps prevent [data breaches](https://www.kaspersky.com/resource-center/definitions/data-breach), whether the data is in transit or at rest. If a corporate device is lost or stolen and its hard drive is properly encrypted, the data on that device will still be secure. Similarly, encrypted communications enable the communicating parties to exchange sensitive data without leaking the data.

**Data integrity**: Encryption also helps prevent malicious behavior such as [on-path attacks](https://www.wallarm.com/what/what-is-an-on-path-attacker). When data is transmitted across the Internet, encryption (along with other integrity protections) ensures that what the recipient receives has not been tampered with on the way.

**Authentication**: Public key encryption, among other things, can be used to establish that a website's owner owns the private key listed in the website's [TLS certificate](https://www.kaspersky.com/resource-center/definitions/what-is-a-ssl-certificate). This allows users of the website to be sure that they are connected to the real website (see [What is public key encryption?](https://digitalguardian.com/blog/what-public-key-cryptography#:~:text=Public%20key%20cryptography%20uses%20a,key%20from%20a%20public%20directory.) to learn more).

**Regulations**: For all these reasons, many industry and government regulations require companies that handle user data to keep that data encrypted. Examples of regulatory and compliance standards that require encryption include HIPAA, PCI-DSS, and the GDPR.

## What is an encryption algorithm?

An encryption algorithm is the method used to transform data into ciphertext. An algorithm will use the encryption key in order to alter the data in a predictable way, so that even though the encrypted data will appear random, it can be turned back into plaintext by using the decryption key.

## What are some common encryption algorithms?

Commonly used symmetric encryption algorithms include:

* AES
* 3-DES
* SNOW

Commonly used asymmetric encryption algorithms include:

* RSA
* Elliptic curve cryptography

## What is a brute force attack in encryption?

A [brute force attack](https://www.varonis.com/blog/brute-force-attack) is when an attacker who does not know the decryption key attempts to determine the key by making millions or billions of guesses. Brute force attacks are much faster with modern computers, which is why encryption has to be extremely strong and complex. Most modern encryption methods, coupled with high-quality passwords, are resistant to brute force attacks, although they may become vulnerable to such attacks in the future as computers become more and more powerful. Weak passwords are still susceptible to brute force attacks.

## How is encryption used to keep Internet browsing secure?

Encryption is foundational for a variety of technologies, but it is especially important for keeping [HTTP](https://www.w3schools.com/whatis/whatis_http.asp) requests and responses secure, and for authenticating website [origin servers](https://www.cdnetworks.com/knowledge-center/what-is-origin-server/#:~:text=An%20origin%20server%20is%20a,to%20end%20users%20when%20requested.). The protocol responsible for this is called [HTTPS](https://www.ssl.com/faqs/what-is-https/) (Hypertext Transfer Protocol Secure). A website served over HTTPS instead of HTTP will have a URL that begins with https:// instead of http://, usually represented by a secured lock in the address bar.

HTTPS uses the encryption protocol called Transport Layer Security (TLS). In the past, an earlier encryption protocol called Secure Sockets Layer (SSL) was the standard, but TLS has replaced SSL. A website that implements HTTPS will have a [TLS certificate](https://www.kaspersky.com/resource-center/definitions/what-is-a-ssl-certificate) installed on its origin server.


Thanks for reading!
