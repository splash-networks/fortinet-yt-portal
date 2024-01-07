# Draytek External Captive Portal

The following actions are required to use the code given in this repo:

## Portal Setup Using Git

Suppose your domain is `hotspot.example.com`. It can be setup like this:

```
cd /var/www
git clone https://github.com/splash-networks/draytek-yt-portal
mv draytek-yt-portal hotspot.example.com
cd /var/www/hotspot.example.com
```

Copy the `.env.example` file to `.env` and set the values of the given environment variables in it:

```
cp .env.example .env
nano .env
```

Navigate to public folder:

`cd /var/www/hotspot.example.com/public`

Use [this](https://getcomposer.org/download/) link to install Composer. Then run `php composer.phar install` to install the packages given in `composer.json`.

## Apache Virtual Hosts

Apache virtual host can be setup on the portal server using the instructions given [here](https://gist.github.com/nasirhafeez/d47c9d68742227a23f1011455a190490#apache-site-setup).

The portal files are in public folder in this repository. DocumentRoot will be:

`/var/www/hotspot.example.com/public`

It has been successfully tested on a Draytek Vigor 2926 device with firmware version `3.9.8`.

## FreeRADIUS Setup

FreeRADIUS setup instructions for Draytek that authorizes all username/passwords are given [here](https://gist.github.com/nasirhafeez/b18b888691212443033f9b7d1ecb5058).