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

Helper apps are really good at tunnelling all the network traffic into the localhost and then sending it through to the external proxy server.

When using these apps the above macOS settings for proxy should be configured to the localhost or `127.0.0.1` and whatever port you use from the app (`3128` in these examples).

### [SquidMan](https://squidman.net/squidman/)

1. Open the app

 ![](../assets/macOS/image14.jpg)

1. Open the preferences `CMD + ,`

1. Under `General`, set the port that the device will use to connect (this example I'm using the same port as the proxy `3128`)

 ![](../assets/macOS/image15.jpg)

1. Go to the `Parent` tab, and if you use multiple locations select the one from the sidebar and enter the proxy settings.

 ![](../assets/macOS/image16.jpg)

 ?> This is my favourite thing about SquidMan - I have a "home" location for wifi, and then a "proxy" wifi

1. If you need to share your internet proxy tunnelling to others that can install or are mobile devices then you have the ability to limit the access

 ![](../assets/macOS/image17.jpg)

1. `Save` the settings, and then press `Start Squid` to start tunnelling

 ![](../assets/macOS/image18.jpg)
 ![](../assets/macOS/image19.jpg)

### [Charles Proxy](https://www.charlesproxy.com)

!> Charles proxy debugging is not supposed to be used for network tunnelling, but it works as a by-product. As a result, leaving it on 24/7 means most of your device's resources get eaten up by the session recorder. This shows you how to turn it off

1. Open the app

 ![](../assets/macOS/image20.jpg)
 ![](../assets/macOS/image21.jpg)

1. Stop the recording and clear the session

 ![](../assets/macOS/image22.jpg)

1. Open the preferences `CMD + ,` and under `Launch` uncheck the `Open new session` and press `OK`

 ![](../assets/macOS/image23.jpg)

1. From the menubar, turn on `macOS Proxy`

 ![](../assets/macOS/image24.jpg)

1. From the menubar, open up the `Proxy Settings...`

 ![](../assets/macOS/image25.jpg)

1. Set the port that the device will use to connect (this example I'm using the same port as the proxy `3128`)

 ![](../assets/macOS/image26.jpg)

1. Under the `macOS` tab that all the options are checked

 ![](../assets/macOS/image27.jpg)

1. From the menubar, open up the `External Proxy Settings...`

 ![](../assets/macOS/image28.jpg)

1. Check the `Use external proxy servers` option and fill in the HTTP and HTTPS settings

 ![](../assets/macOS/image29.jpg)
 ![](../assets/macOS/image30.jpg)

1. Press `OK`

### iOS / iPad OS

The only helpers you can use on iOS devices is using Squid or Charles on another machine, and then point your iOS device to use that as the proxy server.

Charles _does_ have an iOS and iPadOS app, but it is only for debugging not forwarding to the main proxy server :disappointed:

So in short, you're tied in to native proxy settings.

## Other pages

[View Windows proxy settings](/proxy/windows ':class=mb-button')
[View Linux proxy settings](/proxy/linux ':class=mb-button')
[View Applications proxy settings](/proxy/apps ':class=mb-button')
[Go home](/ ':class=mb-button')
