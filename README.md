# Lucca 58HE
The Lucca 58HE is a 58 key hall effect split keyboard!

This keyboard is still very much a work in progress!! Kicad files for PCBs and switch plate, 3d files for case all available. Currently working under KMK!

![IMG_6700](https://github.com/user-attachments/assets/aa22d8b3-7bef-4428-90fe-1be624bb01be)
Maka8295's

## Features

- Fully addressable per-key RGB
- 10-point RGB Underglow on each half
- Full USB-C support
- Hardware support for both SPI and UART communication between halves
- OLED screens
- Rapid Trigger
- 3D Printed Case
- Compatible with standard HE Switches, I reccomend Gateron Jades

![IMG_6701](https://github.com/user-attachments/assets/d41b9f8e-27c2-444f-80f4-b9e1a3898853)
Maka8295's
## Bill of Materials

- Multiplexer - ADG732BSUZ 
- MCU - Waveshare RP2040 Zero 
- OLED - SSD1306 128x32 
- HE Sensor - DRV5053VAQDBZR 
- Resistor, 1.5k Ohm, 0805 package, (for filter)
- resistor, 4.7k Ohm, 0805 package (for I2C/Pullup)
- Resistor, 0 Ohm, 0805 package (for UART mode)
- capacitor, 100nF, 0805 package
- LED, SK6803 MINI-E
- 2.54mm PH5 Short Profile Single Row Straight 1X5P (to be used as a socket for RP2040)
- 2.54mm PH5 Short Profile Single Row Straight 1X9P (to be used as a socket for RP2040)
- 2.54mm PH5 Short Profile Single Row Straight 1X4P (to be used as a socket for OLED, otherwise it can be a pain to access to boot and reset buttons)
- M2.5, 3mm brass stand offs 
- M2.5, 12mm screws with flat tops
- M2.5 x 6 x 0.4mm washers 
- M2.5 nuts 1.8mm thick
- Maka8295's 3d Printed case!

## How To Install

-I sourced the parts on aliexpress and ebay.
- Order of assembly isnt too hard, just dont start with the LED's.  I figured they were the easiest and not too close the other parts... but i was wrong and melted a bunch of the backs.  They are probably still good... but they have some scars due to my deaf hands.  I recommend starting with the HE sensors, then the Capacitors and resistors.
- After that, I recommend installing sockets for the OLED and RP2040.  It's not necessary, but for those who lack the necessary skills to hand solder SMD chips well enough... expect a damaged PCB and the need to remove expensive components without much fuss.
- 

- After assembly, load up the RP2040 with circuitpy

## To do
f
- implement auto calibration
- ZMK port

//Maka8295's notes
  Am currently typing this update from the Lucca58HE! So its fully up and running now! There is definitely a slight latency with UART on the slave half of the keyboard. The
  PCB supports SPI which could potentialy have latency reductions. It might also be possible to get UART latency down too, especially once im using QMK.


  OLD STATUS UPDATES:

  Left half of the keyboard is now perfectly functioning under KMK! changing the actuation from from 0 to 3.5mm is possible, but some weirdness means theres a deadzone
  towards the end of the keystroke, it can be fixed by increasing the distance between the switch plate and PCB so not a big deal. Could probably be avoided with differnt
  HE   sensors?

  Working with QMK has proved a lot more difficult than i thought, so im going to get it working with KMK and circuitpython first, and then worry about QMK support after!

  Hall effect sensors are currently resulting in a resolution of 0.00706mm, so things are looking very promising. My choice of HE sensor results in a voltage range of ~0 to 
  ~0.4v, so using a different HE sensor with a greater sensitivity (not to be confused with resolution) could result in even greater resolution of distance traveled, as the 
  12bit ADC on the RP2040 references the internal 3.3v. Am going on family holiday soon so progress will slow down a lot, may not be able to finish the project until the 
  new year...



![IMG_6613](https://github.com/Maka8295/Lucca-58HE/assets/108311420/4b1c28fb-dfae-451a-887c-c89deb428f4d)
Maka8295's

![IMG_6614](https://github.com/Maka8295/Lucca-58HE/assets/108311420/ee2d040d-f45c-473e-afe9-ba04d163128f)
Maka8295's


