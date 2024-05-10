# HP 840 G3 Hackintosh
Repository to share my prebuilt Hackintosh EFI folder of my HP 840 G3 laptop.

![Group 1](https://github.com/dwtoledo/hp-840-g3-hackintosh/assets/11148858/c22f11ae-1779-497a-ab19-ecb363d65f70)

## Hackintosh details:
macOS version: Sonoma 14.3.1

SMBIO Model: MacBookPro14,1

Platform ID: 0x59160000

[OpenCore](https://github.com/acidanthera/OpenCorePkg) version: 1.0.0

## Hardware Details:
CPU: Intel(R) Core(TM) i5-6300U CPU @ 2.40GHz

Intel Generation: Kaby Lake

iGPU: Intel HD Graphics 520

RAM: 24 GB

Wifi: Intel® Dual Band Wireless-AC 8260

Ethernet: I219-LM 10/100/1000 Ethernet

NVME: 256GB M.2 2280 SATA III NGFF Solid State SSD

SSD: SSD Crucial BX500 480 GB 3D NAND SATA 2,5 pol.

## What is not working?
Fingerprint Reader

Wifi Button

When I have some device connected on USB sometimes the laptop does not shutdown, seems the USB turns the laptop on again.

All others features are working correctly and Wifi kext is using v2.3.0 alpha version of [itlwm](https://github.com/OpenIntelWireless/itlwm).

## Not tested:
SD Card Reader

SC Card Reader (I never used)

Dock station (I don't have one)

## Set bios settings as follows (thanks to [Lost-Entrepreneur439](https://github.com/Lost-Entrepreneur439/hp-elitebook-840-g3-hackintosh)):

Security -> Intel Software Guard Extensions (SGX) -> Disable

Advanced -> Boot Options -> Uncheck “Fast Boot”

Advanced -> Boot Options -> Check “UEFI Boot Order”

Advanced -> Boot Options -> Uncheck “Legacy Boot Order”

Advanced -> Secure Boot Configuration -> Configure Legacy Support and Secure Boot -> Legacy Support Disable and Secure Boot Disable

Advanced -> System Options -> Check “Hyperthreading”

Advanced -> System Options -> Check “Virtualization Technology (VTx)”

Advanced -> System Options -> Uncheck “Virtualization Technology for Directed I/O (VTd)”

Advanced -> Built-In Device Options -> Video memory size -> 64MB or anything higher

## What I have done?

Disabled the Apple chime during boot.

## Important
I'm not a Hackintosh Expert.

I used [Lost-Entrepreneur439](https://github.com/Lost-Entrepreneur439/hp-elitebook-840-g3-hackintosh) project as reference to create my EFI folder and update all necessary things.

Follow the ["Creating the USB"](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/) section in the Dortania guide to get macOS, again, I have Sonoma 14.3.1.

My laptop has a NVMe, so I added the NVMeFix.kext into my Kexts folder, if your laptop doesn't have a NVMe, please correctly remove this kext using an Hackintosh tools (I usually use OCAuxiliaryTools).

Please generated yours "System Serial Number", "MLB", "SystemUUID" and "ROM", I deleted mines from config.plist file.

## Credits
[Lost-Entrepreneur439](https://github.com/Lost-Entrepreneur439/hp-elitebook-840-g3-hackintosh) -- Who starts this amazing project and inspired me.

[Dortania](https://github.com/dortania) -- Made the OpenCore guide which was used to create this EFI

[Acidanthera](https://github.com/acidanthera) -- Made OpenCore, AppleALC, BlueToolFixup, BrightnessKeys, IntelMausi, Lilu, SMCBatteryManager, SMCProcessor, VirtualSMC, VoodooPS2Controller & WhateverGreen

[OpenIntelWireless](https://github.com/OpenIntelWireless) -- Made airportitlwm & IntelBluetoothFirmware

[Avery Black](https://github.com/1Revenger1) -- Made ECEnabler

[钟先耀](https://github.com/zxystd) -- Made IntelBTPatcher

[FireWolf](https://github.com/0xFireWolf) -- Made RealtekCardReader

[USBToolBox](https://github.com/USBToolBox) -- Made USBToolBox & UTBMap

[VoodooSMBus](https://github.com/VoodooSMBus) -- Made VoodooRMI & VoodooSMBus

[CorpNewt](https://github.com/corpnewt) -- Helped me fix external display issues

[HP](https://www.hp.com/us-en/home.html) -- Made the EliteBook 840 G3

[Apple](https://www.apple.com/ca/) -- Made macOS
