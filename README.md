# makeblock-auriga-ms12a-smartservo-python

This is a script to control Makeblock MS12a smart servos connected to a
Makeblock Me Auriga controller.

It was extracted from [https://github.com/tlack/dobot-tcn/](my robot training framework)
because I thought it might be useful to others.

## Features and Status

This supports any number of connected smart servos and reports their positions.

Since this was intended for robotic applications, we refer to each motor as a
"joint" in the code and this document. 

You can move a joint to any position and report on joint positions.

You can set a goal position and receive a callback when it is attained.

You can test motor fitness through a limited range of motions by turning on
"tweaking" for each 

## What's here?

#### Makeblock-Auriga-SmartServoMS12a.ino

This is an Arduino sketch that provides new firmware for your Auriga. This new firmware
is a highly optimized ASCII protocol that allows you to control your bot over serial
from your Raspberry Pi. 

Note that Makeblock provides some connectivity with their standard firmware but the
protocol isn't well documented and frankly I didn't care to bother with it.

**Load this on your Auriga first** before continuing to the Python stage.

#### Auriga.py

This is a PySerial-based wrapper that speaks to the firmware and provides a
super simple class wrapper.
See source for usage.

## Need help?

This is a tiny library. See source. Create a Github issue if you need more help.

