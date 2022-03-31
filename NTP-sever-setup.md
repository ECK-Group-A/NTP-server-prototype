# NTP server setup Raspberry pi
This is a little tutorial to quickly setup an NTP server on the RPi because we will need to do this more than once.

## NTP server setup RPi:

1. Get a terminal running on the RPi and navigate to root.
2. Install the ntp server:
``` bash
sudo apt-get install ntp
```
3. Now install the gpsd daemon which needs to run in the background at startup
``` bash
sudo apt install gpsd gpsd-clients
```
4. Replace /etc/default/gpsd with gpsd in this rep, replace /ect/ntp.conf with ntp.conf in this rep.
5. Start the GPS Daemon and ntp server
```bash
sudo systemctl enable gpsd.service
```
```bash
sudo systemctl start ntp.service
```
6. Connect the TX pin of the GPS to the RX pin of the Raspberry pi (Pin 16 labeled with UART in pinout) Also connect the rest of the GPS propperly to get it in a working state.
7. Do a reboot and check if everything works localy.
```bash
sudo reboot  
```
Overview with GPS information.
```bash
gpsmon
```
ntp server's time and time source
```bash
ntpq -p
```
8. Query the ntp server from windows client to see if it is working:
```shell
w32tm /stripchart /computer:raspberrypi /dataonly /samples:5
```
9. Some other usefull commands:
``` bash
sudo service ntp status
```
``` bash
sudo service ntp start
```
``` bash
sudo service ntp stop
```
``` bash
sudo service ntp restart
```
```bash
ntpq -p
```
