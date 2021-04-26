---
title: 关于EFI中驱动的含义
author: KAZE
avatar: 'https://cdn.jsdelivr.net/gh/kaze0617/cdn@2.3/images/custom/avatar.jpg'
authorLink: /about/
comments: false
date: 2020-03-30 16:19:59
authorAbout: 爱折腾
authorDesc: 爱折腾，热爱二次元。
categories: 支持
tags:
keywords:
description: 理解他的含义，才能更好的安装。
photos: https://cdn.jsdelivr.net/gh/kaze0617/cdn@2.3/images/article/kext.jpg
---
转载自[Hac的小窝](http://hac.fangf.cc/archives/349)
<center>知其然，知其所以然</center>

### <center>必备驱动</center>
|驱动名称|含义|
|:--:|:--:|
|<font color=#e67474>FakeSMC.kext</font>|黑苹果必备驱动之一，用于仿冒苹果SMC设备的驱动文件。|
|<font color=#e67474>VirtualSMC.kext</font>|可替代你的FakeSMC.kext驱动的一个玩意儿。|
|<font color=#e67474>Lilu.kext</font>|黑苹果驱动扩展库，Lilu.kext驱动是黑苹果系统必不可缺的一款驱动；很多黑苹果驱动都需要依赖lilu.kext。|

### <center>有线网卡</center>
|驱动名称|含义|
|:--:|:--:|
|<font color=#e67474>AppleRTL8169Ethernet</font>|Realtek RTL8169 官方驱动|
|<font color=#e67474>AtherosE2200Ethernet.kext</font>|高通 Atheros Killer E2200 系列驱动|
|<font color=#e67474>AtherosL1cEthernet.kext</font>|高通 Atheros AR813x/815x 驱动|
|<font color=#e67474>IntelMausi.kext</font>|英特尔有线网卡 Acidanthera 分支|
|<font color=#e67474>IntelMausiEthernet.kext</font>|英特尔有线网卡原作者|
|<font color=#e67474>NullEthernetInjector.kext</font>|仿冒内建网卡 (没有可用的内建网卡时使用)|
|<font color=#e67474>RealtekR1000SL.kext</font>|Realtek 8111B/C/D/E/EP/F/G/GU/8411B 系列驱动|
|<font color=#e67474>RealtekRTL8100.kext</font>|Realtek RTL810X 系列驱动|
|<font color=#e67474>RealtekRTL8111.kext</font>|Realtek RTL8111/8168 系列驱动|

### <center>Wi-Fi 和 蓝牙</center>
|驱动名称|含义|
|:--:|:--:|
|<font color=#e67474>AirPortAtheros40.kext</font>|高通 Atheros AR92xx/AR93xx 驱动, 仅用于 10.14+|
|<font color=#e67474>AirPortAtheros40.kext</font>|高通 Atheros AR92xx/AR93xx 驱动, 仅用于 10.14+|
|<font color=#e67474>AirportBrcmFixup.kext</font>|非苹果官方博通网卡修复|
|<font color=#e67474>ATH9KFixup.kext</font>|高通 Atheros AR9xxx 无线网卡修复|
|<font color=#e67474>rcmPatchRAM.kext</font>|博通网卡蓝牙固件上传|
|<font color=#e67474>BT4LEContinuityFixup.kext</font>|IOBluetoothFamily 修补|
|<font color=#e67474>MT7610</font>|联发科 MT7610|
|<font color=#e67474>RT5370</font>|联发科 RT5370|
|<font color=#e67474>RTL8192CU</font>|Realtek RTL8192CU 驱动|
|<font color=#e67474>HoRNDIS.kext</font>|解决你没有网络的痛苦。用手机连电脑，让电脑直接用手机上的数据网络上网。|

### <center>键盘, 鼠标 和 触摸设备</center>
|驱动名称|含义|
|:--:|:--:|
|<font color=#e67474>ApplePS2SmartTouchPad.kext</font>|触摸板和键盘|
|<font color=#e67474>AsusSMC.kext</font>|华硕 Fn 键, 键盘背光灯和环境光传感器 驱动|
|<font color=#e67474>NoTouchID.kext</font>|禁用 Touch ID 检测, 修复输密码时卡顿|
|<font color=#e67474>SerialMouse.kext</font>|使用Microsoft 串行鼠标协议的串行鼠标驱动|
|<font color=#e67474>VoodooI2C.kext	I2C</font>|触摸板/屏 驱动|
|<font color=#e67474>VoodooPS2Controller.kext</font>|PS2 键盘/触摸板 驱动|

### <center>显卡 和 声卡</center>
|驱动名称|含义|
|:--:|:--:|
|<font color=#e67474>AppleALC.kext</font>|定制万能声卡驱动|
|<font color=#e67474>AppleHDA.kext</font>|Intel High Definition Audio高保真声卡驱动，大部分集成声卡,例如ALC889A声卡就可以直接用其驱动,禁止与VoodooHDA.kext一起使用！|
|<font color=#e67474>NVIDIA CUDA drivers</font>|NVIDIA CUDA 驱动|
|<font color=#e67474>NVIDIA Web-drivers</font>|NVIDIA 显卡驱动|
|<font color=#e67474>SNBGraphicsMojaveInstaller</font>|二代酷睿核显驱动, 仅用于 10.14+|
|<font color=#e67474>VoodooHDA.kext</font>|万能声卡驱动|
|<font color=#e67474>WhateverGreen.kext</font>|修复黑苹果AMD/NVIDIA/Intel核显显卡黑屏、花屏、睡眠黑评估等各种问题补丁，需要与ilu.kext配合使用。|
|<font color=#e67474>Polaris22Fixup.kext</font>|Polaris22/VegaM 显卡修复|
|<font color=#e67474>NvidiaGraphicsFixup.kext</font>|黑苹果英伟达显卡驱动，解决黑屏、卡顿、驱动不了等问题，而且还添加了HDMI/DP音频输出等功能， 必须搭配最新的Lilu.kext使用。|

### <center>CPU 和 SMC</center>
|驱动名称|含义|
|:--:|:--:|
|<font color=#e67474>CPUFriend.kext</font>|CPU 变频管理|
|<font color=#e67474>FakeSMC.kext and sensors</font>|Clover 官方 FakeSMC|
|<font color=#e67474>HWPEnabler.kext</font>|启用 HWP|
|<font color=#e67474>NullCPUPowerManagement.kext</font>|AMD 和虚拟机专用版本|
|<font color=#e67474>OpcodeEmulator.kext</font>|Opcode 模拟驱动|
|<font color=#e67474>TSCAdjustReset.kext</font>|TSC 频率同步驱动|
|<font color=#e67474>VirtualSMC.kext 及传感器|Acidanthera 的 SMC 和传感器驱动|
|<font color=#e67474>VoodooTSCSync.kext</font>|TSC 频率同步驱动|

### <center>USB 和 其它接口</center>
|驱动名称|含义|
|:--:|:--:|
|<font color=#e67474>IOElectrify.kext</font>|在雷电 3 设备上启用常开电源|
|<font color=#e67474>USBWakeFixup.kext</font>|修复 Skylake 平台 USB 唤醒黑屏|
|<font color=#e67474>SASMegaRAID.kext</font>|LSI MegaRAID SAS 系列 RAID 控制器驱动|
|<font color=#e67474>Sinetek-rtsx.kext</font>|Realtek RTSX SDHC 读卡器驱动|
|<font color=#e67474>VoodooSDHC.kext</font>|SDHC 读卡器驱动|

### <center>其它驱动</center>
|驱动名称|含义|
|:--:|:--:|
|<font color=#e67474>AppleIntelInfo.kext</font>|CPU / 核显 变频测试|
|<font color=#e67474>HibernationFixup.kext</font>|修复因 RTC 变量和 NVRAM 造成的睡眠问题|
|<font color=#e67474>Lilu.kext</font>|SDK & Library|
|<font color=#e67474>LiluFriend.kext</font>|用于确保 Lilu 在 L/E 下正常加载|
|<font color=#e67474>RTCMemoryFixup.kext</font>|修复 BIOS CMOS (RTC) 内存和 AppleRTC 之间的冲突问题|
|<font color=#e67474>NightShiftUnlocker.kext</font>|解锁 NightShift|
|<font color=#e67474>WebCamera.kext</font>|某些旧设备的摄像头驱动|

<style>
    table th {
    font-weight: bold; /*加粗*/
    text-align: center !important; /*内容居中，加上 !important 避免被 Markdown 样式覆盖*/
    background: #FE9600; /*背景色*/
}
    table tbody tr:nth-child(2n) {
    background: #eee; 
}
    table {
    width: 100%; /*表格宽度*/
    max-width: 65em; /*表格最大宽度，避免表格过宽*/
    border: 1px solid #dedede; /*表格外边框设置*/
    margin: 15px auto; /*外边距*/
    border-collapse: collapse; /*使用单一线条的边框*/
    empty-cells: show; /*单元格无内容依旧绘制边框*/
}
table th,
table td {
  height: 35px; /*统一每一行的默认高度*/
  border: 1px solid #dedede; /*内部边框样式*/
  padding: 0 10px; /*内边距*/
}
table td {
    font-weight: bold
}
</style>