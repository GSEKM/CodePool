Add the repositories on the /etc/apt/sources.list:

```
deb http://analizo.org/download/ ./
deb-src http://analizo.org/download/ ./

deb http://debian.joenio.me unstable/
deb-src http://debian.joenio.me unstable/
```
Get the repositories signing key as root(You can use sudo -i for Debian users):

```
wget -O - http://debian.joenio.me/signing.asc | apt-key add -
wget -O - http://analizo.org/download/signing-key.asc | apt-key add -
```

And install the doxyparse 1.8.11 and analizo 1.19.1:

```
apt install doxyparse=1.8.11-1
apt install analizo
```
