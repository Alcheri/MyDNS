# MyDNS

![Python versions](https://img.shields.io/badge/Python-version-blue) ![Supported Python versions](https://img.shields.io/badge/3.9%2C%203.10%2C%203.11%2C%203.12-blue.svg) ![Build Status](https://github.com/Alcheri/My-Limnoria-Plugins/blob/master/img/status.svg) ![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)

## Description

An alternative to Limnoria's DNS function.

Returns the ip of <hostname | URL | nick | IPv4 or IPv6> or the reverse DNS hostname of \<ip\> using Python's socket library.

This plugin uses ipstack to get data. An API (free) key is required.\
Get an API key: [ipstack](https://ipstack.com/)

Unload the Internet plugin as it conflicts with this plugin

```plaintext
/msg yourbot unload Internet
```

## Install

Go into your Limnoria plugin dir, usually ~/runbot/plugins and run:

```plaintext
git clone https://github.com/Alcheri/MyDNS.git
```

To install additional requirements, run from /plugins/URLtitle:

```plaintext
pip install --upgrade -r requirements.txt 
```
Next, load the plugin:

```plaintext
/msg bot load URLtitle
```

## Configuring

* **_config plugins.MyDNS.ipstackAPI [your_key_here]_**

* **_config channel #channel plugins.MyDNS.enable True or False (On or Off)_**

Using

```plaintext
@dns [hostname | URL | nick | IPv4 or IPv6]
```

## Example

> \<Barry\> @dns crawl-203-208-60-1.googlebot.com\
> \<Borg\>  **${\textsf{\color{teal}DNS: }}$** crawl-203-208-60-1.googlebot.com resolves to [203.208.60.1] **${\textsf{\color{teal}LOC: }}$** City:Beijing State:Beijing Long:116.37922668457031
  Lat:39.91175842285156 Country Code:CN Country:China <img src="local/china.png" width="17" height="17"> Post/Zip Code:100000
> 
