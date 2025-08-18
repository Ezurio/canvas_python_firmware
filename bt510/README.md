
<logo>![logo](../img/github_doc_header-dark.png#gh-dark-mode-only)</logo><logo>![logo](../img/github_doc_header-light.png#gh-light-mode-only)</logo>
#  Sentrius BT510 Firmware

<table>
  <tr>
    <th align="center">
      <img width="380" height="1" style="max-width: 100%; height: auto; max-height: 1px; visibility:hidden;"/>
      <a href="img/455-00083.png"><img src="img/455-00083.png"/></a><br/>
      Sentrius™ BT510 Sensor (<a href="https://www.ezurio.com/part/455-00083">455-00083</a>)
    </th>
    <th align="left">
      <h2>Description</h2>
      The Sentrius™ BT510 Sensor is a battery powered, IP67-rated Bluetooth 5 Long Range open development device for robust sensor performance in the harshest environments. The ultra-low power Sentrius™ BT510 packs temperature, door open/close, and motion/impact sensing with Bluetooth LE beaconing.<br/><br/> 
      It’s powered by Ezurio's field-proven BL654 module (Nordic nRF52840) for feature rich development in the Cortex M4F with 1 MB Flash memory for data logging and storage. Its single replaceable CR2477 coin cell battery enables multi-year life and hassle-free, long-term maintenance. <br/><br/>
      Please visit the product page on <a href="https://www.ezurio.com/iot-devices/bluetooth-iot-devices/bt510-bluetooth-5-long-range-ip67-multi-sensor">ezurio.com</a> for more details.
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
          <td>Not Available</td>
          <td></td>
          <td><i>Default REPL Port</i></td>
          <td>UART0</td>
        </tr>
        <tr>
          <td><i>Python Heap Size</i></td>
          <td>~167 kB</td>
          <td></td>
          <td><i>Filesystem Size</i></td>
          <td>96 kB</td>
        </tr>
      </table>
      <h2>External Links</h2>
      <a href="https://www.ezurio.com/documentation/hardware-guide-bt510-sensor-firmware-development">BT510 Hardware Guide</a><br/>
      <a href="https://www.ezurio.com/documentation/product-brief-usb-swd-programming-kit">USB - SWD Programming Kit</a> (Required for development)
    </th>
  </tr>
</table>

## Pinout Diagram <a id="pinout_diagram"></a>[🔗](#pinout_diagram)
[![Sentrius BT510 Sensor Pinout Diagram](img/bt510.svg)](img/bt510.svg)

## Canvas Features <a id="canvas_features"></a>[🔗](#canvas_features)
| | | | | | | | |
|--:|:--|---|--:|:--|---|--:|:-- |
| ![X](../img/check-32px.png) | Bootloader           | | ![X](../img/check-32px.png) | OTA Update                | | ![X](../img/check-32px.png) | RTC                       |
| ![x](../img/check-32px.png) | SPI                  | | ![X](../img/check-32px.png) | ADC                       | | ![X](../img/redx-32px.png)  | PWM                       |
| ![x](../img/check-32px.png) | I2C                  | | ![X](../img/check-32px.png) | GPIO                      | | ![X](../img/check-32px.png) | UART                      |
| ![x](../img/redx-32px.png)  | JSON                 | | ![X](../img/check-32px.png) | CBOR                      | | ![X](../img/redx-32px.png)  | NFC Tag                   |
| ![x](../img/redx-32px.png)  | RE                   | | ![X](../img/redx-32px.png)  | Floating Point            | | ![X](../img/check-32px.png) | Watchdog Timer            |
| ![x](../img/check-32px.png) | BLE Advertiser       | | ![X](../img/check-32px.png) | BLE Scanner               | | ![X](../img/check-32px.png) | BLE Connection            |
| ![x](../img/redx-32px.png)  | .zip App Update      | | ![X](../img/check-32px.png) | mbedTLS                   | | ![X](../img/blank-32px.png) |                           |

## Hardware-Specific Features <a id="hardware_specific_features"></a>[🔗](#hardware_specific_features)
| | | | | | | | |
|--:|:--|---|--:|:--|---|--:|:--|
| ![x](../img/redx-32px.png)  | USB          | | ![X](../img/redx-32px.png)  | RTOS Shell       | | ![X](../img/redx-32px.png)  | Encrypted FS     |
| ![x](../img/redx-32px.png)  | Modem        | | ![X](../img/redx-32px.png)  | Ethernet         | | ![X](../img/redx-32px.png) | Wi-Fi Station    |
| ![x](../img/redx-32px.png) | Wi-Fi AP     | | ![X](../img/redx-32px.png) | Net Client       | | ![X](../img/redx-32px.png) | Net Server       |
| ![X](../img/redx-32px.png)  | UWB Ranging  | | ![X](../img/redx-32px.png)  | LED Strip Driver | | ![X](../img/blank-32px.png) |                  |

## Design Guidelines <a id="design_guidelines"></a>[🔗](#design_guidelines)
- Flash programming and development with the BT510 sensor requires the [Ezurio USB - SWD programming kit](https://www.ezurio.com/wireless-modules/programming-kits/usb-swd-programming-kit) (or equivalent SWD programmer with [TC2050-IDC Tag Connect](https://www.tag-connect.com/product/tc2050-idc-tag-connect-2050-idc) adapter)
- Use the [pyocd tool](https://pyocd.io/) to flash Canvas firmware .hex files.

## Build Variants <a id="build_variants"></a>[🔗](#build_variants)
Firmware versions containing `a.b.99` are development builds and may not be suitable for production use.

**Builds within `erase` subfolders are for utility use only, not development. These builds boot and erase the flash-based filesystem.**

| | |
|--:|:--|
| standard                       | Default BT510 sensor build.     |

---
© Copyright 2025 Ezurio LLC
