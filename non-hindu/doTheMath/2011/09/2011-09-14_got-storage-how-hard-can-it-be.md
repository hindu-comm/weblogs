+++
title = "Got Storage? How Hard"
full_title = "Got Storage? How Hard Can it Be?"
upstream_url = "https://dothemath.ucsd.edu/2011/09/got-storage-how-hard-can-it-be/"
date = "2011-09-14"

+++
Source: [here](https://dothemath.ucsd.edu/2011/09/got-storage-how-hard-can-it-be/).

Got Storage? How Hard Can it Be?

The recent city-wide power outage in San Diego made me appreciate my small off-grid photovoltaic system using four golf-cart batteries to store energy for use at night. Unlike most San Diegans, I did not immediately eat the ice cream in my freezer, which trucked along under stored solar energy just like it does every night. Energy storage becomes more important as we transition away from fossil fuels—already its own energy storage medium—to more intermittent sources. But besides batteries—which offer a limited number of cycles and for some types require monthly maintenance—what other non-fossil in-home energy storage alternatives might we consider, and how much energy might we expect to store in each case? We will look at gravitational storage, flywheels, compressed air, and hydrogen fuel cells as possible options. Some might even cost less than \$100,000 to implement in your home.

## Setting the Scale

We should first establish a meaningful scale and appropriate units for energy storage. Any household will use energy at a certain average *rate*, or [power](https://dothemath.ucsd.edu/useful-energy-relations/#power). The average American household (of which there are about 115 million) uses 30[kWh](https://dothemath.ucsd.edu/useful-energy-relations/#kilowatt-hour) per day of electricity—equivalent to 1.25 kW average power. Additionally, the average American household uses 35kWh of natural gas energy per day, generally for heating applications (natural gas is usually billed per Therm, which is 29.3kWh).

Substantial variation can exist in these numbers in any given house. For example, my wife and I use an average of 10kWh/day in our house for electrical and natural gas energy combined, in roughly equal measure. Storage requirements will therefore vary according to usage. Conversely, the same storage will last longer in some houses compared to others. We will restrict our attention in this post to storing enough energy to cover electrical usage only.

For off-grid applications, the rule of thumb is to have enough storage for three days of zero input. Not to be taken literally, this is effectively the same as 4 consecutive days at 25% of break-even, or 6 days at 50% of break-even—in each case running a deficit of 3 days. The spirit of this post is to establish storage independence within a home, rather than rely on external infrastructure to do it for you. To the extent that you want to rely on the outside world to provide for you, the targets established here can be scaled down accordingly. The ideas explored here are plausible options that might come to mind first in a “why couldn’t we just…” sense.

Since we are trying to fit a storage solution into a home, let’s allocate a fixed volume for each of the solutions. A reasonable choice would be one bedroom-sized space. Let’s say it’s 3m on a side, and 2.5m tall (about 10 by 10 feet, 8 feet tall). The total volume envelope is then 22.5m³.

## Battery Reference

Since we are comparing to batteries, let’s establish a reference case. Batteries are characterized by how many amp-hours they can generate. A 100A-h battery can put out 1A of current for 100 hours, or 10A for 10 hours, for instance (though the rating typically declines for high currents). The electrical power exerted by the battery is just the current times the voltage. So a 12V battery putting out 2A is delivering 12×2 = 24W of power. If rated at 100A-h, this battery would go for (100 A-h)/(2 A) = 50 hours, producing (24 W)×(50 h) = 1200W-h, or 1.2kWh of energy. A rechargeable AA battery holds about 2300mA-h (2.3A-h) of charge, which at 1.3V turns into 3W-h of energy.

[![Four 150 A-h 12-V golf-cart batteries](https://dothemath.ucsd.edu/wp-content/uploads/2011/09/PV-batteries.jpg "PV-batteries")](https://dothemath.ucsd.edu/wp-content/uploads/2011/09/PV-batteries.jpg)

Four golf-cart batteries used in my off-grid home PV system. Each is 12V, 150A-h, thus 1.8kWh of storage apiece.

As detailed in the [Nation Sized Battery post](https://dothemath.ucsd.edu/2011/08/nation-sized-battery/ "Nation Sized Battery Do the Math post"), large lead-acid batteries occupy 13 liters (0.013m³) of volume, and 25kg of mass per kWh of storage.

Practically speaking, we would not fill 100% of a bedroom’s volume with batteries, because we need physical access for maintenance/replacement. If we filled 10m³ of the available volume with actual battery, we would end up with about 750kWh of storage, and a mass of 19 tons (better reinforce the floor!). This bank would provide about 25 days of storage for the average American electricity demand.

The lesson is that batteries are a **can-do** solution in terms of fitting into a house envelope. A more practical few-days of storage is that much easier. Although at approximately \$150 per kWh of storage, three days of storage for the average American house will cost about \$15,000 to cover electricity demand, with the cost recurring every five years or so. But let’s not worry our pretty little heads over mere economic concerns at the moment.

Since lead-acid batteries require monthly equalization and topping-off with water, have a limited number of deep cycles (500–1000 typically), and do not tolerate extended periods at low charge, it would be nice to identify better options.

## Gravitational Storage

Hydroelectric dams and pumped storage solutions rely on the gravitational energy stored in an elevated mass. What could we do in a home environment? Could we get much out of our personal pumped storage tank on-site?

Let’s start small by considering the 3W-h of energy stored in a AA battery, as computed above. One kWh of energy is 3.6×10⁶J of energy, so our AA battery stores 10,800J of energy. A mass of *m* kilograms, hoisted *h* meters high against gravity at *g*≈10m/s² corresponds to *E = mgh* Joules of energy. If we were willing to hoist a mass 3m high, how much mass would we need to replace the AA battery? Have a guess? The answer is 360kg, or about 800lb. A battery the size of your pinky finger beats the proverbial 800lb gorilla lifted onto your roof!

The lesson is that gravitational storage is **incredibly weak**. A volume of water the size of our bedroom raised even 10m above our home in a precarious threat to the neighbors would store 0.625kWh. That’s enough for 30 minutes of typical household electricity consumption. You’ll forgive me if I ignore efficiency losses. It’s not even worth the effort. [It’s *over*](http://www.youtube.com/watch?v=YlGqN3AKOsA "YouTube clip from Portlandia: It's OVER!").

## Flywheel Storage

Let’s put a massive spinning disk in our energy-storage “bedroom.” These might end up being popular in Malibu, as the gyroscopic stability inherent in the spun-up system could be very handy in a mudslide—keeping the house level on its way down the hill, mimicking the surfers it’s been watching all these years.

The kinetic energy stored in the rotation of a cylindrical-shaped solid disk is ¼*mv*², where *m* is the mass of the spinning cylinder and *v* is the velocity at the outer edge. For a fixed mass, it is better to put as much of the mass as possible on the outer edge, in a hollow cylinder (supported by spokes, for instance), which can deliver a factor of two more energy per mass. But in the case where space, not mass, is the constraint, the solid disk has more mass than the hollow version would, making it a net win to just go solid.

How big do we make this thing? Let’s give it a diameter of 2.5m and a height of 2m (need room for mounting, and surrounding container/structure) yielding a 10m³ volume. At the density of steel—about 8× that of water—we get 80 tons (now even *more* important to reinforce that floor!).

How fast do we spin it up? Let’s pick the speed of sound—345m/s—and see where that puts us. Go big, or go home! We get 2.4GJ, or about 650kWh of energy stored in this scary flywheel. That’s somewhat comparable to a similar volume of lead-acid batteries (though four times as massive). We would want to evacuate the air around the spinning disk or we will suffer a drain rate of something like 1kW (consuming 24kWh/day just to keep it spinning; the room would also get warm-ish).

The acceleration at the outer radius is about 10,000 times that of gravity, and it turns out the geometry and speed we picked indeed approaches the yield strength of steel. Structural weaknesses then risk breakup, which would dump the unwelcome energy equivalent of half a ton of TNT in your house. We would need to slow to a speed of 250m/s at the outer rim to provide an adequate material safety factor, resulting in 250kWh of storage. Another safety concern: if the flywheel comes off its support, it could barrel through the neighborhood, popping through houses like they weren’t even there. Not ideal in earthquake country.

Obviously, we can afford to scale things down a bit, since our first cut provided three weeks of storage capacity. The same cylinder spinning at 125 m/s (275 m.p.h.) at the edge gives about 90 kWh of storage, and may be somewhat more tolerable from a safety point of view. Scaling down the size/mass in addition to velocity begins to result in a less useful storage solution for the average house. If you’re going to go through the effort, expense, and sacrifice of space for a scary flywheel, you’d better feel like it provides enough energy storage to be worthwhile.

A recent \$53 million [flywheel storage facility in Pennsylvania](http://investors.beaconpower.com/releasedetail.cfm?ReleaseID=598243) uses 200 large [units storing 25kWh each](http://www.beaconpower.com/products/about-flywheels.asp), working out to \$10,000 per kWh of storage capacity. Each unit’s vacuum chamber looks to be about 1.5m in diameter and 3–4m tall. If we raise the ceiling and squeeze four into our bedroom, we could get 3 days of electricity storage for the typical American house for a cool million bucks. But the frictional losses—while painstakingly minimized—likely preclude these units from being useful over periods of days.

## Compressed Air

We could store energy in something akin to a spring by compressing air. A high-quality tank can store air at 200 atmospheres of pressure. If we make a big bedroom-sized tank in cylindrical form similar to the flywheel dimensions, it has a volume of 10m³. The steel walls would have to be about 6cm thick to withstand the stress, so that the tank would have a mass of approximately 12 tons. You did reinforce the floor, right?

We want to take a volume of air, *V*₀, 200 times larger than our tank volume at atmospheric pressure (*P*₀ = 10⁵Pa) and compress it to fit in the tank (adding two tons of mass!). If done slowly enough to maintain approximately constant temperature (several hours), the energy required is *P*₀*V*₀ln(*P*/*P*₀), where ln() is the natural logarithm function. For our volume, this turns into 1GJ, or almost 300kWh—enough for 10 days of typical American electricity use. So we could get away with a smaller tank or simply charge it to a less extreme pressure.

The efficiency for compressing the air and later turning a turbine for electricity generation may be less than what one might find for a flywheel. The storage itself is not the hard part. I could go out today and get some lab-sized cylinders (~50 liters), which could store 1.5kWh each—about like a golf-cart battery, although heavier and bulkier. But I would have a very difficult time arranging an efficient pumping and extraction/turbine system. If not for that, I would find compressed air to be an attractive system compared to batteries: minimal maintenance; no apparent cycle limitations, reasonably low-tech, and perfectly tolerant of remaining at low charge indefinitely.

Laboratories that frequently use compressed gas cylinders have strict safety protocols to prevent explosions from structural rupture due to mishandling. If houses across the land had high pressure vessels in various states of neglect/corrosion, we’d get the occasional boom. I might worry about having a gun in the house. But I’m guessing that house fires would still represent a bigger net threat.

## Hydrogen Fuel Cell

What about electrolysis of water into hydrogen for later use either in fuel cells or combustion engines? I’ll ignore the combustion option, as the heat engine efficiency would be abysmal compared to the other storage options on the table. Batteries, gravitational storage, and flywheels can achieve better than 80% round-trip efficiency. Compressed air is harder for me to evaluate, lacking adequate knowledge on compression/extraction devices built for efficiency.

Electrolysis for the production of hydrogen tends to range between 50–70% efficient. Then the fuel cell converts the stored energy back into electricity at 40–60% efficiency for a round-trip efficiency of 20–40%. If you happen to want some of the waste heat, then you might boost the efficiency estimate (true for any of these storage methods, actually). But in a straight-up apples-to-apples comparison, the hydrogen method is a very lossy storage option. If it were dirt cheap and low-tech, I might be more excited about its potential, despite the poor efficiency. But since the opposite is true, I’m not revved up over hydrogen storage.

I spent some time searching for a hydrogen fuel cell that I could buy today with a rating in the 10kW range (appropriate for a home). I saw some production models achieving efficiencies ranging from 40–53%, but never a price tag. If you have to submit a query to learn the price, you probably can’t afford it…

## Other Ideas?

Have I exhausted all the possibilities? Certainly not. I picked obvious and representative techniques spanning gravitational, kinetic, spring force (in air), and chemical storage. These are the ideas that come to mind for me, each with some reasonable footprint in the panoply of relevant small-scale “solutions” often discussed. I stayed away from thermal storage because the round-trip efficiency will make hydrogen fuel cells look fabulous. I also stayed away from fossil fuels (gas generators, storing natural gas at home) for the obvious reason that we don’t generally *need* storage as long as we have a reliable supply of fossil fuels.

A short digression to contrast the miraculous energy density in fossil fuels: our 3 days of electricity storage at 30 kWh/day requires just 12 gallons of gasoline (1.6 cubic feet; 45 liters) burned in a 20% efficient generator (it seems like the other 80% is noise!). The Earth’s battery—a one-time gift to us—turns out to be vastly superior to any of these other “solutions” in terms of energy density and long-term storage, measured in millions of years. It will be sorely missed when it’s gone.

## They’re All Hard

With the exception of the feeble gravitational storage example, each of the ideas presented here are technically challenging, expensive, and sometimes dangerous. I am left thinking that batteries look pretty good for home storage. And they *already* perform a key function in my household. But even the cheapest lead-acid solution is still expensive, high-maintenance, and requires replacement every few years. For \$150, you get 1kWh of storage. 500 cycles means 500kWh of service (get about 1000 cycles if half-discharge, but still roughly the same total energy service). This comes to about \$0.30/kWh, which makes it an expensive source of electricity. Even so, lead-acid is the most economic storage medium of choice for off-grid households, and loads better than no storage at all!

For short-term outages, we might get by with storage for critical functions only, like refrigeration and cooking. In a renewable-energy future, where storage must fill a larger role, the solutions are not obvious. As explained in the [post on a nation-sized battery](https://dothemath.ucsd.edu/2011/08/nation-sized-battery/ "Nation Sized Battery Do the Math post"), we can’t simply scale up our trusty lead-acid, lithium, or nickel-based batteries to satisfy our current demands in a fully-renewable energy scenario because of resource limitations. Large-scale pumped storage, subterranean (or underwater) compressed air, and sodium-sulfur batteries may become important players. But these don’t help the independent spirit who wants personal storage, and by now is perhaps feeling—well—powerless.

## The Easy Path: Ratchet Down

Many of the difficulties explored here become immediately easier with a simple reduction of scale. Because my household only uses 5kWh of electricity per day, the 7kWh of lead-acid storage I have in the form of four golf-cart batteries is enough to provide a meaningful service.

For me, the lesson is that adequate storage appears at first-blush to border on impossible under the current profile of consumption in the U.S. But cut consumption down by a factor of five or so, and I become optimistic. Such deep cuts are not impossible: I can personally still participate in a western lifestyle at a fifth of the energy cost at home. It’s a choice, and I’m happy with mine.

Hits: 5620

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2011%2F09%2Fgot-storage-how-hard-can-it-be%2F&linkname=Got%20Storage%3F%20How%20Hard%20Can%20it%20Be%3F "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2011%2F09%2Fgot-storage-how-hard-can-it-be%2F&linkname=Got%20Storage%3F%20How%20Hard%20Can%20it%20Be%3F "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2011%2F09%2Fgot-storage-how-hard-can-it-be%2F&linkname=Got%20Storage%3F%20How%20Hard%20Can%20it%20Be%3F "Email")[](https://www.addtoany.com/share)
