![HP EliteDesk 800 G2 Desktop Mini Business PC](https://ssl-product-images.www8-hp.com/digmedialib/prodimg/lowres/c04876268.png)

### Specs:
- BIOS: N21 Ver.02.23 04/16/2021
- CPU: Intel® Core i7-6700 @ 3.40 GHz processor (65 W)
- GPU: Intel® HD Graphics 530 (2 DisplayPorts + 1 VGA Port)
- Memory: 2 x 8GB Samsung DDR4-2133 SODIMM
- Pri Storage: Samsung 970 EVO Plus 250GB NVMe
- Sec Storage: Crucial MX500 1TB SATA SSD
- LAN: Intel® I219M GbE
- WLAN/BT: BCM94360NG 2.4&5G WiFi Bluetooth 4.0
- Audio: Realtec ALC221 Audio Codec

### This is not a guide, these are pointers on how it currently runs for me.
### Read up on OpenCore, learn, hit & miss, have fun. 

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
  - Everything **Disable**

- Advanced -> Remote Management Options
  - I have not touched anything in here, running defaults AFAIK..



### Current OS
- macOS Big Sur 11.4 (Build 20F71)

### Bootloader
- OpenCore 0.7.1

## Working:
- Allmost everything, see below.

## Known Not working:
- VGA port, throw it to the wolves -unsupported.
- Front audio port (right one) can not act as a 3.5mm Combo version. It is **Line in ONLY**.

## Unused / Not tested:
- Sleep, nap, whatever.. i dont use, might dig into that -in future boredom :)
