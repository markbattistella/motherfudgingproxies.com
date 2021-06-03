# <i class="i-linux"></i> Linux :id=linux

## Ubuntu

<!-- tabs:start -->

### **Desktop**

?> Coming soon

### **Headless**

Edit the environment file by `vi /etc/environment` and add your proxy settings:

```sh
# proxy settings

## lowercase - some look for this specifically
http_proxy="http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128/"
https_proxy="http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128/"

# uppercase - some look for this specifically
HTTP_PROXY="http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128/"
HTTPS_PROXY="http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128/"
```

For things like `apt-get` you need another proxy location. Create a file called `95proxies` in `/etc/apt/apt.conf.d`:

```sh
touch /etc/apt/apt.conf.d/95proxies
```

Then add the details in:

```sh
Acquire::http::proxy  "http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128/";
Acquire::https::proxy "http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128/";
```

<!-- tabs:end -->

## Raspbian

<!-- tabs:start -->

### **Headless**

Edit the environment file by `vi /etc/environment` and add your proxy settings:

```sh
# proxy settings

## lowercase - some look for this specifically
export http_proxy="http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128/"
export https_proxy="http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128/"

# uppercase - some look for this specifically
export HTTP_PROXY="http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128/"
export HTTPS_PROXY="http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128/"
```

For things like `apt-get` you need another proxy location. Create a file called `10proxies` in `/etc/apt/apt.conf.d`:

```sh
touch /etc/apt/apt.conf.d/10proxies
```

Then add the details in:

```sh
Acquire::http::proxy  "http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128/";
Acquire::https::proxy "http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128/";
```

<!-- tabs:end -->

## Redhat / CentOS / Fedora

### YUM

<!-- tabs:start -->

### **Headless**

Edit the `yum.conf` file in: `vi /etc/yum.conf` and your proxy settings:

```sh
# proxy settings
proxy=http://proxy.motherfudgingproxies.com:3128/
proxy_username=jdoe
proxy_password=mypassword
proxy_auth_method=basic
```

<!-- tabs:end -->

### DNF

<!-- tabs:start -->

### **Headless**

Edit the `dnf.conf` file in: `vi /etc/dnf/dnf.conf` and your proxy settings:

```sh
# proxy settings
proxy=http://proxy.motherfudgingproxies.com:3128/
proxy_username=jdoe
proxy_password=mypassword
proxy_auth_method=basic
```

<!-- tabs:end -->

### Environment

<!-- tabs:start -->

### **Headless**

Create a `proxy.sh` file:

```sh
touch /etc/profile.d/proxy.sh
```

Then add the details in:

```sh
# proxy settings
PROXY_URL="http://jdoe:mypassword@proxy.motherfudgingproxies.com:3128/"

http_proxy=$PROXY_URL
https_proxy=$PROXY_URL
ftp_proxy=$PROXY_URL
no_proxy="localhost"

HTTP_PROXY=$PROXY_URL
HTTPS_PROXY=$PROXY_URL
FTP_PROXY=$PROXY_URL
NO_PROXY="localhost"

export http_proxy https_proxy ftp_proxy no_proxy HTTP_PROXY HTTPS_PROXY FTP_PROXY NO_PROXY
```

Apply the settings: `source /etc/profile.d/proxy.sh`

<!-- tabs:end -->

[footer nav](../site/footer.md ':include')
