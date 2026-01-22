# EFI-Ryzentosh

OpenCore (v0.8.8) EFI for my Ryzentosh.

<img width="698" height="463" alt="info" src="https://github.com/user-attachments/assets/ce76b42a-ce3f-4a94-b457-563f83e910e7" />

## Specs

| Component | Model                |
| :-------- | :------------------------- |
| CPU | 3,6 GHz AMD Ryzen 5 5500                                |
| Motherboard | TUF GAMING B550M-PLUS |
| RAM | 32 GB 3200 MHz DDR4 (16GB x 2) |
| GPU | AMD Radeon Saphire RX 580 8 GB |
| Audio Chipset | Realtek ALC S1200A 7.1 |
| Ethernet | Realtek RTL8125B |
| OS Disk (NVMe) | Crucial CT500P2SSD8 500GB |
| WiFi & Bluetooth | Broadcom Broadcom BCM43XX |

## Versions

| Component | Version                |
| :-------- | :------------------------- |
| OpenCore | 0.8.8 |
| Lilu.kext | 1.7.1 |
| VirtualSMC.kext | 1.3.7 |
| AMDRyzenCPUPowerManagement.kext | 0.7.2 |
| AppleALC.kext | 1.9.6 |
| AppleMCEReporterDisabler.kext | 1.2 |
| LucyRTL8125Ethernet.kext | 1.2.2 |
| RadeonSensor.kext | 0.3.1 |
| RestrictEvents.kext | 1.1.6 |
| SMCAMDProcessor.kext | 0.7.2 |
| SMCRadeonGPU.kext | 0.3.1 |
| USBToolBox.kext | 1.1.1 |
| UTBMap.kext | 1.1 |
| WhateverGreen.kext | 1.7.0 |

## What works and what doesn’t

Everything works, but I couldn’t test deep sleep/hibernate (although the computer does go to sleep and wakes up normally).

I used to have a real Mac Pro 5,1 (with two Xeon X5570 CPUs and 32 GB of DDR3 RAM, using the same AMD GPU and Wi-Fi/Bluetooth cards). Since that machine started shutting down randomly, I thought it was about time to replace it. At the time, I was inclined to get a PC (with the specs listed above) and use Linux exclusively. I did that, and later I found out that it was possible to build a Hackintosh with AMD CPUs.

I found a [repository](https://github.com/Vericen/ryzen-hackintosh) with a base OpenCore EFI (which is basically for the exact same hardware) and decided to give it a try. In my case, almost everything worked out of the box. Since then, I’ve updated some kexts and made a few changes to the OpenCore config.plist.

Comparing performance from a user perspective, it feels like using a real Mac-only faster. I’ve been using this machine for a month now, and I can open my projects in Final Cut, Logic, iMovie, and GarageBand without any issues.

## Notes

1. If you decide to use the files in this repository, be aware that I am not responsible for any damage caused to your computer. Use them at your own risk. You should know what OpenCore is and how it works before messing with it. Reading the official documentation is strongly advised.
2. If you decide to use the files in this repository, you must generate your own serial number and motherboard serial to populate the required PlatformInfo sections.
3. There are still a few tweaks that could be done to make my Ryzentosh even more "perfect-ish":
    * Make the PCIe Wi-Fi/Bluetooth adapter appear as internal in macOS. This requires working with USBToolBox. Since it already works as I need it to, I’m not dealing with this for now.
    * Some DeviceProperties were inherited from the original repository. Since they are harmless, I’m leaving them as they are.
4. My PC case is certainly different from yours (I use a Cooler Master 301 Lite), so you will need to remap the USB ports if you want to use the front USB ports on your case.

December 2025.
