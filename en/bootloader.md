# Bootloader

This project uses `USBaspLoader` as a USB bootloader.

- https://www.obdev.at/products/vusb/usbasploader.html
- Customized bootloader for Tartan
  https://github.com/hsgw/USBaspLoader/tree/plaid
- When writing the bootloader to the ATMEGA328P, which has nothing written to it, be sure to write the fuse bit as well.

## If you purchased the kit, the bootloader has already been written to ATMEGA328P

## Windows

Device driver installation is required. Please install
using zadig `libusbK`.

- https://zadig.akeo.ie/
- https://ht-deko.com/arduino/usbasp.html

## How to enter bootloader mode

1. Plug in the USB cable
2. `RESET` Hold down the switch
3. `BOOT` Hold down the switch
4. `RESET` Release the switch
5. `BOOT` Release the switch

If you enter the boot loader mode, it will be recognized as `usbasp` by the device manager of your PC .

## Boot loader is not recognized by PC

- Check parts and soldering near ATMEGA328P

  - Orientation of ATMEGA328P
  - Soldering BOOT switch and RESET switch

    - Short each switch pin

  - USB connector
  - Resistors and Zener diodes

- Try other cables, PCs, USB hubs
- Remove the USB hub and connect directly to the PC

## Testing with avrdude

`usbasp` After being recognized as, execute the following command in the terminal. If you have not set up QMK Firmware, please set up [firmware.md](./firmware.md)

```
avrdude -c usbasp -p m328p
```

If there is no problem, the following display will be displayed.

```
\$ avrdude -c usbasp -p m328p
avrdude.exe: AVR device initialized and ready to accept instructions
Reading | ################################################## | 100% 0.00s
avrdude.exe: Device signature = 0x1e950f (probably m328p)
avrdude.exe done. Thank you.
```

## NEXT

[Build and write QMK Firmware](./firmware.md)
