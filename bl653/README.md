<logo>![logo](../img/github_doc_header-dark.png#gh-dark-mode-only)</logo><logo>![logo](../img/github_doc_header-light.png#gh-light-mode-only)</logo>
#  BL653 Firmware

<table>
  <tr>
    <th align="center">
      <img width="380" height="1" style="max-width: 100%; height: auto; max-height: 1px; visibility:hidden;"/>
      <a href="img/453-00039-k1.png"><img src="img/453-00039-k1.png"/></a><br/>
      BL653 DVK (<a href="https://www.ezurio.com/part/453-00039-k1">453-00039-k1</a>)
    </th>
    <th align="left">
      <h2>Description</h2>
      Ezurio’s BL653 development kits provide a platform for rapid prototyping of BL653 modules. The development boards provide simple, easy-to-use access to the various hardware interfaces and configuration options for the modules. These DVKs are the perfect platform to provide early development testing of BL653 features and functionality.<br/><br/>
      Please visit the product page on <a href="https://www.ezurio.com/wireless-modules/bluetooth-modules/bluetooth-5-modules/bl653-series-bluetooth-51-802154-nfc-module">ezurio.com</a> for more details.
      <h2>Key Specs</h2>
      <table>
        <tr>
          <td><i>Internal Flash</i></td>
          <td>512 kB</td>
          <td></td>
          <td><i>Internal RAM</i></td>
          <td>128 kB</td>
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
          <td>~41 kB</td>
          <td></td>
          <td><i>Filesystem Size</i></td>
          <td>32 kB</td>
        </tr>
      </table>
      <h2>External Links</h2>
      <a href="https://www.ezurio.com/documentation/datasheet-bl653-series">BL653 Series Datasheet</a><br/>
      <a href="https://www.ezurio.com/documentation/user-guide-bl653-development-kit">BL653 DVK User Guide</a>
    </th>
  </tr>
</table>

## Pinout Diagram <a id="pinout_diagram"></a>[🔗](#pinout_diagram)
[![BL653 DVK Pinout Diagram](img/bl653_dvk.svg)](img/bl653_dvk.svg)

## Canvas Features <a id="canvas_features"></a>[🔗](#canvas_features)
| | | | | | | | |
|--:|:--|---|--:|:--|---|--:|:-- |
| ![X](../img/redx-32px.png)  | Bootloader           | | ![X](../img/redx-32px.png)  | OTA Update                | | ![X](../img/check-32px.png) | RTC                       |
| ![x](../img/check-32px.png) | SPI                  | | ![X](../img/check-32px.png) | ADC                       | | ![X](../img/redx-32px.png)  | PWM                       |
| ![x](../img/check-32px.png) | I2C                  | | ![X](../img/check-32px.png) | GPIO                      | | ![X](../img/check-32px.png) | UART                      |
| ![x](../img/redx-32px.png)  | JSON                 | | ![X](../img/check-32px.png) | CBOR                      | | ![X](../img/check-32px.png) | NFC Tag                   |
| ![x](../img/redx-32px.png)  | RE                   | | ![X](../img/check-32px.png) | Floating Point            | | ![X](../img/check-32px.png) | Watchdog Timer            |
| ![x](../img/check-32px.png) | BLE Advertiser       | | ![X](../img/check-32px.png) | BLE Scanner               | | ![X](../img/check-32px.png) | BLE Connection            |
| ![x](../img/redx-32px.png)  | .zip App Update      | | ![X](../img/check-32px.png) | mbedTLS                   | | ![X](../img/blank-32px.png) |                           |

## Hardware-Specific Features <a id="hardware_specific_features"></a>[🔗](#hardware_specific_features)
| | | | | | | | |
|--:|:--|---|--:|:--|---|--:|:--|
| ![x](../img/redx-32px.png) | USB          | | ![X](../img/redx-32px.png) | RTOS Shell       | | ![X](../img/redx-32px.png)  | Encrypted FS     |
| ![x](../img/redx-32px.png) | Modem        | | ![X](../img/redx-32px.png) | Ethernet         | | ![X](../img/redx-32px.png)  | Wi-Fi Station    |
| ![x](../img/redx-32px.png) | Wi-Fi AP     | | ![X](../img/redx-32px.png) | Net Client       | | ![X](../img/redx-32px.png)  | Net Server       |
| ![X](../img/redx-32px.png) | UWB Ranging  | | ![X](../img/redx-32px.png) | LED Strip Driver | | ![X](../img/blank-32px.png) |                  |

## Design Guidelines <a id="design_guidelines"></a>[🔗](#design_guidelines)
**IMPORTANT**
- Pin P0.11 is used by the mcuboot bootloader to enter recovery mode when logic low at boot.
- Pin P0.13 is used by the mcuboot bootloader as its LED indicator. This will be active high if in bootloader recovery mode.
- Due to limited internal Flash available on the BL653, bootloader and OTA update are disabled by default. To support bootloader and OTA update, an additional external SPI Flash and custom build of Canvas firmware are required. Contact [Ezurio Support](https://www.ezurio.com/contact) to request a custom build of Canvas firmware with external Flash support for your design.

## Build Variants <a id="build_variants"></a>[🔗](#build_variants)
Firmware versions containing `a.b.99` are development builds and may not be suitable for production use.

| | |
|--:|:--|
| dvk                         | Default DVK build, 32 kB filesystem, no external SPI flash. |
| dvk_repl_uart               | Moves REPL console to UART0 |

---
© Copyright 2025 Ezurio LLC
