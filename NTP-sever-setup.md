# NTP server setup Raspberry pi
This is a little tutorial to quickly setup an NTP server on the RPi because we will need to do this more than once.

## NTP server setup RPi:

1. Get a terminal running on the RPi and navigate to root.
2. Install the ntp server:
``` bash
sudo apt-get install
```
3. Find the config file:
 ``` bash
    cd /etc/ntp.conf</code>
 ```
4. Replace listed server pool with local servers like: 
<code>0.nl.pool.ntp.org </code>
5. Don't forget to start the server:
```bash
sudo service ntp start    
```

6. Query the ntp server from windows client to see if it is working:
```shell
w32t /stripchart /computer:raspberrypi /dataonly /samples
```

7. Some other usefull commands:
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
