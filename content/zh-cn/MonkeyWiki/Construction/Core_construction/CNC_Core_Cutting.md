---
date: "2019-04-22T08:31:33Z"
title: "数控板芯切割"
gallery: true
aliases:
- /MonkeyWiki/CNC_Core_Cutting/zh-cn
translatedDate: "2019-04-22T08:31:33Z"
translator: "X z"
translatorPage: "/zh-cn/MonkeyWiki/X_z.md"
---
本文概述了我在CNC机床上成型板芯时使用的所有步骤，从[嵌体后清理，最后空白板定型]({{< ref "MonkeyWiki/Construction/Core_construction/Cleanup_after_inlay__and_final_blank_sizing.md" >}})沿着有效边缘镶嵌。空白板在嵌入过程中留有定位孔，这使我可以在CNC机床上正确地重新定位零件。

这是一个简短的视频，展示了从空白板到最终板芯的每个步骤，包括所有的CNC程序。

{{< youtube pQZlsaCv4dY >}}


## 边刃浮雕和对齐标记

 
CNC切割板芯的第一个阶段是沿着板芯的周边为边刃材料创建浅浮雕。移除约0.025英寸(0.635mm)的木材和边墙材料以为边刃留出空间并允许芯部在基部的整个宽度上平放。这一步对于确保底座尽可能平直地从压力机出来是至关重要的。这也确保了板芯和边刃附近的基部之间没有空隙。该区域的空隙将是富含环氧树脂的，因此较弱。用1/4英寸向上切割螺旋钻头切割。

CNC机床也会在最终核心上留下小的对准标记（凹坑）。 这些表示核心的实际中心和有效边缘的中心。这些在核心注册到基地后使用; 将标记转移到边缘基部，然后用于对准模具中的基部。用1/4英寸V型槽钻头切割，沉入零件约0.030”。

{{< gallery  caption="边刃浮雕" >}}
{{< gallery-item src="images/CoreShaping_Edge1.JPG" caption="The grove is cut in two concentric passes by the CNC machine to ensure the full width of the edge material will fit. The cutter is a 1/4\" two flute carbide upcut spiral." >}}
{{< gallery-item src="images/CoreShaping_Edge2.JPG" caption="The grove is cut in two concentric passes by the CNC machine to ensure the full width of the edge material will fit. The cutter is a 1/4\" two flute carbide upcut spiral." >}}
{{< gallery-item src="images/CoreShaping_Edge3.JPG" caption="The grove is cut in two concentric passes by the CNC machine to ensure the full width of the edge material will fit. The cutter is a 1/4\" two flute carbide upcut spiral." >}}
{{< /gallery >}}



## 嵌件和对齐孔

 
接下来，我切割嵌件孔和对齐孔。嵌件孔适合嵌件; 我留下足够的空间让嵌件与一点环氧树脂和凯夫拉背衬一起压入。 嵌件本身与T型螺母非常相似，但法兰是圆形的而不是扁平的。我已经仔细地将嵌件法兰的轮廓与CNC匹配，以确保我在板芯和嵌件法兰之间获得完美的结合。较大的浅孔实际上是微妙的碗，在不同的深度切成约7个同心圆。这是用1/4英寸向上螺旋钻头完成的。

正如你将在后面看到的那样，我沿着滑雪板的中心轴使用两个特殊放置的嵌件，以便在铺层期间提供板芯和底板的完美对齐。这些是你在每个嵌件包中居中看到的额外嵌件孔。

{{< gallery  caption="嵌件" >}}
{{< gallery-item src="images/CoreShaping_Inserts1.JPG" caption="Once again the cutter is a 1/4\" carbide upcut spiral." >}}
{{< gallery-item src="images/CoreShaping_Inserts2.JPG" caption="The CNC controller running the insert program for this custom board." >}}
{{< gallery-item src="images/CoreShaping_Inserts3.JPG" caption="Once again the cutter is a 1/4\" carbide upcut spiral." >}}
{{< gallery-item src="images/CoreShaping_Inserts4.JPG" caption="View of insert holes right after cutting, before any cleanup." >}}
{{< gallery-item src="images/CoreShaping_Inserts5.JPG" caption="Insert holes right after cutting, before any cleanup." >}}
{{< /gallery >}}



## 在翻转之前清理底部

 
一旦完成了板芯的底部（嵌件孔，边刃浮雕，对齐标记），就必须将其翻转，以便可以对顶部进行轮廓分析。为此，板芯必须完全平放在CNC工作台上，因此我首先将板芯放回工作台并清理底部。根据需要，对前面步骤中的任何绒毛进行仔细刮擦，刨光或打磨。此时，板芯的底面基本完成，并且看起来与构建的其余部分一样。
 
板芯被重新定位在CNC工作台上，当沟槽被放入时，留下相同的孔，以便为边墙和白蜡木条留出空间。然而，这次板芯被翻转，使板芯的顶部朝上。先前由CNC机器沿着芯的中心轴切割的孔允许我正确地定位它以切割厚度轮廓。

{{< gallery  caption="底部清理" >}}
{{< gallery-item src="images/CoreShaping_BaseCleanup1.JPG" caption="Most of the work is done with a simple scraper and a small bit of 80 grit sand paper." >}}
{{< gallery-item src="images/CoreShaping_BaseCleanup2.JPG" caption="Most of the work is done with a simple scraper and a small bit of 80 grit sand paper." >}}
{{< gallery-item src="images/CoreShaping_BaseCleanup3.JPG" caption="Note the small divot to the left of the alignment hole above. This was left at a specific offset from 0,0 by the CNC machine using a 1/4\" V-grove bit. If for some reason the CNC looses track of where “home” is (this machine has no homing switches) then we can re-home the machine using the same cutter by carefully lowering it into the center of this divot." >}}
{{< /gallery >}}



## 厚度轮廓

 
使用1.5英寸切割器在多个同心通道中将厚度轮廓施加到芯上。我从中心开始向外工作，直到最终板芯的整个表面都被描绘出来。我的CNC机床设计用于非常精确地控制刀具的深度，我们的定制软件（MonkeyCAM）可以为从斜面到中心到尾部的斜坡产生平滑的样条。 

因为板的刚度很大程度上取决于芯的厚度，我希望这个过程的公差为+/- 0.0025“。我的数控机床的Z轴经过精心设计，确保它可以将刀具的深度调整到远小于0.001英寸，并且在一个完美的世界中就足够了。然而，由于来自切割器的热量导致的木材膨胀，将芯坯保持在工作台上的缺陷等最终确保该步骤永远不会是完美的。我的经验是，经过仔细的工作，厚度在绝大多数时间内都在公差范围内。

{{< gallery  caption="Thickness profile" >}}
{{< gallery-item src="images/CoreShaping_ThicknessProfile1.JPG" caption="Most of the way through applying the thickness profile to a core on the CNC machine." >}}
{{< gallery-item src="images/CoreShaping_ThicknessProfile2.JPG" caption="Most of the way through applying the thickness profile to a core on the CNC machine." >}}
{{< gallery-item src="images/CoreShaping_ThicknessProfile3.JPG" caption="The CNC controller running the thickness profile program for this custom board." >}}
{{< /gallery >}}



## 剪切和最终清理

 
CNC机床的最后一步是将最终的整体形状应用到型芯上，并将其切割出来。这是在多个浅通道中完成的，因为随着所有这些加工步骤的进行，板芯变得越来越精细。此时，板头和板尾通常为0.080英寸厚，并且边墙材料在有效边缘的末端附近同样薄。在这个阶段正确地进行工作对于成功切割是至关重要的。留下四个小标签以将芯保持在坯料的剩余部分上。这使板芯在最后一次通过时保持稳定。这些都是在工作台上用手仔细切割，从坯料的其余部分释放最终的芯。
 
最后，在工作台上花费了一点时间和板芯的边缘。我用一点砂纸或短刨小心地磨掉雕刻机钻头留下的所有毛刺。

{{< gallery  caption="Cutout and final cleanup" >}}
{{< gallery-item src="images/CoreShaping_Cutout1.JPG" caption="The edges are sanded lightly to remove any fuzz from the cutting tools, and any minor adjustments needed to the top profile are handled with some extremely light hand plane work." >}}
{{< gallery-item src="images/CoreShaping_Cutout2.JPG" caption="Overall shape cut." >}}
{{< gallery-item src="images/CoreShaping_Cutout3.JPG" caption="An example of one of the tabs left to hold the core stable during the final machining passes." >}}
{{< gallery-item src="images/CoreShaping_Cutout4.JPG" caption="The edges are sanded lightly to remove any fuzz from the cutting tools, and any minor adjustments needed to the top profile are handled with some extremely light hand plane work." >}}
{{< /gallery >}}



## 参阅

- [雕刻机刀具]({{< ref "MonkeyWiki/Equipment/Small_tools/Router_Bits.md" >}})
- [[Special:MyLanguage/Final cleanup and sidewall preparation|最后的清理与边墙准备]]


