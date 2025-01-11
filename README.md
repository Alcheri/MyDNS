# MyDNS

![Python versions](https://img.shields.io/badge/Python-version-blue) ![Supported Python versions](https://img.shields.io/badge/3.9%2C%203.10%2C%203.11%2C%203.12%2C%203.13-blue.svg) [![Code style: black](https://img.shields.io/badge/code%20style-black-black)](https://github.com/psf/black) ![Build Status](https://github.com/Alcheri/My-Limnoria-Plugins/blob/master/img/status.svg) ![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg) [![CodeQL](https://github.com/Alcheri/Weather/actions/workflows/github-code-scanning/codeql/badge.svg)](https://github.com/Alcheri/Weather/actions/workflows/github-code-scanning/codeql) [![Lint](https://github.com/Alcheri/Weather/actions/workflows/black.yml/badge.svg)](https://github.com/Alcheri/Weather/actions/workflows/black.yml)

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
> \<Barry\> @dns 203.7.22.140\
> \<Borg\>  **${\textsf{\color{teal}DNS: }}$** <203-7-22-140> [203-7-22-140.dyn.iinet.net.au <> 203.7.22.140] **${\textsf{\color{teal}LOC: }}$** City: Ballarat State: Victoria Long: 143.8470458984375 Lat: -37.56332015991211 Country Code: AU Country: Australia <img src="local/australia.png" width="17" height="17"> Post/Zip Code: 3350
>
> \<Barry\> @dns Alice\
> \<Borg\>  **${\textsf{\color{teal}DNS: }}$** [Alice.Bot.mrbenc.net <> 2001:19f0:9002:1806:dead:beef:0:cafe] **${\textsf{\color{teal}LOC: }}$** City: Flagami State: Florida Long: -80.31195831298828 Lat: 25.762859344482422 Country Code: US Country: United States <img src="local/usa.png" width="17" height="17"> Post/Zip Code: 33144
>

<br><br>
<p align="center">Copyright © MMXXV, Barry Suridge</p>
