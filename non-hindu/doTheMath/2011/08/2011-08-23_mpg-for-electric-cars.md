+++
title = "MPG for Electric Cars?"
full_title = "MPG for Electric Cars?"
upstream_url = "https://dothemath.ucsd.edu/2011/08/mpg-for-electric-cars/"
date = "2011-08-23"

+++
Source: [here](https://dothemath.ucsd.edu/2011/08/mpg-for-electric-cars/).

MPG for Electric Cars?

A typical efficient car in the U.S. market gets about 40MPG (miles per gallon) running on gasoline. A hybrid car like the Prius typically gets 50–55MPG. In a [previous post](https://dothemath.ucsd.edu/2011/07/100-mpg-on-gasoline/ "100 MPG on Gasoline: Could We Really?"), we looked at the physics that determines these numbers. As we see more and more plug-in hybrid or pure electric cars on the market, how do we characterize their mileage performance in comparison to gasoline cars? Do they get 100MPG? Can they get to 200? What does it even mean to speak of MPG, when the “G” stands for gallons and a purely electric car does not ingest gallons?

This post addresses these questions.

## Using the Wrong Measure

Okay, first of all, MPG (called fuel economy) has always been a poor choice of units. We don’t usually put a gallon of gas in the car and drive as far as it might take us. Rather, we tend to have a destination in mind and care about how much gas it will take to get there. The inverse, GPM (called fuel consumption), would therefore be a better measure, and is akin to the measure used in some parts of the world (e.g., Europe’s liters per 100 km).

Besides this philosophical advantage, the GPM approach has a numerical advantage. If you have an old truck that gets 12MPG and car that gets 30MPG (let’s say both travel comparable distances in a year) and you want to replace one of the vehicles, are you better off replacing the truck with a 16MPG model or the car with a 40MPG model? Framed this way, the car looks like a better choice: a gain of 10MPG vs. 4MPG.

Let’s say for numerical simplicity that you want to go 240 miles in both. In your initial situation, it takes 20 gallons for the truck and 8 gallons for the car, for 28 gallons total. If you replace the car, the same journey will take 6 gallons for the car for a total of 26 gallons. If you replace the truck, the new one takes only 15 gallons for a total of 23 gallons. It’s a *much* better deal to replace the truck, even though the MPG gain seemed less impressive. We would have had to replace the 30MPG car with one that gets 80MPG to achieve the same 23 gallon result. If we had been using GPM instead of MPG, we’d never get confused on this point, and would therefore make smarter decisions. Try adding the values of 1/MPG to see that this is true, as in the following table.

|                |           |         |            |           |         |           | |----------------|-----------|---------|------------|-----------|---------|-----------| | Scenario       | truck MPG | car MPG | gal/240 mi | truck GPM | car GPM | total GPM | | Original       | 12        | 30      | 28         | 0.0833    | 0.0333  | 0.1167    | | Replace Car    | 12        | 40      | 26         | 0.0833    | 0.025   | 0.1083    | | Replace Truck  | 16        | 30      | 23         | 0.0625    | 0.0333  | 0.0958    | | Equivalent Car | 12        | 80      | 23         | 0.0833    | 0.0125  | 0.0958    |

## A New Measure for All Cars: Electric and Gasoline

With this lesson in mind, we would like a measure of energy per distance traveled. I’m a big fan of picking a universal energy unit and applying it to all forms of energy we use. Among the zoo of energy units: Joule, kilocalorie, Btu, Therm, kilowatt-hour, gallon of gas, barrel of oil, etc., I prefer the [kilowatt-hour](https://dothemath.ucsd.edu/useful-energy-relations/#kilowatt-hour) as a common standard. I like this because my favorite unit is the Watt (is it *wrong* to have a favorite?), and using the kWh makes it straightforward to flip between energy and power. Like ya do.

So I’ll bow to both the American and the scientist in me and try a unit as schizophrenic as an American scientist *must be* when it comes to units: kWh/mi. Lovely.

Let’s look at our 40MPG sedan. A gallon of gasoline contains 36.6kWh of heat energy when combusted, in this case taking us 40 miles down the road in the process. So this car uses 0.915kWh per mile.

We tend not to be fond of puny fractions: especially in America where we like our numbers BIG. So let’s take a hint from the Europeans and use **kWh/100-mi**. Now our sedan has an energy consumption of 91.5kWh/100-mi. Using this measure, we desire a *smaller* number for our car. Energy consumption in these units for gasoline-driven cars can be calculated as 3660/MPGkWh/100-mi. A 12MPG Hummer has an energy consumption of 305kWh/100-mi, while a Prius, at 50MPG has an energy consumption of about 73kWh/100-mi.

How do electric cars or other electric/hybrids stack up? In order of performance: the Chevy Volt gets 35 miles from a 16kWh battery for a consumption of 45kWh/100-mi (*see note below*); the Nissan Leaf gets 73 miles from its 24kWh battery for 33kWh/100-mi; and the pricey Tesla has a 244 mile range using a 53kWh battery, for 22kWh/100-mi. The MPG equivalent of these three figures is approximately 80, 110, and 170, respectively. All are much better deals than gasoline cars deliver, primarily because the electrical drive system is far more efficient than the typical 20% gasoline engine.

\[*Note: a reader informs me that his Volt uses 30 kWh/100-mi, the difference being that the battery is only allowed to use 10.4 kWh of its 16 kWh capacity.*\]

If you pay \$0.10/kWh for electricity, these three cars travel 100mi for costs of \$4.50, \$3.30, \$2.20, respectively (triple this for Hawaii). At \$3.50 per gallon of gasoline, a car getting 50MPG will cost \$7.00 to travel the same distance. So in almost all cases, the “fuel” cost is less to the consumer at current prices.

## Theoretical Expectations

Are the energy consumption numbers we calculated *good*? Besides being obviously better than gasoline cars, are they close to the theoretical limit? To get at this, we follow the analysis developed in the [earlier post on gas mileage](https://dothemath.ucsd.edu/2011/07/100-mpg-on-gasoline/ "100 MPG on Gasoline: Could We Really?"). The energy it takes to fight air resistance when traveling a distance *D* at velocity *v* is *E* = ½*c*_(D)*ρADv*², where *c*_(D) is the drag coefficient (0.25 for the Prius, for example), *ρ*=1.3kg/m³ is the density of air, and *A* is the frontal area (\<2.5m² for a deliberately efficient small car). Putting in 160,934 meters for *D* to represent 100 miles, and converting the result (in Joules) to kWh by dividing by 3,600,000J/kWh, we get 16kWh/100-mi when traveling at a freeway speed of 30m/s (67m.p.h.).

If we add rolling resistance, at about 1% of the car’s weight, we get an additional tax of about 5kWh/100-mi for a 1000kg car, independent of speed. Therefore, the low 20’s is about as good as you might ever see at freeway speeds. For city driving, regenerative braking and the much smaller contribution from air resistance will reduce the theoretical expectation, approaching the rolling resistance limit in extreme cases. The Tesla figure of 22kWh/100-mi, for example, represents a combined profile of driving conditions/speeds. The energy consumption at freeway speeds is undoubtedly higher than the combined figure, and not in danger of challenging the theoretical limit. But on the whole, not a bad show for the first wave of mass-market electric cars.

# Not So Fast

The present analysis leaves out two important bits. First, the energy consumption (and electricity costs) I calculated for the Volt, Leaf, and Tesla simply use the battery capacity—not the electricity delivered for charging. Charging efficiency may be anywhere from 70% to 90%. But that’s a small caveat compared to the second issue (and similar to the 25% energy overhead for refining gasoline from oil—which itself has an energy overhead of only about 5% in the extraction/delivery process).

In order to deliver 30kWh to your house to fully charge the Leaf’s 24kWh battery bank, for example—incorporating the charge efficiency this time, the **source** of electricity becomes a highly relevant factor. Two-thirds of our electricity comes from fossil fuel plants, typically converting 35% of the fossil fuel thermal energy into electricity. Only 90% of this makes it through the transmission system, on average. If your electricity comes from a fossil fuel plant, the 30kWh delivered to your house took about 95kWh of fossil fuel energy. The 73 miles the Leaf travels on a full charge now puts it at an energy efficiency of 130kWh/100-mi. The MPG equivalent number is 28MPG. From a carbon-dioxide standpoint, you’d be better off burning the fossil fuel directly in your car.

I’m not saying that transitioning to electric or hybrid cars is not a good idea. I think it’s an *imperative*, if we want maintain a car culture, given that fossil fuel supplies are going to decline eventually, starting with oil. Obviously, if your power comes from hydroelectric, solar, wind, or even nuclear, you don’t have the same concerns. Also, emissions controls (for things other than CO₂) are vastly better for fossil-fuel power plants than for automobiles, so electric cars are less polluting. But if your priority is either reduced resource consumption *or* climate change and CO₂ reduction, let’s focus on getting electricity from carbon-free sources before transforming our fleet of cars to electric—or at least accomplish the two in tandem.

Hits: 5120

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2011%2F08%2Fmpg-for-electric-cars%2F&linkname=MPG%20for%20Electric%20Cars%3F "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2011%2F08%2Fmpg-for-electric-cars%2F&linkname=MPG%20for%20Electric%20Cars%3F "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2011%2F08%2Fmpg-for-electric-cars%2F&linkname=MPG%20for%20Electric%20Cars%3F "Email")[](https://www.addtoany.com/share)
