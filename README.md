# Lenovo-M710q-QNCT-Hackintosh
EFI for Lenovo-M710q-QNCT with OpenCore 0.6.9 bootloader  
Test for macOS 11.4

### Computer Spec:

| Component        | Specifications                         |
| ---------------- | ---------------------------------------|
| CPU              | Intel® Core™ i7-8850H(ES) (QNCT)       |
| iGPU             | Intel® UHD Graphics 630                |
| RAM              | 2 * 8GB DDR4 2666Mhz                   |
| NVMe             | Kioxia RC10 512GB / WD SN520 512GB     |
| LAN              | Intel I219-V                           |
| Audio            | Realtek ALC294                         |
| WiFi & Bluetooth | Intel Wi-Fi 6 AX200 / 7265AC           |
| SMBIOS           | MacMini8,1                             |
| BootLoader       | OpenCore 0.6.9                         |

### What works:

- [x] Intel Intel® UHD Graphics 630 iGPU DP Output
- [x] ALC294 Internal Speakers
- [x] ALC294 & DP Audio Output
- [ ] ALC294 Audio Input
- [x] All USB Ports
- [x] Intel I219-V
- [x] Intel Wi-Fi & Bluetooth
- [x] NVRAM

### BIOS Settings:

* Update Bios to M1AKT4FA  
* Disable:  
CSM  
VT-d  
SGX  
* Enable:  
VMX  
UEFI only  
* Boot this OpenCore
* Chose UEFI Shell to boot
* Run code to ser 64M DVMT and disable CFG Lock:
```
setup_var   
setup_var 0x7AC 0x2  
setup_var 0x503 0x0  
```
* Reboot to install macOS

#### 说人话
更新bios到最新，不然安装会报多线程的错误（不懂可以看[BV1Ab4y1Z781](https://www.bilibili.com/video/BV1Ab4y1Z781)）  
在BIOS中必须完全关闭CSM，开启纯UEFI启动，开启VMM虚拟化，关闭VT-d，SGX可选择性关闭  
启动这个OpenCore，选UEFI Shell进去执行上面Run code的几个命令  
然后重启安装macOS

## Credits

- [Apple](https://apple.com) for macOS.
- [Acidanthera](https://github.com/acidanthera) for OpenCore and all the lovely hackintosh work.
- [Dortania](https://github.com/dortania) for great and detailed guides.
