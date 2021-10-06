# YOGA-S740 hackintosh

## （[中文](https://github.com/frozenzero123/YOGA-S740/blob/master/README.MD)）


## Device Information：
* Equipment:Lenovo YOGA S740 14llL(China version)
* Graphics: Iris Plus 940 （Iris Plus G7）
* CPU: i7 1065G7
* SSD: WD Blue SN550 NVMe SSD 1T (after pm981a replacement)
* Audio: ALC285 and inter sst mic
* Memory: 16G DDR4X Micron 
* BIOS: BYCN35WW
* CFG lock: Disabled (changed)（important! Must be done！）
* DVMT: 160M (changed)（important! Must be done！）

## Important!Important!Important!

* CFG lock: must change（important! Must be done！）
* DVMT: 64M or higher！（The highest setting is best not to use -dvmt repair is because you can modify the hardware and modify the hardware without affecting win）
* The terminal enters the following content to control the sleep status and achieve the purpose of saving power [source](https://dortania.github.io/OpenCore-Post-Install/universal/sleep.html#preparations)
```
sudo pmset autopoweroff 0
sudo pmset powernap 0
sudo pmset standby 0
sudo pmset proximitywake 0
sudo pmset tcpkeepalive 0
```


## Can drive
|  | Details |
|:-: | :-:|
|Opencore|OpenCore 0.7.3 reless|
|Audio|  only built-in mic no work（The rest are normal） |
|Bluetooth|  The mic of AX201 can be used normally, or it can be solved by replacing it with a Broadcom network card|
|Network| AX201 thanks（[itlwm](https://github.com/OpenIntelWireless/itlwm)）Or replace the Broadcom network card yourself|
|touchpad|MSFT0001 Hot patch (Finally realized the interrupt mode)thanks（[宪武](https://github.com/daliansky/OC-little)）and Allen|
|GPU|normal thanks（(by @0xFireWolf, also thanks @m0d16l14n1 and @kingo132)） |
|Fn Keys| Brightness and volume can be used normally|
|Sleep| aoac sleep Kingston A2000 sleep power consumption 1 hour 3% related machine friends can test by themselves
## Can't drive
|  | Details |
|:-: | :-:|
|Keyboard backlight| The keyboard backlight cannot be turned off automatically, you need to manually control the turn off (especially sleep) fn+spacebar｜
|More|。。。|


## how to use
Apply the file to the downloaded [OpenCorePkg](https://github.com/acidanthera/OpenCorePkg)。At the same time, you need to check whether the contents in the config and kext/acpi folders correspond, and you also need to add platforminfo.Or download the reless version to add three codes and other information to use directly
