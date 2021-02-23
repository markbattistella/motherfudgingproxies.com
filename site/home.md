# Proxies, ugh

If you've ever worked in a corporate environment where you need to authenticate against a proxy server you know one thing for sure - they **suck**.

Sometimes they just work, sometimes they don't. Some apps have settings in built, other times it uses the system.

You really can't win.

My aim is really to make it easy to know what to configure to get your services working and authenticating against the proxy server.

## Why

It may seem easy to set up your proxy configuration on the operating system's settings but a lot of apps don't use these settings or try connecting their servers directly via IP.

Some apps have their own proxy settings, but then don't have fields for authentication, others don't have these configuration settings and ignore your system settings entirely.

All I know is when you're getting a `407 Proxy Authentication Required` message and thinking - _whhhhhhy?_ - then I want that to stop happening!

## Demo credentials

| Field            | Data                             |
|------------------|----------------------------------|
| **Domain**       | `BOO`                            |
| **Username**     | `jdoe`                           |
| **Password**     | `●●●●●●●●●●` or `mypassword`     |
| **Proxy Server** | `proxy.motherfudgingproxies.com` |
| **Proxy Port**   | `3128`                           |

[footer nav](../site/footer.md ':include')

## Contributing

There are way too many proxy setting for [one guy](https://twitter.com/markbattistella) can find, know, or care about.

So if you find one that's missing, then [fork the repo](https://github.com/markbattistella/motherfudgingproxies.com), create a new branch, add your additions, and then request a pull request.

Hopefully by the time we document all the proxies, we won't need them anymore!

[<i class="i-fork"></i>Fork me!](https://github.com/markbattistella/motherfudgingproxies.com ':class=mb-button')
