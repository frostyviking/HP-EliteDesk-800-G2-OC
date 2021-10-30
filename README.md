![HP EliteDesk 800 G2 Desktop Mini Business PC](https://ssl-product-images.www8-hp.com/digmedialib/prodimg/lowres/c04876268.png)
## HP EliteDesk 800 G2 Mini

Updated with macOS Monterey, looking good so far.
System actually feels a bit more snappy, makes that older i7-6700 feel fresh -unexpected.
I went directly from BigSur 11.4 to 11.6.1 and then upgraded to Monterey.
Updates to kext, OpenCore, config + OS updates.
Commands line tools update then brew update.

Total time taken about 2 hours.

**[Dont forget to unzip "unzip_me.zip" in EFI/OC/Resources]** or you wont have a nice gui at boot.

Go forth my brothers and sisters!

## Specs:
- HP EliteDesk 800 65W G2 Desktop Mini PC
- BIOS: N21 Ver.02.23 04/16/2021
- CPU: Intel® Core i7-6700 @ 3.40 GHz processor (65 W)
- GPU: Intel® HD Graphics 530 (2 DisplayPorts + 1 VGA Port)
- Memory: 2 x 8GB Samsung DDR4-2133 SODIMM
- Storage: Crucial MX500 1TB SATA SSD
- LAN: Intel® I219M GbE
- WLAN/BT: BCM94360NG 2.4&5G WiFi Bluetooth 4.0
- Audio: Realtec ALC221 Audio Codec

## BIOS Settings
- Advanced -> Boot Options
  - Startup Delay 5
  - Disable **Fast Boot**
  - Disable **CD-ROM Boot**
  - Enable **USB Storage Boot**
  - Disable **Network (PXE) Boot**
  - After Power Loss **Power Off**
  - UEFI & Legacy Boot order, is up to you.
  
- Advanced -> Secure Boot Configuration
  - Select **Legacy Support Enable and Secure Boot Disable**
  - Everything else unchecked.

- Advanced -> System Options
  - Enable **Turbo-boost**
  - Enable **Hyperthreading**
  - Enable **Multi-processor**
  - Enable **Virtualization Technology (VTx)**
  - Disable **Virtualization Technology for Directed I/O (VTd)**
  - Enable **M.2 WLAN/BT**
  - Enable **M.2 SSD**
  - Enable **Allow PCIe/PCI SERR# Interrupt**
  - Power Button Override **4 sec**

- Advanced -> Built-in Device Options
  - Enable **Embedded LAN Controller**
  - Disable **Wake on LAN**
  - Disable **Dust Filter**
  - Video memory size **64MB**
  - Enable **M.2 USB / Bluetooth**
  - Enable **Audio Device**
  - Enable **Internal Speakers**
  - Increase Idle Fan Speed (%), set at 0

- Advanced -> Port Options
  - Everything **Enabled**
  - Restrict USB Devices **Allow all USB Devices**

- Advanced > Option ROM Launch Policy
  - Configure Option ROM Launch Policy **All UEFI**

- Advanced -> Power Management Options
  - Runtime Power Management **Enable**
  - Extended Idle Power States **Enable**
  - S5 Maximum Power Savings **Disable**
  - SATA Power Management **Enable**
  - PCI Express Power Managment **Disable** (if enabled, it will really screw that native BCM M.2 WiFi performance)
  - Power On from Keyboard Ports **Disable**
  - Unique Sleep State Blink Rates **Disable** 

- Advanced -> Remote Management Options
  - I have not touched anything in here, running defaults AFAIK..



## Current OS
- macOS Monterey 12.0.1 (Build 21A559)

## Bootloader
- OpenCore 0.7.5

## Working:
- Allmost everything, see below.

## Known Not working:
- VGA port, throw it to the wolves -unsupported.
- Front audio port (right one) can not act as a 3.5mm Combo version. It is **Line in ONLY**.

## Unused / Not tested:
- Sleep, nap, whatever.. i dont use, might dig into that -in future boredom :)
