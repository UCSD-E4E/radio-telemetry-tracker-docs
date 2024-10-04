# Radio Telemetry Tracker Hardware Specifications

This document outlines the current hardware specifications for the Radio Telemetry Tracker project's drone system. These specifications are subject to change as the project evolves.

## Drone Payload

![Drone Hardware Setup Diagram](../../diagrams/img/drone_hardware_setup.png)

### Single Board Computer
- Model: UP 7000
- Processor: Intel Processor N100
- Memory: 8GB
- Storage: 64GB
- [Product Link](https://up-shop.org/default/up-7000-series.html)

### GPS + Compass
- Model: SparkFun GPS Breakout - NEO-M9N, U.FL (Qwiic)
- [Product Link](https://mou.sr/3Pt2lmy)

### Software Defined Radio
- Model: USRP B200mini-i
- [Product Link](https://www.ettus.com/all-products/usrp-b200mini-i-2/)

### Low Noise Amplifier
- Model: Nooelec LaNA
- [Product Link](https://www.nooelec.com/store/lana.html?srsltid=AfmBOopzeX7KlBqEZARz0aIcDkEfL9iiwXlTAamh-N2XETJ2ykOVpHGz)

### LoRa Communication
- Model: RFM95W LoRa Radio
- [Product Link](https://www.adafruit.com/product/3072)
- 
## Additional Recommended Components

### Power Source
- DJI Skyport
- Extension Board
- Note: These components provide a reliable power supply for the drone payload.

### Ground Control Station (GCS)
- USB Breakout Board: For connecting the radio to the GCS computer
- Note: This allows for easier connection and management of the radio on the ground.

### Antennas
- It is recommended to use appropriate antennas where possible for both the drone payload and GCS to optimize signal reception and transmission.

Note: The specific models and types of these additional components may vary based on the exact requirements of the setup.
