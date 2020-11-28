# <i class="i-macos"></i> macOS :id=macos

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

### [Proxyman](https://proxyman.io)

1. Open the app

 ![](../assets/macOS/image31.jpg)

1. Stop the recording and clear the session

 ![](../assets/macOS/image32.jpg)

1. Open the preferences `CMD + ,` and under `General` set the port to `3128`, and uncheck `Auto select available port`

 ![](../assets/macOS/image33.jpg)

1. Then go to `Advanced` and install the `Proxy Helper Tool`

 ![](../assets/macOS/image34.jpg)

1. From the menubar, check the `Override macOS Proxy` and then open `External Proxy Settings...`

 ![](../assets/macOS/image35.jpg)

1. Fill in the HTTP and HTTPS settings

 ![](../assets/macOS/image36.jpg)
 ![](../assets/macOS/image37.jpg)

1. _(optional)_ To set up iOS and Android follow the guides in the app

 !> It is important to note that using these proxy settings for iOS / iPadOS / Android don't forward directly to the external proxy server. They go to your macOS machine (so it is really hit-and-miss with success rates)

 ![](../assets/macOS/image38.jpg)
 ![](../assets/macOS/image39.jpg)

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

[footer](../site/footer.md ':include')
