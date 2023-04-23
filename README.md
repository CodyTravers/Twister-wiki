# Twister-wiki

![alt text](https://raw.githubusercontent.com/CodyTravers/Twister-wiki/main/TwisterFPGA.png?raw=true)


Demo images are all 32GB right now. 
I suspect this will change in the future. 

**Wifi:**

To set up wifi, press F9 while in the Menu core. 

```nmcli device wifi connect <NETWORK_NAME> password <PASSWORD>```

Press F12 to return to the Menu core.

**Bluetooth:**

Press F11 while in the Menu core and follow the on screen prompts

**CIFS:**

Edit /etc/systemd/system/media-fat-games.mount 

Press F9 while in the Menu core.

```systemctl enable media-fat-games.mount```

```systemctl start media-fat-games.mount```

To stop/dsable CIFS press F9 while in the Menu core.

```systemctl disable media-fat-games.mount```

```systemctl stop media-fat-games.mount```

**HDMI Audio buffer**

Set the number of frames per buffer, a lower value will decrease the latency, but will increase cpu overhead and glitches. The default value is 256.

The buffer value is set in

/etc/MicrophoneLoopback/MicrophoneLoopback.conf

HDMI Audio is started by systemd the unit can be found at:

/etc/systemd/system/HDMI-audio.service


**Setting timezones**

Press F9 while in the Menu core. 

Find your timezone:

```timedatectl list-timezones```

```timedatectl set-timezone <timezone>```
