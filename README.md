# hydraESP32

HydraESP32 HydraBus v1.0 Shield for ESP-WROOM-32 V1.1 Rev1.0 (Tested) 

https://oshpark.com/shared_projects/dgKJqznH

HydraBus Shield / Breakout board for ESP-WROOM-32 or ESP-32S.

This shield can be used with or without HydraBus board, you can even cut HydraBus specific right side (on the line) to have a tiny ESP-WROOM-32 breakout board.

It is not mandatory to solder the components on this shield in order to use it, you will just need to connect +3v3 on VCC Pin header 

* New features versus previous version [V1.0 Rev1.1](https://oshpark.com/shared_projects/6t5hURXL):
   * Added LDO (TPS73633DBVR SOT23-5) to convert 5V(VUSB) to a clean VCC (+3.3v) for ESP32 and which can be enabled by an HydraBus Pin or  with a JUMPER on J7 (which connect +3.3V from HydraBus to EN of the LDO)
   * Added VCC connector in order to measure ESP32 current/power consumption (if not used to measure current just add a JUMPER on VCC to power the ESP32)
   * Added J6 connector to have access to ESP32 SPI FLASH IOs (now all pins are available)

* This shield can be used only on bottom of HydraBus board (in order to use other shields on top of HydraBus)

* The [HydraBus board](http://hydrabus.com/hydrabus-1-0-specifications/) is a small (60mm x 37mm) and [low cost](http://hydrabus.com/buy-online/), multi-tool extensible board with STM32F405 Cortex M4F 32bits MCU @168MHz with a fully open source firmware [hydrafw](https://github.com/bvernoux/hydrafw) and full online documentation [hydrafw wiki](https://github.com/bvernoux/hydrafw/wiki)

* The ESP-WROOM-32 is a low-power 32-bit 240 MHz dual core MCU Wi-
Fi+BLE combo module that highly integrates TCP/IP network stacks, 12-
bit ADC and HSPI/SDIO/UART/PWM/I2C/I2S interfaces.
See [ESP32 Overview](http://www.espressif.com/en/products/hardware/esp32/overview), [ESP-WROOM-32 link/info](https://espressif.com/en/producttype/esp-wroom-32), [Espressif Products Overview including ESP-WROOM-32 PDF](http://www.elinistech.com/images/esp8266/Espressif%20Introduction-EN.pdf)

* Design based on official [esp_wroom_32_datasheet_en.pdf (September 26, 2016)](https://espressif.com/sites/default/files/documentation/esp_wroom_32_datasheet_en.pdf)

BOM:

| Qty | Value | Device | Package | Parts | Description |
|------|----------|------------|-------------|---------|------------------|
| 1   | -        | ESP_WROOM_32 or ESP-32S        | ESP-WROOM-32 or ESP-32S          | U1        | Espressif ESP-WROOM-32 or ESP-32S Module    |
| 1   | -        | TPS73633 | SOT23-5L              | U2        | Texas Instrument LDO             |
| 1   | 2.2uF    | CAPACITOR_NPOL-0603 | C603                  | C1        | SMD Non-Polarized capacitor          |
| 1   | 1uF      | CAPACITOR_NPOL-0603 | C603                  | C2        | SMD Non-Polarized capacitor          |
| 2   | 100nF    | CAPACITOR_NPOL-0603 | C603                  | C3, C4    | SMD Non-Polarized capacitor          |
| 2   | 10K      | RESISTOR-0603       | R603                  | R1, R2    | SMD Resistor                                 |
| 1   | -        |                     | HYDRABUS_SHIELD_M2X7  | J1        | 2x7 Pin header      |
| 4   | -        |                     | HYDRABUS_SHIELD_M2X10 |J2, J3, J4, J5    | 2x10 Pin header                  |
| 2   | -        |                     | HYDRABUS_SHIELD_M1X6  | J6, SWD_DEBUG | 1x6 Pin header |
| 2   | -        |                     | Jumper - 2 Pin  | J7, VCC   |  Jumper 2 Pin |
| 2   | -        |                     | CON_HEADER_1X02-PTH   | J7, VCC   | 1x2 Pin header |

Note1: LDO U2 can be also replaced by MIC5319-3.3YD5-TR (Microchip)

Note2: If you do not want to solder those components you can avoid them and directly connect HydraBus 3v3 to VCC Pin near J5 marking

For more details see also [HydraBus_1_0_Shield_ESP_WROOM_32_v1_1_Rev1_BOM.csv](HydraBus_1_0_Shield_ESP_WROOM_32_v1_1_Rev1_BOM.csv)

Tested with success with an ESP-32S Module from Ai-Thinker (it is recommended to use official Espressif ESP-WROOM-32)

![HydraBus__Shield_ESP_WROOM_32_v1_1_Rev1 with ESP-32S](https://hydrabus.com/wp-content/uploads/2016/11/HydraBus__Shield_ESP_WROOM_32_v1_1_Rev1_ESP-32S_final_small.jpg "HydraBus__Shield_ESP_WROOM_32_v1_1_Rev1 with ESP-32S")

HydraBus_1_0_Shield_ESP_WROOM_32_v1_1_Rev1_Top:
[HydraBus_1_0_Shield_ESP_WROOM_32_v1_1_Rev1_Top](HydraBus_1_0_Shield_ESP_WROOM_32_v1_1_Rev1_Top.png)

HydraBus_1_0_Shield_ESP_WROOM_32_v1_1_Rev1_Bottom:
[HydraBus_1_0_Shield_ESP_WROOM_32_v1_1_Rev1_Bottom](HydraBus_1_0_Shield_ESP_WROOM_32_v1_1_Rev1_Bottom.png)
