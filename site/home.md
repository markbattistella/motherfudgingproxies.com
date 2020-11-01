# Proxies, ugh

If you've ever worked in a corporate environment where you need to authenticate against a proxy server you know one thing for sure - they **suck**.

Sometimes they just work, sometimes they don't. Sometimes you need a custom area for your app, other times it uses the system. We really can't win.

## My Aim

My aim with this site is really to make it easy to know what to configure to get your services working and authenticating against the proxy server.

## Why

Even though it may seem easy to set up the basic proxy configuration on an operating system, there are a lot of in-built apps, or poorly configured ones that don't use these settings.

Sometimes they need their own configuration, other times they are connecting directly to the mothership's IP address and bypassing the proxy (well timing out). Sometimes, you're just getting a `407 Proxy Authentication Required` message and thinking - _whhhhhhy?_

## Proxy details

For this site demo, we're going to use the following as dummy data:

| Field | Data |
| :---- | :--- |
| **Username** | `jdoe` |
| **Password** | `MySecurePassword` |
| **Proxy Server** | `proxy.motherfudgingproxies.com` |
| **Proxy Port** | `3128` |

## Areas

### Windows

In Windows there are two places to set the proxies:

1. Control Panel
1. Settings App

Why _both_ exist is still beyond me, but if you're using anything Windows 10 (or Windows Server 2012) and above you have two places to check!

Windows 8 and below, you only have the Control Panel to worry about! :tada:

[View Windows proxy settings](/proxy/windows ':class=mb-button')

### macOS

Apple macOS has only one place to set your proxy settings, but you also have the option to set it per network interface (ethernet, or wifi).

macOS has a big issue with some of the in-built apps that don't use the proxy settings and attempt to contact Apple directly.

[View macOS proxy settings](/proxy/macos ':class=mb-button')

### Linux

Depending if you're using a GUI or CI proxies go two ways - easy or easier!

Linux is one of the better proxy handlers, but it does mean you need to set per-application proxies more often.

But we all know that unless you're in some whiz-bang-super workplace, you're not using Linux as your go to operating system.

[View Linux proxy settings](/proxy/linux ':class=mb-button')

### Applications

There is an endless list of applications that use proxies to access the internet.

Some use the system's settings, some have their own pop-up authenticators, others need their config files set.

The ones listed in here are a start!

[View Applications proxy settings](/proxy/apps ':class=mb-button')

## Contributing

There are way too many proxy setting for one guy ([me](https://twitter.com/markbattistella)) can find or know about.

So if you find one that's missing, then [fork this repo](https://github.com/markbattistella/motherfudgingproxies.com), create a new branch, add your additions, and then request a pull request.

Hopefully by the time we document all the proxies, we won't need them anymore!

<a href="https://github.com/markbattistella/motherfudgingproxies.com" class="mb-button" style="background:#2A2A72;">Fork me!</a>
