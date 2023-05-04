---
dateFromWiki: "2019-04-10T02:45:51Z"
title: "压机温控箱和加热设备"
gallery: true
aliases:
- /MonkeyWiki/Press_heat_control_and_thermocouples/zh-cn
translatedDate: "2019-04-10T02:45:51Z"
translator: "X z"
translatorPage: "/zh-cn/MonkeyWiki/X_z"
---
{{< img src="images/Press_HeatControllerOutside.JPG" caption="_Heat controller on the Monkey Press._" >}}这是我气动压力机上加热系统的详细概述。


## 电热毯

 

{{< img src="images/Press_Blanket.JPG" >}}压力机用两根来自[radar/ MEI](http://michaelsenter)定制的硅热毯加热，每一个14英寸x85英寸，在240v上运行2,083瓦。它们非常快速均匀地加热，具有弹性，并且可以承受压力机内的压力。温度必须在约10分钟内从室温升至175°F，然后保持在+/- 5度范围内一小时，这些橡皮布与良好的控制器相结合，可以很好地完成工作。

毯子由两片0.032“5052-H32铝制成保护。毯子相当精致; 他们需要保护免受任何挤压或刺穿，或者他们可能会短路，甚至引发火灾。每个橡皮布都撒上滑石粉，使它们可以在两片铝片之间轻松滑动，并在一端用一点电工胶带粘在一起。

{{< img src="images/Press_BlanketPlugs.JPG" >}}放置橡皮布使得一端上较厚的电源连接从不在铝板之间压缩。铝的每一端都已经平整，并用一些红色电工胶带包裹，以确保没有锋利的末端挖入毯子的末端。 

毯子通过普通的240v 15A插头连接到控制箱。在压力机上工作时，有时可以断开橡皮布的连接。 


## 控制器

 

热量由定制控制器控制，使用固态继电器，具有斜坡/保温编程功能的PID控制器，接触器，几个保险丝和一对热电偶。我们没有花时间绘制原理图，但电路非常简单。电源进入接触器，并从那里分配到热毯的连接器。其中一个热引线通过固态继电器（SSR），它连接到斜坡/保温PID控制器。 热电偶也连接到PID控制器，传感端放置有热毯。如果需要，SSR可以在一秒钟内切换，从而可以很好地控制通过毯子传递多少热量。

SSR是一款额定25A的Continental RVDA。

The contactor with panel-mount switch is part #SD1-025-RR from [Automation Direct](http://www.automationdirect.com).

图中较大的方形控制器是我在eBay上找到的便宜的斜坡/浸泡PID控制器。较小的一个也是一个PID控制器（非斜坡/浸泡），也可以在eBay上找到，但它被配置为温度监控器。 这些控制器在eBay和其他地方以很多不同的名字出售......如果你看到一个看起来像其中之一，它可能是同样的事情。

我发现我必须修改两个控制器中的设置以平滑温度测量，以解决毯子的一些噪音。 

{{< gallery  caption="The inside of the heating controller on the Monkey Press" >}}
{{< gallery-item src="images/Press_Controller91.JPG" caption="Heat controller on the Monkey Press." >}}
{{< gallery-item src="images/Press_Controller46.JPG" caption="Head controller on the Monkey Press." >}}
{{< gallery-item src="images/Press_Controller96.JPG" caption="Head controller on the Monkey Press." >}}
{{< gallery-item src="images/Press_Controller98.JPG" caption="Heat controller on the Monkey Press." >}}
{{< gallery-item src="images/Press_Controller99.JPG" caption="Heat controller on the Monkey Press." >}}
{{< gallery-item src="images/Press_Controller04.JPG" caption="Heat sink on the SSR in the heat controller on the Monkey Press." >}}
{{< gallery-item src="images/Press_Controller60.JPG" caption="The SSR in the heat controller on the Monkey Press." >}}
{{< gallery-item src="images/Press_Controller62.JPG" caption="The contactor in the heat controller on the Monkey Press." >}}
{{< /gallery >}}



### 原理图和电气建议

我实际上并不想在这里提供精确的原理图或电气建议。这是我不太喜欢做的少数事情之一。如果不清楚如何从上面的描述和这里的几张图片构建这个控制器，那么你应该咨询电工或已经在这方面有很多知识的朋友。 


### PID控制器

我使用具有“斜坡/浸泡”功能的Auber PID控制器。手册如下：[[File：Auber SYL Part1.pdf | File：Auber SYL Part1.pdf]]，[[File：Auber SYL Part2.pdf | File：Auber SYL Part2.pdf]]

有时配置这些有点痛苦。阅读说明书，并在合理的压力下使用压力机中的旧滑雪板至少自动调整一次。这样可以更好地模拟层压板的热特性，自动调谐可以做得更好。

作为参考，以下是我的控制器中所有参数的值：

{| class="wikitable"
|-
!Setting
!Value
|-
!ALM1!!225
|-
!ALM2!!32
|-
!Hy-1!!10
|-
!Hy-2!!9999
|-
!Hy!!0.3
|-
!At!!3
|-
!I!!83
|-
!P!!74
|-
!d!!3
|-
!T!!2
|-
!Sn!!0
|-
!DP!!0
|-
!P-SL!!-100
|-
!P-SH!!2500
|-
!Pb!!0.0
|-
!OP-A!!0
|-
!OutL!!0
|-
!OutH!!100
|-
!AL-P!!17
|-
!Cool!!10
|-
!Addr!!1
|-
!Baud!!4800
|-
!FILt!!6
|-
!A-M!!2
|-
!Lock!!808
|}


## 热电偶

 

{{< img src="images/Press_Thermo84.JPG" caption="_Thermocouples used on the Monkey Press._" >}}热电偶来自[Omega](http://www.omega.com)，部分＃5SRTC-TT-K-36-36适用于5型 K个热电偶和＃RMJ-KS用于控制箱上的连接器。热电偶为36AWG（0.005“），因此足够小，可以直接放在热毯的顶部而不会损坏橡皮布。我在每个毯子上放置一个，传感器末端在毯子的中心。底部的热电偶连接到斜坡/保温PID控制器，而顶部的热电偶仅用于监控层压板两侧之间的温差。

热电偶还与插头连接，这使得我们可以在装载层压板之前将热电偶放入毯子中，并在热电偶损坏时轻松更换热电偶。

{{< gallery  caption="Thermocouples used on the Monkey Press" >}}
{{< gallery-item src="images/Press_Thermo70.JPG" caption="Thermocouples used on the Monkey Press." >}}
{{< gallery-item src="images/Press_Thermo74.JPG" caption="Thermocouples used on the Monkey Press." >}}
{{< gallery-item src="images/Press_Thermo76.JPG" caption="Thermocouples used on the Monkey Press." >}}
{{< gallery-item src="images/Press_Controller65.JPG" caption="The thermocouple connectors, from the inside, on the heat controller on the Monkey Press." >}}
{{< gallery-item src="images/Press_Controller68.JPG" caption="Thermocouple connectors on the heat controller on the Monkey Press." >}}
{{< /gallery >}}



## 另见

- [Monkey 压力机制造]({{< ref "MonkeyWiki/Equipment/Snowboard_press/Monkey_Press_Construction.md" >}})


