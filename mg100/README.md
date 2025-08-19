
<logo>![logo](../img/github_doc_header-dark.png#gh-dark-mode-only)</logo><logo>![logo](../img/github_doc_header-light.png#gh-light-mode-only)</logo>
#  Sentrius MG100 Firmware

<table>
  <tr>
    <th align="center">
      <img width="360" height="1" style="max-width: 100%; height: auto; max-height: 1px; visibility:hidden;"/>
      <a href="img/450-00054-k1.png"><img src="img/450-00054-k1.png"/></a><br/>
      Sentrius™ MG100 Gateway<br/>(<a href="https://www.ezurio.com/part/450-00054-k1">450-00054-K1 Shown</a>)
    </th>
    <th align="left">
      <h2>Description</h2>
      The Sentrius™ MG100 is a Python scriptable Bluetooth Low Energy (BLE) to LTE-M/NB-IoT cellular gateway supporting low power IoT solutions. With the addition of the optional battery backup, it provides uninterrupted cloud connectivity to BLE devices. Sentrius MG100 bridges BLE and the cloud.<br/><br/>
      Based on Ezurio's Pinnacle™ 100 modem, the Sentrius MG100 Gateway communicates with Bluetooth 5 devices providing a relay to the cloud via a global low power cellular LTE-M/NB-IoT connection (supports LTE bands 1, 2, 3, 4, 5, 8, 12, 13, 20, and 28). The embedded Nordic nRF52840-based radio supports features like CODED PHY, 2M PHY, and LE Advertising Extensions.<br/><br/>
      Please visit the product page on <a href="https://www.ezurio.com/iot-devices/bluetooth-iot-devices/sentrius-mg100-gateway-lte-mnb-iot-and-bluetooth-5">ezurio.com</a> for more details.
      <h2>Key Specs</h2>
      <table>
        <tr>
          <td><i>Internal Flash</i></td>
          <td>1024 kB</td>
          <td></td>
          <td><i>Internal RAM</i></td>
          <td>256 kB</td>
        </tr>
        <tr>
          <td><i>SPI Flash</i></td>
          <td>8192 kB</td>
          <td></td>
          <td><i>Default REPL Port</i></td>
          <td>UART0 (via USB)</td>
        </tr>
        <tr>
          <td><i>Python Heap Size</i></td>
          <td>~81 kB</td>
          <td></td>
          <td><i>Filesystem Size</i></td>
          <td>6144 kB</td>
        </tr>
      </table>
      <h2>External Links</h2>
      <a href="https://www.ezurio.com/documentation/hardware-guide-mg100-gateway">MG100 Hardware Guide</a><br/>
      <a href="https://www.ezurio.com/documentation/product-brief-usb-swd-programming-kit">USB - SWD Programming Kit</a> (Flash programming adapter)<br/>
      <a href="https://www.tag-connect.com/product/tc2030-idc-6-pin-tag-connect-plug-of-nails-spring-pin-cable-with-legs">Tag-Connect TC2030-IDC</a> (Matches SWD footprint)
    </th>
  </tr>
</table>
<h2>Supported Hardware Variants</h2>
<table>
  <tr>
    <td>450-00011-K1</td><td>Internal Antenna, No Battery</td>
  </tr>
  <tr>
    <td>450-00038-K1</td><td>Internal Antenna, Lithium Ion 18650 Backup Battery</td>
  </tr>
  <tr>
    <td>450-00039-K1</td><td>External Antenna, No Battery</td>
  </tr>
  <tr>
    <td>450-00054-K1</td><td>External Antenna, Lithium Ion 18650 Backup Battery</td>
  </tr>
</table>

## Pinout Diagram <a id="pinout_diagram"></a>[🔗](#pinout_diagram)
[![Sentrius MG100 Gateway Pinout Diagram](img/mg100.svg)](img/mg100.svg)

**NOTE:** Pins prefixed with HL7800 route directly to the HL7800 modem and are not accessible from Python.

## Canvas Features <a id="canvas_features"></a>[🔗](#canvas_features)
| | | | | | | | |
|--:|:--|---|--:|:--|---|--:|:-- |
| ![X](../img/check-32px.png) | Bootloader           | | ![X](../img/check-32px.png) | OTA Update                | | ![X](../img/check-32px.png) | RTC                       |
| ![x](../img/check-32px.png) | SPI                  | | ![X](../img/check-32px.png) | ADC                       | | ![X](../img/redx-32px.png)  | PWM                       |
| ![x](../img/check-32px.png) | I2C                  | | ![X](../img/check-32px.png) | GPIO                      | | ![X](../img/check-32px.png) | UART                      |
| ![x](../img/check-32px.png) | JSON                 | | ![X](../img/check-32px.png) | CBOR                      | | ![X](../img/check-32px.png) | NFC Tag                   |
| ![x](../img/check-32px.png) | RE                   | | ![X](../img/check-32px.png) | Floating Point            | | ![X](../img/check-32px.png) | Watchdog Timer            |
| ![x](../img/check-32px.png) | BLE Advertiser       | | ![X](../img/check-32px.png) | BLE Scanner               | | ![X](../img/check-32px.png) | BLE Connection            |
| ![x](../img/check-32px.png)  | .zip App Update      | | ![X](../img/check-32px.png) | mbedTLS                   | | ![X](../img/blank-32px.png) |                           |

## Hardware-Specific Features <a id="hardware_specific_features"></a>[🔗](#hardware_specific_features)
| | | | | | | | |
|--:|:--|---|--:|:--|---|--:|:--|
| ![x](../img/redx-32px.png)   | USB          | | ![X](../img/redx-32px.png)  | RTOS Shell       | | ![X](../img/redx-32px.png)  | Encrypted FS     |
| ![x](../img/check-32px.png)  | Modem        | | ![X](../img/redx-32px.png)  | Ethernet         | | ![X](../img/redx-32px.png)  | Wi-Fi Station    |
| ![x](../img/redx-32px.png)   | Wi-Fi AP     | | ![X](../img/check-32px.png) | Net Client       | | ![X](../img/redx-32px.png)  | Net Server       |
| ![X](../img/redx-32px.png)   | UWB Ranging  | | ![X](../img/redx-32px.png)  | LED Strip Driver | | ![X](../img/blank-32px.png) |                  |

## Design Guidelines <a id="design_guidelines"></a>[🔗](#design_guidelines)
- Flash programming of the MG100 gateway is available via J5 Tag-Connect footprint. J5 is compatible with [Tag-Connect TC2030-IDC](https://www.tag-connect.com/product/tc2030-idc-6-pin-tag-connect-plug-of-nails-spring-pin-cable-with-legs) or [TC2030-CTX ARM® Cortex™-M4 CPU](https://www.tag-connect.com/product/tc2030-ctx-6-pin-cable-for-arm-cortex) line of plug-of-nail cables and requires this [ARM20-CTX Adapter](https://www.tag-connect.com/product/arm20-ctx-20-pin-to-tc2030-idc-adapter-for-cortex) or [J-Link 9-Pin Cortex-M Adapter](https://www.segger.com/products/debug-probes/j-link/accessories/adapters/9-pin-cortex-m-adapter/). The [Ezurio USB - SWD programming kit](https://www.ezurio.com/wireless-modules/programming-kits/usb-swd-programming-kit) or equivalent SWD programmer may be used, though the TC2030-IDC Tag Connect adapter must be purchased separately.

- Use the [pyocd tool](https://pyocd.io/) to flash Canvas firmware .hex files.

## Build Variants <a id="build_variants"></a>[🔗](#build_variants)
Firmware versions containing `a.b.99` are development builds and may not be suitable for production use.

**Builds within `erase` subfolders are for utility use only, not development. These builds boot and erase the flash-based filesystem.**

| | |
|--:|:--|
| standard                       | Default MG100 gateway build.     |

---
© Copyright 2025 Ezurio LLC
