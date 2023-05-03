---
date: "2019-03-23T20:06:27Z"
title: "Pneumatic Pressing"
aliases:
- /MonkeyWiki/Pneumatic_Pressing
- /MonkeyWiki/Pneumatic_Pressing/en
---
# Raw Notes
This is a temporary page containing raw, unedited notes on this subject. This page and the information here is incomplete, and may be inaccurate. 

- Press prep, precheck, etc.
- Compressor full and ready
- Mold configuration and alignment. This may warrant its own page.
- Thermocouple placement, testing of heat system, reset heat system.
- Talc for the blankets
- Setup for easy insertion
- Alignment during insertion.
- Initial pressure and verification.
- Full pressure. What pressure and why. Why more isn't better.
- Heat on and ramp, soak, ramp down, total time of each.
- Maintaining even heat top to bottom during ramp up.
- Catching resin overflow if you used too much.
- When to remove it. I remove it after about 30min after the soak time is over, because I'm impatient. Some people pull it out right away with no cooling. Some people leave it in overnight to completely cool before removing it. So what's right?

# Old notes on pressing, also raw

Pressing process

Overview of what the press is, what it is used for, how to operate it, etc. Essentially, the process of using the press to build a board: heating evenly, pressure, time, cooling, etc.

I press the average width board at right around 50psi. This presses the laminate completely into the mold, and results in good squeeze out without removing too much resin. I compute the fiber fraction of every board I build and carefully track this to ensure I’m getting the ratio of glass to resin we’re after. For especially narrow boards I drop the pressure proportionally. Pneumatic presses are capable of amazing pressures, but too much pressure is just as bad as too little. Too much pressure results in a dry laminate that is weak and prone to delamination.

The press heats both the top and bottom of the laminate to 175F with two 2,083 watt heat blankets that provide direct, even, controlled heat to the board to properly cure the epoxy. The combination of pressure and heat results in a very flat board on top and bottom, appropriate squeeze out of excess epoxy, and perfectly consolidated fiberglass layers.

The heater control has one PID controller with ramp/soak for controlling the heat of both blankets. Temperature is measured below the center of the board. It also has a second temperature sensor to monitor the heat transfer in other locations. It’s helpful to see the lag between the heat on the bottom and on the top of the board during pressing.

I ramp the heat up from room temperature to 175F slowly, then hold the heat steady for a one hour cure under pressure. The laminate is cooled slowly down to about 145F, over the course of 30 min, before being removed from the mold. The laminate is the allowed to rest for two days before first flex to allow the epoxy to continue to cure undisturbed.




