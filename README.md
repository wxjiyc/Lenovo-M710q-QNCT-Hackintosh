# Lenovo-M710q-QNCT-Hackintosh
EFI for Lenovo-M710q-QNCT with OpenCore 0.6.8 bootloader

### Computer Spec:

| Component        | Specifications                         |
| ---------------- | ---------------------------------------|
| CPU              | Intel® Core™ i7-8850H(ES)              |
| iGPU             | Intel® UHD Graphics 630                |
| RAM              | 2 * 8GB DDR4 2400Mhz                   |
| NVMe             | WD SN520 512GB                         |
| LAN              | Intel I219-V                           |
| Audio            | Realtek ALC294                         |
| WiFi + Bluetooth | Intel® Wi-Fi 6 AX200 + Bluetooth 5.2   |
| SMBIOS           | MacMini8,1                             |
| BootLoader       | OpenCore 0.6.9                         |

### What works:

- [x] Intel Intel® UHD Graphics 630 iGPU DP Output
- [x] ALC294 Internal Speakers
- [x] ALC294 DP Audio Output
- [x] All USB Ports
- [x] Intel I219-V
- [x] Intel® Wi-Fi 6 AX200 + Bluetooth
- [x] NVRAM

### BIOS Settings:

Update to M1AKT4FA
#DVMT 64M
GRUB> setup_var 0x7AC 0x2
#CFG Lock
GRUB> setup_var 0x503 0x0

Disable:
CSM
VT-d
SGX

Enable:
VMX
UEFI only

## Credits

- [Apple](https://apple.com) for macOS.
- [Acidanthera](https://github.com/acidanthera) for OpenCore and all the lovely hackintosh work.
- [Dortania](https://github.com/dortania) for great and detailed guides.
