
<logo>![logo](../img/github_doc_header-dark.png#gh-dark-mode-only)</logo><logo>![logo](../img/github_doc_header-light.png#gh-light-mode-only)</logo>
#  nrf52840 Firmware

<table>
  <tr>
    <th align="center">
      <img width="380" height="1" style="max-width: 100%; height: auto; max-height: 1px; visibility:hidden;"/>
      <a href="img/pca-10059.png"><img src="img/pca-10059.png"/></a><br/>
      Nordic nRF52840 Dongle (<a href="https://www.nordicsemi.com/Products/Development-hardware/nRF52840-Dongle">PCA10059</a>)
    </th>
    <th align="left">
      <h2>Description</h2>
The nRF52840 Dongle is a small, low-cost USB dongle that supports Bluetooth 5.4, Bluetooth mesh, Thread, Zigbee, 802.15.4, ANT and 2.4 GHz proprietary protocols. The Dongle is the perfect target hardware for use with nRF Connect for Desktop as it is low-cost but still support all the short range wireless standards used with Nordic devices.<br/><br/>
Custom applications can be compiled and downloaded to the Dongle. It has a user programmable RGB LED, a green LED, a user programmable button as well as 15 GPIO accessible from castellated solder points along the edge.
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
          <td>None</td>
          <td></td>
          <td><i>Default REPL Port</i></td>
          <td>nRF USB</td>
        </tr>
        <tr>
          <td><i>Python Heap Size</i></td>
          <td>~155 kB</td>
          <td></td>
          <td><i>Filesystem Size</i></td>
          <td>380 kB</td>
        </tr>
      </table>
      <h2>External Links</h2>
      <a href="https://www.nordicsemi.com/-/media/Software-and-other-downloads/Product-Briefs/nRF52840-Dongle-product-brief.pdf">nRF52840 Dongle product brief</a><br/>
    </th>
  </tr>
</table>

## Pinout Diagram <a id="pinout_diagram"></a>[🔗](#pinout_diagram)
[![nRF52840 Dongle Pinout Diagram](img/nrf52840dongle.svg)](img/nrf52840dongle.svg)

## Canvas Features <a id="canvas_features"></a>[🔗](#canvas_features)
| | | | | | | | |
|--:|:--|---|--:|:--|---|--:|:-- |
| ![X](../img/check-32px.png) | Bootloader *         | | ![X](../img/redx-32px.png)  | OTA Update                | | ![X](../img/check-32px.png) | RTC                       |
| ![x](../img/check-32px.png) | SPI                  | | ![X](../img/redx-32px.png)  | ADC                       | | ![X](../img/redx-32px.png)  | PWM                       |
| ![x](../img/redx-32px.png)  | I2C                  | | ![X](../img/check-32px.png) | GPIO                      | | ![X](../img/check-32px.png) | UART                      |
| ![x](../img/redx-32px.png)  | JSON                 | | ![X](../img/check-32px.png) | CBOR                      | | ![X](../img/redx-32px.png)  | NFC Tag                   |
| ![x](../img/redx-32px.png)  | RE                   | | ![X](../img/check-32px.png) | Floating Point            | | ![X](../img/check-32px.png) | Watchdog Timer            |
| ![x](../img/check-32px.png) | BLE Advertiser       | | ![X](../img/check-32px.png) | BLE Scanner               | | ![X](../img/check-32px.png) | BLE Connection            |
| ![x](../img/redx-32px.png)  | .zip App Update      | | ![X](../img/check-32px.png) | mbedTLS                   | | ![X](../img/blank-32px.png) |                           |

\* Supports the Nordic DFU bootloader only

## Hardware-Specific Features <a id="hardware_specific_features"></a>[🔗](#hardware_specific_features)
| | | | | | | | |
|--:|:--|---|--:|:--|---|--:|:--|
| ![x](../img/redx-32px.png) | USB          | | ![X](../img/redx-32px.png) | RTOS Shell       | | ![X](../img/redx-32px.png)  | Encrypted FS     |
| ![x](../img/redx-32px.png) | Modem        | | ![X](../img/redx-32px.png) | Ethernet         | | ![X](../img/redx-32px.png)  | Wi-Fi Station    |
| ![x](../img/redx-32px.png) | Wi-Fi AP     | | ![X](../img/redx-32px.png) | Net Client       | | ![X](../img/redx-32px.png)  | Net Server       |
| ![X](../img/redx-32px.png) | UWB Ranging  | | ![X](../img/redx-32px.png) | LED Strip Driver | | ![X](../img/blank-32px.png) |                  |

## Design Guidelines <a id="design_guidelines"></a>[🔗](#design_guidelines)
**IMPORTANT**
- Pressing the RESET button places the dongle into nRF DFU/bootloader mode. This mode is only useful for programming firmware (e.g., Canvas) to the device using nrfutil or the nRFConnect Desktop Programmer.
- If using mcuboot, Pin P1.06 is used by the mcuboot bootloader to enter recovery mode when logic low at boot.<br/>*(NOTE: default Canvas firmware variant does not use mcuboot on this part.)*
- If using mcuboot, Pin P0.06 is used by the mcuboot bootloader as its LED indicator. This is active high if in bootloader recovery mode.<br/>*(NOTE: default Canvas firmware variant does not use mcuboot on this part.)*

## Build Variants <a id="build_variants"></a>[🔗](#build_variants)
Firmware versions containing `a.b.99` are development builds and may not be suitable for production use.

| | |
|--:|:--|
| dongle                      | Targets the [Nordic nRF52840 dongle (PCA10059)](https://www.nordicsemi.com/Products/Development-hardware/nRF52840-Dongle). |

---
© Copyright 2025 Ezurio LLC
