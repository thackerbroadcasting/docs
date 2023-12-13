---
title: What Security Measures are used to Protect me and my Music?
icon: material/server-security
---

!!! note "TL;DR"
    Physical, Proxy, Encryption

There are a variety of measures we take to protect your customer data and the music you enjoy.

- There is physical security of the device itself. Protected by a password, physical locks, disabling USB ports, and disabling wireless connectivity helps prevent your device from being found and accessed, both physically and wirelessly.
- When the device is installed on your network, we will segregate it from the rest of your network. What this simply means is that it will be locked in its own little network area, unable to talk to any of your local devices. That way, local customers won’t be able to accidentally (or even purposefully) find and try to take control of the device.
- Your device will talk directly to a proxy service. This will help prevent your business’ public IP address from being spilled or broadcast to the internet. We utilize Cloudflare which is very fast and secure. In addition, all of our websites use the latest encryption to ensure that your data is transported safely and securely. Cloudflare helps us ensure that your data is protected while helping your music be delivered as fast as possible.
- We only use cloud providers that support the industries latest security measures. This helps prevent unauthorized access should a security breach happen.
- The servers we use are physically protected by our cloud providers. Digitally, they are protected by SHA-256 encryption keys that are physically separated from any of our publicly accessible content. These keys are stored on a server that will never touch the internet. Any updates we have to do on this server must be done in an offline fashion