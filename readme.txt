owm - weewx extension that sends data to OpenWeatherMap
Copyright 2014-2020 Matthew Wall
Distributed under the terms of the GNU Public License (GPLv3)

Installation instructions:

1) download

wget -O weewx-owm.zip https://github.com/matthewwall/weewx-owm/archive/master.zip

2) run the installer:

weewx version <= 4.10:
wee_extension --install weewx-owm.zip

weewx version >= 5.0 (not need download previously):
weectl extension install https://github.com/matthewwall/weewx-owm/archive/master.zip

3) modify weewx.conf:

[StdRESTful]
    [[OpenWeatherMap]]
        appid = OWM_APPID
        station_id = STATION_ID

4) restart weewx

sudo /etc/init.d/weewx stop
sudo /etc/init.d/weewx start

or

sudo service weewx restart
