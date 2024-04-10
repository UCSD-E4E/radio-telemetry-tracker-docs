# Radio Telemetry Tracker New Payload Hardware Proposal

## Current Hardware of Interest
- UP Core (Single Board Computer)
- U-Blox GPS + Compass T002 Version XL

## Problem
### UP Core
Our main problem is that the **UP Core is no longer available for commercial purchase**. This means we cannot recommend collaborators to use the UP Core confidently, as it is no longer sold by UP. Although we still have three UP Cores available in Sealab, **they have an unconventional form factor** which makes them difficult to work with. Furthermore, we may face unknown integration issues with more common form factors like the RPi. Because of the unusual form factor, the **UP Core also requires the development of a PCB**, which is not ideal for our development and testing. This limitation restricts us from using different peripherals and testing various hardware that we would like to use.

### U-Blox GPS + Compass T002 Version XL
With more options available to us, we'd like to replace the current GPS/Compass with a more accurate and recent one.

## Solution
To summarize, the proposed solution is to **upgrade to UP's newer boards, specifically the UP 4000 series.**

UP has released three generations of boards in their RPi form factor series. The Board, the 4000 series, and the 7000 series. While the Board has already been discontinued, it is worth noting that all three generations share the same form factor as the RPi, making it easier to swap out the single-board computer (SBC) and develop on them. This is beneficial as many hobbyist and professional products are designed with the RPi form and pins in mind.

However, the new 4000 series SBCs are powered by 12v instead of 5v, which means we would need to adjust the way we power them. For the drone system, we are already using a 5v regulator to handle the high amperage that the Skyport V2 Extension Board's 13.6v power output provides. As for the tower system, the batteries will already output 12v, so there should not be any issues with power compatibility.

## Products
[UP Shop](https://up-shop.org/) order breakdown:
| Product                                                                                                                  | Cost    | Quantity | Description           |
| ------------------------------------------------------------------------------------------------------------------------ | ------- | -------- | --------------------- |
| [UP 4000 (Intel Pentium N4200, 4GB Mem, 32 GB Storage)](https://up-shop.org/default/up4000series.html)                   | $199.00 | 2        | Single Board Computer |
| [UP7000/UP 4000/UPS V2/UPC Plus power supply 12V@5A](https://up-shop.org/default/up-core-plus-power-supply-12vat5a.html) | $12.99  | 1        | Power Cable           |
| Shipping                                                                                                                 | $37.54  |          |                       |
| Total                                                                                                                    | $488.53 |          |                       |

---
[SparkFun](https://www.sparkfun.com/) order breakdown:
| Product                                                                                  | Cost   | Quantity | Description   |
| ---------------------------------------------------------------------------------------- | ------ | -------- | ------------- |
| [SparkFun GPS Breakout - NEO-M9N, U.FL (Qwiic)](https://www.sparkfun.com/products/15712) | $69.95 | 1        | GPS + Compass |
| [Molex Flexible GNSS Antenna - U.FL (Adhesive)](https://www.sparkfun.com/products/15246) | $4.50  | 1        | Antenna       |
| Shipping                                                                                 | $10.90 |          |               |
| Total                                                                                    | $85.35 |          |               |
---

Misc Items Breakdown:
| Product                                                                                                                      | Cost   | Quantity |
| ---------------------------------------------------------------------------------------------------------------------------- | ------ | -------- |
| [13.6v to 12v Voltage Regulator](https://www.amazon.com/Stabilizer-Converter-Waterproof-Automatic-Transformer/dp/B097BHZW7N) | $20.99 | 3        |
| Total                                                                                                                        | $62.97 |          |
---
Grand Total: ~$680 (Adjusted for any hidden costs)
