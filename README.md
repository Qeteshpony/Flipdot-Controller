# Flipdot Controller

[![CI](https://github.com/Qeteshpony/Flipdot-Controller/actions/workflows/ci.yml/badge.svg)](https://github.com/Qeteshpony/Flipdot-Controller/actions/workflows/ci.yml)


![3D Render](https://qeteshpony.github.io/Flipdot-Controller/3D/Flipdot%20Controller-3D_top.png)

[Documentation](https://qeteshpony.github.io/Flipdot-Controller)


Replacement controller for a Lawo Luminator Flipdot Display

(This was designed and built in 2022, I just never published the sources so here we go)

The project is based around a Raspberry Pi Zero W which replaces the microcontroller/EPROM combination from the original controller board. I reverse engineered the original board and used some of its components, the two transistor arrays, to control the lines of the display. The columns are driven by the original FP2800A drivers. 

The board is designed using KiCAD with production and assembly by JLCPCB in mind. All parts are selected to be available from JLCPCB at the time of writing and as many parts as possible are used from their basic library.

It is made to fit onto the screw holes for the original board with help of a little 3D-printed adapter that also holds a 18V power supply. 

The ATtiny is connected to the raspberry pi via I2C and controls the backlight of the display which I replaced with UV LED strips. 

### FlipDotControllerBackpanel
This folder contains the sources for a small board I mounted into the casing backpanel of the display to show state of the raspberry pi and have a way to shut it down through a button. 
