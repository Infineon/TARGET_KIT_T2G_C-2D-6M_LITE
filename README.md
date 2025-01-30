# KIT_T2G_C-2D-6M_LITE BSP

## Overview

The KIT_T2G_C-2D-6M_LITE, a 327-pin evaluation board is based on the TRAVEO™ T2G family of devices. T2G-C-2D MCU is designed for  automotive and industrial applications. The evaluation board carries a T2G-C-2D 6M microcontroller,and headers compatible with Arduino for interfacing Arduino shields. In addition, the board features an on-board programmer/debugger (KitProg3),  a 512-Mbit QSPI NOR flash, CAN FD transceiver, Single-channel FPD-Link/LVDS interface for up to 1920 x 720 video output  MIPI-CSI2 camera connector, PMOD connector to support external ethernet PHY (also supports DP83848 Ethernet board) a Shield2Go connector interface and MikroBUS connector interface, two user LEDs, one potentiometer, and one user push buttons. USB Type-C connector for powering-up the kit and for FX3 output streaming. The board supports operating voltages from 1.1 V to 5.0 V for T2G-C-2D device.

**Note:**
KIT_T2G_C-2D-6M_LITE is the board support package for the T2G-C-2D 6M Lite Evaluation board  with CYT4DNJBZS MCU. 

![](docs/html/board.png)

To use code from the BSP, simply include a reference to `cybsp.h`.

## Features

### Kit Features:

* CYT4DNJBZS 6MB Flash 327-pin LQFP device
* Programming interface (Arm® Standard JTAG, Cortex® Debug + ETM with Arm® ETM Mictor)
* Reset control with manual reset switch and voltage supervision
* CAN FD interface
* One 512-Mbit external Semper SPI NOR Flash that provides a fast, expandable memory for data and code
* One 64-Mbit external Hyperram that provides a fast, expandable memory for data
* KitProg3 on-board SWD programmer/debugger, USB-UART and USB-I2C bridge functionality
* A Shield2Go connector interface and a MikroBUS connector interface
* Two user LEDs, one user buttons, and a reset button for the T2G-C-2D device
* A potentiometer which can be used to simulate analog sensor output
* A mode button and a mode LED for KitProg3

### Kit Contents:

* T2G-C-2Dd evaluation board
* USB Type-A to Micro-B cable
* Quick start guide (printed on the kit package)
* See 
[Peripheral driver library (PDL) library](https://infineon.github.io/mtb-pdl-cat1/pdl_api_reference_manual/html/index.html)

## BSP Configuration

The BSP has a few hooks that allow its behavior to be configured. Some of these items are enabled by default while others must be explicitly enabled. Items enabled by default are specified in the KIT_T2G_C-2D-6M_LITE.mk file. The items that are enabled can be changed by creating a custom BSP or by editing the application makefile.

Components:
* Device specific category reference (e.g.: CAT1) - This component, enabled by default, pulls in any device specific code for this board.

Defines:
* CYBSP_WIFI_CAPABLE - This define, disabled by default, causes the BSP to initialize the interface to an onboard wireless chip if it has one.
* CY_USING_HAL - This define, enabled by default, specifies that the HAL is intended to be used by the application. This will cause the BSP to include the applicable header file and to initialize the system level drivers.
* CYBSP_CUSTOM_SYSCLK_PM_CALLBACK - This define, disabled by default, causes the BSP to skip registering its default SysClk Power Management callback, if any, and instead to invoke the application-defined function `cybsp_register_custom_sysclk_pm_callback` to register an application-specific callback.

### Clock Configuration

| Clock    | Source    | Output Frequency |
|----------|-----------|------------------|
| FLL      | ECO       | 100.0 MHz        |
| PLL      | ECO       | 200.0 MHz        |
| CLK_HF0  | CLK_PATH6 | 200 MHz          |
| CLK_HF1  | CLK_PATH1 | 320 MHz          |
| CLK_HF2  | CLK_PATH7 | 100 MHz          |
| CLK_HF3  | CLK_PATH6 | 100 MHz          |
| CLK_HF4  | CLK_PATH6 | 50 MHz           |
| CLK_HF5  | CLK_PATH2 | 196 MHz          |
| CLK_HF6  | CLK_PATH2 | 196 MHz          |
| CLK_HF7  | CLK_PATH2 | 196 MHz          |
| CLK_HF8  | CLK_PATH3 | 320 MHz          |
| CLK_HF9  | CLK_PATH3 | 320 MHz          |
| CLK_HF10 | CLK_PATH4 | 250 MHz          |
| CLK_HF11 | CLK_PATH5 | 220 MHz          |
| CLK_HF12 | CLK_PATH8 | 200 MHz          |
| CLK_HF13 | CLK_PATH9 | 0 MHz            |

### Power Configuration

* System Idle Power Mode: Deep Sleep
* VDDA Voltage: 3300 mV
* VDDD Voltage: 3300 mV

See the [BSP Setttings][settings] for additional board specific configuration settings.

## API Reference Manual

The KIT_T2G_C-2D-6M_LITE Board Support Package provides a set of APIs to configure, initialize and use the board resources.

See the [BSP API Reference Manual][api] for the complete list of the provided interfaces.

## More information
* [KIT_T2G_C-2D-6M_LITE BSP API Reference Manual][api]
* [KIT_T2G_C-2D-6M_LITE Documentation](https://www.infineon.com/cms/en/product/evaluation-boards/kit_t2g_c-2d-6m_lite)
* [Cypress Semiconductor, an Infineon Technologies Company](http://www.cypress.com)
* [Infineon GitHub](https://github.com/infineon)
* [ModusToolbox™](https://www.cypress.com/products/modustoolbox-software-environment)

[api]: https://infineon.github.io/TARGET_KIT_T2G_C-2D-6M_LITE/html/modules.html
[settings]: https://infineon.github.io/TARGET_KIT_T2G_C-2D-6M_LITE/html/md_bsp_settings.html

---
© Cypress Semiconductor Corporation (an Infineon company) or an affiliate of Cypress Semiconductor Corporation, 2019-2024.