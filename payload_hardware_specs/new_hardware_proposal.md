# Radio Telemetry Tracker Change Payload Hardware Proposal

## Current Hardware of Interest
- UP Core (Single Board Computer)
- U-Blox GPS + Compass T002 Version XL

## Problem
### UP Core
Our main problem is that the **UP Core is no longer available for commercial purchase**. This means we cannot recommend collaborators to use the UP Core confidently, as it is no longer sold by UP. Although we still have three UP Cores available in Sealab, **they have an unconventional form factor** which makes them difficult to work with. Furthermore, we may face unknown integration issues with more common form factors like the RPi. Because of the unusual form factor, the **UP Core also requires the development of a PCB**, which is not ideal for our development and testing. This limitation restricts us from using different peripherals and testing various hardware that we would like to use.

### U-Blox GPS + Compass T002 Version XL
With more options available to us, we'd like to replace the current GPS/Compass with a more accurate and recent one.

## Solution
To summarize, the proposed solution is to **upgrade to UP's current boards, specifically the UP 7000 series.**

UP has released three generations of boards in their RPi form factor series. The Board, the 4000 series, and the 7000 series. While the Board has already been discontinued, it is worth noting that all three generations share the same form factor as the RPi, making it easier to swap out the single-board computer (SBC) and develop on them. This is beneficial as many hobbyist and professional products are designed with the RPi form and pins in mind. The UP 7000 also provides a sizable upgrade in processing power compared to the UP Core which gives us room to improve what computations are done in real-time and improving the digital signal processing module.

The 7000 series SBCs are powered by 12v instead of 5v, which means we would need to adjust the way we power them. For the drone system, we are already using a 5v regulator to handle the high amperage that the Skyport V2 Extension Board's 13.6v power output provides. As for the tower system, the batteries will already output 12v, so there should not be any issues with power compatibility.

## Products
| Product                                                                                                                  | Vender   | Vender SKU          | Cost    | Quantity | Description           |
| ------------------------------------------------------------------------------------------------------------------------ | -------- | ------------------- | ------- | -------- | --------------------- |
| [UP 7000 (Intel Processor N100, 8GB Mem, 64 GB Storage)](https://up-shop.org/default/up-7000-series.html)                | AAEON UP | UP-ADLN100-A10-0864 | $239.00 | 2        | Single Board Computer |
| [UP7000/UP 4000/UPS V2/UPC Plus power supply 12V@5A](https://up-shop.org/default/up-core-plus-power-supply-12vat5a.html) | AAEON UP | EP-PS12V5A60WFJ     | $12.99  | 2        | Power Supply          |
| [Power cord (U.S. plug)](https://up-shop.org/default/power-cord-u-s-plug.html)                                           | AAEON UP | EP-CBPC125V3PUS     | $4.99   | 2        | Power Cord            |
| [SparkFun GPS Breakout - NEO-M9N, U.FL (Qwiic)](https://mou.sr/3Pt2lmy)                                                  | SparkFun | GPS-15712           | $64.95  | 1        | GPS + Compass         |
| [ACTPAT154 Active GPS Antenna](https://mou.sr/49vBspl)                                                                   | Inventek | ACTPAT154-01-IP     | $7.23   | 1        | Antenna               |
| [13.6v to 12v Voltage Regulator](https://www.amazon.com/dp/B081RG8XP5)                                                   | DROK     | B081RG8XP5          | $16.99  | 3        |                       |
|                                                                                                                          |          |                     |         |          |                       |
| Cost                                                                                                                     |          |                     | $637.11 |          |                       |
| S&H/Tax Estimation (+25%)                                                                                                |          |                     | $159.28 |          |                       |
|                                                                                                                          |          |                     |         |          |                       |
| Total                                                                                                                    |          |                     | $796.39 |          |                       |

