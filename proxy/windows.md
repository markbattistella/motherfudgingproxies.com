# <i class="i-windows"></i> Windows :id=windows

Windows was fairly consistent in their proxy settings up until they released their new interfaced version and new transitional Settings App.

Usually when you configure one of the places for proxies in Windows it does filter to the other, but it is always good practice to make sure!

## Standard way

### Control Panel

1. Open the `Start` menu and search for `Internet Options` and open it

 ![](../assets/windows/image01.jpg)

1. Go to the `Connections` tab

 ![](../assets/windows/image02.jpg)

1. Towards the bottom, press the `LAN settings` button

 ![](../assets/windows/image03.jpg)

1. With the pop up dialogue window, check the `Use a proxy server for your LAN`

 ![](../assets/windows/image04.jpg)

1. In the address enter the proxy server address and port number

1. Check the `Bypass proxy server for local addresses`

  ?> This setting means anything that is within the scope of `.local` or in the domain will not use the proxy

1. Press the `Advanced` button to open the advanced Proxy Settings menu

 ![](../assets/windows/image05.jpg)

1. Specify separate proxy addresses for each of the protocols if you need to, otherwise press `OK`

1. Open Internet Explorer (_yes_ it has to be this) and log in with your proxy credentials

 ![](../assets/windows/image06.jpg)

 ?> You have to use Internet Explorer as this is the default tunnelling application on Windows. When you launch Chrome or Firefox or another app, they will prompt you again for their own authentication, but anything using the internal proxy settings channels Internet Explorer

### Settings App

1. Open the `Start` menu and search for `Settings` and open it

 ![](../assets/windows/image07.jpg)

1. In the Settings app, search for **proxy** and select `Change proxy settings`

 ![](../assets/windows/image08.jpg)

1. Under proxy, turn on `Use a proxy server` and enter the proxy details

 ![](../assets/windows/image09.jpg)

1. Press `Save` - or else your details won't work

?> Sometimes you need to open Internet Explorer and authenticate, sometimes you don't and it will ask when you open the desired app. Sometimes you can use Edge, sometimes you can't. Microsoft, right?

## Helpers

Helper apps are really good at tunnelling all the network traffic into the localhost and then sending it through to the external proxy server.

When using these apps the above Windows settings for proxy should be configured to the localhost or `127.0.0.1` and whatever port you use from the app (`3128` in these examples).

### [Charles Proxy](https://www.charlesproxy.com)

!> Charles proxy debugging is not supposed to be used for network tunnelling, but it works as a by-product. As a result, leaving it on 24/7 means most of your device's resources get eaten up by the session recorder. This shows you how to turn it off

1. Open the app

 ![](../assets/windows/image10.jpg)

1. Stop the recording and clear the session

 ![](../assets/windows/image11.jpg)

1. Open the preferences `CTRL + ,` and under `Launch` uncheck the `Open new session` and press `OK`

 ![](../assets/windows/image12.jpg)

1. From the menubar, open up the `Proxy Settings...`

 ![](../assets/windows/image13.jpg)

1. Set the port that the device will use to connect (this example I'm using the same port as the proxy `3128`)

 ![](../assets/windows/image14.jpg)

1. Under the `Windows` tab that all the options are checked

 ![](../assets/windows/image15.jpg)

1. From the menubar, open up the `External Proxy Settings...`

 ![](../assets/windows/image16.jpg)

1. Check the `Use external proxy servers` option and fill in the HTTP and HTTPS settings

 ![](../assets/windows/image17.jpg)
 ![](../assets/windows/image18.jpg)

1. Press `OK`

[footer](../site/footer.md ':include')
