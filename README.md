# Twister-wiki

![alt text](https://raw.githubusercontent.com/CodyTravers/Twister-wiki/main/TwisterFPGA.png?raw=true)


Most demo images are all 32GB other than install images.

**Install img files**

Install image files include a first boot process that auto-expands the /media/fat/ partition to fill the remaining space on SD Card with an exfat partition. Install image files require an SD Card of 8GB or larger.

The first boot process takes under 2 minutes and the will reboot to the MiSTer Menu when complete. 

Twister can then be updated via the normal update process (when this becomes avalible).


**Wifi:**

To set up wifi, press F9 while in the Menu core. 

```nmcli device wifi connect <NETWORK_NAME> password <PASSWORD>```

Press F12 to return to the Menu core.

**Bluetooth:**

Press F11 while in the Menu core and follow the on screen prompts

**CIFS:**

Press F9 while in the Menu core.

Edit /etc/systemd/system/media-fat-cifs.mount and add the correct information.

```systemctl enable media-fat-cifs.mount```

```systemctl start media-fat-cifs.mount```

To stop/dsable CIFS press F9 while in the Menu core.

```systemctl disable media-fat-cifs.mount```

```systemctl stop media-fat-cifs.mount```

**HDMI Audio buffer**

Set the number of frames per buffer, a lower value will decrease the latency, but will increase cpu overhead and glitches. The default value is 256.

The buffer value is set in

/etc/MicrophoneLoopback/MicrophoneLoopback.conf

HDMI Audio is started by systemd, the unit can be found at:

/etc/systemd/system/HDMI-audio.service


**Setting timezones**

Press F9 while in the Menu core. 

Find your timezone:

```timedatectl list-timezones```

```timedatectl set-timezone <timezone>```

**Updates**


```apt update```

```apt upgrade```

```apt install twister-console```

```apt install twister-arcade```

```apt install twister-computer```

```apt install twister-utils```


