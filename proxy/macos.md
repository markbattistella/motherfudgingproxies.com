# macOS

## Standard way

### System Preferences

1. Open `System Preferences`

 ![](../assets/macOS/image01.jpg)

1. Select `Network`

 ![](../assets/macOS/image02.jpg)

1. Click the network adapter from the side bar, and press `Advanced`

 ![](../assets/macOS/image03.jpg)

1. Go to the `Proxies` tab

 ![](../assets/macOS/image04.jpg)

1. Check `Web Proxy (HTTP)`, `Secure Web Proxy (HTTPS)`, and `FTP Proxy`

 ![](../assets/macOS/image05.jpg)<br>
 ![](../assets/macOS/image06.jpg)<br>
 ![](../assets/macOS/image07.jpg)

1. Enter your proxy settings in the right side pane:

   1. Proxy server: `proxy.motherfudgingproxies.com`
   1. Proxy port: `3128`
   1. Username: `jdoe`
   1. Password: `MySecurePassword`

1. Press `OK` and `Apply`

 ![](../assets/macOS/image08.jpg)

1. You will need to repeat this for every network adapter you use for internet

?> This site also assumes you're using standard proxies, and not SOCKS

### Settings (iOS and iPadOS)

1. Open the `Settings` app

 ![](../assets/macOS/image09.jpg)

1. Enter the Wi-Fi settings view

 ![](../assets/macOS/image10.jpg)

1. Press the :information_source: icon

 ![](../assets/macOS/image11.jpg)

1. Scroll to the bottom, and press `Configure Proxy`

 ![](../assets/macOS/image12.jpg)

1. Change the setting to `Manual`, and enter the proxy settings. Press `Save` _not_ back or else you'll lose everything you just entered :facepalm:

 ![](../assets/macOS/image13.jpg)

## Helpers

### [SquidMan](https://squidman.net/squidman/)

### [Charles Proxy](https://www.charlesproxy.com)

### iOS / iPad OS

The only helpers you can use on iOS devices is using Squid or Charles on another machine, and then point your iOS device to use that as the proxy server.

Charles _does_ have an iOS and iPadOS app, but it is only for debugging not forwarding to the main proxy server :disappointed:

So in short, you're tied in to native proxy settings.

## Other pages

[View Windows proxy settings](/proxy/windows ':class=mb-button')
[View Linux proxy settings](/proxy/linux ':class=mb-button')
[View Applications proxy settings](/proxy/apps ':class=mb-button')
[Go home](/ ':class=mb-button')
