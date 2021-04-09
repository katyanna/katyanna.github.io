---
layout: post
title: "[study notes] IP Address"
date: 2021-04-09 14:00:00
categories: notes computer-science network
---

Every device needs a label to be able to communicate with others via a network, this label is called
Internet Protocol Address (IP Address). It is a unique identifier, but not necessarily permanent.
Most devices don't need a static IP address, those are needed when external applications need to
have this one specific address stored. Instead we're usually using dynamic IP addresses, they're
assigned by the network and frequently change, making it more difficult for unwanted requests to
reach your device.

&nbsp;

### IPv4

![185.199.111.153](/public/images/ipv4.png)

At first, the IP Address looked only like this `185.199.111.153`. That's an IPv4
([Internet Protocol Version 4](https://tools.ietf.org/html/rfc6864)) format. It's a sequence of 4
numbers ranging from 0 to 255 separated by dot. When translating it to binary amounts to 32 bits.
The maximum number of numeric combinations within this format is **4.294.967.296**.

&nbsp;

### IPv6

![2001:0db8:85a3:0000:0000:8a2e:0370:7334](/public/images/ipv6.png)

Over the past decades, the number of devices connecting to the internet increased rapidly and
suparssed the amount of possible unique IPv4 addresses, so we had to come up with a new format. The
IPv6 ([Internet Protocol Version 6](https://tools.ietf.org/html/rfc8200)) has a theoretical maximum
of **~340.282.366.920.938.463.463.374.607.431.768.211.456**, we're confident that this number will
not be reached any time soon (probably never). It amounts to 128 bits and looks like:
`2001:0db8:85a3:0000:0000:8a2e:0370:7334`.
