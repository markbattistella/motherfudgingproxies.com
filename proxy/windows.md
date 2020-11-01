# Windows

Windows was fairly consistent in their proxy settings up until they released their new interfaced version and new transitional Settings App.

Usually when you configure one of the places for proxies in Windows it does filter to the other, but it is always good practice to make sure!

## Standard way

### Control Panel

1. Open the `Start` menu

1. Search for `Control Panel` and open it

1. Press `Internet Options`

1. Go to the `Connections` tab

1. Towards the bottom, press the `LAN settings` button

1. With the pop up dialogue window, check the `Use a proxy server for your LAN`

1. In the address enter the proxy server address (e.g. `proxy.motherfudgingproxies.com`) and the port enter the proxy port number (e.g. `3128`)

1. Check the `Bypass proxy server for local addresses`

  ?> This setting means anything that is within the scope of `.local` or in the domain will not use the proxy

1. Press the `Advanced` button to open the advanced Proxy Settings menu

1. If you need to specify separate proxy addresses for each of the protocols you can do that here, or if you need to bypass other IP addresses or domains you can do it at the bottom too

### Settings App

## Helpers

### Charles

I'm usually not for applications that need to manage in-built functionality but sometimes you just need them.

Charles proxy is one of those great applications (and no, I'm not affiliated with them. They've just saved me many hours of debugging).

Charles Web Debugging, once installed actually will let you know what is trying to access the outbound traffic. But the cool extra feature it has is forwarding to an external proxy.

Why is this :sparkles: cool :sparkles:? Because every piece of traffic automatically gets forwarded through Charles.

Now you can:

1. Monitor what applications are accessing the outside world

1. See How often then are accessing other sites

1. Funnel all traffic via the external proxy

This last point means no matter what external address an app is trying to access, it will always resolve to `localhost`. If the external app doesn't support or failed to implement user credential authorisation - who cares, Charles will forward it for you!

## Other pages

[View macOS proxy settings](/proxy/macos ':class=mb-button')
[View Linux proxy settings](/proxy/linux ':class=mb-button')
[View Applications proxy settings](/proxy/apps ':class=mb-button')
[Go home](/ ':class=mb-button')
