![header](img/canvas_logo-dark.png#gh-dark-mode-only)
![header](img/canvas_logo-light.png#gh-light-mode-only)

### Python Application Development for Embedded Wireless Products

**Canvas Software Suite** is Ezurio's embedded microcontroller-based software platform enabling Python application development to speed scaling from PoC to production.

Write your embedded app in Python without setting up complex SDKs or time-consuming build steps.

Python support is based on the [MicroPython](https://github.com/micropython/micropython) engine.

### Canvas Software Suite Firmware

To get started developing Python applications with Canvas, download the firmware image file(s) and program them onto your Canvas-enabled module, development kit or IoT product. Firmware files and documentation for supported hardware platforms can be found at the links below.

- [BL5340](bl5340)
- [BL54L10](bl54l10)
- [BL54L15](bl54l15)
- [BL653](bl653)
- [BL654](bl654)
- [Lyra24](lyra24)
- [nRF52840 USB Dongle](nrf52840/dongle)
- [Pinnacle 100](pinnacle_100)
- [Sentrius BT510](bt510)
- [Sentrius BT610](bt610)
- [Sentrius MG100 Gateway](mg100)
- [Sentrius RS26x](rs26x)
- [Sera NX040](sera_nx040)
- [Veda SL917](veda_sl917)

For more information about Canvas Software Suite see [the Ezurio website](https://www.ezurio.com/canvas/software-suite).

### Erase Builds

For products supporting filesystems and secondary bootloader update areas, a special `erase`
build may be available alongside the `firmware` directory. The builds in the `erase` directory
**will erase** the contents of filesystems and secondary bootloader update areas when executed.
Only use these builds if you have a need to erase a device. Once the firmware has finished erasing,
it will print a `Board is erased` message. At this point, the normal Canvas firmware should
be reflashed onto the device.

**Do not use** `erase` builds for normal Canvas development.
