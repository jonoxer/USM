Universal State Monitor
=======================

Copyright 2019-2021 SuperHouse Automation Pty Ltd  www.superhouse.tv

A binary state monitor for DIY home automation projects.

This system uses UTP cable (typically Cat-5e because it's cheap) to
connect binary sensors to a central controller. The sensors can be 
buttons or switches mounted in wall plates for lighting control, reed 
sensors attached to doors or windows, PIR sensors for motion 
detection, or anything else that reports a binary state.

It also supports rotary encoders (using 2 data lines) to allow up/down
control for media player volume, light dimming, etc.

When a sensor state change is detected the USM will publish an MQTT 
message to the configured MQTT broker for further processing by your
home automation system.


HARDWARE
--------
The USM firmware is compatible with the [Light Switch Controller](https://github.com/SuperHouse/LSC) (LSC) 
and is designed to run on the [Universal Rack Controller](https://github.com/SuperHouse/URC).

The LSC hardware provides 12V power down the line, which can be used
for powering sensors (e.g. PIRs), or illuminating LEDs on light switch
wall plates.

The sensors pull one of 4 signal wires in the cable to 0V to indicate
that they have been activated. The LSC hardware has physical pull up 
resistors to pull the signal wires high and detects when they are pulled low.

More information:

 * http://www.superhouse.tv/lsc
 * http://www.superhouse.tv/urc


CREDITS
-------
 * Jonathan Oxer jon@oxer.com.au
 * Ben Jones <ben.jones12@gmail.com>
 * Moin <https://github.com/moinmoin-sh>


LICENSE
-------
Copyright 2020-2021 SuperHouse Automation Pty Ltd  www.superhouse.tv  

The software portion of this project is licensed under the Simplified
BSD License. The "licence" folder within this project contains a
copy of this license in plain text format.
