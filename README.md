# Hackintosh for Dell Latitude 5400 (forked from https://github.com/msbence/hackintosh-DellLatitude5400 but these are my own EFI files with some borrowing from msbence)

---

**NOTE: I originally used msbence's EFI files to get my Latitude 5400 working, which worked perfectly but I noticed a few things like the lack of HfsPlus.efi, a lot of redundant files that either aren't present or are disabled in the config.plist, as well as the config.plist patch for ECDV to EC but there not being any SSDT patches for this**

**In any case, I created my own SSDT patches using SSDTTime (from Windows) and MaciASL for the most part, with some borrowing again from msbence**

**SSDT-GPRW.aml and SSDT-UPRW.aml are not needed as per the official Dortania guide for this (when testing returned values from my own DSDT file show I don't need these patches)**

---

**OpenCore version: 0.9.0**

![About my Mac](/system.png)

## Specification

| | |
|-|-|
|**CPU**|Intel i7-8665U CPU @ 1.90GHz (Whiskey Lake)|
|**RAM**|32GB DDR4 2666MHz|
|**IGPU**|Intel UHD 620|
|**SSD**|Samsung 970 EVO NVMe 500GB|
|**ETH**|Intel I217-LM|
|**WLAN+BT**|BCM94360NG|
|**WWAN**|Empty|
|**Audio**|Realtek ALC236|
|**Ports**|USB-C (PD+DP-AltMode), 3xUSB3.0, HDMI, microSD, Multi-Jack, DC|

## Not working

- HDMI coldplug (hotplug is OK)
- *Hibernation (none of Hackintoshes can do that)*

## Working

- **Everything what is not in the Not working section :D**
- Dedicated brightness control keys
- Bluetooth (4.0, LE, Handoff) [out-of-the-box, no kext needed]
- WLAN [no kext needed] (recommended)
- Intel WLAN [kexts added, but not that stable]
- Ethernet
- HDMI, DisplayPort Alt Mode (all with sound, but no volume adjustment)
- USB-C (I'm using it with a docking station all the time)
- WWAN (good speed, 4G, works fine, tho Apple kinda abandoned this feature)
- USB ports mapped, working after sleep
- TrackPad with gestures (visible as Magic Trackpad 2)
- Audio, with speaker and microphone support
- QE/CI
- Sleep
- MicroSD card reader
- TouchPad buttons
- TrackStick
- Multi-Jack (both cold- and hotplug)

## Some random text

