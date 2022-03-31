# NTP-server-prototype
This rep tracks the NTP server development. This will eventually be used to precisely timestamp camera and lidar data for autonomous driving applications.

## Who are we?
We (ECK-Group-A) will be working on this, and some other components, for a school project

## First version
We can currently get an NTP server running on the RPi and we are able to succesfully get time data from it. At the moment the server gets it's time data from the GPS it's NMEA messages. More information on how to setup the server [here](NTP-sever-setup.md).

## Future versions
Eventually the NPT server should be able to sync up with PPS signals from a GPS. It should do so automatically when the RPi boots. 

