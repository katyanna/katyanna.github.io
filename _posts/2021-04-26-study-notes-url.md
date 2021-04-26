---
layout: post
title: "[study notes] URL"
date: 2021-04-26 21:00:00
categories: notes computer-science url internet
---
Remembering phone numbers is a skill we're trying to leave in the past, so of course no one is going
to memmorize IP addresses for all the websites one visits either (that's not a challenge, be cool).

**URLs** (Universal Resource Locators), a.k.a. web addresses, are what we actually use on our human
day-to-day activities.

&nbsp;

### Basic B of URLs

![simple url](/public/images/simple_url.png)

- **Scheme <`https`>**:

    The scheme is the protocol, it sets the rules the requests must follow. Usually *http*
    (HyperText Transfer Protocol) or *https* (HyperText Transfer Protocol Secure), but there are
    others like *mailto* or *ftp* (File Transfer Protocol).

- **Domain name <`website-name`>**:

    The name of the website 🕵️

- **TLD <`.com`>**:

    The Top Level Domain is the "category" of the website, it groups websites facilitating
    the DNS job. *.com* usually indicates it's a commercial website; other examples would be
    *.org,* indicating non-profit organization and *.net,* which was originally intended for the
    internet businesses.

&nbsp;

### But there might be some more information in it

![bigger url](/public/images/bigger_url.png)

- **Subdomain <`WWW`>**:

    World Wide Web, identifies the link as a website that communicates through HTTP.

    **Fun Fact**:
    > The use of WWW has been around since the creation of the internet, and its widespread use as a subdomain was largely accidental. The [first web server was nxoc01.cern.ch.](http://info.cern.ch/) When publishing the website, the creators fully intended for *info.cern.ch* to be their home page, and WWW, as such, was excluded. The Domain Name System records for the server were never switched, and the use of WWW became an unintentional standard practice.
    *[source](https://wpengine.com/resources/http-vs-www-urls-for-seo/)*

- **Port <`80`>**:

    Usually omitted, because default values are used, the port indicates the
    technical "gate" through which the resources may be accessed. The combo of domain
    name, TDL and port is called **Authority**.

- **Path <`path/to/file.html`>**:

    Not necessarily the exact path to a file in the server, but an abstraction of it.

- **Parameters <`?key1=value1&key2=value2`>**:

    Information sent to the server through the request. It consists on a list of
    key and value, initiated with `?` separated by `&`. The use of this data is custom
    and determined by the server.

- **Anchor <`#specific`>**:

    Also known as fragment, the anchor bookmarks a specific part of the page. This
    never goes into the request.
