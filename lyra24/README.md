<logo>![logo](../img/github_doc_header-dark.png#gh-dark-mode-only)</logo><logo>![logo](../img/github_doc_header-light.png#gh-light-mode-only)</logo>
#  Lyra24 Firmware

<table>
  <tr>
    <th align="center">
      <img width="380" height="1" style="max-width: 100%; height: auto; max-height: 1px; visibility:hidden;"/>
      <a href="img/453-00142-k1.png"><img src="img/453-00142-k1.png"/></a><br/>
      Lyra™ 24 P10 (<a href="https://www.ezurio.com/part/453-00142-k1">453-00142-k1</a>)
    </th>
    <th align="left">
      <h2>Description</h2>
      The Lyra 24P Development Kit has been designed to simplify IoT development with the Lyra 24P wireless module. The kit includes a mikroBUS™
socket and Qwiic® connector, allowing users to add features to the kit with a large selection of off-the-shelf boards.<br/><br/>
Programming the Lyra 24P Development Kit is easily done using a USB Micro-B cable and the on-board J-Link debugger and a USB virtual COM port
provides a serial connection to the target application.<br/><br/>
The kit provides 20 breakout pads for peripherals from the Lyra 24P such as I2C, SPI, UART and GPIOs. The mikroBUS socket allows inserting mikroBUS add-on boards which interface with the Lyra 24P through SPI, UART or I2C. The Qwiic connector can be used to connect hardware from the Qwiic Connect System through I2C.<br/><br/>
      Please visit the product page on <a href="https://www.ezurio.com/wireless-modules/bluetooth-modules/bluetooth-5-modules/lyra-24-series-bluetooth-5-modules">ezurio.com</a> for more details.
      <h2>Key Specs</h2>
      <table>
        <tr>
          <td><i>Internal Flash</i></td>
          <td>1536 kB</td>
          <td></td>
          <td><i>Internal RAM</i></td>
          <td>256 kB</td>
        </tr>
        <tr>
          <td><i>SPI Flash</i></td>
          <td>None</td>
          <td></td>
          <td><i>Default REPL Port</i></td>
          <td>EUSART0<br/>(USB VCOM)</td>
        </tr>
        <tr>
          <td><i>Python Heap Size</i></td>
          <td>128 kB</td>
          <td></td>
          <td><i>Filesystem Size</i></td>
          <td>128 kB</td>
        </tr>
      </table>
      <h2>External Links</h2>
      <a href="https://www.ezurio.com/documentation/datasheet-sera-nx040-series">Lyra 24 P10 Datasheet</a><br/>
      <a href="https://www.ezurio.com/documentation/user-guide-sera-nx040-dvk">Sera NX040 DVK User Guide</a><br/>
      <a href="https://www.ezurio.com/documentation/user-guide-sera-nx040-software">Sera Nx040 Software User Guide</a>
    </th>
  </tr>
</table>
<h2>Supported Hardware Variants</h2>
<table>
  <tr>
    <td>453-00142-K1</td><td>Lyra 24P Series - Development Kit - Bluetooth PCB Module (10dBm) with integrated antenna</td>
  </tr>
  <tr>
    <td>453-00145-K1</td><td>Lyra 24P Series - Development Kit - Bluetooth PCB Module (20dBm) with integrated antenna</td>
  </tr>
  <tr>
    <td>453-00148-K1</td><td>Lyra 24P Series - Development Kit - Bluetooth PCB Module (20dBm) with RF Trace Pad</td>
  </tr>
  <tr>
    <td>453-00170-K1</td><td>Development Kit, SIP, LYRA 24S, Integrated Antenna</td>
  </tr>
</table>

## Pinout Diagram <a id="pinout_diagram"></a>[🔗](#pinout_diagram)
[![Lyra 24 P10 Development Board Pinout Diagram](img/lyra24_p10.svg)](img/lyra24_p10.svg)

## Pinout Table <a id="pinout_table"></a>[🔗](#pinout_table)
| Pin | Canvas Pin Strings |
|-----|--------------------|
| PB04 | PB04,PB4,SIO6,MB_PWM |
| PB03 | PB03,PB3,SIO5,MB_INT |
| PB02 | PB02,PB2,SIO4,MB_RX |
| PB01 | PB01,PB1,SIO3,MB_TX |
| PB00 | PB00,PB0,SIO2,MB_AN |
| PA06 | PA06,PA6 |
| PA08 | PA08,PA8,SIO1,LED |
| PD03 | PD03,PD3,MB_SDA |
| PD02 | PD02,PD2,SIO13,MB_SCL |
| PC02 | PC02,PC2,SIO7,MB_SCK |
| PC03 | PC03,PC3,SIO8,MB_CS |
| PC04 | PC04,PC4,SIO9,MB_MOSI |
| PC05 | PC05,PC5,SIO10,MB_MISO |
| PC06 | PC06,PC6,SIO11,MB_RST |
| PC07 | PC07,PC7,SIO12,BTN0 |

## Peripheral/Bus Table <a id="peripheral_bus_table"></a>[🔗](#peripheral_bus_table)
| Peripheral/Bus | Canvas Peripheral/Bus Strings |
|---|---|
| I2C | I2C0 |
| I2C | I2C1 |
| SPI | SPI0 |
| UART | USART0 |
| UART | EUSART1 |

## Canvas Features <a id="canvas_features"></a>[🔗](#canvas_features)
| | | | | | | | |
|--:|:--|---|--:|:--|---|--:|:-- |
| ![X](../img/check-32px.png) | Bootloader           | | ![X](../img/check-32px.png) | OTA Update                | | ![X](../img/check-32px.png) | RTC                       |
| ![x](../img/check-32px.png) | SPI                  | | ![X](../img/check-32px.png) | ADC                       | | ![X](../img/redx-32px.png)  | PWM                       |
| ![x](../img/check-32px.png) | I2C                  | | ![X](../img/check-32px.png) | GPIO                      | | ![X](../img/check-32px.png) | UART                      |
| ![x](../img/check-32px.png) | JSON                 | | ![X](../img/check-32px.png) | CBOR                      | | ![X](../img/redx-32px.png)  | NFC Tag                   |
| ![x](../img/check-32px.png) | RE                   | | ![X](../img/check-32px.png) | Floating Point            | | ![X](../img/check-32px.png) | Watchdog Timer            |
| ![x](../img/check-32px.png) | BLE Advertiser       | | ![X](../img/check-32px.png) | BLE Scanner               | | ![X](../img/check-32px.png) | BLE Connection            |
| ![x](../img/check-32px.png) | .zip App Update      | | ![X](../img/check-32px.png) | mbedTLS                   | | ![X](../img/blank-32px.png) |                           |

## Hardware-Specific Features <a id="hardware_specific_features"></a>[🔗](#hardware_specific_features)
| | | | | | | | |
|--:|:--|---|--:|:--|---|--:|:--|
| ![x](../img/redx-32px.png)  | USB          | | ![X](../img/redx-32px.png)  | RTOS Shell       | | ![X](../img/redx-32px.png)  | Encrypted FS     |
| ![x](../img/redx-32px.png)  | Modem        | | ![X](../img/redx-32px.png)  | Ethernet         | | ![X](../img/redx-32px.png)  | Wi-Fi Station    |
| ![x](../img/redx-32px.png)  | Wi-Fi AP     | | ![X](../img/redx-32px.png)  | Net Client       | | ![X](../img/redx-32px.png)  | Net Server       |
| ![X](../img/redx-32px.png)  | UWB Ranging   | | ![X](../img/redx-32px.png) | LED Strip Driver | | ![X](../img/blank-32px.png) |                  |

## Design Guidelines <a id="design_guidelines"></a>[🔗](#design_guidelines)
- Make sure to use the Canvas firmware build matching the specific Lyra 24 series part you are using.

## Build Variants <a id="build_variants"></a>[🔗](#build_variants)
Firmware versions containing `a.b.99` are development builds and may not be suitable for production use.

| | |
|--:|:--|
| dvk_p10               | Default Lyra 24P10 DVK build |
| dvk_p20               | Default Lyra 24P20 DVK build |
| dvk_prf               | Default Lyra 24P RF Trace DVK build |
| dvk_s10               | Default Lyra 24S DVK build |
| usb_p20               | Default Lyra 24P USB dongle build |

---
© Copyright 2025 Ezurio LLC
