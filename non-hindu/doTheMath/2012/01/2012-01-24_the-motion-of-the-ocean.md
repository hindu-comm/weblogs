+++
title = "The Motion of the Ocean"
full_title = "The Motion of the Ocean"
upstream_url = "https://dothemath.ucsd.edu/2012/01/the-motion-of-the-ocean/"
date = "2012-01-24"

+++
Source: [here](https://dothemath.ucsd.edu/2012/01/the-motion-of-the-ocean/).

The Motion of the Ocean

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/01/Waves_July_2009-1-150x150.jpg "Waves_July_2009-1")](https://dothemath.ucsd.edu/wp-content/uploads/2012/01/Waves_July_2009-1.jpg)With the exception of tidal energy, our focus thus far has been on land-based energy sources. Meanwhile, the ocean absorbs a prodigious fraction of the Sun’s incident energy, creating thermal gradients, currents, and waves whipped up by winds. Let’s put some scales on the energetics of these sources and see if we may turn to them for help. We’ve got our three boxes ready: abundant, potent, and niche (puny). Time to do some sorting!

### Thermal Gradients

Wherever there is a thermal gradient, our eyes light up because we can create a *heat flow* across the gradient and capture some fraction of the energy flow to do useful work. This is called a **heat engine**, the efficiency of which is capped by the theoretical maximum (*T*_(h)−*T*_(c))/*T*_(h), where “h” and “c” subscripts refer to absolute temperatures of the hot and cold reservoirs, respectively. In the ocean, we are rather limited in how much gradient is available. The surface does not tend to exceed 30°C (303K), while the depths cannot get much cooler than 0°C (273K; pressure and salinity allow it to go a few degrees negative). The maximum thermodynamic efficiency therefore tops out at 10%, and in practice we might get half of this in a real application. The general scheme of producing energy from thermal gradients in the ocean is called ocean thermal energy conversion (OTEC).

#### [![](https://dothemath.ucsd.edu/wp-content/uploads/2012/01/sea-surf-temp.gif "sea-surf-temp")](https://dothemath.ucsd.edu/wp-content/uploads/2012/01/sea-surf-temp.gif)OTEC Potential

How much energy is available? First of all, water is *tremendously* efficient at storing thermal energy, packing 4184 Joules per liter per degree (definition of the [kilocalorie](https://dothemath.ucsd.edu/useful-energy-relations/#kcal "Do the Math: kilocalorie")). Therefore, extracting the heat from a cubic meter of water at 30°C—leaving it at 0°C—represents 125MJ of energy. Turned into electricity at 5% efficiency, we would need to process 160 cubic meters per second to generate a standard power plant’s output of 1GW. Remember that we’re using the most extreme temperature difference for our figures. Given that the elevated surface temperatures will only be found in the top 100m of water (above the thermocline), we must chew through 1.6m² of ocean area per second to make our gigawatt. In a day, we convert a square patch 370m on a side.

But this doesn’t get at how much can be sustainably recharged. The thermal energy derives, after all, from solar input. In the tropics, we might expect a patch of ocean to receive 250W/m² of sunlight on average. It takes a square area 9km on a side to annually recharge the 1GW draw (at 5% extraction efficiency: the other 95% is dumped into the depths as waste heat at close to 0°C). This figure ignores thermal exchange with the air, which will tend to be in the range of 5–20W/m² per °C difference between air and water. Also, radiative losses will reach 150W/m² in clear skies. Approximating these effects to produce a net 100W/m² retained as heat, we need our annual square to be about 14km on a side.

The 200km² patch we need to supply a 1GW “plant” gets multiplied by 13,000 to hit our 13TW global appetite. That’s an area comparable to the land area of the Indonesian islands: New Guinea, Borneo, Sumatra, etc. (wanted to pick something in warm water to stare at on map). Clearly we have the oceanic space. And as such, we throw OTEC into the “abundant” box. It’s basically a form of solar power at 5% efficiency available over a large fraction of the globe. So no real surprise that it should be abundant.

I did not factor in evaporative cooling, which can be rather significant. But it would have a hard time knocking the total resource out of the abundant box. In rough numbers, half of the total solar energy budget reaches the ground, and something like 70% of this is absorbed by oceans, for 35% of the total. Meanwhile, evaporation claims 23% of the solar budget, effectively taking a 2/3 bite out of the thermal energy deposited. So we need something like the area of Australia in the ocean. Like I say—still abundant.

Comparing the daily volume/area draw to the recharge area, we compute an interesting timescale: 4 years. In other words, if we isolated a patch of ocean 14km on a side that could generate 1GW of OTEC power, it would take 4 years to process the entire volume (above 100m depth). This is reassuringly longer than the one year recharge time, allowing for seasonal variation and adequate mixing.

#### OTEC Wrinkles

A look at the map above shows the regions for which our 30°C assumption is valid. These regions tend *not* to be near the major demand. If we want to park an OTEC plant off the shore of a more temperate location, several things happen. The temperature difference and therefore the quantity of thermal storage obviously shrinks (by roughly factor of two). The thermodynamic efficiency likewise takes a factor of two hit. And the warm layer is shallower at higher latitudes (say a factor of two). The net effect is a factor of 8 greater area of water processing per 1GW OTEC plant. The area for solar collection likewise increases—by almost a factor of two for reduced insolation, and by an additional factor of two to account for reduced efficiency.

Since the energy produced is a quadratic function of *ΔT*, a temperate OTEC plant becomes seriously impaired in the winter. At 40° latitude off the U.S. coast, I calculate that the winter production is at 40% the summer production in both the Atlantic and Pacific oceans.

Operating and maintaining an offshore power plant in seawater, transmitting the power to land, dealing with storms and other mishaps are serious challenges. OTEC reduces to a low efficiency, operationally difficult method for harvesting solar thermal energy. It seems we would be better off getting 15% in solar thermal plants in sunny areas. I’m not sure why we’d waste our time on OTEC when there are better (cheaper) ways to collect the abundant energy of the Sun. OTEC has some advantage in not having to build the collector, and in the fluid delivery system, but this would seem to be a minor plus stacked against the operational disadvantages. OTEC deserves a spot in the abundant box, but practicalities limit its likely role.

### Ocean Currents

Much as tuna was once marketed as the “chicken of the sea,” ocean currents are the “wind energy of the sea.” Recalling that the kinetic power in a fluid flow is ½*ρAv*³, where *ρ* is the density of the fluid, *A* is the area described by the collecting rotor, and *v* is the velocity of the fluid, we note that the density of water is about 800 times that of air. Big score! But the velocity tends to be smaller, and has a cubic power to knock it back. A strong mid-ocean current might reach 2 knots, or 1m/s. Compared to a wind speed of 10m/s (22m.p.h.), we get 1000 times less power per rotor area. So we’re right back to where we were with wind.

We have a lot more ocean area than land area. And we are not *as* constrained in the ocean as we are on land to keep our turbines near the surface, so we could exploit more vertical space—to a point. Ocean currents tend to be confined to the upper 400 meters of water, so the depth gain is only a factor of 2–3 times what we access for wind. On the plus side, we note that ocean currents are *far* more steady/robust, so we would not be plagued by intermittency the way we are with solar and wind. On balance, wind fell into the “potent” box, so ocean currents surely deserve at least this rating—practicalities aside, of course.

We would naturally first want to exploit pinch-points (straits, narrow inlets, etc.), where currents may be up to 5m/s, now delivering 100 times the power per area compared to a windmill at 10m/s. But currents tend to be large in these pinch points due to tidal fluctuations, not steady flow, so we’re just tapping into the tidal energy budget—[previously characterized as a niche source](https://dothemath.ucsd.edu/2011/12/can-tides-turn-the-tide/ "Do the Math: Tidal Power"). To the extent that steady-current pinch points exist, they make a natural choice for locating underwater turbines, but such places are limited—especially in terms of area or they would not be “pinch” points—so the total power available is small.

#### Given a Choice?

We saw that a given rotor area will deliver comparable power whether placed in open ocean currents or on land in a moderate wind. Now I ask you: is it easier/cheaper to put a giant turbine on land, or upside-down at sea? Think about access for maintenance, salt water corrosion, transmission of electric power, all the bruised fish, etc.

### Wave Energy

Most of us have marveled at the awesome power of waves crashing into a beach, pier, or headland. It’s enough to knock us over, unlike solar or wind power. And all that coastline—surely it’s a winner!

#### Wave Energetics

Waves represent third-string solar energy: solar energy is absorbed by land and sea, making thermal gradients in the air that generate wind. Wind then pushes on the surface of water, building up waves. The wind-wave interaction is self-reinforcing: the higher a wave sticks up, the more energy the wind can dump into it. Many of the waves arriving on a coastline were generated in storms somewhere across the ocean.

The Earth absorbs about 120,000TW of solar energy (that which isn’t directly reflected). About 1% of this ends up being dissipated in winds (1200TW). Of this, about 5% ([60TW](http://www.whoi.edu/science/po/people/rhuang/publication/2004Waves.pdf)) goes into wave generation. Some of this fights itself (wind against wave), some wave energy dissipates on its own via viscosity and turbulence, and some gets eaten up in shallow waters (e.g., around archipelagos) without making landfall. All of these chip away at the amount of wave energy accessible near land. I might venture a guess that we receive something comparable to our 13TW global demand on our shores.

I want to satisfy myself with a ground-up estimate to see if the numbers make sense. Let’s say a 2m-high wave (trough to crest) arrives every ten seconds, traveling at a jogging speed of 3m/s. The waves are therefore 30m apart. Each meter of wave-front then has a volume of about 30 cubic meters (average height is 1m above the trough for a sinusoidal shape). The gravitational potential energy, *mgh*, above the trough comes to 225kJ, and the kinetic energy, ½*mv*², is 135kJ. If we were able to capture *all* of this energy, we would collect 360kJ every 10 seconds, or 36kW of power for each meter of coastline. Compared to solar or wind power density—at approximately 200 and 30W/m², respectively—this sounds like a huge number: 36,000W/m. But the fact that the denominator is *linear* in length and not a *square* makes a gigantic difference. The Earth has far more square meters than linear meters of coastline.

Happily, my figure compares well with values you can find by searching for “wave energy potential map” in Google. A 2000km coastline might therefore net 70GW if one could catch all the energy at 100% efficiency. The lower-48 in the U.S. might then collect something like 200GW of wave power to the chagrin of surfers, representing something like 7% of the total domestic power demand. A [very recent report](http://www.mercurynews.com/business/ci_19777304?source=email) puts the wave energy off California’s 1800km coastline at 140TWh per year, working out to an average of 16GW—coming in a good deal less than my stupid calculation.

The [full report](http://www1.eere.energy.gov/water/pdfs/mappingandassessment.pdf "EERE wave energy assessment") for the U.S. cites a total available continental shelf wave energy for the lower 48 states as 910 TWh per year, amounting to 104 GW of continuous power. But only about half of this is deemed to be recoverable, totaling 54 GW. This puts it in the same ballpark as hydroelectric, if fully developed across our continental shelves.

Using my 35 kW/m number for a global calculation, I will make the crude estimate that there is enough coastline to circle the globe twice—considering that not all coastline faces the prevailing swell and is therefore penalized. Whatever. This makes for 80,000km of coastline, delivering 2.8TW—or about 20% of global demand, if fully developed.

A quick Google search shows estimates of global wave power of 2TW, 3.5TW, 1–10TW: all roughly consistent with my crude estimate.

#### Waves in a Box

The numbers push me into putting wave energy in the “niche” box, since my criterion for “potent” is the ability to satisfy a quarter of our need if *fully* developed. It might possibly qualify as potent, but it’s borderline. Where did the 60TW of total dissipation into wave energy go? A bit of digging suggests that half is lost in deep-water breaking (think of the “roaring 50’s” in the southern hemisphere). The rest is lost in wave-turbulence interaction and bottom friction. It would seem that there is greater inefficiency than I appreciated in delivering wave energy to land.

### Critters in Common

Each of the three energy resources we’ve discussed here require placement of energy conversion equipment into the sea. I’ve seen what sunken ships look like even after a few decades. They’re beautiful in one sense—teeming with colorful life—but not so much if functionality is more important. I cringe to think of the maintenance costs of our energy infrastructure placed out to sea.

### Washed Up?

The ocean covers 72% of the Earth’s area, absorbing vast amounts of solar energy as heat, moving around the globe in great conveyor belts, and capturing some fraction of wind energy in its waves. Ocean thermal earns a spot in the abundant box, ocean currents easily meet the potent criterion—being greater than wind potential, while waves fall short into the niche box. All three forms of ocean energy just add to the pile of alternative methods for creating electricity, being useless for heat or directly as transportation fuel.

Furthermore, only wave energy is conveniently delivered to our shores. Practically speaking, scaling facilities to capture ocean thermal and ocean current energy crosses a line of practicality that we are unlikely to exceed as long as other large-scale energy options (solar photovoltaics, solar thermal, wind, nuclear) remain more convenient. And yes, for all its complication, I would still guess nuclear to be easier to accomplish at scale than the ocean technologies. Anything on land gets an immediate boost in my book.

In this sense, ocean energy—much like solar energy in space, or pools of methane on Titan—falls into more of a “so what” category for me. Sure, it’s there, and I’m pleased to say it is even abundant. But practicalities will likely preclude us from pursuing it in a big way—at least in the near term when we face our great transition from fossil fuels. Wave energy is slightly less impractical, but the widely varying technologies I have seen demonstrated strike me as no more than cute, given the puny amount of power available in total.

So as I cast about looking for reasons why I should not worry about our energy future, I find little solace when I look to the sea. We’ll see nuclear fusion next week. No, really.

Hits: 1355

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2012%2F01%2Fthe-motion-of-the-ocean%2F&linkname=The%20Motion%20of%20the%20Ocean "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2012%2F01%2Fthe-motion-of-the-ocean%2F&linkname=The%20Motion%20of%20the%20Ocean "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2012%2F01%2Fthe-motion-of-the-ocean%2F&linkname=The%20Motion%20of%20the%20Ocean "Email")[](https://www.addtoany.com/share)
