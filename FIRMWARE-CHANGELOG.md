# Changelog

All notable changes to the firmware will be documented in this file.

## [1.5.0]

### Fixes

- Make led non-blinking white in start / stop mode, the prevent a rainbow effect when running for a long while.
- Revert stopping of the bluetooth handsfree profile, because it made some phones not starting AA at all anymore (constant blinking green).
- Reboot the device on stop in start / stop mode, to force the phone to disconnect from WiFi.
- VAG fix improvements: in some situations VAG headunits still crashed. This still is a workaround, it's an inherent issue in Technisat headunits, we can never fix this completely.

## [1.4.0]

### Fixes

- Add "Default" USB mode which should remove the need for the different USB modes.
- Stop handsfree Bluetooth profile when AA is running, to force phones to switch to the handsfree of the car, should fix phones not using the handsfree of the car for phone calls.  

## [1.3.0]

### Fixes

- Remove time correction setting and replace by VAG head unit crash fix.
- Improve start / stop functionality

## [1.2.1-3]

### Fixes

- “DRAM fix” is integrated in this OTA update. If you update to 1.2.3, you don’t need the “DRAM fix” tool anymore. However for some devices it might almost be impossible to do an OTA update because of instability, for those devices you do need to apply the DRAM fix first.
- Wifi stuttering / crashes fixed for some devices.

## [1.2.0]

### Features

- Add auto video focus function: This function makes AA automatically show on screen for some cars, instead of manually having to press a button to start AA. It might also fix AA never showing, or not be able to start AA on the head unit.
- Start / stop with car: On some cars the USB port always stays powered, which means AAWireless will constantly try to connect to the phone, even when the car is off. We implemented functionality to start up AAWireless when the phone connects to the Bluetooth Headset connection of the car and disconnects when the Bluetooth Headset connection is lost.
- Change WiFi connect timeout. Some phones sometimes don’t connect to the Wifi hotspot of AAWireless when AA is started. AAWireless has a timeout of 20 seconds by default (30 seconds in 1.0.0) for restarting the whole process. This can be a bit long, so we made it configurable.

### Fixes

- The “Mazda” fix: On some cars, AAWireless only connects the first time on pairing, and after that it is very hard to connect. There was a bug in the code which caused a delay, and this influenced the “startup” phase of Android Auto.
- We updated the Android Auto protocol messages which should fix weird issues for some, for example having the wrong screen resolution when not in Passthrough mode.
- Bug report functionality has been fixed. We will also improve the app side next week in order to improve feedback about what is happening.

## [1.1.0]

### Fixes

- Fix debug logging.
