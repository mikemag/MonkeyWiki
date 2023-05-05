---
dateFromWiki: "2019-02-03T02:38:18Z"
title: "Do you need a CNC machine?"
aliases:
- /MonkeyWiki/Do_you_need_a_CNC_machine
- /MonkeyWiki/Do_you_need_a_CNC_machine/en
- /MonkeyWiki/Do_you_need_a_CNC_machine?
- /MonkeyWiki/Do_you_need_a_CNC_machine?/en
weight: 2
---
A lot of people see CNC machines and think they will allow them to do something faster, more accurately, or have it do something they can’t do by hand. These are wonderful goals, and they are achievable, but like all things in life there are tradeoffs.
 
First, I’ll say flat out that there’s a big difference between owning a CNC machine, and programming and running a CNC machine. It sounds simple, but lots and lots of people fall into this trap. The machine isn’t magic. It won’t know anything you don’t know. It’s up to you to decide how to create your part, and then to program and test the machine. Sometimes it's much harder and more time consuming to get a CNC machine to do something than it is to do it by hand.
 
First, consider carefully whether or not a CNC machine will be able to cut the parts you want to make. A 3-axis CNC machine moves a spinning cutter in 3 dimensions while holding the cutter perpendicular to the work surface. Can you make your part with that, or do you need to tilt the cutter? (5-axis machines exist which allow tilting, but they are significantly more expensive.) 

Will you be able to make your part by just cutting one side, or will you need to turn it over? If so, how will you ensure accurate placement of the part when you turn it? How will you hold the part down during the machining process? Can you clamp, screw, or glue the part to the table, or do you need a vacuum table? Do you need multiple cutters to create the part, or just one?
 
Next, consider how you will program the machine. The first step is typically to draw the part in a Computer Aided Design (CAD) program. After this is complete, you need to create tool paths that specify how the machine moves the cutter in order to create the part. This is called Computer Aided Machining, or CAM, which is why you often hear the term CAD/CAM. 

It is extremely rare that a part you create in a CAD program can be automatically converted by a CAM program into tool paths that run a CNC machine. It typically requires someone with machining experience. Their experience with cutters and materials allows them to take into account the work holding, the capabilities of the cutter, and the order in which the cuts should be made. Keeping these things in mind, they can carefully guide the CAM program to construct the correct tool paths. 

This can be a surprisingly time consuming part of the process, and it is often error prone. A mistake in programming here can result in real damage to the machine. The machine (and its cutter) doesn’t know the difference between your raw material, a clamp, or even its own frame. Additionally, good CAM software usually costs a few thousand dollars.
 
Finally, consider whether or not you actually need a robot to cut the part for you. There are three primary advantages to using a CNC machine: accuracy, automation, and repetition. If you need twenty of something, then taking the few hours to program and test the machine may make a lot of sense. If you need one of something, then the only advantages the CNC machine brings are accuracy and automation. Do you need the accuracy? If not, then a CNC machine is likely overkill. Is the part you want to make so intricate that it would take hours for you to make by hand? If so, then it may be reasonable to take a few hours programming it, then let the machine take four more to do the work while you do something more productive.
 
There are a lot of factors to consider. Running a CNC machine really involves combining your normal craft (i.e., woodworking) with CAD and CAM, and for a time it will require an equal investment in each.
 
CNC machines are really great for lots of things. I use mine for the following:
1. Cutting snowboard cores. Here accuracy is king. The effort to program the machine is completely worth it because, honestly, you just can’t get the accuracy you need doing this by hand, even with templates to help out.
1. Cutting mold parts. These are simple shapes, usually cut out of 3/4″ MDF, but I usually need twenty-one of each one. It's a big win to take the time to make a program to cut twenty-one of these out of a sheet of MDF while I do something else in the shop.
1. Creating table saw zero-clearance insert plates. I make these out of nice Baltic birch plywood usually 4-6 at a time. I spent an hour measuring the plate that came with my table saw and tweaking the program. Now I can make more of these disposable items anytime I want. I can have a few more ready to go in about twenty minutes.
1. Complicated one-off projects, like ornate wall brackets, templates for cutting other shapes, etc. Again, these end up being worth it due to the complexity of the shape. I usually start these in a CAD program anyway, and if they’re two dimensional, then it’s usually reasonable to convert these to a few simple tool paths and let the machine do the cutting for me.



