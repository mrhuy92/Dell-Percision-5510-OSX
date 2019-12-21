# Dell Precision 5510 Hackintosh Catalina

## My Configuration
* CPU: Intel Core i7 6820HQ 
* GPU: Intel HD Graphics 530 HD530 
* RAM: 32GB DDR4 2133 MHz
* NVME: WD Black SN720 250GB
* WIFI: Dell DW1560
* MONITOR: 4K IZGO
* BIOS: 1.12.0
* This repo is based on: 
  * [soulomoon repo](https://github.com/soulomoon/Dell-Precision-5510-OSX)
  * [wmchris repo](https://github.com/wmchris/DellXPS15-9550-OSX)
* All third party kexts being installed in **Clover/Kext/Other**.

## What not Working
* SD-Card reader
* Intel 8260NGW (rarely used in the 5510, though if you have it, it must be replaced, recommend is DW1560 for p/p)
* nVidia Graphics card
* Thunderbolt 3

## HDMI
* To enable HDMI output, add the key/string to location below: 
```
/System/Library/Extensions/AppleGraphicsControl.kext/Contents/PlugIns/AppleGraphicsDevicePolicy.kext/Contents/Info.plist:
	ConfigMap:
		Dictionary:
			<key>Mac-A5C67F76ED83108C</key>
			<string>none</string>
``` 
* Rebuild kext cache using 
`sudo kextcache -i /`

* Enter command below before HDMI enable edit
```
sudo mount -uw /
sudo killall Finder
```
## Tools
* [Kext Utility](http://cvad-mac.narod.ru/index/0-4)
* [Hackintool](https://www.tonymacx86.com/threads/release-hackintool-v2-8-6.254559/)
## Credits
* This patch had edited & optimized by **mrhuy**
