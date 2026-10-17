---
title: Component Selection 
---

**Voltage Regulator**

1. Texas Instruments UA7805CKCS

    ![](image1.png)

    * $1.63/each
    * [link to product](http://www.digikey.com/product-detail/en/ECS-40.3-S-5PX-TR/XC1259TR-ND/827366)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Established 7805 style regulator design | Linear regulator heat losses still apply |
    | Fixed 5 V output requires no ouput voltage adjustment | Confirm the exact part's datasheet, package, and availability before ordering |
    | Through hole versions are suitable for prototyping | May cost more than other 7805 compatible options |

1. STMicroelectronics L7805CV

    ![](image3.png)

    * $1.08/each
    * [Link to product](http://www.digikey.com/product-detail/en/636L3I001M84320/CTX936TR-ND/2292940)

    | Pros                                                     | Cons                |
    | ---------------------------------------------------------| ------------------- |
    | Fixed 5 V output simplifies circuit design               | Needs an input voltage above 5 V, with sufficient headroom.|
    | Through-hole TO-220 package is relatively easy to solder | Excess input voltage is dissipated as heat. |
    | Includes overtemperature and short-circuit protection    | The 1.5 A rating does not guarantee that it can deliver 1.5 A continuously without appropriate thermal management.                     |

**Choice:** Option 2: CTX936TR-ND surface mount oscillator

**Rationale:** A clock oscillator is easier to work with because it requires no external circuitry in order to interface with the PSoC. This is particularly important because we are not sure of the electrical characteristics of the PCB, which could affect the oscillation of a crystal. While the shipping speed is slow, according to the website if we order this week it will arrive within 3 weeks.
