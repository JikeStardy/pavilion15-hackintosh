# 光影精灵4 i5-8300H + GTX1050Ti 黑苹果 Hackintosh EFI

[![996.icu](https://img.shields.io/badge/link-996.icu-red.svg)](https://996.icu)

_PAVILION 15-CX Hackintosh Clover EFI_
_光影精灵4 i5-8300H + GTX1050Ti 黑苹果EFI_

&emsp;&emsp;很久以前就想搞黑苹果玩了，奈何伴我多年的老爷机是AMD的。在上大学前买了光影精灵4，足够的性能（主要是Intel的CPU哈哈）让我重新燃起了想搞黑苹果的想法（当然现在也是日常使用的系统啦，主要敲敲Java代码，玩玩Steam小游戏，逛逛b站这样）
&emsp;&emsp;本EFI是在[黑果小兵的部落阁](https://blog.daliansky.net/)中的EFI整合里发现了[canwdev](https://github.com/canwdev/omen15dc-hackintosh)写好的一份暗影4的EFI，当时在想光影精灵4与暗影精灵4几乎是同一个时间出的机子，他们的EFI会不会能通用呢？（更重要的是当时找光影4的EFI真的找到绝望了）

# 说明
- UHD630 正常驱动
- 可以正常调节亮度，记忆亮度信息
- 内置键盘、触控板<sup>[①](#first)</sup>正常驱动
- 有线上网、USB接口功能
- 电池电量显示
- 温度传感器
- 开机不黑屏<sup>[②](#second)</sup>
- Type-C<sup>[③](#third)</sup>
- 蓝牙<sup>[④](#fourth)</sup>
- 扬声器外放
- WiFi<sup>[⑤](#fifth)</sup>

<span id="first"><font size=2>①还没想到怎么解决多点触控和手势问题</font></span>
<span id="second"><font size=2>②这个开机不黑屏挺玄学的，一时时的</font></span>
<span id="third"><font size=2>③实测可以TypeC转HDMI输出HDMI信号，但最好在机子开好了再接上，不然内屏会黑掉一直亮不起来（有亮度但没画面）</font></span>
<span id="fourth"><font size=2>④需要先打开Windows再重启到macOS里</font></span>
<span id="fourth"><font size=2>⑤这个东西是无解的（除非你内置的网卡恰恰好是博通？），对WiFi功能有需要就去买USB网卡或者换掉内置的网卡（这样还能顺带解决蓝牙的问题），具体怎么选择USB无线网卡的型号参考[这个USB网卡驱动的Readme](https://github.com/chris1111/Wireless-USB-Adapter-Clover)（我选了TPLink的wn725nV3，一开始下载的官方驱动，搞得我心态都炸了，然后发现这个好用，完美驱动起wn725n）</font></span>

# 让机子记忆上次开机使用的亮度的方法（有时候会抽一下）
因为不能利用原生nvram来储存亮度，所以利用RC scripts来保存，安装Clover时选择RC scripts即可
![亮度保存](https://spxg.me/wp-content/uploads/2019/07/QQ20190706-141105.png)

# 参考教程
- [macOS安装教程(以小米Pro为例子)](https://blog.daliansky.net/MacOS-installation-tutorial-XiaoMi-Pro-installation-process-records.html)
- [CPU性能模式的调整(大佬写好了很方便的脚本)](https://github.com/stevezhengshiqi/one-key-cpufriend)
- [HIDPI的启动(也是大佬写好的脚本)](https://github.com/xzhih/one-key-hidpi)

# 鸣谢
- [黑果小兵](https://github.com/daliansky)
- [canwdev](https://github.com/canwdev)  
- [xzhih](https://github.com/xzhih)
- [stevezhengshiqi](https://github.com/stevezhengshiqi)
