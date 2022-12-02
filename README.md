# Hackintosh-OC-Asus-B560MN-i7-11700K-Rocketlake-UHD750
About B560M-N i7-11700K UHD750 Hackintosh (macOS 13 Ventura) - OpenCore

## Support Versions

| macOS Versions | Build    | Support Status |
|----------------|----------|:--------------:|
| 13.0.1    	 | 22A400   |       ✅       |

Support Status Explanation：
* ✅ Fully supported, including developer versions
* ⚠️ Partially supported, consumer version only
* 🚧 Exploration in progress, not supported

## Computer Hardware

* Motherboard Brand: Asus
* Motherboard Model: B560M-N
* Motherboard Chipset: Intel Tiger Point B560, Intel Rocket Lake-S

* CPU: OctalCore Intel Core i7-11700K, 4600 MHz (46 x 100)
* Graphics Card: Intel(R) UHD Graphics 750
* Nvidia/AMD Graphics Card: None
* Audio Card：Realtek ALC897

See detailed configuration at Report.txt(CN)

## SMBIOS

MacPro7,1

## OpenCore Version

| Kext                       | Version              |
|----------------------------|----------------------|
| OpenCore                   | 0.8.7		        |
| AppleALC.kext              | 1.7.7                |
| Lilu.kext                  | 1.6.3      			|
| VirtualSMC.kext            | 1.3.1                |
| WhateverGreen.kext         | 1.6.2       			|
| USBInjectAll.kext          | 0.7.8                |
| RestrictEvents.kext 		 | 1.1.0				|
| IntelMausi.kext        	 | 1.0.7                |

## BIOS Configuration

If you have the same as my motherboard model and system version, you can refer to the position in the brackets and use the BIOS shell to modify.

### Disabled

* CFG lock (0x44 Set to 0x0)
* VT-d (0xD3 Set to 0x0)
* SGX 
* CSM
* ResizeAppleGpuBars (0x3CA Set to 0x0)

### Enabled

* VT-x
* Above 4G Decoding (0xD4 Set to 0x1)
* Hyper-threading (0x6 Set to 0x1)
* Execute Disable Bit
* EHCI Hand-off (0x2B Set to 0x1)

## What does NOT work  ⚠️
iGPU can not be drived, you need to install an external gpu.

## Images

![info](https://raw.githubusercontent.com/zmlu/Hackintosh-OC-Asus-B560MN-i7-11700K-Rocketlake-UHD750/main/images/Screenshot-2022-12-02_10-24-35.jpg "info")

## Attention ⚠️

Please change MLB, SystemSerialNumber, SystemUUID into your own `config.plist`.

```xml
<dict>
    ...
    <key>MLB</key>
    <string>xxxxxxxxxxxxxxx</string>
    ...
    <key>SystemSerialNumber</key>
    <string>xxxxxxxxxxx</string>
    ...
    <key>SystemUUID</key>
    <string>xxxxxxxx-xxxxx-xxxxx-xxxx-xxxxxxxx</string>
</dict>
```

## Update Log

* 2022.12.02
    * New Config Support macOS 13 (Ventura) 🎉