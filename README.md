# Lenovo-M710q-QNCT-Hackintosh
EFI for Lenovo-M710q-QNCT with OpenCore 0.7.2 bootloader  
Test for macOS 12.0

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
| BootLoader       | OpenCore 0.7.2                         |

### What Works:

- [x] Intel Intel® UHD Graphics 630 iGPU DP Output
- [x] ALC294 Internal Speakers
- [x] ALC294 & DP Audio Output
- [x] ALC294 Audio Input
- [x] All USB Ports
- [x] Intel I219-V
- [x] Intel Wi-Fi & Bluetooth
- [x] NVRAM

### BIOS Settings:

* Update BIOS to M1AKT50A  
* Disable:  
CSM   
* Boot this OpenCore
* Press the space bar
* Choose "SetupVar"
* Run code to set 64M DVMT:
```
setup_var 0x7AC 0x2   
```
* Reboot to install macOS

#### 说人话
更新BIOS到最新，不然安装会报多线程的错误（不懂可以看[BV1Ab4y1Z781](https://www.bilibili.com/video/BV1Ab4y1Z781)）  
在BIOS中必须完全关闭CSM，然后启动这个OpenCore，在引导主题界面按下空格，进入SetupVar输入setup_var 0x7AC 0x2回车  
然后重启安装macOS  
0.7.0版本中加入了引导主题和开机声音，4K显示器显示主题可能会有黑边，把config.plist里NVRAM中的UIScale改为02即可  

## Credits

- [Apple](https://apple.com) for macOS.
- [Acidanthera](https://github.com/acidanthera) for OpenCore and all the lovely hackintosh work.
- [Dortania](https://github.com/dortania) for great and detailed guides.
