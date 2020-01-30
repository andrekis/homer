<img src="https://user-images.githubusercontent.com/1423657/55069501-8348c400-5084-11e9-9931-fefe0f9874a7.png" width=200/>

# HOMER 7.7 _(Seven)_
#### 100% Open-Source VoIP & RTC Capture, Troubleshooting & Monitoring


![H5](https://img.shields.io/badge/HOMER-7-red.svg)
![HEP](https://img.shields.io/badge/proto-hep_eep-blue.svg)
![HEP](https://img.shields.io/badge/proto-sip-brightgreen.svg)
![HEP](https://img.shields.io/badge/proto-rtcp-brightgreen.svg)
![HEP](https://img.shields.io/badge/proto-rtcp_xr-brightgreen.svg)
![HEP](https://img.shields.io/badge/proto-rtp_stats-brightgreen.svg)
![HEP](https://img.shields.io/badge/text-QoS-green.svg)
![HEP](https://img.shields.io/badge/text-syslog-green.svg)
![HEP](https://img.shields.io/badge/text-CDRs-green.svg)

**HOMER** is a robust, carrier-grade, scalable Packet and Event capture system and VoiP/RTC Monitoring Application based on the [HEP/EEP](http://github.com/sipcapture/hep) protocol and ready to process & store insane amounts of signaling, rtc events, logs and statistics with instant search, end-to-end analysis and drill-down capabilities.

**HOMER** is already used by large enterprises, voice network operators, voip service providers and traffic carriers worldwide, has been implemented as a service in 3rd party voice platforms and is suitable for production. 

**HOMER** 7+ is designed and delivered as a set of modular components and building blocks to be used stand-alone or in combination with other platforms.
<br/>

##### Core Features
* Based on HEP Encapsulation, available everywhere
* Stand-Alone Capture Servers & Agents for any OS
* Supports advanced SIP, RTP/RTCP Reports, RTC Events and Custom protocols
* Multiple Database backend support for Packets, Logs, Timeseries in parallel
* Dynamic Mapping and Correlation for internal and external data sources
* Made by Humans, and Supported by the best community ever

#### :construction: This is a work in progress, the process and instructions might change at any given time.

## Introduction
Unlike its predecessors, HOMER Seven is completely dynamic, meaning there are many database, timeseries and logging backend combinations possible - even at the same time! This opens up a number of new use-case options some users might find overwhelming at first - don't worry, *its just about freedom of choice!* If you're unsure or just want a stand-alone capture system, please consider using the below options or joining our friendly [users mailing list](https://groups.google.com/forum/#!forum/homer-discuss) where our community will welcome and help you move the first steps.

![image](https://user-images.githubusercontent.com/1423657/72265062-1e168d00-361c-11ea-9662-1663f3d9f38b.png)

### Presentations
If you'd like to get an idea about what HOMER is and what HOMER does, consider watching one of our presentations or workshops:

* [HOMER 7: The Power of Timeseries & Machine Learning](https://vimeo.com/302849555) @Voip2Day 2018 [spanish](https://vimeo.com/302408369)
* [HOMER 7: RTC Features](https://www.youtube.com/watch?v=xQ0rvpQURR0) @OpenSIPS Summit 2019
* [HOMER 7: Docker Workshop](https://www.youtube.com/watch?v=6teucQPAaWI) @KamailioWorld 2019


## Installation
Ready to Install? Choose your preferred method from our [Wiki](https://github.com/sipcapture/homer/wiki/Quick-Install)

<!--
### :hand: Manual Setup
Installing HOMER 7.x is simple and does not require skills other than patience.

##### Requirements
Before proceeding, install the database requirements for HOMER 7.7:
* Postgres 11+ w/ root account for `DATA` and `API`
* Prometheus or InfluxDB for `TIMESERIES`
* _(optional)_ Loki for `LOGS`

Once ready, proceed to install your HEP Stack:
* Install the [sipcapture](https://github.com/sipcapture/homer/wiki/Quick-Install) package repositories
* Install [heplify-server](https://github.com/sipcapture/heplify-server)
  * Configure with your Postgres instance for storing `DATA`
  * Configure with your Loki instance for storing `LOGS`
  * Configure Prometheus scrapers to `HOMER:9096/metrics`
* Install [homer-app](https://github.com/sipcapture/homer-app)
  * Configure with your Postgres instance for `API` 
  * Configure with your Prometheus or InfluxDB instances for reading `TIMESERIES`
  * Configure with your Loki instance for reading `LOGS`
* Install and Configure a HEP Capture Agent
  * Install [heplify](https://github.com/sipcapture/heplify) on a host with SIP/RTCP traffic
    * Configure with your SIP/RTCP portrange and send `HEP` traffic to `heplify-server` on port `9060`
      * example: ` ./heplify -i eth0 -pr 5060-5080 -hs 10.20.30.40:9060`
  * Use a native HEP client in [Kamailio](https://github.com/sipcapture/homer/wiki/Examples%3A-Kamailio), [OpenSIPS](https://github.com/sipcapture/homer/wiki/Examples%3A-OpenSIPS), [Asterisk](https://github.com/sipcapture/homer/wiki/Examples%3A-Asterisk), [Freeswitch](https://github.com/sipcapture/homer/wiki/Examples%3A-FreeSwitch) and [others](https://github.com/sipcapture/homer/wiki)
* Start your services and login on port `9080` as `admin` with password `sipcapture` _(change it!)_

----

### :whale: Docker Containers
Starting Fresh or Testing? A ready to fire set of [Docker containers](https://github.com/sipcapture/homer7-docker/tree/7.7/heplify-server) is available in many flavours, ready to capture in minutes!

----

### :package: BASH Script
Installing on a fresh, dedicated *all-in-one* server? Try our [installer script](https://github.com/sipcapture/homer-installer/tree/7.7) supporting the latest Debian and CentOS releases.



  
-->
----------------

### Support
For professional support, remote installations, customizations or commercial requests please contact: support@sipcapture.org

For community support, updates, user discussion and experience exchange please join our users   [Mailing-List](https://groups.google.com/forum/#!forum/homer-discuss)

For commercial licensing and support, please contact the QXIP Team at [http://qxip.net]

<img src="http://i.imgur.com/9AN08au.gif" width=100% height=50 >



### Developers
Contributors and Contributions to our project are always welcome! If you intend to participate and help us improve HOMER by sending patches, we kindly ask you to sign a standard [CLA (Contributor License Agreement)](http://cla.qxip.net) which enables us to distribute your code alongside the project without restrictions present or future. It doesn’t require you to assign to us any copyright you have, the ownership of which remains in full with you. Developers can coordinate with the existing team via the [homer-dev](http://groups.google.com/group/homer-dev) mailing list. If you'd like to join our internal team and volunteer to help with the project's many needs, feel free to contact us anytime!


### License & Copyright

![H5](https://img.shields.io/badge/license-GNU_AGPL_v3-blue.svg)

Homer components are released under the GNU Affero General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

*(C) 2008-2020 [QXIP BV](http://qxip.net)*

----------

#### Made by Humans
This Open-Source project is made possible by actual Humans without corporate sponsors, angels or patreons.<br>
If you use this software in production, please consider supporting its development with contributions or [donations](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=donation%40sipcapture%2eorg&lc=US&item_name=SIPCAPTURE&no_note=0&currency_code=EUR&bn=PP%2dDonationsBF%3abtn_donateCC_LG%2egif%3aNonHostedGuest)

[![Donate](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=donation%40sipcapture%2eorg&lc=US&item_name=SIPCAPTURE&no_note=0&currency_code=EUR&bn=PP%2dDonationsBF%3abtn_donateCC_LG%2egif%3aNonHostedGuest) 
