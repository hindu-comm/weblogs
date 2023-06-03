+++
title = "A SolarPowered Car?"
full_title = "A SolarPowered Car?"
upstream_url = "https://dothemath.ucsd.edu/2011/11/a-solar-powered-car/"
date = "2011-11-22"

+++
Source: [here](https://dothemath.ucsd.edu/2011/11/a-solar-powered-car/).

A Solar-Powered Car?

[![](https://dothemath.ucsd.edu/wp-content/uploads/2011/11/Reeses-Cup-300x117.jpg "Reeses-Cup")](https://dothemath.ucsd.edu/wp-content/uploads/2011/11/Reeses-Cup.jpg)If you like the sun, and you like cars, then I’m guessing you’d love to have a solar-powered car, right? This trick works well for chocolate and peanut butter, but not so well for garlic bread and strawberries. So how compatible are cars with solar energy? Do we relish the combination or spit it out? Let’s throw the two together, mix with math, and see what happens.

## What Are Our Options?

Short of some solar-to-liquid-fuel breakthrough—which I dearly hope can be realized, and described near the end of [a recent post](https://dothemath.ucsd.edu/2011/11/the-biofuel-grind/ "Do the Math: The Biofuel Grind")—we’re talking **electric cars** here. This is great, since electric drive trains can be marvelously efficient (ballpark 85–90%), and immediately permit the clever scheme of regenerative braking.

Obviously there is a battery involved as a power broker, and this battery can be charged (at perhaps 90% efficiency) via:

- on-board internal combustion engine fueled by gasoline or equivalent; - utility electricity; - a fixed solar installation; - on-board solar panels.

Only the final two options constitute what I am calling a solar-powered car, ignoring the caveat that hydro, wind, and even fossil fuels are ultimately forms of solar energy. The last item on the list is the dream situation: no reliance on external factors other than weather. This suits the independent American spirit nicely. And clearly it’s possible because there is an annual race across the Australian desert for 100% on-board solar powered cars. Do such successful demonstrations today mean that widespread use of solar cars is just around the corner?

## Full Speed Ahead!

First, let’s examine the requirements. For “acceptable” travel at freeway speeds (30m/s, or 67m.p.h.), and the ability to seat four people comfortably, we would have a very tough job getting a frontal area smaller than 2m² and a drag coefficient smaller than *c*_(D)=0.2—yielding a “drag area” of 0.4m². Even a bicyclist tends to have a larger drag area than this! Using the sort of math developed in the post on [limits to gasoline fuel economy](https://dothemath.ucsd.edu/2011/07/100-mpg-on-gasoline/ "Do the Math: 100 MPG on Gasoline"), we find that our car will experience a drag force of *F*_(drag)=½*ρc*_(D)*Av*²≈250 Newtons (about 55lbs).

Work is force times distance, so to push the car 30 meters down the road each second will require about 7,500J of energy (see the [page on energy relations](https://dothemath.ucsd.edu/useful-energy-relations/ "Do the Math: Useful Energy Relations") for units definitions and relationships). Since this is the amount of energy needed each second, we can immediately call this 7,500 Watts—which works out to about ten horsepower. I have not yet included rolling resistance, which is about 0.01 times the weight of the car. For a super-light loaded mass of 600kg (6000N), rolling resistance adds a 60N constant force, requiring an additional 1800W for a total of about 9kW.

What can solar panels deliver? Let’s say you can score some space-quality 30% efficient panels (i.e., twice as efficient as typical panels on the market). In full, overhead sun, you may get 1,000W/m² of solar flux, or a converted 300W for each square meter of panel. We would then need 30 square meters of panel. Bad news: the top of a normal car has well less than 10 square meters available. I measured the upward facing area of a sedan (excluding windows, of course) and got about 3m². A truck with a camper shell gave me 5m².

If we can manage to get 2kW of instantaneous power, this would allow the car in our example to reach a cruising speed on the flats of about 16m/s (35m.p.h.). In a climb, the car could lift itself up a grade at only one vertical meter every three seconds (6000J to lift the car one meter, 2000J/s of power available). This means a 5% grade would slow the car to 6.7m/s, or 15 miles per hour—in full sun. Naturally, batteries will come in handy for smoothing out such variations: charging on the downhill and discharging on the uphill, for an average speed in the ballpark of 30m.p.h.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2011/11/prius-solar-roof-300x156.jpg "prius-solar-roof")](https://dothemath.ucsd.edu/wp-content/uploads/2011/11/prius-solar-roof.jpg)

Image from toyota.com.

So this dream of a family being comfortably hurtled down the road by real-time sun will not come to pass. (Note: some Prius models offered a solar roof option, but this just drove a fan for keeping the car cooler while parked—maybe simply offsetting the extra heat from having a dark panel on the roof!) But what of these races in Australia? We have real-live demonstrations.

## The Dream Realized

[![](https://dothemath.ucsd.edu/wp-content/uploads/2011/11/Tokai_Challenger-300x204.jpg "Tokai_Challenger")](https://dothemath.ucsd.edu/wp-content/uploads/2011/11/Tokai_Challenger.jpg)

Tokai Challenger. Look at that speed!

In recent years, the Tokai Challenger, from Tokai University in Japan, has been a top performer at the World Solar Challenge. They use a 1.8kW array of 30% efficient panels (hey—my guess was right on!), implying 6 square meters of panel. The weight of the car plus driver is a mere 240kg. As with most cars in the competition, the thing looks like a thin, worn-down bar of soap with a bubble for the driver’s head: both the drag coefficient (a trout-like 0.11) and the frontal area (I’m guessing about 1m², but probably less) are trimmed to the most absurd imaginable limits. From these numbers, I compute a freeway-speed aerodynamic drag of about 60 Newtons and a rolling resistance of about 25N, for a total of 85N: about 35% of what we computed for a “comfortable” car. Solving for the speed at which the combination of air drag plus rolling resistance requires 1.8kW of power input, I get 26m/s, or 94km/h, or 58m.p.h., which is very close to the reported speed.

## Bring on the Batteries: Just Add Sun

We have seen that a practical car operating strictly under its own on-board power turns in a disappointing performance. But if we could use a large battery bank, we could store energy received when the car is not in use, or from externally-delivered solar power. Even the Australian solar racers are allowed 5kWh of storage on board. Let’s beef this up for driving in normal conditions. Using today’s production models as examples, the Volt, Leaf, and Tesla carry batteries rated at 16, 24, and 53kWh, respectively.

Let’s say we want a photovoltaic (PV) installation—either on the car or at home—to provide all the juice, with the requirement that one day is enough to fill the “tank.” A typical location in the continental U.S. receives an average of 5 full-sun hours per day. This means that factoring in day/night, angle of the sun, season, and weather, a typical panel will gather as much energy in a day as it would have if the high-noon sun persisted for five hours. To charge the Volt, then, would require an array capable of cranking out 3kW of peak power. The Tesla would require a 10kW array to provide a daily charge. The PV areas required vastly exceed what is available on the car itself (need 10m² even for the 3kW system at a bank-breaking 30% efficiency; twice this area for affordable panels).

But this is not the best way to look at it. Most people care about *how far* they can travel each day. A typical electric car requires about [30kWh per 100 miles driven](https://dothemath.ucsd.edu/2011/08/mpg-for-electric-cars/ "Do the Math: MPG for Electric Cars"). So if your daily march requires 30 miles of round-trip range, this takes about 10kWh and will need a 2kW PV system to provide the daily juice. You *might* be able to squeeze this onto the car roof.

How do the economics work out? Keeping up this 30 mile per day pattern, day after day, would require an annual gasoline cost of about \$1000 (if the car gets about 40MPG). Installed cost of PV is coming in around \$4 per peak Watt lately, so the 2kW system will cost \$8000. Thus you offset (today’s) gas prices in 8 years. This math applies to the standard 15% efficient panels, which precludes a car-top solution. For this reason, I will primarily focus on stationary PV from here on.

## Practicalities: Stand-Alone or Grid-Tie?

Ah—the practicalities. Where dreams get messy. For the purist, a totally solar car is not going to be so easy. The sun does not adhere to our rigid schedule, and we often have our car away from home during the prime-charging hours anyway. So to stay truly solar, we would need significant home storage to buffer against weather and charge-schedule mismatch.

The idea is that you could roll home at the end of the day, plug up your car, and transfer stored energy from the stationary battery bank to your car’s battery bank. You’d want to have several days of reliable juice, so we’re talking a battery bank of 30–50kWh. At \$100 per kWh for lead-acid, this adds something like \$4000 to the cost of your system. But the batteries don’t last forever. Depending on how hard the batteries are cycled, they might last 3–5 years. A bigger bank has shallower cycles, and will therefore tolerate more of these and last longer, but for higher up-front cost.

The net effect is that the stationary battery bank will cost about \$1000 per year, which is exactly what we had for the gasoline cost in the first place. However, I am often annoyed by economic arguments. More important to me is the fact that you **can do it**. Double the gas prices and we have our 8-year payback again, anyway. Purely economic decisions tend to be myopic, focused on the conditions of today (and with some reverence to trends of the past). But fundamental phase transitions like peak oil are seldom considered: we will **need** alternative choices—even if they are more expensive than the cheap options we enjoy today.

The other route to a solar car—much more widespread—is a grid-tied PV system. In this case, your night-time charging comes from traditional production inputs (large regional variations in mix of coal, gas, nuclear, and hydro), while your daytime PV production helps power other people’s air conditioners and other daytime electricity uses. Dedicating 2kW of panel to your transportation needs therefore offsets the net demand on inputs (fossil fuel, in many cases), effectively acting to flatten demand variability. This is a good trend, as it employs otherwise underutilized resources at night, and provides (in aggregate) peak load relief so that perhaps another fossil fuel plant is not needed to satisfy peak demand. Here, the individual does not have to pay for a stationary battery bank. The grid acts as a battery, which will work well enough as long as the solar input fraction remains small.

As reassuring as it is that we’re dealing with a possible—if expensive—transportation option, I must disclose one additional gotcha that makes for a slightly less rosy picture. Compared to a grid-tied PV system, a standalone system must build in extra overhead so that the batteries may be fully charged and conditioned on a regular basis. As the batteries approach full charge, they require less current and therefore often throw away potential solar energy. Combining this with charging efficiency (both in the electronics and in the battery), it is not unusual to need twice the PV outlay to get the same net delivered energy as one would have in a grid-tied system. Then again, if we went full-scale grid-tied, we would need storage solutions that would again incur efficiency hits and require a greater build-up to compensate.

## A Niche for Solar Transport

[![](https://dothemath.ucsd.edu/wp-content/uploads/2011/11/UCSD-solar-cart-300x225.jpg "UCSD-solar-cart")](https://dothemath.ucsd.edu/wp-content/uploads/2011/11/UCSD-solar-cart.jpg)

UCSD golf cart with PV roof.

There *is* a niche in which a vehicle with a PV roof could be self-satisfied. Golf carts that can get up to 25m.p.h. (40km/h) can be useful for neighborhood errands, or for transport within a small community. They are lightweight and slow, so they can get by with something like 15kWh per 100 miles. Because travel distances are presumably small, we can probably keep within 10 miles per day, requiring 1.5kWh of input per day. The battery is usually something like 5kWh, so can store three days’ worth right in the cart. At an average of five full-sun hours per day, we need 300W of generating capacity, which we can achieve with 2 square meters of 15% efficient PV panel. Hey! This could work: self-contained, self-powered transport. Plug it in only when weather conspires against you. And unlike unicorns, I’ve *seen* one of these beasts tooling around the UCSD campus!

## Digression: Cars as the National Battery?

What if we eventually converted our fleet of petroleum-powered cars to electric cars with a substantial renewable infrastructure behind it. Would the cars themselves provide the storage we need to balance the system? For the U.S., let’s take 200 million cars, each able to store 30kWh of energy. In the extreme, this provides 6 billion kWh of storage, which is about 50 times smaller than the [full-scale battery](https://dothemath.ucsd.edu/2011/08/nation-sized-battery/ "Do the Math: Nation Sized Battery") that [I have argued](https://dothemath.ucsd.edu/2011/11/pump-up-the-storage/ "Do the Math: Pumped Storage") we would want to allow a complete renewable energy scheme. And this assumes that the cars have no demands of their own: that they obediently stay in place during times of need. In truth, cars will operate on a much more rigorous daily schedule (needing energy to commute, for instance) than what Mother Nature will throw at our solar/wind installations.

We should take what we can get, but using cars as a national battery does not get us very far. This doesn’t mean that in-car storage wouldn’t provide some essential service, though. Even without trying to double-task our electric cars (i.e., never demanding that they feed *back* to the electricity grid), such a fleet would still relieve oil demand, encourage renewable electricity production, and act as load balancer by preferentially slurping electricity at night.

## I Want a Solar-Powered Car

I also want a land speeder from Star Wars, a light saber while we’re at it, and a jet pack. And a pony. But unlike many of these desires, a solar powered car *can be* a practical reality. I could go out tomorrow and buy a Volt or a Leaf and charge it with my home-built off-grid PV system (although I would first need to beef it up a bit to cover our modest weekly transportation needs). Alternatively, I could park a solar-charged golf cart in the sun—or charge an electric-assist bicycle with a small PV system, for that matter—to get around my neighborhood. Slightly less satisfying, I could install a grid-tied PV system with enough yearly production to offset my car’s electricity take. The point is, I could make stops at the gas station a thing of the past (or at least rare, in the case of a plug-in hybrid).

So solar powered cars fall solidly on the reality side of the reality-fantasy continuum. That said, pure solar transport (on board generation) will suffer serious limitations. More reliable transport comes with nuances that may be irritating to the purist. You can apply a bumper sticker that says SOLAR POWERED CAR, but in most cases, you will need to put an asterisk at the end with a lengthy footnote to explain exactly how you have realized that goal.

Hits: 6234

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2011%2F11%2Fa-solar-powered-car%2F&linkname=A%20Solar-Powered%20Car%3F "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2011%2F11%2Fa-solar-powered-car%2F&linkname=A%20Solar-Powered%20Car%3F "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2011%2F11%2Fa-solar-powered-car%2F&linkname=A%20Solar-Powered%20Car%3F "Email")[](https://www.addtoany.com/share)
