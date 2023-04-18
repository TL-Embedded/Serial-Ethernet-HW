# Serial-Ethernet-HW

This is an Ethernet to Serial adaptor.
See [Serial-Ethernet-FW](https://github.com/TL-Embedded/Serial-Ethernet-FW) for the firmware project.

The processor is a STM32G061.

# Ethernet
The ethernet is managed by a SPI attached W5500. The ethernet is capable of 10/100 speeds.

# Serial
The serial is a TTL level serial targeted at certain test equipment. Series resistance is used to tolerate both 3V3 and 5V0 devices.

**This is not compatible with RS232 level serial**

# Power
The device is powered from 5V. This can be supplied via:
 * USB Connector
 * Debug connector
 * DB9 pin 1 (omit L2 if this is not desired)

# Debugging
The debugging connector is a TC2050 compatible footprint. See the [SWD-UART_CTX-10](https://github.com/TL-Embedded/SWD-UART-CTX-10) project for the adaptor board.

This can be used to:
 * Connect to the STM32 via STLINK
 * Supply 5V
 * Connect a UART

The debugging connector has no input/output protection - so take care not to supply power or UART when the DB9 is connected.
