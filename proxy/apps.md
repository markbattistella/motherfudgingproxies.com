# <i class="i-apps"></i> Applications / Services :id=applications

## git

Run this from your terminal:

```sh
# http proxy
git config --global http.proxy  http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128

# https proxy
git config --global https.proxy http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128

# sometimes you need to specify
git config --global http.proxyAuthMethod  'basic'
git config --global https.proxyAuthMethod 'basic'
```

Or you can edit directly your ~/.gitconfig file with the following structure:

```sh
[http]
    proxy = http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128
    proxyAuthMethod = 'basic'

[https]
    proxy = http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128
    proxyAuthMethod = 'basic'
```

## npm

Run this from your terminal:

```sh
# http proxy
npm config set proxy http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128
npm config set http-proxy http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128

# http proxy
npm config set https-proxy http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128
```

Or you can edit directly your `~/.npmrc` file with the following structure:

```sh
proxy=http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128
https-proxy=http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128
https_proxy=http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128
```

## yarn

Run this from your terminal:

```sh
# http proxy
yarn config set proxy http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128

# https proxy
yarn config set https-proxy http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128
```

## wget

Create a new file in the `etc` directory: `vi /etc/wget` and write up your proxy in the following format:

```sh
# proxy settings
http_proxy   = http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128
https_proxy  = http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128
ftp_proxy    = http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128
```

## cUrl

Create a new file in the home directory: `vi ~/.curlrc` and write up your proxy in the following format:

```sh
# proxy settings
proxy = proxy.motherfudgingproxies.com:3128
proxy-user = "jdoe:mypassword"
```

## Docker

### Docker environment

Edit your `/etc/sysconfig/docker` file:

```sh
# proxy settings
http_proxy="http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128"
https_proxy="http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128"

HTTP_PROXY="http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128"
HTTPS_PROXY="http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128"
```

### Docker service

First make the directory (if it doesn't exist), and create the `http-proxy.conf` file:

```sh
mkdir /etc/systemd/system/docker.service.d
touch /etc/systemd/system/docker.service.d/http-proxy.conf
```

Then add the proxy details to the `http-proxy.conf` file:

```sh
[Service]
Environment="HTTP_PROXY=http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128"
Environment="HTTPS_PROXY=http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128"
```

### Docker user

First make the directory (if it doesn't exist), and create the `config.json` file:

```sh
mkdir /root/.docker
touch /root/.docker/config.json
```

Then add the proxy details to the `config.json` file:

```json
{
    "proxies": {
        "default": {
            "httpProxy": "http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128",
            "httpsProxy": "http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128"
        }
    }
}
```

[footer](../site/footer.md ':include')
