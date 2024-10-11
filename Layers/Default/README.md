# Board: STMicroelectronics [STM32F769I-DISCO](https://www.st.com/en/evaluation-tools/32f769idiscovery.html)

## Default Board Layer

Device: **STM32F769NIHx**

System Core Clock: **216 MHz**

This setup is configured using **STM32CubeMX**, an interactive tool provided by STMicroelectronics for device configuration.
Refer to ["Configure STM32 Devices with CubeMX"](https://github.com/Open-CMSIS-Pack/cmsis-toolbox/blob/main/docs/CubeMX.md) for additional information.

### System Configuration

| System resource       | Setting
|:----------------------|:--------------------------------------
| Heap                  | 64 kB (configured in the STM32CubeMX)
| Stack (MSP)           |  1 kB (configured in the STM32CubeMX)

### STDIO mapping

**STDIO** is routed to Virtual COM port on the ST-LINK (using **USART1** peripheral)

### CMSIS-Driver mapping

| CMSIS-Driver          | Peripheral            | Board connector/component                     | Connection
|:----------------------|:----------------------|:----------------------------------------------|:------------------------------
| Driver_ETH_MAC0       | ETH                   | Ethernet RJ45 connector (CN10)                | CMSIS_ETH
| Driver_ETH_PHY0       | LAN8742A (external)   | Ethernet RJ45 connector (CN10)                | CMSIS_ETH
| Driver_GPIO0          | GPIO                  | Arduino digital I/O pins D2..D10, D14..D19    | ARDUINO_UNO_D2..D10, D14..D19
| Driver_I2C1           | I2C1                  | Arduino I2C pins D20..D21                     | ARDUINO_UNO_I2C
| Driver_MCI2           | SDMMC2                | MicroSD card connector (CN5)                  | CMSIS_MCI
| Driver_SPI2           | SPI2                  | Arduino SPI pins D10..D13                     | ARDUINO_UNO_SPI
| Driver_USART1         | USART1                | ST-LINK connector (CN16)                      | STDIN, STDOUT, STDERR
| Driver_USART5         | UART5                 | Extesion connector pins WIFI_RX, WIFI_TX (CN2)| CMSIS_USART
| Driver_USART6         | USART6                | Arduino UART pins D0..D1                      | ARDUINO_UNO_UART
| Driver_USBD1          | USB_OTG_HS            | USB OTG HS connector (CN15)                   | CMSIS_USB_Device
| CMSIS-Driver VIO      | GPIO                  | LEDs (LD1, LD2) and USER button (B1)          | CMSIS_VIO

Reference to [Arduino UNO connector description](https://github.com/Open-CMSIS-Pack/cmsis-toolbox/blob/main/docs/ReferenceApplications.md#arduino-shield).

### CMSIS-Driver Virtual I/O mapping

| CMSIS-Driver VIO      | Board component
|:----------------------|:--------------------------------------
| vioBUTTON0            | USER button (B1)
| vioLED0               | LED red     (LD1)
| vioLED1               | LED green   (LD2)
