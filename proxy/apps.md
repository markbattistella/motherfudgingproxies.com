# <i class="i-apps"></i> Applications / Services :id=applications

## git

```sh
# http proxy
git config --global http.proxy  http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128

# https proxy
git config --global https.proxy http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128

# sometimes you need to specify
git config --global http.proxyAuthMethod  'basic'
git config --global https.proxyAuthMethod 'basic'
```

## npm

## yarn

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

- item1
- item2
- item3

[footer](../site/footer.md ':include')
