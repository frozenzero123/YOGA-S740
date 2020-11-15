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



## Can drive
|  | Details |
|:-: | :-:|
|Opencore|OpenCore 0.6.0 Debug|
|Audio|  only built-in mic no work（The rest are normal） |
|Bluetooth|  At present, it is found that AX201's built-in Bluetooth cannot output the mic level of AirPods pro |
|Network| AX201 thanks（[itlwm](https://github.com/OpenIntelWireless/itlwm)）|
|touchpad|MSFT0001 Hot patch thanks（[宪武](https://github.com/daliansky/OC-little)）|
|GPU|There is a problem of starting the screen, but it is normal after startingby thanks（[FireWolf](https://github.com/0xFireWolf/WhateverGreen)） |
|Fn Keys| Brightness and volume can be used normally|
## Can't drive
|  | Details |
|:-: | :-:|
|Sleep| AOAC ( There is a problem with sleep, and it cannot be completed temporarily. Consider the problem with the graphics card driver)  |                                                                                    |
|More|。。。|


## how to use
Apply the file to the downloaded [OpenCorePkg](https://github.com/acidanthera/OpenCorePkg)。At the same time, you need to check whether the contents in the config and kext/acpi folders correspond, and you also need to add platforminfo.
