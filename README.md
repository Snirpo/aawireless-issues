# AAwireless issue board for beta testers

## Issues
Please use https://github.com/Snirpo/aawireless-issues/issues to post your issues :) You can use the bug report template to report bugs.

## Installation instructions for SD card on Rock Pi S:
1) Open Android Auto Settings on the phone and make sure that Wireless projection is enabled. If it's not please turn on developer mode in Android Auto by tapping the version number 10 times, and enable Wireless projection under developer settings. (See: https://youtu.be/C_XbIW6SLtg)
2) Download and extract the image.
3) Use Win32DiskImage Writer or BalenaEtcher to write it to an SD card
4) Put in the card into the Rock Pi S

## Installtion instructions for NAND:
Please follow this guide:
https://wiki.radxa.com/RockpiS/dev/sdnand-install
To put the 1.1 board into MASKROM please hold button for 10 sec then release.

## Native bluetooth bootstrap:
1) Go to Settings -> BT and unpair any current AAWireless-xxx device
2) Go to the car, plug in the pi to the car and start the car 
2) After about 20 seconds on the phone go to Settings -> BT -> Pair new device
3) Look for AAWireless-xxx device and pair with it
5) Wait a bit longer, you should see the phone connecting to a wifi called AAWireless (keep the screen on)
6) After this you should see a black screen flashing and AA asking you to set up assistant again, then it should show up on the car screen.


## HTTP Endpoints in browser
Remember that these might not work if you don't disable you 4G data.
http://10.42.1.1:8080 -> SWU Update endpoint 
http://10.42.1.1:8000/syslog -> Download latest log
