******************************
Appendix G Advanced Networking
******************************

nm-tray has the benefit of being Qt instead of GTK (use already loaded libraries, consuming less resources) and lighter than conman. But, it is a little short for more complicated networking like VPN.

VPN:
To configure a VPN the best way to do it is with "Advanced Network Confiruation" in the Menu under Preferences. That will open network-manager-gnome you will need also to install the correaponding packages. In case of pptp those will be network-manager-pptp and network-manager-pptp-gnome. The you can follow the confiruation instruction for each VPN type.
After the creation, it will appear as a new connection in nm-tray. One thing to consider is that nm-tray does not support password asking, so either you save the password FOR ALL USERS or you will need to connect diffently. 
One of the  option is throug terminal with typing "nmcli con up id <VPN_name> --ask" changing <VPN_name> with the actual VPN connection name.
The other option is to use nm-applet, the "simil" to nm-tray from network-manager.gnome. You can run it from the terminal typing "nm-applet", and you will end up with 2 connection indicators in the tray. The you can connect to the vpn with nm-applet and after the connection is established, you can close nm-applet and the connection will still be present.

Changing nm-tray for nm-applet
If you don't want to run by terminal nm-applet you could change nm-tray for nm-applet. You will need to change the autostart. The easiest form to do this from the GUI is in the Menu going to Preferences -> LXQt configuration -> Session Configuration. There go to "Automatic Startup". You will see a list with checked and unchecked box, to autostart nm-applet, check "Network" to disable autostart for nm-tary uncheck nm-tray.
