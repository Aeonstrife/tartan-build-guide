# Firmware

# Firmware location

It is in the QMK Firmware head family.

https://github.com/qmk/qmk_firmware

## QMK Firmware setup

- https://github.com/qmk/qmk_firmware
- https://docs.qmk.fm/#/newbs_getting_started

## Build and write default keymaps

In the terminal, go to the directory to QMK Firmware

#### Firmware build only

```
make dm9records/tartan:default
```

#### Build and write to Plaid

After putting Tartan in bootloader mode

```
make dm9records/tartan:default:flash
```

## Tested with jumper wire

After writing the default keymap for the first time, it is recommended to test if you can actually type with a suitable jumper wire and resistor foot before soldering the keyswitch.

## Keymap customization

- https://docs.qmk.fm/#/newbs_building_firmware

## After improving the firmware

Send PR!

## NEXT

[Switch soldering and bottom PCB installation](./complete.md)
