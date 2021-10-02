# YOGA-S740 黑苹果

## （[English](https://github.com/frozenzero123/YOGA-S740/blob/master/README-EN.md)）


## 设备信息：
* 设备:Lenovo YOGA S740 14llL(China version)
* 显卡: Iris Plus 940 （Iris Plus G7）
* 处理器: i7 1065G7
* 硬盘: 西数 SN550 NVMe SSD 1T (替换了pm981a)
* 声卡: ALC285 和inter sst内麦
* 内存: 16G DDR4X Micron 
* BIOS: BYCN36WW
* CFG lock: Disabled (changed)（重点！必须完成）
* DVMT: 160M (changed)（重点！必须完成）

## 重点！重点！重点！

* CFG Lock 必须解锁

* DVMT设置必须64M或者更高（设置最高最好之所以不使用-dvmt修复是因为能修改硬件就修改硬件不影响win）



## 能够驱动
|  | 细节 |
|:-: | :-:|
|OC版本|OpenCore 0.6.3 reless|
|声卡|  内麦无法驱动(耳麦正常) |
|蓝牙|  目前发现AX201自带蓝牙无法输出AirPods pro 的mic电平 ,替换为博通网卡可解决|
|网卡| AX201 感谢（[itlwm](https://github.com/OpenIntelWireless/itlwm)）或者自己更换博通网卡|
|触控板|MSFT0001 Hot patch （终于实现了中断模式）感谢（[宪武](https://github.com/daliansky/OC-little)）和 触摸群Allen|
|显卡|终于正常 感谢（ @0xFireWolf, also thanks @m0d16l14n1 and @kingo132)） |
|Fn按键|亮度和音量可以正常使用|
## 暂时无法驱动
|  | 细节 |
|:-: | :-:|
|睡眠| AOAC ( 睡眠有问题，但是似乎可以完成，有能力的人可以自行完善)|
|更多|。。。|


## 如何使用
将文件套用到下载的OC模板[OpenCorePkg](https://github.com/acidanthera/OpenCorePkg)
同时，自行添加网卡信息。需要核对config与kext/acpi文件夹里的内容是否对应，还需自行添加三码等机型信息。
或者下载reless版添加三码等信息直接使用。
