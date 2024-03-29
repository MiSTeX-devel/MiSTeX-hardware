# **MiSTeX Board**

### Connectors and main headers

- Headers for QMTech 128 pins FPGA format (2x 2x32)
- MiSTer SDRAM module header (Terasic 2x20)
- RPi header (Orange Pi 2W) (2x20)
- SNAC user port for gamepads / mt32pi (USB3)
- VGA video out (DB15)
- HDMI video out
- Analog audio out (delta sigma) (jack 3.5) 
- SPDID audio out (Toslink)
- Secondary uSD Card
- PMOD J11 header (GPIO / I2S / Delta-sigma)
- USB C for RP2040 programming
- USB C power supply



### Power Supply

It is recommended to use the USB power port since it uses a voltage filter. This port supply power to FPGA and Orange Pi as well.

The Jumper on the power port is for an external power switch mounted in a case for example. 

<u>J18 needs to be shorted with a jumper if no switch is placed</u>.

![image](https://github.com/MiSTeX-devel/MiSTeX-hardware/assets/148607/bc3dd750-81ea-4263-94c7-44f6ad40ac5e)

You can of course also power the board from the core board barrel jack.



### FPGA programming

Connect an USB-C from RP2040 port to the USB HUB you are using

Connect Dupont wires from FPGA JTAG to JTAG header on MiSTeX board



### Switches / Jumpers / small headers / Leds

J9 RC2040 Boot jumper. Short to reprogram RC2040 firmware

J10 SCART VGA pin 9 jumper. Short to use a VGA to SCART cable

J18 Power switch (or either place a jumper if no switch is added)

IO6 Jumper - By default shorted 2-3 for most gamepads. Some accessories require additional 3V3 power supply, in that case put jumper in position 1-2 next to +3V3 text.



SW1 Button User (RPi/Orange Pi)

SW2 Button OSD  (RPi/Orange Pi)

SW3 Button Reset  (RPi/Orange Pi)

SW4 Button Menu  (RPi/Orange Pi)



The side switches SW5, SW6 are currently unused and have been erroneously momentary in rev1, but should actually be latching which has been fixed in rev2

- SW5 (FPGA) will be used to switch the Pmod signals from I2S to general purpose use

- SW6 (RPi/Orange Pi)  is intended to switch the SNAC port from SNAC to mt32pi mode

  

The DIP switches are currently unused too  (RPi/Orange Pi).



User / HDD / Power Leds



DBG J7 Debug UART (RC2040)

SWD J12 Header (RC2040)

JTAG J6 Header   (RC2040)

ADC J14 Header (3 ADC + 1 GPIO)  (RC2040)



### SD image (placed at Orange Pi SD slot)

```sh
$ ffsend download http://files.hans-baier.de:1443/download/c89c19c1d909e5d4/#E7y8NQxA-L7gW781eJqsCw
```

The boot image needs the menu core at /media/fat/menu.bit
or menu.rbf for Altera boards
The sdcard image above is preconfigured for the Artix 100t QmTech with pre built cores
But A200T and K325T cores are included too
You only need to copy the right one to menu.bit



### RP2040 firmware

You need to bridge the boot jumper J9 and plug the RC2040 USB port into a PC to flash this firmware: https://github.com/MiSTeX-devel/pico-dirtyJtag/releases/tag/v0.0.1
The core FPGA board needs to be present there because it powers the 2040 except you power the 3.3v rails from another source.

Connect power supply either to FPGA barrel or USB-C power port.

Copy the uf2 file into the mass storage device that appears on PC. When the file disappears it means it is flashing the firmware. Wait a bit and disconnect USB-C and remove jumper.
