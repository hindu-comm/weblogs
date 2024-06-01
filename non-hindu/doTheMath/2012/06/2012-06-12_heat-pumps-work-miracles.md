+++
title = "Heat Pumps Work Miracles"
full_title = "Heat Pumps Work Miracles"
upstream_url = "https://dothemath.ucsd.edu/2012/06/heat-pumps-work-miracles/"
date = "2012-06-12"

+++
Source: [here](https://dothemath.ucsd.edu/2012/06/heat-pumps-work-miracles/).

Heat Pumps Work Miracles

\[*An updated treatment of some of this material appears in Chapter 6 of the [Energy and Human Ambitions on a Finite Planet](https://escholarship.org/uc/energy_ambitions) (free) textbook.*\]

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/06/heat-pump-150x150.png "heat-pump")](https://dothemath.ucsd.edu/wp-content/uploads/2012/06/heat-pump.png)Part of the argument that we cannot expect growth to continue indefinitely is that efficiency gains are capped. Many of our energy applications are within a factor of two of theoretical efficiency limits, so we can’t squeeze too much more out of this orange. After all, nothing can be more than 100% efficient, can it? Well, it turns out there is *one* domain in which we can gleefully break these bonds and achieve far better than 100% efficiency: heat pumps (includes refrigerators). Even though it sounds like magic, we still must operate within physical limits, naturally. In this post, I explain how this is possible, and develop the thermodynamic limit to heat engines and heat pumps. It’s a story of entropy.

### Entropy, Quantified

Whole books can be written about the gnarly properties of entropy. Put simply, entropy is a measure of disorder. Strictly speaking, entropy is all about counting the number of quantum-mechanical states that can be occupied at a certain system energy. In this sense, the total entropy of a system is *S=k_(B)*ln(*Ω*), where *Ω* is the number of states available (a rather large number), ln(x) is the natural log function, and *k_(B)* is the Boltzmann constant, having a value of 1.38×10⁻²³J/K (Joules per Kelvin) in SI units.

Okay, that’s deep and cool, but let’s not bog ourselves down counting states. The main purpose of the previous paragraph is to indicate that entropy has a fundamental prescription, and that it carries *actual units*. Mostly entropy is discussed in a hand-wavy way, but it *can* be pinned down.

### Change Heat: Change Entropy

More relevant to *our* discussion is the thermodynamic result that if we add/subtract thermal energy (heat) to/from a thermal “bath” (large reservoir of thermal energy, like outside air, a body of water, rock) at a temperature *T*—measured on an absolute scale like Kelvin—the entropy changes according to:

> ΔQ=TΔS

We read this to mean that adding an amount of heat (*ΔQ*: negative if removing heat) will result in a concomitant increase in entropy (decrease if negative) with the bath temperature as the proportionality constant. Looking at this equation, the units of J/K for entropy (*S*) should make more sense.

Wait a minute! Did I just allow for the condition that entropy could decrease? Isn’t one of the fundamental rules of thermodynamics that entropy can never go down?

Almost right. The entropy of a *closed system* cannot decrease. But it can easily decrease locally at the expense of an increase elsewhere. You can re-stack books on the shelves after an earthquake, restoring order.
But via exertion, you transfer heat to the ambient air in the process—increasing its entropy.

### Moving Heat

A **heat pump**, rather than *creating* heat, simply **moves heat**. It may move thermal energy from cooler outdoor air into the warmer inside, or from the cooler refrigerator interior into the ambient air. It pushes heat in a direction counter to its normal flow (cold to hot, rather then hot to cold). Thus the word *pump*.

So let’s imagine I have a cold environment at temperature *T*_(c) and a hot environment at *T*_(h). Cold and hot are relative terms here: the “hot” environment could be uncomfortably cool—it just needs to be hotter than the “cold” environment.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/06/heat-pump-245x300.png "heat-pump")](https://dothemath.ucsd.edu/wp-content/uploads/2012/06/heat-pump.png)If I pull an amount of heat, *ΔQ*_(c) out of the cold environment and put it into the warmer environment, I reduce the entropy in the cold region by *ΔS*_(c)=*ΔQ*_(c)/*T*_(c). Both *ΔQ*_(c) and *ΔS*_(c) are negative in this case.

Inevitably, I have to run some machinery to affect this flow of heat against the natural gradient (pushing heat uphill). Let’s call the amount of work (energy) needed to force this thermal extraction *ΔW*. That mechanical/electrical/whatever energy also ultimately turns to heat, and if I cleverly send this additional energy to the hot place, I end up pumping an amount of heat into the hot environment that is *ΔQ*_(h)=−*ΔQ*_(c)+*ΔW* (just the sum of the two; as indicated by arrow thicknesses in the diagram above).

The entropy change in the hot environment is determined by *ΔS*_(h)=*ΔQ*_(h)/*T*_(h). Because total entropy must increase, we need the sum of entropy changes to be positive: *ΔS*_(c)+*ΔS*_(h)\>0—remembering that *ΔS*_(c) is negative.

So where does this leave us? If we’re trying to heat a home, we care about how much heat is delivered into the home: *ΔQ*_(h)=−*ΔQ*_(c)+*ΔW*. And we’d like to do as little work, *ΔW*, as possible to pull this off. So an appropriate figure of merit is *ε*=*ΔQ*_(h)/*ΔW*.

A little algebra with the relations above (the steps are shown in the following graphic) results in the maximum efficiency of a heat pump of *ε\<T*_(h)/*ΔT*, where *ΔT=T*_(h)−*T*_(c) is the temperature difference between hot and cold baths.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/06/entropy-eff-300x255.png "entropy-eff")](https://dothemath.ucsd.edu/wp-content/uploads/2012/06/entropy-eff.png)If, instead, you want to cool something down (refrigeration, A/C), the figure of merit is how much heat is removed from the cold zone divided by the input work: *ε*=−*ΔQ*_(c)/*ΔW*. In this case, the maximum efficiency works out to *ε\<T*_(c)/*ΔT*.

#### Heat Engines

As an aside, if we turn the heat flow around, so that *ΔQ*_(h) flows naturally *out* of the hot source (*ΔQ*_(h) is negative in this case) and a lesser *ΔQ*_(c) flows *into* the cold source (positive), the same entropy considerations lead us to derive a maximum amount of work that is extractable from the heat flow, and the efficiency, *ε=ΔW/ΔQ*_(h) works out to be no better than *ΔT/T*_(h). (The bolder among you may want to take up the algebraic challenge.) This is the familiar thermodynamic limit for the amount of work obtainable from a **heat engine**, like a car’s engine, a coal-fired power plant, or even a nuclear plant. The reason we hit a maximum efficiency is really all about not violating the second law of thermodynamics: that the total entropy of a system may never decrease.

### Extreme Efficiency

The remarkable thing about the heat pump efficiencies we derived above is that *ΔT* is *in the denominator*! Since *T* is absolute temperature (Kelvin), typical situations will have *T*≈300K, and *ΔT* often a few tens of Kelvin—leading to efficiencies around **10×**, or 1000%!! *How can this possibly be true?* It seems like a total cheat on nature.

The key is that unlike an electric coil or a flame, the heat pump does not *create* the thermal energy, it *moves* thermal energy that already exists. A heat pump is always moving thermal energy from a cooler environment to a warmer one. That means that a heat pump heating a house in the winter is grabbing heat from outside and shoving it inside. This may seem counter-intuitive, but I assure you, even freezing air has plenty of thermal energy, being hundreds of degrees above absolute zero. Capturing some of that energy and moving it can take a lot less energy than creating it directly.

One aspect of heat pump efficiency worthy of note is that the theoretical limit gets better as *ΔT* gets smaller. So a refrigerator in a hot garage will not only have to work harder to maintain a larger *ΔT*, but it becomes *less efficient* at the same time, compounding the problem. Likewise, heat pumps operate more efficiently in mild-winter climates than in extreme arctic zones. For instance, the theoretical efficiency of a heat pump operating between 293K indoors (20°C, or 68°F) and freezing outside is 293/20=14.7, while a frigid −20°C (−4°F) would only allow a theoretical efficiency of 7—half as good.

### COP and EER

If shopping for heat pumps, one should look for the specification called the Coefficient of Performance, or COP, which is essentially the same *ε*=*ΔQ*_(h)/*ΔW* metric from before. Realized values are typically around 3–4. This is a factor of several below the theoretical limit, as is so often the case. But still, it’s **rather impressive** to me that I can add 4J of heat energy into my home while expending only 1J to make it happen (apply any energy unit you wish: kWh, Btu, etc. and get the same 4:1 ratio for a COP=4).

But before we get carried away, let’s say your electricity comes from natural gas turbines, converted to electricity at 40% efficiency (via a heat engine). Coupled with a heat pump achieving a COP of 3.5, each unit of energy injected at the natural gas plant yields 0.4×3.5 units of thermal energy in the home, for a net gain of 40% over just burning the gas directly in the home. I’ll take the gain, but the benefit goes from overwhelming to just plain whelming. If carbon intensity is your thing, then a heat-pump supplied with coal-fired electricity does worse than burning gas directly in a home furnace, since coal generates 70% more CO₂ per unit of energy delivered than does gas, eating up the 40% margin previously detailed. We only get the full factor of 3.5 improvement if replacing *electric* heat.

For cooling applications, one may also see a COP reported. But in the U.S., the efficiency metric is often the Energy Efficiency ratio, or EER The EER. is a freak of nature, and I hope it asphyxiates on its own stupidity. It is the rate of heat extraction, in Btu/hr, divided by the electrical power supplied, in Watts. Geez—Btu/hr is already a power: 1Btu/hr is 1055J in 3600s, or 0.293J/s=0.293W. Why complicate things?! So multiply EER by 0.293 to get an apples-to-apples comparison, arriving at a COP for cooling that corresponds to our measure from before: *ε*=−*ΔQ*_(c)/*ΔW*. Air conditioners getting EER values above about 11 qualify as Energy Star, corresponding to a COP above about 3.

### My Fridge Performance

I had a thought that I could test the \> 100% efficiency delivered by a heat pump by watching my fridge go through a defrost cycle. The idea is that a bunch of heat is dumped into the coils periodically to melt accumulated ice. I noticed that the first cooling cycle after the defrost is always longer, as the deposited heat must be removed.

My fridge normally runs on an off-grid stand-alone photovoltaic (PV) system, and I record the system energy expenditures at 5 minute resolution. I see defrost cycles routinely in the data (every day or two). But because of the coarse sample rate and the indirectness of the measurement (measuring battery current, not AC power), I prefer to use TED (the energy detective) data, when available. During unusually cloudy periods, the PV system switches over to utility input, in which case the fridge is monitored by TED and I get one minute samples of direct AC power. One such sequence is shown for my fridge in October, 2011.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/06/fridge-111020-1024x768.png "fridge-111020")](https://dothemath.ucsd.edu/wp-content/uploads/2012/06/fridge-111020.png)

A prominent defrost cycle consumed 155Wh of energy. The energy and average power associated with each cooling cycle is also shown.

We can see in the figure above a baseload power of 108W, two normal fridge cycles preceding the defrost pulse at 12:30 AM (and a partial cooling cycle on its leading edge). The first cooling cycle after the defrost deposit is obviously longer than the rest, and subsequent cycles may be slightly fatter and more frequent. The energy expenditure (above baseline) is reported for each cooling pulse in Watt-hours, as is the corresponding average cooling-cycle power measured from the start of one pulse to the start of the next.

Performing a careful accounting for the energy expended while cooling vs. the energy deposited during defrost, and projecting the rate of power use prior to defrosting (43W) forward, we find that we would have expected to spend 163Wh over the time interval between the first cooling cycle and the last (the pre-cycles are 19.7Wh each), but the actual expenditure cooling was 184Wh, leaving an extra 21Wh-worth of cooling (roughly equivalent to one extra cycle). Meanwhile, the defrost activity expended 155Wh in 23 minutes (400W). So it took 21Wh of wall-plug energy in cooling mode to remove 155Wh of deposited thermal energy, implying a coefficient of performance around 7.5!

Impossibly high, methinks. One problem is that the defrost cycle puts energy into melting ice, which subsequently runs out to a drip pan below the refrigerator. So the refrigerator does not later need to remove this heat: it found another sort of exit. The heat of fusion barrier that must be overcome amounts to 334J/g (compared to about 20J/g to raise the temperature of water by 5°C, or ice by 10°C). If the defrost cycle produces two cupfuls of water (about a half-liter) each time, the investment is approximately 50Wh of energy. This brings the COP estimate down to 5. Additionally, since time elapses after the defrost injection is complete, some portion of the heat no doubt diffuses out from the cold coils to the hot fins before the cooling kicks in.

In retrospect, the defrost cycle is not the best way to experimentally determine the COP—despite the fact that the “experiment” runs all the time without my having to lift a finger.

### A More deliberate Experiment

Taking matters into my own hands, I rigged an incandescent light bulb operating on a timer and stuffed in the fridge (in a clip-light fixture). I set the timer to pop the light on from 3AM to 4AM, figuring the fridge would be perfectly quiescent (no door openings, etc. during that time). A couple of long, tapered pieces of wood provided a channel for the cord without compromising the door seal. I shifted the fridge over to utility for the night so TED would catch the action. It took three times to get a good result. “When are you going to take that light out of the fridge?!”

#### Take One

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/06/fridge-pic1.jpg "fridge-pic1")](https://dothemath.ucsd.edu/wp-content/uploads/2012/06/fridge-pic1.jpg)

Initial location of light in upper left of refrigerator volume

I placed the light high in the refrigerator, and shone the light onto aluminum foil on an otherwise empty glass shelf (the foil was to keep direct light off the food below). The data were beautifully collected, but the refrigerator stayed on the entire time the light was on. The bulb was rated at 60W, and the refrigerator typically runs around 120W, so instantly I knew the measurement indicated a COP less than 1. Not good.

I presume the bulb was near enough to the thermostat as to elevate the local temperature and fool the refrigerator into staying on the full time. Bet the ice cream got rock hard…

#### Take Two

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/06/fridge-pic2.jpg "fridge-pic2")](https://dothemath.ucsd.edu/wp-content/uploads/2012/06/fridge-pic2.jpg)

This time, the light is lower in the fridge.

I moved the light to a lower portion of the refrigerator, hopefully well-enough baffled that the thermostat would not be impacted. This time, I was foiled by a sleepless wife, who turned on and off all manner of electrical devices during the course of the experiment. The refrigerator itself was not disturbed, and if pressed, I could still identify cooling cycles and extract useful data. Just like in astronomy, crummy nights produce crummy data, and you have to work much harder to get marginally useful results. Better to wait for a clear night, if you can. I could at least see that the fridge *cycled* this time during the light-on phase.

#### Take Three

Fool me once, shame on you. Fool me twice, shame on me. Since the saying has no “thrice” aspect, I felt I had no choice but to make it work. Actually, I did nothing different (no straps to confine wife to bed—patience was already wearing thin on the interminable experiment in the refrigerator). But fortunately, a quiet night resulted in a clean dataset.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/06/fridge-bulb-1024x768.png "fridge-bulb")](https://dothemath.ucsd.edu/wp-content/uploads/2012/06/fridge-bulb.png)

Light pulse demanded more cooling. Note coincidental defrost at end.

The bulb turned out to expend energy at a rate of 52W. Subtracting a baseload of 44W, the first five cycles averaged 35.4W to keep the fridge cold. The light bulb was on for a bit over 56 minutes, depositing 49Wh of energy. From the time the light bulb came on until the end of the last cooling pulse before the defrost cycle began (spanning 131 minutes), five cycles totaled 57 minutes of on-time, using 113Wh of electrical energy. Yet we would have expected 35.4×131/60=77Wh at the nominal rate. Thus the refrigerator consumed an extra 36Wh of energy to remove the 49Wh deposited by the light. We calculate a COP of *ΔQ*_(c)/*ΔW*=49/36=1.36.

Hmmm. Not in the ballpark of 3. It’s bigger than 1, at least—indicating *some* degree of heat-pump magic. But I am disappointed in the result.

#### Reflections on the Experiments

My mode of testing certainly deviated from the intended operation of refrigerators. A concentrated pulse of constant heat is not *quite* the same as putting warm food into the refrigerator. It may also be that the freezer achieves a COP around 3 while the refrigerator volume does not. I would be curious to know how the COP is actually measured. Do we realize similar values in daily operation? After all, the light bulb test fell short. If I average the ice-melt-corrected defrost value and the light bulb value, I get a COP around 3, but I have no solid justification for performing this average.

Alternative tests may include placing a known thermal mass into the refrigerator and seeing how much energy is required to bring it to temperature. Door access is a problem, though.

### Close the Door!

While I’m on the subject of refrigerators, how about a quick detour to assess how problematic it is to stand with the door open, or to repeatedly and inefficiently access items within. Should I be irked?

Let’s say the inner refrigerator volume is half a cubic meter (about 17 cubic feet; American freezer + fridge often are in the low 20’s). Air has a specific heat capacity of 1000J/kg/K. At a density of 1.2kg/m³, we’re talking 0.6kg of air, total. And let’s assume a *ΔT* of 20K between ambient air and fridge air.

A *complete* air exchange then costs 12kJ (3.3Wh). Even at a COP of 1.0, the refrigerator will remove this amount of energy in 100 seconds at a power of 120W. It’s a tiny fraction of the daily work of the refrigerator: 0.3%.

A more serious problem is condensation. If the outside air is saturated (100% humidity), containing about 20 g/m³ of water, we deposit 10 g into the fridge. The latent heat of vaporization means that 2257J are deposited for every gram of water condensing, plus about 800J to cool the water down. In total, we drop another 23 kJ (6.5Wh) of energy into the fridge.

So depending on how moist the air is, we may drop anywhere from 12–35 kJ. Our 0.3% becomes a 1% effect. Open the fridge 20 times in a day, and you might have a significant issue.

Another consideration is that each door opening may trip the thermostat before it ordinarily would have been. In doing so, the cooling “schedule” advances forward, and could result in more “on” activity than would otherwise occur.

### Parting Perspective

Heat pumps are really cool, and seem to violate our sense that 100% is the best efficiency we can ever get. Cooling applications have little choice but to use heat pumps, as cooling inevitably involves getting rid of (moving; pumping) thermal energy. Heating applications can see a factor of three or more increase in efficiency over direct heating.
Increasingly, the stable thermal mass of the ground is used as the “bath”—often erroneously referred to as geothermal.

So I’m generally a fan of seeing more use of heat pumps. Replacing direct electrical heating with a heat pump is a clear win. Replacing a gas furnace with a heat pump is a marginal win if your electricity comes from gas; not so much for coal-derived electricity. But heat pumps pave the way for efficient use of renewable energy sources, like solar or wind. In this sense, getting away from gas furnaces while promoting non-fossil electricity generation may be the best ticket—especially when coupled with concerns over global warming.

Hits: 9333

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2012%2F06%2Fheat-pumps-work-miracles%2F&linkname=Heat%20Pumps%20Work%20Miracles "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2012%2F06%2Fheat-pumps-work-miracles%2F&linkname=Heat%20Pumps%20Work%20Miracles "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2012%2F06%2Fheat-pumps-work-miracles%2F&linkname=Heat%20Pumps%20Work%20Miracles "Email")[](https://www.addtoany.com/share)
