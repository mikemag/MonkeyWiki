---
dateFromWiki: "2019-02-03T02:40:59Z"
title: "Press heat control and thermocouples"
gallery: true
aliases:
- /MonkeyWiki/Press_heat_control_and_thermocouples
- /MonkeyWiki/Press_heat_control_and_thermocouples/en
---
{{< img src="images/Press_HeatControllerOutside.JPG" caption="_Heat controller on the Monkey Press._" >}}This is a detailed overview of the heating system on my pneumatic press.


## Blankets 
 

{{< img src="images/Press_Blanket.JPG" >}}The press is heated with two custom silicon heat blankets from [MEI](http://michaelsenterprises.com/), each one 14” x 85”, 2,083 watts running on 240v. They heat very quickly and evenly, are flexible, and they can take the pressure within the press. The temperature must be ramped up from room temperature to 175F over about 10 min, then held within +/- 5 degrees of that for one hour, and these blankets coupled with a good controller get the job done well.

The blankets are protected by two sheets of 0.032” 5052-H32 aluminum. The blankets are fairly delicate; they need to be protected from any pinching or puncture or they may short out, and even start a fire. Each blanket is dusted with talcum powder to allow them to slide easily between the two sheets of aluminum, and taped in place on one end with a bit of electrical tape.

{{< img src="images/Press_BlanketPlugs.JPG" >}}The blankets are placed so that the thicker power connection on one end is never compressed between the aluminum sheets. Each end of the aluminum has been filed smooth, and wrapped with a bit of red electrical tape to ensure that no sharp end digs into the end of the blanket. 

The blankets are connected to the control box with normal 240v 15A plugs. Being able to disconnect the blankets is helpful sometimes when working on the press. 


## Controller 
 

The heat is controlled by a custom-built controller using a solid state relay, a PID controller with ramp/soak programming features, a contactor, a few fuses, and a couple of thermocouples. We’ve not taken the time to draw a schematic, but the circuit is pretty straightforward. Power comes in to the contactor, and from there is distributed to connectors for the heat blankets. One of the hot leads is passed through a solid state relay (SSR), which is connected to the ramp/soak PID controller. A thermocouple is connected to the PID controller as well, with the sensing end placed with the heat blankets. The SSR can switch may times a second if necessary allowing pretty fine control over how much heat is delivered via the blankets.

The SSR is a Continental RVDA rated for 25A.

The contactor with panel-mount switch is part #SD1-025-RR from [Automation Direct](http://www.automationdirect.com).

The larger square controller pictured is a cheap ramp/soak PID controller I found on eBay. The smaller one is also a PID controller (non-ramp/soak), also found on eBay, but is configured just as a temperature monitor. These controllers are sold under a lot of different names on eBay and elsewhere… if you see one that looks like one of these, it’s probably the same thing.

I found I had to modify the settings in both controllers to smooth out the temperature measurements, to account for a bit of noise from the blankets. 

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



### Schematics and Electrical Advice 
I don’t actually want to provide precise schematics or electrical advice here. It’s one of the few things I’m just not comfortable doing. If it’s not obvious how to build this controller from the description above and the few pictures here then you should consult either an electrician, or a friend who already has a lot of knowledge in this area. 


### PID Controller 
I use an Auber PID controller with the “ramp/soak” feature. The manuals are here: [[File:Auber SYL Part1.pdf|File:Auber SYL Part1.pdf]], [[File:Auber SYL Part2.pdf|File:Auber SYL Part2.pdf]]

Configuring these is a bit of a pain sometimes. Read the manual, and let it auto tune at least once with an old snowboard in the press under reasonable pressure. This will better simulate the thermal characteristics of your laminate and the auto-tune will do a better job.

For reference, here are the values for all parameters in my controller:

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


## Thermocouples 
 

{{< img src="images/Press_Thermo84.JPG" caption="_Thermocouples used on the Monkey Press._" >}}The thermocouples are from [Omega](http://www.omega.com), part #5SRTC-TT-K-36-36 for 5 type K thermocouples, and #RMJ-K-S for the connectors on the control box. The thermocouples are 36AWG (0.005”), and are therefore small enough to be placed directly on top of the heat blankets without harming the blanket. I place one with each of the blankets, with the sensor end in the center of the blanket. The thermocouple on the bottom is connected to the ramp/soak PID controller, while the one on the top is used simply to monitor the temperature differential between the two sides of the laminate.

The thermocouples are also connected with plugs which allows us to place the thermocouples in with the blankets before loading the laminate, and to easily replace thermocouples if they get damaged.

{{< gallery  caption="Thermocouples used on the Monkey Press" >}}
{{< gallery-item src="images/Press_Thermo70.JPG" caption="Thermocouples used on the Monkey Press." >}}
{{< gallery-item src="images/Press_Thermo74.JPG" caption="Thermocouples used on the Monkey Press." >}}
{{< gallery-item src="images/Press_Thermo76.JPG" caption="Thermocouples used on the Monkey Press." >}}
{{< gallery-item src="images/Press_Controller65.JPG" caption="The thermocouple connectors, from the inside, on the heat controller on the Monkey Press." >}}
{{< gallery-item src="images/Press_Controller68.JPG" caption="Thermocouple connectors on the heat controller on the Monkey Press." >}}
{{< /gallery >}}



## See Also 
- [Monkey Press Construction]({{< ref "MonkeyWiki/Equipment/Snowboard_press/Monkey_Press_Construction.md" >}})



