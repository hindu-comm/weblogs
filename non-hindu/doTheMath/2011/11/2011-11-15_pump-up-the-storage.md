+++
title = "Pump Up the Storage"
full_title = "Pump Up the Storage"
upstream_url = "https://dothemath.ucsd.edu/2011/11/pump-up-the-storage/"
date = "2011-11-15"

+++
Source: [here](https://dothemath.ucsd.edu/2011/11/pump-up-the-storage/).

Pump Up the Storage

[![](https://dothemath.ucsd.edu/wp-content/uploads/2011/11/Racoomtn.jpg "Racoomtn")](https://dothemath.ucsd.edu/wp-content/uploads/2011/11/Racoomtn.jpg)If we adopt solar and wind as major components of our energy infrastructure as we are weaned from fossil fuels, we have to solve the energy storage problem in a big way. An [earlier post](https://dothemath.ucsd.edu/2011/08/nation-sized-battery/ "Do the Math: Nation Sized Battery") demonstrated that we do not likely possess enough materials in the world to simply build giant lead-acid (or nickel-based or lithium-based) batteries to do the job. Comments frequently pointed to pumped hydro storage as a far more sensible answer. Indeed, pumped storage is currently the dominant—and nearly only—grid-scale storage solution out there. Here, we will take a peek at pumped hydro and evaluate what it can do for us.

## Gravitational Storage Basics

When you lift an object, you must supply a *force* to counter gravity (the weight of the object) and apply this force over the *height* through which you lift the object. The weight of an object—and therefore the force applied to lift it—is its mass times the acceleration due to gravity (application of Newton’s *F*=*ma*; in this case, *mg*, where *g* is the gravitational acceleration, or about 10m/s²). Work is defined as force times distance, so lifting an object of mass *m* a height *h* results in an energy (work) investment of *mgh*. This is called *gravitational potential energy*.

It is called a potential energy because it is possible to put the invested energy on a shelf—literally, in fact—to be accessed later. A dropped brick that had previously been given gravitational potential energy can do useful work, like driving a nail into a piece of wood (huge force times small distance = same work). The stored energy does not degrade one iota over time: in that sense it represents perfect long-term storage.

The idea for pumped hydro storage is that we can pump a mass of water up into a reservoir (shelf), and later retrieve this energy at will—barring evaporative loss. Pumps and turbines (often implemented as the same physical unit, actually) can be something like 90% efficient, so the round-trip storage comes at only modest cost.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2011/11/raccoon_mtn.jpg "raccoon_mtn")](https://dothemath.ucsd.edu/wp-content/uploads/2011/11/raccoon_mtn.jpg)

Raccoon Mountain pumped storage concept.

The main problem with gravitational storage is that it is **incredibly** weak compared to chemical, compressed air, or flywheel techniques (see the [post on home energy storage options](https://dothemath.ucsd.edu/2011/09/got-storage-how-hard-can-it-be/ "Do the Math: Got Storage?")). For example, to get the amount of energy stored in a single AA battery, we would have to lift 100kg (220lb) 10m (33ft) to match it. To match the energy contained in a gallon of gasoline, we would have to lift 13 tons of water (3500 gallons) one kilometer high (3,280 feet). It is clear that the energy density of gravitational storage is severely disadvantaged.

What we lack in energy density, we make up in volume. Lakes of water behind dams, for instance represent substantial storage.

## Flow Power

When water is let out from the bottom of a dam, it carries energy as if it had been “shelved” at the surface of the lake behind the dam. How does water at the bottom “know” how high the lake surface is? Pressure—which is proportional to the weight of water overhead. So let’s take a cubic meter of water, at a mass of 1000kg, and send it through the turbine. The *mgh* energy in the cube of water for a 100m high dam is (1000kg)(10m/s²)(100m) = 10⁶J, or one megajoule.

If this 100m high dam only has one cubic meter per second flowing through, it would produce 1MJ/sec, or 1MW. I am ignoring the roughly 90% efficiency of hydroelectric turbines to keep numbers tidy and approximate. More typically, flow rates are measured in the 1000m³/s range, so that our 100m dam would produce 1GW at this scale.

So the recipe is simple for understanding a hydroelectric dam: multiply the height of water behind the dam (in meters) by ten-thousand times the flow rate in cubic meters per second to get the power in Watts.

## We Need *How* Much Storage?

The U.S. has a power diet of about 3×10¹²W, or 3TW. Two-thirds of this feeds heat engines (power plants, cars, etc.), at an average efficiency of 30%, delivering 0.6TW of useful work in the bargain. The other 1TW is direct heat (lots of this in industrial process heat), and electricity from nuclear and hydro sources. Imagining that we replace our heat engines with direct electricity and electrified transport, we need something like 2TW of total power, accounting for some inefficiency. If you’re happier with half this, fine—a factor of two will not qualitatively change the giant scale of the problem.

The next question is: how long do we need our storage to last? In the [Nation Sized Battery post](https://dothemath.ucsd.edu/2011/08/nation-sized-battery/ "Do the Math: Nation Sized Battery"), I argued that we need 7 days of storage for it to be invisible to the end-user. That is, if Americans insist on not changing any of their habits, and having *zero* storage-crunch outages on a decade timescale (read about the total shutdown of San Diego in a recent [county-wide power outage](https://dothemath.ucsd.edu/2011/09/power-out-people-out/ "Do the Math: Power Out, People Out")), then 7 days is probably not far from the mark. I got flak for this choice, but I use it again here because A) it is not all that unreasonable, B) it allows side-by-side comparison to the national battery calculation, and C) you’ll see it does not make or break the case: even one day of storage is super-hard. Divide all my scale numbers by 7 if you wish that I had used one day of storage, for instance.

Note that 7 days of storage does not literally mean that we are prepared to experience 7 days with zero input from the renewable infrastructure. Operating at 30% of the break-even amount over a period of 10 days also leaves the system with a 7-day energy deficit, for instance. This circumstance is not too difficult to imagine: a cloudy winter week over the southwest while the wind speed over the country is half its average value (means eight times less power) over the same period.

So 2TW for 7 days means 336 billion kWh of storage capability.

## First-Blush Pumped Hydro

What scale would this amount of storage require if we did a pumped-hydro scheme? One immediate scale reference is to note that we have 78GW of installed hydroelectric power in the U.S., amounting to 4% of the target 2TW demand. Our traditional hydro capacity could not be scaled up by even a factor of two—since the premier river sites have been plucked already.

What about potential pumped hydro installations: not on current rivers, but in the mountains where we could wall off a high valley and fill it with water?

I say mountains because we need a significant height differential for pumped storage to make much sense. We won’t see pumped storage in the plains. The horizontal distance must also be minimized, so we need sharp relief—meaning mountains.

To first approximation, we can imagine mountains as lumps. They have pointy tops that point up. They are distinctly not very bowl-like. Upside-down bowls, maybe. They do, however, often produce hollows (“hollers” in some parts) ringed by arms/ridges of the mountain. Walling off the opening to the hollow allows us to fill this useless void with water. The pikas and marmots can just learn how to swim! We also need another equal-volume body of water below, to catch the water in the storage cycle.

I can’t say that I’ve studied the topography of our lands to see how many places are amenable to these grand-scale engineering marvels. I may be oblivious to the widespread existence of natural bowls perched on the edges of cliffs. Whatever the case, the 22GW of pumped storage we *do* have at present presumably picked the primo spots. Instead of fussing over topographical maps, I am using the simple “hollow” model informed by my time in the mountains and staring at relief maps.

In any case, let’s not allow these details to prevent us from doing some math! Let’s say our average candidate hollow allows a 500m high wall (1650ft) on one end, and another few-hundred-meter wall lower down for the lower reservoir (the hollow is wider here—maybe even a vale by now—so the same volume is accommodated by less depth and more area).

[![](https://dothemath.ucsd.edu/wp-content/uploads/2011/11/filled-hollow-300x277.jpg "filled-hollow")](https://dothemath.ucsd.edu/wp-content/uploads/2011/11/filled-hollow.jpg)

Simple model for filling a hollow with water to height, h.

My model for the hollow will have a V-shaped profile, with sides at a 20% slope and the hollow floor running up at a 10% slope. Thus the 500-m-high dam wall is 5km across at the top, and the lake extends 5km back in a triangle. This geometry produces a reservoir 2 cubic kilometers in volume. Considering the tapering shape, the stored gravitational potential energy is 2 billion kWh. We just need to build 170 of these things. Never-mind the fact that we have never built a wall of such proportions. Or the fact that the largest pumped storage facility to date stores 0.034 billion kWh—60 times less capacity.

But let’s continue to play the game: If we indeed demanded 2TW of power from about 170 pumped-hydro stations, we’re talking 12GW of production capability each. This is significantly larger than the biggest hydroelectric installation in the U.S. (Grand Coulee, at 6.8GW). Times 170.

Perhaps I was too ambitious in starting with a 500m dam height. A greater number of smaller reservoirs would allow more sensible power stations and perhaps avoid turning the seven wonders of the world into the 177 wonders of the world (with lots of redundancy).

The energy stored in the walled-off-hollow scales like the reservoir height to the **fourth** power! So if we drop to 250m height (still impressive to me, being taller than Hoover Dam), we need 16 times as many installations (over 2,500), each with 600MW capacity. For scale, we currently have 24 hydroelectric installations in the U.S. rated at \> 600MW capacity.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2011/11/Hoover_dam_from_air.jpg "Hoover_dam_from_air")](https://dothemath.ucsd.edu/wp-content/uploads/2011/11/Hoover_dam_from_air.jpg)

Hoover Dam: 221 m high; 2.0 GW power; 2.5 million cubic meters of concrete.

I think at this point, you can see why quibbling about the need for 1TW vs. 2TW or requiring 2 days of storage vs. 7 days is not going break the logjam of a hard problem. Even accomplishing 1% of the requirement I have laid out would be super-impressive.

## All That Concrete!

These dam walls will require a lot of concrete. A survey of dam construction suggests that the base thickness is approximately 65–90% the height of the dam. Picking 75% and tapering to a cusp, our foregoing geometry requires a concrete volume 25% larger than *h*³, where *h* is the dam height. For our 250m set of dams, we need 19 million cubic meters of concrete apiece. Each dam then contains as much concrete as exists in the Three Gorges and Grand Coulee dams combined! And this is the “**small**” version of our dams. And we need over 2,500 of them. I’m just sayin’.

At an energy cost of 2.5GJ per ton of concrete, and a density of 2.4 tons per cubic meter, we end up needing 32 billion kWh of energy per dam, and 90 trillion kWh total. This over 250 times the amount of energy impounded by the dams, and represents three years of the *total* energy appetite of the U.S. today.

Note that I’m totally ignoring requirements for the lower reservoir.

## Ample Room for Water Skiing

I’m keen now to understand what this looks like relative to our landscape. How much area will all these lakes take?

In the 500m dam-height model, the area of the upper reservoir is 12.5 square kilometers. Times 170 reservoirs is 2125 square kilometers. In the 250m model, we have 3 square kilometers per reservoir, or 8500km² for the whole set. So the total necessary area scales like the inverse square of the characteristic dam height.

We also need to add the area for the lower reservoir. Since the terrain is likely less sloped lower down, let’s assume that the lower reservoir surface area is twice as big as the upper reservoir, so now we have about 25,000km² in new lake area (both reservoirs are not full at once, but this land is no place to build a mall).

We get an area equivalent to 160km on a side. This is the same area as Lake Erie (and more than its volume). Add another Great Lake’s worth of space to the map. No trivial affair. I haven’t asked yet where we get the water for this endeavor. Good thing water shortages are of no concern on this planet.

It is worth also comparing to the area of a photovoltaic system providing the 2TW of average power. Such performance would require 10TW of installed capacity (accounting for day/night, sun angle, weather). At 15% efficiency and 1kW/m² of incident peak solar energy, we need about 65,000 square kilometers of panel—roughly comparable scales. Keep in mind that the water area is based on over 2,500 gigantic 250m dams, each taller than Hoover Dam, and containing 8 times as much concrete. For smaller, more realistic projects, the area of water could easily exceed the solar panel area. Converting land to pumped storage carries **far** greater environmental impact than converting to a solar farm, so that storage concerns dominate. Wind takes substantially more land (about 50 times) than solar, so the pumped storage lakes would not rival the area dedicated to wind farms.

## Variations and Scalings

We’ve relied on loads of assumptions in our exploration of the potential for pumped storage. It is easy to lose track of the choices and the impacts they have. Is the 20% slope on the sides important? How do things scale with the dam height?

In a general analysis, it works out that the number of dams needed is proportional to the total energy storage required times the side-slope of the hollow (in %, e.g.) times the slope of the hollow floor divided by the height of the dam to the fourth power. But interestingly, the *total* volume (and therefore energy) required for concrete only depends on the hollow floor slope divided by the height of the dam.

The result is that one 500m dam replaces 16 250m dams, while taking only half the total amount of concrete. Scaling therefore favors the big projects over the dinky. Of course the number of acceptable sites for the mega-projects may be too slim, while the pressure to find 16 times as many lesser sites is no walk in the park.

Total lake area scales as the inverse of side slope and the inverse square of the dam height. So, naturally, broader shallower lakes will be more evident from space. Total water volume needed just follows the inverse height of the dams.

Of course any real implementation would have a wide variety of dam heights in the set. I treat them all as the same to establish baseline numbers. Strict averages do not work due to scalings that are not linear, but this at least gives us an idea. An analysis where I allowed a distribution of dam heights would just waste my time and yours.

A common trick is to build a large feed-tube from the bottom of the upper dam to a turbine/pump located far below. This will not be easy to accomplish everywhere, but an additional 500m drop improves the 250m dam by a factor of 3.6, and a 500m dam by a factor of 2.3. Doing this reduces the number of such projects needed by a similar factor (still large numbers). But don’t get too excited by this option: we still need a place to put the lower reservoir. If you give up too much height, you run out of natural walls and vertical relief, demanding a very large flooded area to catch the water.

## Comparison to Real Examples

[![](https://dothemath.ucsd.edu/wp-content/uploads/2011/11/ludington.jpg "ludington")](https://dothemath.ucsd.edu/wp-content/uploads/2011/11/ludington.jpg)

Ludington pumped storage: 110 meters; 1.87 GW; 15 hours; 27 million kWh.

Enough fooling around. Let’s compare this fantasyland to something real. We have 22GW worth of pumped storage in the U.S., which is about 1% of my 2TW goal. But they tend to be sprinters rather than marathon runners (typically about 12 hour run-time at capacity), so the actual storage falls short of what we need by a factor of 1500 or so. Think we only need one day of storage? Still a factor of 200 off.

The largest pumped hydro installation in the U.S. (in terms of energy, not power) is at Raccoon Mountain, in Tennessee. I owe much of my air-conditioned comfort as a kid to this facility. Sitting atop a mountain, the reservoir unloads to the Tennessee River 300m below (technically Nickajack reservoir). The installed capacity is 1.532GW, implying a flow rate of 575m³/s. The upper reservoir provides an unusually long 22 hours of service, so that the volume of useful water is 45×10⁶m³, and the energy storage is 34 million kWh. The surface area of the lake is 2.16 square kilometers, resulting in an average depth of 21m. The (earthen) dam is 70m high and 1800m long, from which I calculate a dam volume of about 10⁶m³—about half that of Hoover Dam.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2011/11/Racoomtn.jpg "Racoomtn")](https://dothemath.ucsd.edu/wp-content/uploads/2011/11/Racoomtn.jpg)

Raccoon Mountain: 302 m; 1.53 GW; 22 hours; 34 million kWh.

What can these *real* numbers tell me about my simplified geometry and the guesses that went in? The main difference is that the Raccoon Mountain geometry has much gentler slopes: something like 3–5% up the “hollow,” and about 8% up the sides. We would need 10,000 Raccoon Mountains to meet my baseline energy capacity—although we could scale back on power per unit. This becomes 50,000 if you can’t use the trick of dumping to a reservoir far below. For 10,000 replicas of Raccoon Mountain, the total lake area (including the area of the lake below) is about three times the size of Lake Erie (Lake Superior-size). The dam volume is about one-fifth what we had before, becoming comparable to the extent that the deep-drop trick is not employed. The total volume of water sequestered is comparable for the two cases (because this is just *mgh*, and our baseline had *h*=250m, while Raccoon Mountain uses *h*=300m).

## Re-purposing the Hydroelectric Infrastructure

If at any point in this development you thought, “wait a minute: why build all these giant dams in the mountains when we’ve got large lakes and dams already, with water already delivered to the doorstep?!” then you are not alone: I wondered the same thing.

The first note is that our installed hydroelectric capacity in the U.S. is 78GW; a factor of 25 short of the necessary full-scale capacity.

The next note is that water flow is not always available to realize the capacity of the installed power. For instance, the U.S. hydroelectric plants produce about 270 billion kWh each year, which is only 40% what would be delivered if all dams ran at 100% capacity all year round. For example, Hoover Dam has an annual production of 4.2 billion kWh, which is 23% of what the 2.08GW installed capacity could churn out in a year. Even the mighty Columbia fluctuates enough that the Grand Coulee dam only realizes 35% of its capacity.

These points are relevant because in order to achieve the necessary 2TW power output, we need to multiply the hydroelectric capacity **flow** by a factor of 25, or a factor of 60 greater than the average flow. We might predict a few erosion problems here and there.

## Let’s Do It Anyway!

Let’s not be wimps. Let’s just beef up our hydroelectric capacity at the developed sites and ask whether we have enough energy storage behind the dams. One way to look at this is to figure out how much power would be generated if all lakes impounded behind hydroelectric plants dropped by one meter over a 24 hour period. Computing this for each dam based on each lake’s surface area yields a total of 170GW of power. We need more than this. Our demand for electricity alone in this country averages 450GW, and of course we’re shooting for about four times this to cover all our energy demands.

The upshot is that getting sufficient energy out of the current infrastructure would require draining each reservoir by a little more than 10 meters per day. But as the lakes drain, the surface area shrinks, so that my ten meter estimate is too low. Additionally, many dams will tap out once we get beyond the 10 meter range, and the fact that the energy delivered drops as the height of water drops reduces the capacity further. Using the volume reported behind each dam, I find that draining all reservoirs over a 7-day period delivers a power of 500GW. Of course dams are often serial along a river, so we get to re-use water along the way. This will give us a factor of several, and put us close to our need.

But let’s not forget that our scheme here involves emptying all the lakes and rivers of water, and at a rate far in excess of what the channels are accustomed to carrying. It’s an extreme maneuver.

## Drain the Great Lakes

While we’re having “fun,” let’s see what we could get out of the Great Lakes. The upper four lakes are all at essentially the same elevation (6 meter drop from Superior to Erie), while there is a 99m drop between Erie and Ontario. We call this Niagra Falls, although only half the drop is developed across the falls proper.

If we drained one meter from every upper lake, we would get 54 billion kWh of energy: about a sixth of the target capacity. If performed over seven days, the flow would be 375,000 cubic meters per second, or 125 times the normal flow over the falls. Now I’d pay to see that! But I would first want to visit every town along the St. Lawrence River one last time.

If we tried to trap the water in Lake Ontario so-as to spare those downstream of the wrath, its level would rise 12 meters (39 feet). Watch out Toronto & Rochester!

The pipe delivering this water to the turbines would have to be over 125 meters in diameter (or 160 tubes each 10m in diameter) to limit the velocity of the water through the pipes/turbines to below freeway speeds! What fun.

## Am I Insane?

Why do I always do this: pick a challenge and show how ridiculous it is to solve the problem by a monolithic approach? Maybe *I’m* the one being ridiculous!

This tendency is a reflection of my quest to understand how we might face the tremendous energy challenges ahead. The first step is always to assess the *potential* of a solution relative to the full-scale demand. If it wipes the floor with an excess capacity, then great: it is inarguably a no-brainer go-to solution. If it comes up short, that’s very informative too.

Yes, a diverse portfolio of a half-dozen inadequate solutions *may* be able to add to an adequate solution. But a half-dozen **woefully inadequate** solutions cannot pull off the same stunt. So far, my quest keeps turning up the woefully inadequate type. The scale of fossil fuel replacement is **so daunting** that we very quickly get into trouble when putting numbers to proposed solutions.

A common reaction to the Nation Sized Battery post—especially on the [Oil Drum Forum](http://www.theoildrum.com/node/8237 "The Oil Drum: A Nation-Sized Battery")—was that I was being silly by considering a full-scale lead-acid battery, and that pumped storage was such a more obvious solution to the problem. It was not obvious to me, but I had not yet done the math. The fact that just one of the “small” dams considered here has as much concrete as the Three Gorges and Grand Coulee dams combined is humbling. I would be impressed if we made one. I would be astounded if we made 25. And this just gets us to 1% of our need (or 7% if you still bristle at a 7-day battery).

It is clear enough that pumped storage exists and works quite well in certain locations. But demonstration does not imply scalability, and scaling the existing installations did not deliver a radically different answer (in fact, demanding *more* installations). The enormous scale I calculate means simple factors of two or even ten here and there do not change the overall flavor of the conclusion.

Let’s be clear that I am not making any claim that large scale storage at the level we need is *impossible*. But it’s far more daunting than almost anyone realizes. It’s not a matter of “just” building up when the time comes. We could easily find ourselves ill-prepared and suffering insufficient energy supplies, intermittency, and a long, slow economic slide because we collectively did not anticipate the scale of the challenges ahead.

*Acknowledgment: Thomas Tu contributed research on hydroelectric installations, consolidating capacity, height, and capacity factors for dams, along with surface areas and volumes of impounded lakes.*

Hits: 20261

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2011%2F11%2Fpump-up-the-storage%2F&linkname=Pump%20Up%20the%20Storage "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2011%2F11%2Fpump-up-the-storage%2F&linkname=Pump%20Up%20the%20Storage "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2011%2F11%2Fpump-up-the-storage%2F&linkname=Pump%20Up%20the%20Storage "Email")[](https://www.addtoany.com/share)
