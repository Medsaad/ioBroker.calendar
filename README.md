![Logo](admin/calendar.png)
# ioBroker.calendar

[![NPM version](http://img.shields.io/npm/v/iobroker.calendar.svg)](https://www.npmjs.com/package/iobroker.calendar)
[![Downloads](https://img.shields.io/npm/dm/iobroker.calendar.svg)](https://www.npmjs.com/package/iobroker.calendar)
![Number of Installations (latest)](http://iobroker.live/badges/calendar-installed.svg)
![Number of Installations (stable)](http://iobroker.live/badges/calendar-stable.svg)
[![Dependency Status](https://img.shields.io/david/WLAN-Kabel/ioBroker.calendar.svg)](https://david-dm.org/WLAN-Kabel/iobroker.calendar)
[![Known Vulnerabilities](https://snyk.io/test/github/WLAN-Kabel/ioBroker.calendar/badge.svg)](https://snyk.io/test/github/WLAN-Kabel/ioBroker.calendar)

[![NPM](https://nodei.co/npm/iobroker.calendar.png?downloads=true)](https://nodei.co/npm/iobroker.calendar/)

**Tests:** [![Travis-CI](http://img.shields.io/travis/WLAN-Kabel/ioBroker.calendar/master.svg)](https://travis-ci.org/WLAN-Kabel/ioBroker.calendar) [![AppVeyor](https://ci.appveyor.com/api/projects/status/github/WLAN-Kabel/ioBroker.calendar?branch=master&svg=true)](https://ci.appveyor.com/project/WLANKabel/ioBroker-calendar/)

## Calendar adapter for ioBroker

Read your google calendar.

## Todo
* Add Outlook calendar
* Add function to add events to calendar
* Extend  vis widget

## Google Authentication
The following step is only needed if your ioBroker is installed on another computer/server and you cannot acces the webinterface via localhost.

### Windows:

Run ```nodepad.exe``` with admin right and open the ```C:\Windows\System32\drivers\etc\hosts``` file.
Add a entry like ```192.168.0.10    example.com //<IP-Adress ioBroker>     <FQDN>```
Save the file and open the webinterface via the <FQDN> you have written in the hosts file. Example: http://example.com:8081

### Linux:

    Comming soon ...

### Mac

    Comming soon ...

### Google API Key
You need an api key. Visit https://console.cloud.google.com/apis/dashboard and login with your google account.

Open the list in the header and create a new project. Enter a project name like "ioBroker Calendar" and click create.

Make sure you have selected the right project from the list. Open the library tab. Search for "Calendar" and click on "Google Calendar API".

Click "activate" and then click on "APIs & Services". Open the tab "OAuth consent screen" and type a application name like "ioBroker Calendar". You can also upload a logo, but this is not necessary.

Open the "Credentials" tab, click the "Create credentials" dropdown and select "OAuth client ID". In the next step choose "Web application". Type a name like "ioBroker" or "Webclient". Add ```http://<FQDN>:<Port from adapter config>``` to authorised JavaScript origins. Add ```http://<FQDN>:<Port from adapter config>/google``` and ```http://<FQDN>:<Port from adapter config>/google/``` to Authorised redirect URIs.

Create the client id and copy the displayed client ID and the client secret.

Go to the adapter config an add the client ID and the client secret.

## Changelog

### 0.1.0
* (WLAN-Kabel) Added calendar widget
* (WLAN-Kabel) Cron job and server will stopped on unload
* (WLAN-Kabel) Fixed an issue where not all states were deleted
* (WLAN-Kabel) Added some debug messages
* (WLAN-Kabel) Removed adapter from state settings
* (WLAN-Kabel) Fixed problem where series appointments were not loaded

### 0.0.1
* (WLAN-Kabel) Initial release

## License
MIT License

Copyright (c) 2019-2020 WLAN-Kabel <wlan-kabel@outlook.de>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
