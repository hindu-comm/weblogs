+++
title = "Let’s Blow this Joint"
full_title = "Let’s Blow this Joint"
upstream_url = "https://dothemath.ucsd.edu/2013/03/lets-blow-this-joint/"
date = "2013-03-05"

+++
Source: [here](https://dothemath.ucsd.edu/2013/03/lets-blow-this-joint/).

Let’s Blow this Joint

I have a confession to make. When we moved into our current house three years ago, we had to sell our clothes dryer due to gas/electric incompatibility (happens every time we move!). So we lived without a dryer for three years, hanging clothes out to dry, and generally being frugal about washing vs. re-wearing clothes. Well, after several weather-induced trips to the laundromat this winter, we (or can I lay this all at my wife’s feet?) finally broke down and bought a used washer/dryer set on Craigslist. We’ll still let the sun dry our clothes 95% of the time, but have other options now.

Even though this little vignette *does* relate to the common Do the Math theme of [![](https://dothemath.ucsd.edu/wp-content/uploads/2013/03/blower_front-150x150.jpg "blower_front")](https://dothemath.ucsd.edu/wp-content/uploads/2013/03/blower_front.jpg)[low-energy lifestyles](https://dothemath.ucsd.edu/2012/05/my-neighbors-use-too-much-energy/ "My Neighbors Use Too Much Energy"), the actual point of bringing it up is that the washer/dryer came from a house that had just been on display as a model for energy efficiency—including the washer and dryer. At the house, we met Jason Beckman, of Classic Residential, Inc., who had carried out many of the efficiency upgrades to the house. I thought it would be instructive to have him perform an energy audit at our home—especially a blower door test to expose ventilation issues.

As a bonus, after the nominal audit activities were over, I was able to spend some quality time with the blower door, doing extensive tests in virtually every room in the house. What I found was certainly instructive for me, and hopefully will be useful to a broad audience as well.

## Drafts Prevent Suffocation

Air infiltration can be a major piece of a house’s thermal loss budget. We all know that “drafty” homes are cold in the winter. Yet obviously we need enough circulation to breathe. As reported in [a previous post](https://dothemath.ucsd.edu/2012/11/this-thermal-house/ "This Thermal House"), one can find several different standards for air exchanges per hour. Modern construction aims for a “tight” house to register 0.35 air exchanges per hour. Effectively, this means that the rate of air infiltration (in m³/s or cfm: cubic feet per minute) divided by the volume of the living space should come out to something around three hours. [Another site](http://www.toolbase.org/Home-Building-Topics/Remodeling/house-air-leakage "toolbase.org: air leakage")
points to ASHRAE Standard 62.2, which uses a more targeted approach specific to a home’s footprint. For example, my home calculates to an ideal rate of 0.22 air exchanges per hour. I have also seen a building tightness limit (BTL) standard of 15 cubic feet per minute per occupant, which translates to 0.15 exchanges per hour for my situation. Just open the window a crack if guests stay over…

## Blower Door Concept

A blower door is a fan that fits into a doorway, and seals against the doorframe so that a house may be pressurized (or depressurized) by the action of the fan. A two-channel pressure meter (manometer) monitors the difference between internal and external pressure, and also between internal and fan intake pressure. The latter maps to the rate of airflow provided by the fan.

In a typical test, the house is pressurized to 50Pa (1 Pascal is 1 N/m² or about 0.00015 psi), and the airflow rate is measured. I think of it as being analogous to an electrical circuit: the pressure corresponds to voltage; the airflow is current; the ratio of pressure to airflow (voltage to current) is *resistance*—just as in Ohm’s law. So the goal is to measure the “tightness” or resistance to airflow of the house.
For reference, 50 Pa is the amount of pressure difference one experiences by descending 3.5 m (~11 ft) down a hill, or “diving” under 5 mm of water. In other words, your ears don’t pop due to the change.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2013/03/blower_LR.jpg "blower_LR")](https://dothemath.ucsd.edu/wp-content/uploads/2013/03/blower_LR.jpg)

Blower set up in living room, in door to (open) garage. The sealed central air intake is seen at lower left. The manometer sits on the arm of the chair. The door to the rest of the house, at left, is taped all around (plus a towel for good measure). Different “range configurations” are available for the fan intake: here shown with eight equal holes open.

Let’s hang some numbers on the concept. The interior air space in my house (excluding walls) is 1540 square feet (143m²). This makes for a volume of 12,300ft³ (350m³). When I pressurize my house to 50Pa, I find a calibrated airflow of about 2530cfm (cubic feet per minute; 1.17m³/s). Divide these two numbers and we get 5 minutes. So this suggests 12 air exchanges per hour under a 50Pa pressure differential. We could express the house’s resistance (in the tragic units of Pa/cfm) to be 0.02.

Because we only have two pressures at play, and all leaks between the inside and outside act in parallel, we will be better served by characterizing the *conductance* of the house: the inverse of resistance. In this case, my house has a conductance of 2530/50=50.6cfm/Pa.

But the blower door imposes an extreme condition on the house in terms of differential pressure. How do we translate this into normal conditions? After all, the implied 12 air exchanges per hour is 60 times bigger than my ideal target of around 0.2.

## Calibrating to Normalcy

The blower door asserts 50Pa of pressure, and although this is only 0.05% of atmospheric pressure (~10⁵Pa, or ~15psi), it is substantially larger than natural conditions tend to produce. And natural conditions vary from one place to the other. We’re really talking about wind here: it is the interaction of wind with a house that creates pressure differentials inside and outside of the house.

The Lawrence Berkeley Laboratory has defined a [correction factor (PDF)](http://www.waptac.org/data/files/Website_docs/Technical_Tools/Building%20Tightness%20Limits.pdf "LBL N factor chart/map") by zone for the U.S. and Canada. The conversion factor tends to be around 20, implying that a natural pressure differential between inside and out is around 2.5Pa. Interpreting this as a Bernoulli pressure or ram pressure for moving air: *p*=½*ρv*², where *p* is pressure, *ρ* is air density (1.2kg/m³), and *v* is velocity in m/s, we equate 2.5Pa with a wind velocity of 2m/s (4.4m.p.h.), which seems perfectly reasonable.

For San Diego, a normally-shielded (by trees, structures) single-story house has a conversion factor of 24.5. It’s higher because San Diego is less windy than the average location. Let’s call it 25, so that my normal pressure differential is 2Pa. Scaling down the 2530cfm measurement, I would then expect a natural airflow rate of 100cfm, amounting to about 0.5 air exchanges per hour. So my house is not nearly as bad as I expected: not terribly far from the tight building standard of 0.35 exchanges per hour (72cfm for me), but still a factor of 2.2× the more targeted ASHRAE standard (45cfm for me).

## Thermal Impact

We care about limiting ventilation primarily for thermal reasons. We don’t want ambient air (hot or cold) infiltrating our house and defeating our efforts to stay comfortable. So how serious is a bit of leakage? For every 100m² (1076ft²) of floorspace, an air exchange rate of once per hour will require 85W of power for every 1°C (1.8°F) of temperature difference between inside and outside. So if it’s at the freezing point outside and 20°C (68°F) inside, an air exchange rate of once per hour will require 1700W to neutralize (per 100m² of floorspace).

Putting this into perspective, the ugly theorist’s home modeled in [a previous post](https://dothemath.ucsd.edu/2012/11/this-thermal-house/ "This Thermal House") with a floor area of 225m² had a thermal loss rate of 280W/°C when fully insulated. If this house has an air exchange rate of once per hour, we add 190W/°C, nearly doubling the energy required for warmth (or significantly lowering the temperature inside if you, like me, don’t habitually heat your home). Cutting this by a factor of three to achieve the “tight” standard of 0.35 exchanges per hour results in air infiltration dropping from a 40% contribution to a 20% contribution.

So air leaks certainly can be responsible for a substantial fraction of thermal loss. For my house, the (measured) impact translates to 60W/°C (72 when the fireplace damper is left open, as it had been for years). This is clearly an important thermal contribution, but not nearly enough to explain the horrendous (measured) heating requirement of 1465W/°C for my house, as detailed in [an earlier post](https://dothemath.ucsd.edu/2012/09/rocking-the-ac/ "Rocking the AC"). I had hoped that sticking a blower door on my house would allow me to account for the difference, and reveal the culprits that I could then remedy. I still have a mystery on my hands, but nonetheless managed to learn a bunch from the blower door experiments.

## Blower Door Extravaganza

Getting a whole-house measurement from a blower door is a useful bit of information. But just as it is hard to decide on specific energy reductions by looking at a monthly energy bill, it is hard to know what the blower door test is telling us to *do*, without performing some breakdown.

Seeing how much fun I was having gathering blower door data, Jason was kind enough to give me some time alone with the blower door. We did it in every room. No—my wife is *not* jealous; accustomed, more like.

### Room by Room

The first interesting test one can perform is to close all interior doors in the house to reduce the volume under test by the (front door) blower. Then opening up one door at a time provides an understanding of that room’s contribution. Because the blower senses and maintains a constant pressure difference, the airflow through any given leak is not altered by the opening or closing some other part of the house. In what follows, I will quantify each room’s conductance in units of cfm/Pa (straight division of cfm read off the meter by the 50Pa operating point). Adding conductances for every room should match the whole-house measure. Since the whole house measured 2530cfm, the total conductance is 50.6 units.

I should note from the start that closing doors is an imperfect sealing technique. Gaps around the edges (especially the base) can let a substantial amount of air whistle through. In fact, I found that simply closing the door can still let 50% of the airflow get through. Putting a towel at the bottom of the door can knock this down to 20% flow. But in my tests, I taped around all four edges of each door with painter’s tape to be sure I cut off the room entirely. I was amazed at how much air could move through a doorjamb gap even when it looked reasonably snug by eye.

The other necessary preparation for this room-by-room test is sealing off all central heating/cooling vents and intake. Otherwise the rooms are still connected by unseen tubes, and sealing off a door is wasted effort. Technically, one vent or one intake could be left open, but we’ll get to that later.

Below is a table of the separate partitions in my house and how much conductance I found for each, along with some indication about what makes that room have the characteristics it does. Cans refer to can lights. Doors refer to external-access doors.

|                 |          |                                                       |                 | |-----------------|----------|-------------------------------------------------------|-----------------| | **Section**     | **Area** | **Features**                                          | **Conductance** | | Kitchen/DR/Hall | 29%      | fireplace, 7 cans, hood/vent, attic access, 2 windows | 17.8            | | Master Suite    | 28%      | double door, 8 cans, two vent fans, 2 skylights       | 11.8            | | Living Room     | 24%      | sliding door, door to garage, 10 cans, skylight       | 8               | | Guest Bath      | 2.7%     | vent fan, 3 cans, skylight                            | 5.4             | | Bedroom         | 9.1%     | 1 window                                              | 1.6             | | Bedroom         | 2.4%     | 1 window                                              | 1.2             | | Ducting         | —        | intake and 12 vents                                   | 4.8             |

The common area connected to the front door in my house includes the kitchen, dining room, and hallway. Of significance, this space hosts a fireplace, a ventilation hood, 7 can lights in the ceiling, and three central air ducts. I measured a conductance of 17.8 (890cfm at 50Pa). Opening the fireplace damper added a whopping 11 units of conductance.

Opening up the guest bathroom (3 can lights, one exhaust fan, one skylight) showed its conductance to be 5.4 units. The master bedroom suite (two exhaust fans, 8 can lights, two skylights) displays a conductance around 12. The living room (10 can lights) has an intermediate conductance around 8. Two smaller bedrooms have relatively tiny conductances between 1–2 units.

The ducting for heating/cooling—though seldom used in my house— contributes nearly 10% of the air infiltration due to leaks in the ductwork.

So now I know where I stand room by room. This can help focus attention on the worst areas. But to really dig down, some nit-picky detail work needs to be done.

### Really Room by Room

My next round of explorations involved setting up the blower door in individual rooms to measure their airflow in isolation of the rest of the house. The numbers were generally consistent with the whole-house approach, if not tending to be a little higher (suspect some leakage around blower foor frame). But the main advantage of narrowing the scope of the blower was that I could detect relatively small changes from sealing one thing or another.

Here’s what I learned, in a nutshell:

- Can lights average about 0.4 cfm/Pa apiece. Taken together, the 28 can
  lights in my house contribute 22% of the air infiltration. - The central air ducting in my home accounts for 9% of the leaks. My
  ductwork is not particularly leaky. The energy audit turned up an 8%
  loss rate of forced air used for cooling/heating. Under 10% is
  considered good, and 6% is a “green” home target. - Bathroom ventilation fans contribute an average of 1.6 cfm/Pa apiece.
  The three fans in my home contribute 9% of the air infiltration. - A poorly-sealed stove hood duct (where it goes into the attic)
  contributes 2.7 cfm/Pa, amounting to 5% of our house’s loss. - Electrical outlets and light switches average 0.03 cfm/Pa apiece.
  While this is a small number, my house contains about 75 instances,
  amounting to about 2.3 cfm/Pa, or 4.5% of the house. - The attic access hole, covered with a slightly bent piece of
  sheetrock,  
  contributes 2 cfm/Pa, or about 4% of our house total. - The fireplace, with damper closed, still drew 0.9 cfm/Pa, making for a
  1.7% house contribution.

Lots of nickel-and-dime stuff here. Adding it all up, I can account for over half of the air loss in the house. I suspect that the remainder is from doors, windows, plumbing entry/exit, and the odd gap hiding behind baseboards or other moulding. But the good news is that I have a list of action items that collectively could make my house twice as tight as it is. Throw on some better door seals and pay attention to plumbing entry/exit and I may even be able to accomplish a factor of three reduction.

## Is it really so simple?

I’ve been treating my house like a big resistor following the oh-so-linear Ohm’s Law analogy. Does this assumption hold up? I did a mapping of airflow vs. pressure in steps of 10Pa, finding that the relationship is sub-linear. In particular, I found an exponent of 0.66. For example, at one point I had tightened down my common area to 645cfm at 50Pa (started at 890; could have gone to 435 if I blocked all known offenders), then measured airflow at different pressures. I got the curve shown below, with a fit of 225×(*P*/10Pa)^(0.66).

[![](https://dothemath.ucsd.edu/wp-content/uploads/2013/03/press-curve-1024x768.png "press-curve")](https://dothemath.ucsd.edu/wp-content/uploads/2013/03/press-curve.png)It was only after this that I understood one of the features of the manometer I was using for the blower door test. If the system could not achieve the pressure setpoint (due to excessive airflow for its range configuration), it would extrapolate to the standard value—usually 50Pa. The user had a choice for which exponent to use in the extrapolation. From the manual:

> **n**: sets the slope of the @-Pressure extrapolation line. Use 0.65 > for tight houses and 0.60 for ducts and large buildings.

So there we are. Confirmed experimentally in Joe Random House.

What this means is that the factor of 20 (or 25 in San Diego) adjustment used to convert the 50Pa test into natural conditions does not simply map to 2.5 (or 2.0) Pascals of inside/outside pressure differential in the linear way. Instead, we hit a factor of 20 in flow at a pressure of 0.53Pa indoor/outdoor differential. The implied wind speed using a simple Bernoulli pressure is now down to about 1m/s, but I’m not going to worry myself over what this means in practice. What I *can* say is that windier days will increase the indoor/outdoor pressure differential and promote more vigorous air exchange according to something like the graph above. The fact that the curve is steep at its beginning means that small changes in pressure/wind can have outsized impacts on airflow.

### A Side Experiment

While checking an especially tight room, I had the blower at 50Pa of pressure and only 125cfm of flow. Then I opened the window to a 1-inch (25mm) gap, 44 inches tall. The airflow soared higher by 550cfm. At half that gap width, I saw a 340cfm increase over the baseline. Half again and we’re at 255cfm. Then I closed the window until I saw no daylight, but it was not pushed all the way into its housing against the seal: 85cfm over the baseline. Roughly, we’re looking at a scaling law with an exponent around 0.55 as a function of crack width. This general curve shape is again indicating that gaps and cracks don’t act linearly: reducing the area of a gap by a factor of two or four reduces the flow not by the same factors, but by about 1.5 and 2, respectively. So attention to detail becomes important. The little gaps matter. This is also reflected in my finding that I had to tape all sides of a door, even if the gap looked tight, in order to knock out all the flow.

## My Take-Away

I am simultaneously pleased and disappointed by the blower door results. In the plus column, I now have a measure of my house’s permeability, and can point to over 50% of the offenders, which means I can start knocking them off at will. Additionally, my house was not a drafty embarrassment by modern green standards, which I fully expected to be the case. On the down side, the source of almost half my air leaks remain mysterious—although I do have my suspicions. Also, the air leaks I measure cannot come close to accounting for the exorbitant heating/cooling requirements I previously measured for my house. The books remain open. One approach at this stage would be to seal up known leakers (at known impact), and repeat a heating/cooling test.

For my action items, I could retrofit my can lights with airtight trim units. Since we generally do not use our central air services, I could make sure all the vents are closed (even if imperfect) and even seal off the intake in an easily reversible way (substitute a piece of plywood for the air filter). Sealing the hood vent’s attic penetration is a quick and easy job. Likewise for the attic access. Updated door seals and stuffing old socks around plumbing penetrations may buy a little bit as well. I am less sure about finding bathroom vents that aren’t leaky. They usually have a flap that rests against the exhaust tube when the fan is off, but maybe better designs exist that are more completely sealed when not in use. And I don’t know if it is code-compliant to have a fully-sealed fireplace that is fitted with a gas line.

All the same, I have some work to do. And most rewarding: I have a sense for the sources and relative scales of airflow problems in houses.

Hits: 1197

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2013%2F03%2Flets-blow-this-joint%2F&linkname=Let%E2%80%99s%20Blow%20this%20Joint "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2013%2F03%2Flets-blow-this-joint%2F&linkname=Let%E2%80%99s%20Blow%20this%20Joint "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2013%2F03%2Flets-blow-this-joint%2F&linkname=Let%E2%80%99s%20Blow%20this%20Joint "Email")[](https://www.addtoany.com/share)
