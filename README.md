# My Desk Clock

I'm building a custom desk clock using an ESP32. The idea is to make a clock that automatically synchronises its time over Wi-Fi, so there's no need to set the time manually.

I designed the circuit schematic and PCB in KiCad and am also working on a custom 3D-printed enclosure. The clock uses an ESP32 for Wi-Fi connectivity and a dedicated RTC for timekeeping.

## Features

- ESP32-WROOM-32E microcontroller
- Automatic time synchronisation over Wi-Fi using NTP
- DS3231M real-time clock
- Rechargeable battery-based power supply
- USB-C charging and power input
- Custom PCB designed in KiCad
- Five tactile push buttons
- Passive buzzer
- Custom 3D-printed enclosure

# 3D Model

This is the 3D model of the clock enclosure. I designed it around the PCB so that all the components fit inside without making the clock unnecessarily bulky.

<img width="370" height="179" alt="3D model" src="https://github.com/user-attachments/assets/541deb6c-161d-4264-a900-c63a6d3ecd68" />

# 3D Render

Here's the 3D render of the clock. It gives a better idea of how the finished enclosure is supposed to look.

<img width="624" height="534" alt="3D render" src="https://github.com/user-attachments/assets/2988c435-79ba-460f-bce5-c49354b0d591" />

# Physical PCB Layout

The PCB was designed in KiCad. I arranged the components around the ESP32, RTC, and power management circuit while keeping the board compact enough to fit inside the enclosure.

<img width="323" height="326" alt="Physical PCB layout" src="https://github.com/user-attachments/assets/a71009a6-d55c-4bf0-b014-7da1fef2bd0e" />

# Circuit Schematic

The schematic shows how the different sections of the clock connect together, including the ESP32, RTC, battery charging circuit, buck-boost converter, buttons, and buzzer.

<img width="820" height="532" alt="Circuit schematic" src="https://github.com/user-attachments/assets/669f1709-b347-49ba-8c0e-2a64fab8e93c" />

# How It Works

The ESP32 is the main controller of the clock. It connects to a Wi-Fi network and retrieves the current time from an NTP server.

The DS3231M RTC provides independent timekeeping, allowing the clock to keep track of time even when Wi-Fi isn't available. The ESP32 can synchronise the RTC when an internet connection is available.

The five tactile buttons are intended for physical controls, while the buzzer can be used for sound alerts.

## Power Management

I designed the power circuit around a rechargeable battery.

- **BQ24074:** Handles battery charging and power management.
- **TPS63031:** Provides regulated power using a buck-boost converter.
- **USB-C connector:** Provides the charging and power input.

The idea is to have a clock that can run without needing to stay connected to a USB cable all the time.

# Design Files

The project includes the KiCad schematic, PCB layout, and 3D enclosure model.

These files can be used to inspect the circuit, modify the PCB, or manufacture your own version of the clock.

# Acknowledgements

This project was designed using **KiCad EDA**. Thanks to the KiCad developers and the open-source hardware community for making PCB design tools accessible.

---

# License

This project is open-source. Feel free to inspect, modify, and build upon the design.

---

# Bill of Materials (BOM)

The following table contains the components used in the clock, along with their quantities, supplier links, and estimated prices.

## Main BOM

| **Item** | **Link** | **Quantity** | **Cost (USD)** | **Notes** |
|---|---|---:|---:|---|
| CR2032 battery holder | [Lion Circuits](https://www.lioncircuits.com/parts/1057) | 1 | $2.11 | Keystone 1057 |
| Passive buzzer | [Robu.in](https://robu.in/product/ac1470-cldz-piezoelectric-passive-buzzer-1-25v14x7mm/) | 1 | $0.09 | 12 × 9.5 mm footprint |
| 100 nF capacitors | [Robu.in](https://robu.in/product/100nf-0805-surface-mount-multilayer-ceramic-capacitor-pack-of-40/) | 3 | $0.03 | 0805 |
| 10 µF capacitors | [Robu.in](https://robu.in/product/0805x106k250nt-fh-25v-10uf-x5r%C2%B110-0805-multilayer-ceramic-capacitors-mlcc-smd-smt-rohs/) | 6 | $0.31 | 0805 |
| 1 µF capacitors | [Robu.in](https://robu.in/product/1uf-1000nf-50v-capacitor-0805-smd-package-pack-of-10/) | 2 | $0.03 | 0805 |
| 4.7 µF capacitor | [Robu.in](https://robu.in/product/20121h475k125ab-tdk-ap-smd-ml-4-7-%c2%b5f-50-v-0805-pack-of-1/) | 1 | $0.15 | 0805 |
| 1×6 pin header | [Robu.in](https://robu.in/product/2-54mm-1x40-pin-male-single-row-straight-short-header-strip-pack-of-3/) | 1 | $0.10 | 2.54 mm |
| 1×4 pin header | [Robu.in](https://robu.in/product/2-54mm-1x40-pin-male-single-row-straight-short-header-strip-pack-of-3/) | 1 | $0.10 | 2.54 mm |
| USB-C receptacle | [Robu.in](https://robu.in/product/u262-161n-4bs165-xkb-5a-1-16p-female-type-c-smd-usb-connectors-rohs/) | 1 | $0.33 | 16-pin |
| JST PH 2-pin connector | [Robu.in](https://robu.in/product/wafer-xh2-54-2pzz-xunpu-1x2p-xh-2p/) | 1 | $0.00 | Verify connector type and price |
| 1.5 µH inductor | [Robu.in](https://robu.in/product/dfe252012p-1r5mp2-murata-power-inductor-smd-1-5-%c2%b5h-shielded-3-a1008-2520-metric/) | 1 | $0.03 | SMD |
| NPN transistor | [Robu.in](https://robu.in/product/s8050-kuu-25v-300mw-500ma-npn-sot-23-bipolar-bjt-rohs/) | 1 | $0.01 | SOT-23 |
| 10 kΩ resistors | [Robu.in](https://robu.in/product/rc0805jr-0710kl-yageo-smd-chip-resistor-10-kohm-pack-of-10/) | 3 | $0.01 | 0805 |
| 4.7 kΩ resistors | [Robu.in](https://robu.in/product/crcw08054k70fkeac-vishay-intertech-4-7k-0805-chip-resistor/) | 3 | $0.02 | 0805 |
| 100 kΩ resistors | [Robu.in](https://robu.in/product/rc0805fr-13100kl-yageo-smd-chip-resistor-100-kohm/) | 2 | $0.02 | 0805 |
| 1 kΩ resistor | [Robu.in](https://robu.in/product/1k-ohm-1-4w-0805-surface-mount-chip-resistor-pack-of-10/) | 1 | $0.00 | 0805 |
| 5.1 kΩ resistors | [Robu.in](https://robu.in/product/era6aeb102vpanasonicsmd-chip-resistor-1-kohm/) | 2 | $0.08 | Verify listing value |
| 1.78 kΩ resistor | [Mouser India](https://www.mouser.in/en/ProductDetail/Panasonic-Industry/ERJ-P06F1781V) | 1 | $0.23 | SMD |
| 3 kΩ resistor | [Robu.in](https://robu.in/product/rc0805fr-073kl-yageo-res-thick-film-0805-3k-ohm/) | 1 | $0.00 | 0805 |
| Tactile push buttons | [Robu.in](https://robu.in/product/6x6x5mm-tactile-push-button-switch-pack-of-20/) | 5 | $0.09 | 6 × 6 mm |
| ESP32-WROOM-32E | [Robu.in](https://robu.in/product/espressif-esp32-wroom-32-4m-32mbit-flash-wifi-bluetooth-module/) | 1 | $3.21 | Main controller |
| DS3231M RTC | [Robu.in](https://robu.in/product/ds3231mtrl-analog-devices-real-time-clock-ic/) | 1 | $3.84 | Real-time clock |
| BQ24074 charger IC | [Robu.in](https://robu.in/product/bq24075rgtt-texas-instruments-vqfn-16-ep3x3-battery-management-rohs/) | 1 | $1.92 | Verify exact part number |
| TPS63031 buck-boost IC | [Robu.in](https://robu.in/product/tps63031dskr-texas-instruments-buck-boost-switching-regulator-ic/) | 1 | $1.90 | Power regulation |

## Cost Summary

| **Item** | **Cost (USD)** |
|---|---:|
| Components | $14.60 |
| PCB | $12.00 |
| **Total estimated cost** | **$26.60** |





