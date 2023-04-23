# Twister-wiki

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



