
![http://creativecommons.org/licenses/by-sa/4.0/]
[Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](http://creativecommons.org/licenses/by-sa/4.0/deed.en_US)


# All-in-one FPGA companion

This device is designed to be a highly versatile companion to any FPGA board.
It allows programming of FPGA devices and is also useful interface to them.

In early developer it useful by providing virtual serial interfaces to easily
start debugging.

In late development when loaded with custom firmware it provides a high speed
(>30 mega**bytes**/s) interface for getting data into and out of the FPGA which
can emulate most consumer devices such as storage, camera or displays.




## Basic Features

 * Acts as a JTAG programmer compatible with both the NeroJTAG and XXXX
   protocols (allowing usage with libfpgalink and XXXX).

 * 



This device is very similar to the XXX logic analyzers but has two major
differences,

 * It uses the higher pin count FX2 chip giving hardware UARTs.
 * It has the pins mapped suitable to JTAG and PMOD style headers for easy
   connection to an FPGA.
 * The design and firmware are all open source.

## BOM

 * Cypress FX2 IC.
 * EEPROM.
 * Micro USB header.
 * 5V to 3.3V regulator.
 * Pin headers.
 * Misc passives (decoupling caps, protection resistors, etc)

## Features

JTAG header compatible with NeroJTAG (libfpgalink) / urjtag. Can program FPGAs,
SPI flashes, etc.

The remaining FX2 pins are broken out onto "dual" PMOD compatible headers.
Each PMOD header can act PMOD slave be talked to by an FPGA or other device,
or as a PMOD host and talk to many PMOD expansion boards[1]. 

The I2C bus on the FX2 is mapped to an "I2C PMOD" compatible header. Note
that I2C is used to boot the FX2 chip so if using this header care should
be taken to not interfere with the boot process.

PMOD header XXX is mapped to the hardware UART in the FX2 chip. This PMOD
header is able to operate serial protocols significantly faster then the other
bit banging ports.

Any of the PMOD headers are able to operate as a TTL serial to USB converter
however the speed is limited. The PMOD header XXXX is able operate in this mode
significantly faster.

PMOD header XXX, XXX and XXX can be combined together and then custom firmware
loaded onto the FX2 for a very high speed USB2.0 interface (>30 megabytes/s).



 [1]: Compatibility with PMOD expansion boards depends on I/O voltages and
      speed required. 

The device is compatible with the "XXXX" firmware allowing it to also be a
generic, low speed logic analyzer.

