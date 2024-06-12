# Proxies, ugh

If you've ever worked in a corporate environment where you need to authenticate against a proxy server, you know one thing for sure - they **suck**.

Sometimes they work seamlessly, and other times they don't. Some apps have built-in settings, while others rely on the system configuration. It's a constant battle.

My goal is to simplify the process of configuring your services to authenticate against proxy servers effectively.

## Why

While setting up proxy configurations on your operating system might seem straightforward, many apps don't use these settings or attempt to connect directly via IP addresses.

Some apps have their own proxy settings but lack fields for authentication. Others ignore your system settings entirely. It's a frustrating experience.

When you see the dreaded `407 Proxy Authentication Required` message and think - *whhhhhhy*? - I'm here to help you stop that from happening!

## Demo credentials

These are the demo credentials we'll be using around the website so you can see where to put information, where.

| Field            | Data                             |
|------------------|----------------------------------|
| **Domain**       | `BOO`                            |
| **Username**     | `jdoe`                           |
| **Password**     | `● ● ● ● ● ●` or `mypassword`     |
| **Proxy Server** | `proxy.motherfudgingproxies.com` |
| **Proxy Port**   | `3128`                           |

[footer nav](../site/footer.md ':include')

## Contributing

There are far too many proxy settings for [one person](https://github.com/markbattistella) to find, know, or care about.

If you find any missing information, please [fork the repo](https://github.com/markbattistella/motherfudgingproxies.com/fork), create a new branch, add your additions, and then submit a pull request.

Hopefully, by the time we document all the proxies, we won't need them anymore!

[<i class="i-fork"></i>Fork me!](https://github.com/markbattistella/motherfudgingproxies.com/fork ':class=mb-button')
