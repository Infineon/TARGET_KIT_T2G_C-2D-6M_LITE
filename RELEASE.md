# KIT_T2G_C-2D-6M_LITE BSP Release Notes
The KIT_T2G_C-2D-6M_LITE, a 327-pin evaluation board is based on the TRAVEO™ T2G family of devices. T2G-C-2D MCU is designed for  automotive and industrial applications. The evaluation board carries a T2G-C-2D 6M microcontroller,and headers compatible with Arduino for interfacing Arduino shields. In addition, the board features an on-board programmer/debugger (KitProg3),  a 512-Mbit QSPI NOR flash, CAN FD transceiver, Single-channel FPD-Link/LVDS interface for up to 1920 x 720 video output  MIPI-CSI2 camera connector, PMOD connector to support external ethernet PHY (also supports DP83848 Ethernet board) a Shield2Go connector interface and MikroBUS connector interface, two user LEDs, one potentiometer, and one user push buttons. USB Type-C connector for powering-up the kit and for FX3 output streaming. The board supports operating voltages from 1.1 V to 5.0 V for T2G-C-2D device.

**Note:**
KIT_T2G_C-2D-6M_LITE is the board support package for the T2G-C-2D 6M Lite Evaluation board  with CYT4DNJBZS MCU. 
**Note:**
Some additional setups will allow you to use more code examples than those shown on the next page. Click 
[here ](https://github.com/Infineon/TRAVEO_T2G_code_examples#how-to-setup)
for setup instructions.

NOTE: BSPs are versioned by family. This means that version 1.2.0 of any BSP in a family (eg: XMC™ ) will have the same software maturity level. However, not all updates are necessarily applicable for each BSP in the family so not all version numbers will exist for each board. Additionally, new BSPs may not start at version 1.0.0. In the event of adding a common feature across all BSPs, the libraries are assigned the same version number. For example if BSP_A is at v1.3.0 and BSP_B is at v1.2.0, the event will trigger a version update to v1.4.0 for both BSP_A and BSP_B. This allows the common feature to be tracked in a consistent way.

### What's Included?
The KIT_T2G_C-2D-6M_LITE library includes the following:
* BSP specific makefile to configure the build process for the board
* cybsp.c/h files to initialize the board and any system peripherals
* cybsp_types.h file describing basic board setup
* Linker script & startup code for GCC and ARM toolchains
* Configurator design files (and generated code) to setup board specific peripherals
* .lib file references for all dependent libraries
* API documentation

### What Changed?
#### v3.1.0
* Add additional capabilities and disable dcache for KIT_T2G_C-2D-6M_LITE
* Update BSP template to v1.7.2
#### v3.0.1
* Add additional capabilities and summary for KIT_T2G_C-2D-6M_LITE
#### v3.0.0
* Updated the MTB-HAL version's BSP for KIT_T2G_C-2D-6M_LITE
#### v2.2.0
* Added the BSP for KIT_T2G_C-2D-6M_LITE
#### v2.1.0
* Updated the KIT_XMC72_EVK, KIT_XMC72_EVK_MUR_43439M2, KIT_XMC71_EVK_LITE_V1 and KIT_XMC71_EVK_LITE_V2 BSPs to use ECO as main clock source
#### v2.0.2
* Updated the BSP description for KIT_XMC71_EVK_LITE_V1 and KIT_XMC71_EVK_LITE_V2 BSPs
#### v2.0.1
* Updated the description in README file for KIT_XMC72_EVK and KIT_XMC72_EVK_MUR_43439M2 BSPs
#### v2.0.0
* Fixed issue where CM0P prebuilt image would enable both CM7 cores on devices which contain
  two CM7 cores, even for single core applications.
* Updated default clock divider selections to better align with frequency limitations documented
  in the datasheet.

##### Known issues:
Issue: Wifi companion radio connection may fail when the board is programmed using `make program`

Workaround: Program the board using an IDE launch config.
#### v1.2.1
* Updated the description in README file for KIT_XMC72_EVK and KIT_XMC72_EVK_MUR_43439M2 BSPs
#### v1.2.0
* Updated linker scripts and startup code to align with mtb-pdl-cat1 v3.4.0
* Added functionality to enable BSP Assistant chip flow
* Added capabilities to match BSPS created by BSP Assistant chip flow
#### v1.1.0
* Add macro `CYBSP_USER_BTN_DRIVE` indicating the drive mode that should be used for user buttons
#### v1.0.0
Note: This revision is only compatible with ModusToolbox Tools 3.0 and newer.
* Initial production release

### Supported Software and Tools
This version of the KIT_T2G_C-2D-6M_LITE BSP was validated for compatibility with the following Software and Tools:

| Software and Tools                        | Version |
| :---                                      | :----:  |
| ModusToolbox™ Software Environment        | 3.1.0   |
| GCC Compiler                              | 12.2.1  |
| IAR Compiler                              | 9.40.2  |
| ARM Compiler                              | 6.16    |

Minimum required ModusToolbox™ Software Environment: v3.0.0

### More information
* [KIT_T2G_C-2D-6M_LITE BSP API Reference Manual][api]
* [KIT_T2G_C-2D-6M_LITE Documentation](https://www.infineon.com/cms/en/product/evaluation-boards/kit_t2g_c-2d-6m_lite)
* [Cypress Semiconductor, an Infineon Technologies Company](http://www.cypress.com)
* [Infineon GitHub](https://github.com/infineon)
* [ModusToolbox™](https://www.cypress.com/products/modustoolbox-software-environment)

[api]: https://infineon.github.io/TARGET_KIT_T2G_C-2D-6M_LITE/html/modules.html

---
© Cypress Semiconductor Corporation (an Infineon company) or an affiliate of Cypress Semiconductor Corporation, 2019-2024.