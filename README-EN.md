# YOGA-S740 hackintosh

## （[中文](https://github.com/frozenzero123/YOGA-S740/blob/master/README.MD)）


## Device Information：
* Equipment:Lenovo YOGA S740 14llL(China version)
* Graphics: Iris Plus 940 （Iris Plus G7）
* CPU: i7 1065G7
* SSD: kingston A2000 NVMe SSD 1T (after pm981a replacement)
* Audio: ALC285 and inter sst mic
* Memory: 16G DDR4X 3733 Micron 
* BIOS: BYCN39WW
* CFG lock: Disabled (changed)（important! Must be done！）
* DVMT: 160M (changed)（important! Must be done！）

## Important!Important!Important!

* CFG lock: must change（important! Must be done！Or enable AppleCpuPmCfgLock and AppleXcpmCfgLock, but this is only temporary）
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
|Open the cover and brighten the screen|After injecting the corrected ecdt,but it also makes the brightness shortcut key invalid|
## Can't drive
|  | Details |
|:-: | :-:|
|Keyboard backlight| The keyboard backlight cannot be turned off automatically,need to use fn+spacebar  to turn off (especially when the lid is closed｜
|Brightness shortcut key| you need to use fn+f11, f12 to manually control the brightness (set in the settings)｜
|More|。。。|
<img width="666" alt="截屏2022-01-28 13 24 44" src="https://user-images.githubusercontent.com/52648473/151494656-f86cc64e-cf6d-4463-b254-4253bd272567.png">
<img width="587" alt="截屏2022-01-28 13 27 25" src="https://user-images.githubusercontent.com/52648473/151494677-0cc6f563-0f05-4cc2-81c1-e4b7db17f296.png">





## how to use
Apply the file to the downloaded [OpenCorePkg](https://github.com/acidanthera/OpenCorePkg)。At the same time, you need to check whether the contents in the config and kext/acpi folders correspond, and you also need to add platforminfo.Or download the （[Releases](https://github.com/frozenzero123/YOGA-S740/releases)） version to add three codes and other information to use directly
