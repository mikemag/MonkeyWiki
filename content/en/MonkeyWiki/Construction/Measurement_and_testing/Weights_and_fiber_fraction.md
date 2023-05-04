---
dateFromWiki: "2019-02-12T01:38:39Z"
title: "Weights and fiber fraction"
aliases:
- /MonkeyWiki/Weights_and_fiber_fraction
- /MonkeyWiki/Weights_and_fiber_fraction/en
---
A number of questions invariably come up about the weight of a completed snowboard or ski. Does it have to be as heavy as it is? Is its weight reasonable? What’s the best way to try to save some weight? After you investigate these questions to some degree inevitably another arises: does the board contain a reasonable amount of epoxy?

To answer these questions you need to take some careful measurements along the way and apply a smidge of math.


## Weigh Everything 
Weigh everything that goes into a board before you laminate it. Some things are easy to measure, like the weight of the base and edges. Just toss them on a scale and see how many grams they weigh. You can do this for the core and inserts too. You can also do it for things that are extremely light when most of the material remains in the board. The VDS rubber is a great example of this: all of the rubber that goes into a reasonable sized snowboard weighs roughly 24g and more than half it typically stays in the board, so just toss it on a scale and don’t worry about what gets trimmed off in the end. The amount of error you can introduce via the VDS weight is miniscule.

But what about materials that you don’t shape to the exact size of the board, like the top sheet or the fiberglass? We typically oversize these pieces and trim the excess off later to account for minor alignment errors during layup. These are heavy, and often there’s a lot outside of the board to be trimmed off. If you just toss your top sheet on a scale you’ll overestimate its contribution to the final board weight.

For these, you need the area of your board. Any reasonable CAD program will be able to help you compute this very accurately. You can weigh a square meter of your fiberglass and top sheet material and then compute how much will be left in the board when it is trimmed out. 

Let’s take the last board I built with a plastic top sheet as an example. It is a powder board, 168cm long, 24.8cm at the waist, an 11m sidecut, and 3cm of taper nose-to-tail.  

- The easy things to weigh:
  - I weigh the base and edges together after I attach the edges: 668g.
  - VDS rubber: 24g.
  - Core, with sidewalls attached: 1409g.
  - Eight inserts for a single binding position (hey, the board is just for me!): 40g.

- The more annoying things to weigh:
  - The area of this board is 659.81 square inches, which is 0.42568302 square meters.
  - The 22oz fiberglass I use is 810.79g per square meter. So the glass that will remain in the board is 690.2791g for the two layers of glass. Do the math to convert 22oz per square yard to grams per square meter (or just put that into Bing) and you’ll see that my “22oz” glass is really almost 24oz. The data sheet for the [VectorPly E-TLX 2200](http://vectorply.com/wp-content/uploads/2015/06/E-TLX-22001.pdf) says it should be 23.55oz, but my measurement of a few cuts of glass yielded the numbers I have here.
  - The PBT top sheet I used on this board weighs 693.077778g per square meter, so the top sheet that will remain after I trim the board is 295.0314g.

So far we’re up to 3126.3105g. But that’s not everything that goes into a snowboard. What’s left is the epoxy. It’s easy to know how much gets mixed (for this board, 750g in total, way too much as you’ll see) but how do you know what remains in the board? We can weigh the board after it has been pressed and trimmed out, but before any processing that would change the weight of the heavy things above. Trimming the board out cuts off some VDS as I’ve already noted, but that’s minor. A base grind would change the weight of the base and edges by quite a lot though. 

So, simply weigh the board after you’ve trimmed it out reasonably well, then subtract everything else. What’s left is a very reasonable approximation of the weight of the epoxy which remains in the board. In this example, the final board weighed 3586g, so we estimate the epoxy weight at 459.6895g.


## Fiber Fraction 
The ratio of glass fibers to the epoxy surrounding them is called the "fiber fraction", and it's a good thing to measure for every board you build. You want to strive for a "high" fraction of fibers to epoxy. How high is high enough is debatable, but in applications like ours a ratio of 50% to 65% is reasonable. If you go too high you'll likely end up with dry areas of glass that are very weak, and if you go too low then you'll have too much epoxy without supporting fibers, which is also weak.

You can end up too low if you use way too much epoxy, or if you leave pools of epoxy during layup. You can end up too high if you over-press your boards, which can squeeze out more epoxy than you expect.

The 460g of epoxy we computed above is in the board above in various places: infused into the top and bottom glass layers, in the small pores of the base material and PBT top sheet, and in the pores of the wood core (which are surely deeper and larger than those of the plastics involved). If we assume that the amount of epoxy that has been pushed into these other materials is small then the vast majority of it must be mixed in the glass layers. If you look at a cross-section of a cut board this is a reasonable assumption.

Given this we can compute the fiber fraction of our glass layers, i.e., the fraction of these layers which are glass fibers. In this case, with 690.2791g of glass and 459.6895g the fiber fraction is 60.03%.

This is also called a "fiber volume ratio", or "fiber volume fraction", and the Wikipedia page [Fiber Volume Ratio](https://en.wikipedia.org/wiki/Fiber_volume_ratio) is a good place to start for further reading.

## Saving Weight 
So, where can you save weight in a ski or snowboard? The best place to start is by looking at where the current weight has come from. Here’s the consolidated breakdown of the board above:

- Core with sidewalls: 1409g (39.29%)
- Glass: 690g (19.25%)
- Base and edges: 668g (18.63%)
- Epoxy: 460g (12.82%)
- PBT top sheet: 295g (8.23%)
- Inserts (8): 40g (1.12%)
- VDS rubber: 24g (0.67%)

Some of these things you can’t change much, like the base and edges. In my case I did a full-wrap edge, so a partial edge would save some weight. I’ve never measured the weight of the edges alone, so I don’t have hard data about how much I could save by doing that, but I’d guess it would be a small percentage. 

I could try to ensure less epoxy remains in the board; however a fiber fraction of 60% is actually pretty reasonable already. Going much further would likely result in a resin-starved laminate. 

I could try to use a lighter top sheet material. The PBT on this board was 0.024” thick, and there is a 0.018” version. The thinner PBT is right about 25% lighter, so I could shave off a whopping 73g or so… that’s about the same as removing a few inserts from the board, which I already did in this case. (Having had some experience with the thinner PBT I’ll gladly pay the extra 73g for the thicker top sheet!)

The best places to try to save weight are really in the core and the glass. Note that lighter glass will also support less epoxy, so the epoxy weight will go down as the glass weight goes down. I could use lighter glass and add in carbon or Kevlar to make up the difference. I have some [E-TLX 1900](http://vectorply.com/wp-content/uploads/2015/06/E-TLX-19001.pdf) which is roughly 669g per square meter, which would make a glass weight of about 569g, a savings of about 18%. If we assume (without evidence, but it seems reasonable) that the epoxy weight goes down by 18% too then I’d drop the final board weight by about 204g, or about 5.6%. 

Of course I’ve just guessed as the epoxy savings, and I haven’t accounted for the extra weight of the carbon or Kevlar I’d use to make up for the stiffness, but it’s a reasonable ballpark estimate that is useful to help decide if a test is worth it or not. You might make other reasonable estimates using data about different wood weights, a projection of the weight of a thinner core, etc. 


## Other Variables 
You may note above that I did leave out one part of the snowboard: the nose and tail spacers. I don’t have those measurements for the board I used in the example above, but the weight of these is typically quite small in my construction. They should be included, though, to be complete.

I’ve also used an example where the top sheet is plastic, i.e., it absorbs a minimal amount of epoxy. This allows me to assume that the vast majority of epoxy is in the glass, and thus compute a reasonable fiber fraction. However, I tend to use wood veneer top sheets now, which absorb a lot of epoxy and also have some epoxy on the top. This obviously makes the fiber fraction computation above invalid unless we take into account what fraction of the epoxy is in the top sheet. And I haven’t really found a good way to measure that yet. 



