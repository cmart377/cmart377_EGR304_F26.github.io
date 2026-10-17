---
title: Component Selection 
---

**Voltage Regulator**

1. Texas Instruments UA7805CKCS Voltage Regulator 

    ![](https://github.com/cmart377/cmart377_EGR304_F26.github.io/blob/main/docs/02-Component-Selection/Screenshot%202026-10-16%20230513.png?raw=true)

    * $1.63/each
    * [link to product](https://www.st.com/content/ccc/resource/technical/document/datasheet/41/4f/b3/b0/12/d4/47/88/CD00000444.pdf/files/CD00000444.pdf/jcr:content/translations/en.CD00000444.pdf)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Established 7805 style regulator design | Linear regulator heat losses still apply |
    | Fixed 5 V output requires no ouput voltage adjustment | Confirm the exact part's datasheet, package, and availability before ordering |
    | Through hole versions are suitable for prototyping | May cost more than other 7805 compatible options |

1. STMicroelectronics L7805CV Voltage Regulator 

    ![](https://github.com/cmart377/cmart377_EGR304_F26.github.io/blob/main/docs/02-Component-Selection/Screenshot%202026-10-16%20230541.png?raw=true)

    * $1.08/each
    * [Link to product](https://www.ti.com/lit/ds/symlink/lm7800.pdf?ts=1792218175071&ref_url=https%253A%252F%252Fwww.ti.com%252Fproduct%252FLM7800%252Fpart-details%252FLM7805CT%252FNOPB)

    | Pros                                                     | Cons                |
    | ---------------------------------------------------------| ------------------- |
    | Fixed 5 V output simplifies circuit design               | Needs an input voltage above 5 V, with sufficient headroom.|
    | Through-hole TO-220 package is relatively easy to solder | Excess input voltage is dissipated as heat. |
    | Includes overtemperature and short-circuit protection    | The 1.5 A rating does not guarantee that it can deliver 1.5 A continuously without appropriate thermal management.                     |

1. NTE960 Voltage Regulator 

    ![](https://github.com/cmart377/cmart377_EGR304_F26.github.io/blob/main/docs/02-Component-Selection/Screenshot%202026-10-16%20230557.png?raw=true)

    * $1.50/each
    * [Link to product](https://vetco.net/products/nte960_5_volt_1a_voltage_regulator_3-pin_to220_-_nte960?utm_source)

    | Pros                                                     | Cons                |
    | ---------------------------------------------------------| ------------------- |
    | Fixed 5 V output         | Lower current rating than proposed 1.5 A regulator|
    | Through hole package is convenient for assembly | Must verify that the actual system current is within its rating. |
    |  Its 1 A output rating may be sufficient for a modest logic board | Still require thermal analysis |
**Choice:** Option 2: STMicroelectronics L7805CV Voltage Regulator

**Rationale:** The L7805CV was selected because it provides a fixed 5 V output. Its simple design makes it easy to integrate into the PCB. Its through-hole package also makes assembly easier. However, its current capacity and heat dissipation must be verified before final selection.

**External Power Supply**

1. 12 V, 1 A DC Wall Adapter External Power Supply

    ![](https://github.com/cmart377/cmart377_EGR304_F26.github.io/blob/main/docs/02-Component-Selection/Screenshot%202026-10-16%20230608.png?raw=true)

    * $7.20/each
    * [link to product](https://www.newegg.com/imbaprice-imba-12v1a-1pk/p/2RC-0264-001Y1?utm_source)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Supplies up to 1 A at 12 V | A linear 5 V regulator will dissipate substantial heat dropping 12 V to 5 V |
    | Convenient for a stationary prototype | The adapter's connector and polarity  must match your board |
    | Provides more input voltage than a 5 V rail requires | Its current capacity must be checked against the calculated system load |

1. Avue 12V, 1 A Adapter External Power Supply

    ![](https://github.com/cmart377/cmart377_EGR304_F26.github.io/blob/main/docs/02-Component-Selection/Screenshot%202026-10-16%20230621.png?raw=true)

    * $9.99/each
    * [Link to product](https://www.microcenter.com/product/449788/avue-dc12v-1a-power-adapter?utm_source)

    | Pros                                                     | Cons                |
    | ---------------------------------------------------------| ------------------- |
    | A readily purchasable wall adapter. | Same linear regulator heat concern as option 1. |
    | Rated for 12 W of output power. | The connector and polarity must be verified. |
    | Suitable for evaluating a stationary prototype if the connector and electrical specifications match.| Must have sufficient current remaining after accounting for all loads. |

1. Truetone 1 SPOT 9 V Adapter External Power Supply 

    ![](https://github.com/cmart377/cmart377_EGR304_F26.github.io/blob/main/docs/02-Component-Selection/Screenshot%202026-10-16%20230634.png?raw=true)

    * $27.99/each
    * [Link to product](https://www.sweetwater.com/store/detail/1Spot9v--truetone-1-spot-slim-9v-dc-adapter)

    | Pros                                                     | Cons                |
    | ---------------------------------------------------------| ------------------- |
    | Supplies 9 V DC and is intended for continuous equipment power. | More expensive than the other candidates. |
    | Lower input voltage than 12 V reduces the regulator's voltage drop and heat. | Its center-negative connector may not match your board. |
    | Listed output current is 1.7 A. | A linear regulator will still dissipate heat, and actual current demand must be calculated. |
   
**Choice:** Option 3: Truetone 1 SPOT 9 V Adapter External Power Supply 

**Rationale:** The 9 V adapter was selected because it provides a practical power source for a stationary prototype. It produces less heat than a 12 V adapter in a linear regulator. It can provide consistent power without requiring a battery. Its polarity, connector, and current capacity must be verified before use.

**PCB Temperature Sensor**

1. Microchip MCP9700 Temperature Sensor

    ![](https://github.com/cmart377/cmart377_EGR304_F26.github.io/blob/main/docs/02-Component-Selection/Screenshot%202026-10-16%20230651.png?raw=true)

    * $0.42/each
    * [link to product](https://www.microchip.com/en-us/product/mcp9700?utm_source)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Analog output can be read by the PIC's ADC. | The PIC must convert and interpret the analog voltage. |
    | Operates from a 2.3–5.5 V supply. | Measurement accuracy must be considered when choosing the cutoff temperature. |
    | Temperature range is −40°C to 150°C.| Additional circuitry is needed if the sensor must directly trigger a hardware cutoff. |

1. Analog Devices DS18B20 Temperature Sensor

    ![](https://github.com/cmart377/cmart377_EGR304_F26.github.io/blob/main/docs/02-Component-Selection/Screenshot%202026-10-16%20230702.png?raw=true)

    * $2.83/each
    * [Link to product](https://www.analog.com/en/products/DS18B20.html?utm_source)

    | Pros                                                     | Cons                |
    | ---------------------------------------------------------| ------------------- |
    | Digital 1-Wire interface uses only one data pin.| Requires firmware to read and interpret the digital data. |
    | Typical accuracy is ±0.5°C from −10°C to +85°C. | Uses a digital interface rather than a direct analog ADC input. |
    | Supports programmable resolution and configurable temperature alarms.| A separate power-disconnection mechanism is still needed for an independent failsafe. |

1. TMP102 Temperature Sensor

    ![](https://github.com/cmart377/cmart377_EGR304_F26.github.io/blob/main/docs/02-Component-Selection/Screenshot%202026-10-16%20230715.png?raw=true)

    * $5.95/each
    * [Link to product](https://cdn.robotshop.com/media/s/spa/rb-spa-882/pdf/digital-temperature-sensor-tmp102-datasheet.pdf)

    | Pros                                                     | Cons                |
    | ---------------------------------------------------------| ------------------- |
    | Supplies 9 V DC and is intended for continuous equipment power. | More expensive than the other candidates. |
    | Lower input voltage than 12 V reduces the regulator's voltage drop and heat. | Its center-negative connector may not match your board. |
    | Listed output current is 1.7 A. | A linear regulator will still dissipate heat, and actual current demand must be calculated. |
   
**Choice:** Option 1: MCP9700 Temperature Sensor 

**Rationale:** The MCP9700 was selected because its analog output can be read directly by the PIC's ADC. This simplifies temperature monitoring and reduces interface complexity. It operates within a voltage range suitable for many low-voltage circuits. An additional threshold circuit is needed to trigger an automatic thermal shutdown.

**Power Switching Components**

1. Texas Instruments TPS22919 Power Switch

    ![](https://github.com/cmart377/cmart377_EGR304_F26.github.io/blob/main/docs/02-Component-Selection/Screenshot%202026-10-16%20230728.png?raw=true)

    * $0.32/each
    * [link to product](https://www.ti.com/lit/ds/symlink/tps22919.pdf?ts=1792216512151&ref_url=https%253A%252F%252Fwww.google.com%252F)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Supports 1.6–5.5 V input and up to 1.5 A continuous current. |Small SC-70 package is more difficult to solder than a through-hole part. |
    | Includes thermal shutdown and short-circuit protection. | Requires a control signal to enable or disable the output. |
    | Provides controlled power-up and output discharge. | Its built-in thermal shutdown is not a substitute for a separately specified board-temperature threshold. |

1. Texas Instruments TPS22917 Power Switch 

    ![](https://github.com/cmart377/cmart377_EGR304_F26.github.io/blob/main/docs/02-Component-Selection/Screenshot%202026-10-16%20230739.png?raw=true)

    * $0.16/each
    * [Link to product](https://www.ti.com/lit/ds/symlink/tps22917.pdf?ts=1792159789155&ref_url=https%253A%252F%252Fwww.google.com%252F)

    | Pros                                                     | Cons                |
    | ---------------------------------------------------------| ------------------- |
    | Offers a compact integrated power-switching solution.  | Confirm the exact current rating and operating voltage for the selected package.|
    | Has controlled turn-on and output-discharge functionality. | Small package may be challenging to assemble.|
    | Can reduce the number of discrete switching components.  | Requires additional temperature-sensing and control circuitry for a defined PCB cutoff temperature.|

1. Texas Instruments TPS22991 Power Switch

    ![](https://github.com/cmart377/cmart377_EGR304_F26.github.io/blob/main/docs/02-Component-Selection/Screenshot%202026-10-16%20230754.png?raw=true)

    * $0.08/each
    * [Link to product](https://www.ti.com/lit/ds/symlink/tps22991.pdf?ts=1792190270993)

    | Pros                                                     | Cons                |
    | ---------------------------------------------------------| ------------------- |
    | Integrated load-switch solution. | Verify the exact input-voltage and current specifications before selection.|
    | Includes controlled turn-on and output-discharge features. | Small surface-mount package requires careful PCB footprint and assembly. |
    | Offers another commercial option for comparison with the TPS22919. | Does not replace a separately designed temperature-threshold circuit. |
**Choice:** Option 3: Texas Instruments TPS22991 Power Switch

**Rationale:** The TPS22919 was selected because it provides compact electronic power control. Its integrated design can reduce the number of separate components on the PCB. It also includes thermal shutdown and short-circuit protection for the switch itself. An external temperature-threshold circuit is still needed to disconnect the protected power rail when the PCB overheats.
