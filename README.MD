# YOGA-S740 黑苹果

## （[English](https://github.com/frozenzero123/YOGA-S740/blob/master/README-EN.md)）


## 设备信息：
* 设备:Lenovo YOGA S740 14llL(China version)
* 显卡: Iris Plus 940 （Iris Plus G7）
* 处理器: i7 1065G7
* 硬盘: intel 545s 外置ssd (屏蔽了pm981a)，金士顿A2000
* 声卡: ALC285 和inter sst内麦 外置mic
* 内存: 16G DDR4X 3733 Micron 
* BIOS: BYCN39WW
* CFG lock: Disabled (changed)（重点！必须完成）
* DVMT: 160M (changed)（重点！必须完成）

## 重点！重点！重点！

* CFG Lock 必须解锁(或者开启AppleCpuPmCfgLock和AppleXcpmCfgLock，但这只是暂时的)

* DVMT设置必须64M或者更高（config内添加了相关设定应该可以不予更改，但还是建议调整dvmt）


* 终端输入以下内容来控制睡眠状况，达到节省电量的目的 [来源](https://dortania.github.io/OpenCore-Post-Install/universal/sleep.html#preparations)
```
sudo pmset autopoweroff 0
sudo pmset powernap 0
sudo pmset standby 0
sudo pmset proximitywake 0
sudo pmset tcpkeepalive 0
```


## 能够驱动
|  | 细节 |
|:-: | :-:|
|OC版本|OpenCore 0.7.7 reless|
|声卡|  内麦无法驱动(耳麦正常，使用id88外置mic，如不需要可用id61) |
|蓝牙|  AX201已经可以正常使用 ,或者替换为博通网卡也可解决|
|网卡|  AX201 感谢（[itlwm](https://github.com/OpenIntelWireless/itlwm)）或者自己更换博通网卡|
|触控板|MSFT0001 Hot patch （终于实现了中断模式） 感谢（[宪武](https://github.com/daliansky/OC-little)）和 触摸群Allen|
|显卡|终于正常 感谢（ @0xFireWolf, also thanks @m0d16l14n1 and @kingo132)） |
|Fn按键|音量可以正常使用，添加yogasmc后可用实现一些fn快捷键 |
|睡眠|aoac睡眠 金士顿A2000（推荐三星ssd） 睡眠耗电1小时3% 呼吸灯和键盘灯修复 相关机友可自行测试|
|开盖亮屏|在注入修正后的ecdt后，实现了开盖亮屏的功能但是也使得亮度快捷键失效了|
## 暂时无法驱动
|  | 细节 |
|:-: | :-:|
|更多|。。。|


<img width="587" alt="截屏2022-01-28 13 27 25" src="https://user-images.githubusercontent.com/52648473/151492271-8452c63e-4b79-4755-a80e-d0524ad32393.png">



## 如何使用
将文件套用到下载的OC模板[OpenCorePkg](https://github.com/acidanthera/OpenCorePkg)
同时，自行添加网卡信息。需要核对config与kext/acpi文件夹里的内容是否对应，还需自行添加三码等机型信息。
或者下载（[Releases](https://github.com/frozenzero123/YOGA-S740/releases)）版添加三码等信息直接使用。

## 附言
分享的东西拿来售卖的无良奸商死全家！
