# atsamd-usb-host

[![Documentation](https://docs.rs/atsamd-usb-host/badge.svg)](https://docs.rs/atsamd-usb-host)
[![Testing](https://api.travis-ci.org/repos/bjc/atsamd-usb-host.svg?branch=master)](https://travis-ci.org/bjc/atsamd-usb-host)

This is a [usb-host](https://github.com/bjc/usb-host) driver for
Atmel's SAMD series of chips.

# Examples

## (Sort of) Simple Example

This assumes you have an [Adafruit Trinket
M0](https://www.adafruit.com/product/3500). You'll need to make
modifications to `Makefile` and `examples/simple/main.rs` for your
board otherwise.

You'll need at least `bossac` installed somewhere in your path in
order to actually do the flashing. You'll also need rust installed for
your target device.

1) Connect a serial port to your device (the Trinket M0 uses pin 4 to
do UART transmission at TTL voltage).

2) Plug the device in, put it into firmware-update mode (double-tap
the reset button on the Trinket M0) and run `make flash`. When it's
done you should see boot messages on your serial device.

3) Unplug the device from the computer, hook it up to another power
supply somehow (I wire GND to ground and USB to 5V), plug in a
keyboard, and hit some keys. You should see it print out the keyboard
reports as keys are pressed and released. Alternately, you may see
error messages if something is broken.
