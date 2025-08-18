
<logo>![logo](../img/github_doc_header-dark.png#gh-dark-mode-only)</logo><logo>![logo](../img/github_doc_header-light.png#gh-light-mode-only)</logo>
#  Veda SL917 Firmware (Pre-Release)

<table>
  <tr>
    <th align="center">
      <img width="380" height="1" style="max-width: 100%; height: auto; max-height: 1px; visibility:hidden;"/>
      <a href="img/453-00222-K1.png"><img src="img/453-00222-K1.png"/></a><br/>
      Veda SL917 Explorer Kit (<a href="https://www.ezurio.com/part/453-00222-k1">453-00222-K1</a>)
    </th>
    <th align="left">
      <h2>Description</h2>
      The Veda SL917 Module Wi-Fi 6 and Bluetooth LE Explorer Kit is focused on rapid prototyping and concept creation of IoT applications. It is designed around the SL917 SoC module based upon Silicon Labs SiWx917 chipset, which is an ideal module family for developing energy-friendly connected IoT applications.<br/><br/>
      The Ezurio Explorer kit features a USB Type-C interface, an on-board SEGGER J-Link debugger, two user-LEDs and two buttons, and support for hardware add-on boards via a mikroBus socket and a Qwiic connector. The hardware add-on support allows developers to create and prototype applications using a virtually endless combination of off-the-shelf peripheral boards from MIKROE, SparkFun, Adafruit, and Seeed Studio.<br/><br/>
      Please visit the product page on <a href="https://www.ezurio.com/product/veda-sl917-wi-fi-6-bluetooth-le-5-4-module">ezurio.com</a> for more details.
      <h2>Key Specs</h2>
      <table>
        <tr>
          <td><i>QSPI Flash</i></td>
          <td>8192 kB</td>
          <td></td>
          <td><i>Internal RAM</i></td>
          <td>672 kB</td>
        </tr>
        <tr>
          <td><i>Python Heap Size<br/>(w/QSPI PSRAM)</i></td>
          <td>~160 kB<br/>(8192 kB)</td>
          <td></td>
          <td><i>Default REPL Port</i></td>
          <td>ULP_UART</td>
        </tr>
        <tr>
          <td></td>
          <td></td>
          <td></td>
          <td><i>Filesystem Size</i></td>
          <td>1024 kB</td>
        </tr>
      </table>
      <h2>External Links</h2>
      <a href="https://www.ezurio.com/documentation/datasheet-veda-sl917-soc-module">Veda SL917 SoC Datasheet</a><br/>
      <a href="https://www.ezurio.com/documentation/user-guide-veda-sl917-explorer-board">Veda SL917 Explorer Kit User Guide</a>
    </th>
  </tr>
</table>

## Pinout Diagram <a id="pinout_diagram"></a>[🔗](#pinout_diagram)
[![Veda SL917 Explorer Kit Pinout Diagram](img/brd2911a.svg)](img/brd2911a.svg)

## Canvas Features <a id="canvas_features"></a>[🔗](#canvas_features)
| | | | | | | | |
|--:|:--|---|--:|:--|---|--:|:-- |
| ![X](../img/redx-32px.png)  | Bootloader*          | | ![X](../img/redx-32px.png)  | OTA Update*               | | ![X](../img/check-32px.png) | RTC                       |
| ![x](../img/check-32px.png) | SPI                  | | ![X](../img/check-32px.png) | ADC                       | | ![X](../img/check-32px.png) | PWM                       |
| ![x](../img/check-32px.png) | I2C                  | | ![X](../img/check-32px.png) | GPIO                      | | ![X](../img/check-32px.png) | UART                      |
| ![x](../img/check-32px.png) | JSON                 | | ![X](../img/check-32px.png) | CBOR                      | | ![X](../img/check-32px.png) | NFC Tag                   |
| ![x](../img/check-32px.png) | RE                   | | ![X](../img/check-32px.png) | Floating Point            | | ![X](../img/check-32px.png) | Watchdog Timer            |
| ![x](../img/check-32px.png) | BLE Advertiser       | | ![X](../img/check-32px.png) | BLE Scanner               | | ![X](../img/check-32px.png) | BLE Connection            |
| ![x](../img/check-32px.png) | .zip App Update      | | ![X](../img/check-32px.png) | mbedTLS                   | | ![X](../img/blank-32px.png) |                           |

\* Planned for official release, not available in current pre-release firmware

## Hardware-Specific Features <a id="hardware_specific_features"></a>[🔗](#hardware_specific_features)
| | | | | | | | |
|--:|:--|---|--:|:--|---|--:|:--|
| ![x](../img/redx-32px.png)  | USB          | | ![X](../img/redx-32px.png)  | RTOS Shell       | | ![X](../img/redx-32px.png)  | Encrypted FS     |
| ![x](../img/redx-32px.png)  | Modem        | | ![X](../img/redx-32px.png)  | Ethernet         | | ![X](../img/check-32px.png) | Wi-Fi Station    |
| ![x](../img/check-32px.png) | Wi-Fi AP     | | ![X](../img/check-32px.png) | Net Client       | | ![X](../img/check-32px.png) | Net Server       |
| ![X](../img/redx-32px.png)  | UWB Ranging  | | ![X](../img/redx-32px.png)  | LED Strip Driver | | ![X](../img/blank-32px.png) |                  |

## Design Guidelines <a id="design_guidelines"></a>[🔗](#design_guidelines)
$\textsf{\color{salmon}{IMPORTANT}}$
- Canvas firmware releases depend on a specific WiSeConnect connectivity firmware version. Both .rps files are provided in each release, be sure to flash both firmware images before developing with Canvas.
- Use Simplicity Commander tool from Silicon Labs to program .rps files.
- External PSRAM support is experimental.

## Build Variants <a id="build_variants"></a>[🔗](#build_variants)
Firmware versions containing `a.b.99` are development builds and may not be suitable for production use.

**Builds within `erase` subfolders are for utility use only, not development. These builds boot and erase the flash-based filesystem.**

| | |
|--:|:--|
| brd2708a                    | SiLabs SiWX917Y SoC Module Explorer Kit build.     |
| brd2708ap                   | Adds External QSPI PSRAM support.                  |
| brd2911a                    | Default Veda SL917 Explorer Kit build.             |
| brd2911ap                   | Adds External QSPI PSRAM support.                  |

---
© Copyright 2025 Ezurio LLC
