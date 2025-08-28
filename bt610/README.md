
<logo>![logo](../img/github_doc_header-dark.png#gh-dark-mode-only)</logo><logo>![logo](../img/github_doc_header-light.png#gh-light-mode-only)</logo>
#  Sentrius BT610 Firmware

<table>
  <tr>
    <th align="center">
      <img width="380" height="1" style="max-width: 100%; height: auto; max-height: 1px; visibility:hidden;"/>
      <a href="img/450-00121-k1.png"><img src="img/450-00121-k1.png"/></a><br/>
      Sentrius™ BT610 Sensor (<a href="https://www.ezurio.com/part/450-00121">450-00121-K1</a>)
    </th>
    <th align="left">
      <h2>Description</h2>
      Ezurio's Sentrius™ BT610 I/O Sensor is a battery-operated Bluetooth 5 open development device that helps turn your wired sensors into wireless nodes via robust, secure, and cloud ready messaging. It leverages our BL654 module for full industrial and equipment monitoring applications.<br/><br/>
      Please visit the product page on <a href="https://www.ezurio.com/iot-devices/bluetooth-iot-devices/sentrius-bt610-io-sensor">ezurio.com</a> for more details.
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
          <td>UART0</td>
        </tr>
        <tr>
          <td><i>Python Heap Size</i></td>
          <td>~169 kB</td>
          <td></td>
          <td><i>Filesystem Size</i></td>
          <td>7168 kB</td>
        </tr>
      </table>
      <h2>External Links</h2>
      <a href="https://www.ezurio.com/documentation/bt610-hardware-configuration-and-installation-guide">BT610 Hardware Configuration and Installation Guide</a><br/>
      <a href="https://www.ezurio.com/documentation/application-note-ac-current-sensor-demo">Canvas AC Current Sensor Demo</a><br/>
      <a href="https://www.ezurio.com/documentation/product-brief-usb-swd-programming-kit">USB - SWD Programming Kit</a> (Required for development)
    </th>
  </tr>
</table>

## Pinout Diagram <a id="pinout_diagram"></a>[🔗](#pinout_diagram)
[![Sentrius BT610 Sensor Pinout Diagram](img/bt610.svg)](img/bt610.svg)

## Canvas Features <a id="canvas_features"></a>[🔗](#canvas_features)
| | | | | | | | |
|--:|:--|---|--:|:--|---|--:|:-- |
| ![X](../img/check-32px.png) | Bootloader           | | ![X](../img/check-32px.png) | OTA Update                | | ![X](../img/check-32px.png) | RTC                       |
| ![x](../img/check-32px.png) | SPI                  | | ![X](../img/check-32px.png) | ADC                       | | ![X](../img/redx-32px.png)  | PWM                       |
| ![x](../img/check-32px.png) | I2C                  | | ![X](../img/check-32px.png) | GPIO                      | | ![X](../img/check-32px.png) | UART                      |
| ![x](../img/redx-32px.png)  | JSON                 | | ![X](../img/check-32px.png) | CBOR                      | | ![X](../img/redx-32px.png)  | NFC Tag                   |
| ![x](../img/redx-32px.png)  | RE                   | | ![X](../img/check-32px.png) | Floating Point            | | ![X](../img/check-32px.png) | Watchdog Timer            |
| ![x](../img/check-32px.png) | BLE Advertiser       | | ![X](../img/check-32px.png) | BLE Scanner               | | ![X](../img/check-32px.png) | BLE Connection            |
| ![x](../img/redx-32px.png)  | .zip App Update      | | ![X](../img/check-32px.png) | mbedTLS                   | | ![X](../img/blank-32px.png) |                           |

## Hardware-Specific Features <a id="hardware_specific_features"></a>[🔗](#hardware_specific_features)
| | | | | | | | |
|--:|:--|---|--:|:--|---|--:|:--|
| ![x](../img/redx-32px.png)  | USB          | | ![X](../img/redx-32px.png)  | RTOS Shell       | | ![X](../img/redx-32px.png)  | Encrypted FS     |
| ![x](../img/redx-32px.png)  | Modem        | | ![X](../img/redx-32px.png)  | Ethernet         | | ![X](../img/redx-32px.png)  | Wi-Fi Station    |
| ![x](../img/redx-32px.png)  | Wi-Fi AP     | | ![X](../img/redx-32px.png)  | Net Client       | | ![X](../img/redx-32px.png)  | Net Server       |
| ![X](../img/redx-32px.png)  | UWB Ranging  | | ![X](../img/redx-32px.png)  | LED Strip Driver | | ![X](../img/blank-32px.png) |                  |

## Design Guidelines <a id="design_guidelines"></a>[🔗](#design_guidelines)
- Flash programming and development with the BT610 sensor requires the [Ezurio USB - SWD programming kit](https://www.ezurio.com/wireless-modules/programming-kits/usb-swd-programming-kit) (or equivalent SWD programmer with an [ARM Cortex M 0.05" pitch SWD debug header](https://www.segger.com/products/debug-probes/j-link/accessories/adapters/9-pin-cortex-m-adapter/))
- Use the [pyocd tool](https://pyocd.io/) to flash Canvas firmware .hex files.

## Build Variants <a id="build_variants"></a>[🔗](#build_variants)
Firmware versions containing `a.b.99` are development builds and may not be suitable for production use.

**Builds within `erase` subfolders are for utility use only, not development. These builds boot and erase the flash-based filesystem.**

| | |
|--:|:--|
| standard                       | Default BT610 sensor build.     |

---
© Copyright 2025 Ezurio LLC
