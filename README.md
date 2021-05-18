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

说人话就是要根据D大教程合成刷入最新版的BIOS，不然安装会报多线程的错误。在BIOS中必须完全关闭CSM，开启纯UEFI启动，开启VMM虚拟化，关闭VT-d，SGX可选择性关闭，然后U盘上放入GRUB引导，进入GRUB命令行输入setup_var 0x7AC 0x2回车，setup_var 0x503 0x0回车重启，这样就分别解锁了DVMT和CFG Lock，这样就可以顺利使用本引导了。

## Credits

- [Apple](https://apple.com) for macOS.
- [Acidanthera](https://github.com/acidanthera) for OpenCore and all the lovely hackintosh work.
- [Dortania](https://github.com/dortania) for great and detailed guides.
