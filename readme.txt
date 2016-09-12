McRoboFace
==========

McRoboFace has 17 smart pixels organised as a Face
- 0 to 13 for the mouth
- 14 for the nose
- 15 and 16 for the eyes

Each pixel is individually addressable and has 8 bits to define the brightnes of each colour (Red, Green and Blue).

The LEDs are on pin 12 (GPIO 18) of the Raspberry Pi GPIO connector and can be driven in python using the rpi_ws281x.py base library and neopixel.py wrapper

Software Installation
=====================

Ensure your Raspberry Pi is connected to the internet

$ git clone https://github.com/4tronix/mcroboface
$ cd ~/mcroboface
$ sudo apt-get install python-pip python-dev
$ sudo python setup.py install

NB. For Raspbian Jessie release 10th May 2016 (and probably later versions also) you will need to add the following lines in config.txt:
  hdmi_force_hotplug=1
  hdmi_force_edid_audio=1

Now you can run the strandtest.py demo as follows. This is a generic test which displays various colour sequences on all pixels. It doesn't know about the McRoboFace layout
$ sudo python strandtest.py

Also included is a simple demo of the McRoboFace which displays various facial expressions
$ sudo python mcroboface.py


