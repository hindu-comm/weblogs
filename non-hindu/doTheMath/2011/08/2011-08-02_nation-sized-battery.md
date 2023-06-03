+++
title = "A NationSized Battery"
full_title = "A NationSized Battery"
upstream_url = "https://dothemath.ucsd.edu/2011/08/nation-sized-battery/"
date = "2011-08-02"

+++
Source: [here](https://dothemath.ucsd.edu/2011/08/nation-sized-battery/).

A Nation-Sized Battery

As we look to transition away from fossil fuels, solar and wind are attractive options. Key factors making them compelling are: the inexhaustibility of the source with use (i.e., renewable); their low carbon footprint; and the independence that small-scale distribution can foster (I’ll never put a nuclear plant on my roof, even if it would make me the coolest physicist ever!).

[![lovely future of solar, wind, and honking-big battery](https://dothemath.ucsd.edu/wp-content/uploads/2011/07/us-battery.jpg "us-battery")](https://dothemath.ucsd.edu/wp-content/uploads/2011/07/us-battery.jpg)

With full-scale solar in the desert southwest, and wind in the plains states, we're going to need a big battery (items not to scale!).

But solar and wind suffer a serious problem in that they are not always available. There are windless days, there are sunless nights, and worst of all, there are windless nights. Obviously, this calls for **energy storage**, allowing us to collect the energy when we *can*, and use it when we *want*.

Small-scale off-grid solar and wind installations have been doing this for a long time, typically using lead-acid batteries as the storage medium. I myself have four golf-cart batteries in my garage storing the energy from eight 130W solar panels, and use these to power the majority of my electricity consumption at home.

It’s worth pausing to appreciate this fact. Compare this scheme to the dream source of fusion. Why do people go ga-ga over fusion? Because there is enough deuterium in water (sea water is fine) to provide a seemingly inexhaustible source of energy, and there are no atmospheric emissions in the process. Meanwhile, solar provides a source that will last longer (billions of years), produces even *less* pollution (no radioactive contamination of containment vessel), and is **here today**! It’s even affordable enough and low-tech enough to be *on my roof and in my garage*! People—we have arrived!

Storage works on the small scale, as many stand-aloners can attest. How would it scale up? Can it?

## Meeting Requirements

So what would it take? We’re not a nation tolerant of power outages. Those big refrigerators can spoil a lot of food when the electricity drops away. A rule of thumb for remote solar installations is that you should design your storage to last for a minimum of three days with no energy input. Even then, sometimes you will “go dark” in the worst storm of the winter.This does not mean literally three days of total deprivation, but could be four consecutive days at 25% average input, so that you only haul in one day’s worth over a four day period, leaving yourself short by three.

So let’s buy ourselves security and design a battery that can last a week without any new inputs (as before this is not literally 7 days of zero input, but could be 8 days at 12.5% average input, or 10 days at 30% input). This may be able to manage the worst-case “perfect” storm of persistent clouds in the desert Southwest plus weak wind in the Plains.

Let’s also plan ahead and have *all* of our country’s energy needs met by this system: transportation, heating, industry, etc. The rate at which we currently use energy in all forms in the U.S. is 3TW. If we transition everything to electricity, we can get by with 2TW, assuming no growth in demand. Why? Because we currently use two-thirds of our energy supply (or 2TW) to run heat engines, getting only about 0.6TW out for useful purposes in the bargain. An electrical system could deliver this same 0.6TW for only 1TW of input, considering storage and transmission efficiencies.

Running a 2TW electrified country for 7 days requires 336 billion kWh of storage. We could also use nuclear power as a baseload to offset a significant portion of the need for storage—perhaps chopping the need in two. This post deals with the narrower topic of what it would take to implement a full-scale renewable-energy battery. Scale the result as you see fit.

## Lead-Acid Delivers

I’ll use lead-acid batteries as a baseline. Why? Because lead-acid batteries are the cheapest way to store electricity today. They’re bulky, sloshy, and very heavy, which makes them unsuitable for electric cars or laptop computers. But they’re very efficient, commonly achieving 85% or better energy efficiency in a charge cycle. The technology is well tested, having been around since 1859. And lead is a common element, being the endpoint of the alpha-decay chain of heavy elements like uranium and thorium. Their economic favorability makes lead-acid batteries hands-down the most common battery type in stand-alone renewable systems worldwide.

Large lead-acid batteries occupy a volume of 0.013 cubic meters (13 liters) per kWh of storage, weigh 25kg/kWh (55lb/kWh), and contain about 15 kg of lead per kWh of storage.

How do we put this into more familiar terms? A 12 V battery rated at 200 A-h (amp-hours) of charge capacity stores 2400 W-h (watt-hours: just multiply voltage and charge capacity), or 2.4 kWh. 200 A-h means that the battery could discharge a 10 amp current (120 watts) for 20 hours, or a one amp current (12 watts) for 200 hours—though in actual practice the capacity is lower at higher currents.

I can’t resist the temptation to ask: what is the minimum amount of lead that is theoretically needed to build the battery? The chemical reaction for a lead-acid battery is such that each interaction involving the transformation of one lead atom to PbSO₄ liberates one electron at a 2.1-volt potential. This electron then is bestowed 2.1 electron-volts (eV) of energy, amounting to 3.4×10⁻¹⁹J (see [page on energy relations](https://dothemath.ucsd.edu/useful-energy-relations/#electron-volt "Useful Energy Relations: Electron volt")). One kilowatt-hour is 3.6 million Joules (1000W times 3600 seconds), so that it takes 10²⁵ lead atoms (where *every one* participates). If you remember that Avogadro’s number is 6×10²³, we need about 20 moles of lead atoms. At 207g/mol, this comes out to about 4kg per kWh of energy, which is a factor of four less than the realized value above. Real implementations always fall short of theoretical ideals, so this isn’t new. We would do well to push for future improvements on this score, although we should bear in mind that lead-acid has had 150 years of development before we get carried away by dreams of perfection.

## The National Battery

Putting the pieces together, our national battery occupies a volume of 4.4 billion cubic meters, equivalent to a cube 1.6km (one mile) on a side. The size in itself is not a problem: we’d naturally break up the battery and distribute it around the country. This battery would demand 5 trillion kg (**5 billion tons**) of lead.

## Get the Lead Out!

A [USGS report from 2011](http://minerals.usgs.gov/minerals/pubs/commodity/lead/mcs-2011-lead.pdf) reports 80 million tons (Mt) of lead in known reserves worldwide, with 7Mt in the U.S. A note in the report indicates that the recent demonstration of lead associated with zinc, silver, and copper deposits places the estimated (undiscovered) lead resources of the world at 1.5 billion tons. That’s still not enough to build the battery for the U.S. alone. We could chose to be optimistic and assume that more lead will be identified over time. But let’s not ignore completely the fact that at this moment in time time, no one can point to a map of the world and tell you where even 2% of the necessary lead would come from to build a lead-acid battery big enough for the U.S. And even the undiscovered, but suspected lead falls short.

What about cost? At today’s price for lead, \$2.50/kg, the national battery would cost \$13 trillion in lead alone, and perhaps double this to fashion the raw materials into a battery (today’s deep cycle batteries retail for four times the cost of the lead within them). But I guarantee that if we really want to use more lead than we presently estimate to exist in deposits, we’re *not* dealing with *today’s* prices. Leaving this caveat aside, the naïve \$25 trillion price tag is more than the annual U.S. GDP. Recall that lead-acid is currently the *cheapest* battery technology. Even if we sacrificed 5% of our GDP to build this battery (would be viewed as a *huge* sacrifice; nearly a trillion bucks a year), the project would take decades to complete.

But even then, we aren’t done: batteries are good for only so many cycles (roughly 1000, depending on depth of discharge), so the national battery would require a rotating service schedule to recycle each part once every 5 years or so. This servicing would be a massive, expensive, and never-ending undertaking.

## Who Needs Lead-Acid?

I focus here on lead-acid because it’s the devil we know, it’s the cheapest storage at present, and the materials are far more abundant than lithium (13 Mt reserves worldwide, 33 Mt estimated global resources), or nickel (76 Mt global reserves, 130 Mt estimated land resources worldwide). If we ever got serious about building big storage, there will be choices other than lead-acid. But I nonetheless find it immensely instructive (and daunting) to understand what it *would* mean to scale a mature technology to meet our needs. It worries me that the cheapest solution we have today would break the bank just based on today’s cost of raw materials, and that we can’t even identify enough in the world to get the job done.

This post does not proclaim that there is no way to build adequate storage to accommodate a fully-renewable energy infrastructure. A distributed grid helps, and an armada of gas-fired peak-load plants would offset the need for full storage. Storage can be augmented by pumped hydro, compressed air, flywheels, other battery technologies, etc.

Rather, the lesson is that we must work within serious constraints to meet future demands. We can’t just scale up the current go-to solution for renewable energy storage—we are yet again fresh out of silver bullet solutions. More generally, large scale energy storage is *not* a solved problem. We should be careful not to trivialize the problem, which tends to reduce the imperative to work like mad on establishing adequate capabilities in time (requires decades of fore-thought and planning).

Hits: 5348

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2011%2F08%2Fnation-sized-battery%2F&linkname=A%20Nation-Sized%20Battery "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2011%2F08%2Fnation-sized-battery%2F&linkname=A%20Nation-Sized%20Battery "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2011%2F08%2Fnation-sized-battery%2F&linkname=A%20Nation-Sized%20Battery "Email")[](https://www.addtoany.com/share)
