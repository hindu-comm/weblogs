+++
title = "Battery Performance"
full_title = "Battery Performance Deficit Disorder"
upstream_url = "https://dothemath.ucsd.edu/2012/08/battery-performance-deficit-disorder/"
date = "2012-08-21"

+++
Source: [here](https://dothemath.ucsd.edu/2012/08/battery-performance-deficit-disorder/).

Battery Performance Deficit Disorder

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/04/800px-Chevrolet_Volt_WAS_2010_8845-150x150.jpg "800px-Chevrolet_Volt_WAS_2010_8845")](https://dothemath.ucsd.edu/wp-content/uploads/2012/04/800px-Chevrolet_Volt_WAS_2010_8845.jpg)Batteries fail—as certainly as death and taxes. Rechargeable batteries at least offer the possibility of repeating the cycle, so are in this sense more like recurrent taxes than death. But alas, the story cannot repeat indefinitely. One cheerful thought after the other, yes? But wait, there’s more… Add to their inevitable demise an overall lackluster performance in battery storage technology, and we have ourselves the makings of a blog post on the failure of batteries to live up to their promises.

To set the stage, the specific energy of gasoline—measured in kWh per kg, for instance—is about 400 times higher than that of a lead-acid battery, and about 200 times better than the Lithium-ion battery in the Chevrolet Volt. We should not expect batteries to rival the energy density delivered by our beloved fossil fuels—ever.

A [recent article in APS News](http://www.aps.org/publications/apsnews/201207/electriccars.cfm "APS article on electric car batteries") reported on an emerging view that batteries are failing to live up to our dreams in the electric car realm:

> Despite their many potential advantages, all-electric vehicles will > not replace the standard American family car in the foreseeable > future. This was the perhaps reluctant consensus at a recent symposium > focused on battery research.

I was somewhat stunned to see this article. I am accustomed to seeing articles emphasizing the *possible*—albeit often improbable, in my mind. Also appearing in the article is a quote from Paul Alivisatos, an accomplished physicist, summarizing the need for further research:

> “It remains true today, as in the past, that we need a fundamental > understanding of the physics of how energy-conversion processes take > place, at a much deeper level, in order to achieve a truly sustainable > energy future.”

Rephrasing: the physics we currently understand is not sufficient to deliver the kind of battery we need to make the future work without fossil fuels. Red flags go up for me when it is our *understanding of physics* rather than practical engineering challenges standing in the way—as serious as the latter can be. Physics limitations instantly present a much taller order to overcome.

### Anecdotes

I’m sure everyone has tales of how batteries have let them down—ranging from the merely annoying to life-threatening situations. I find that I am more often disappointed than pleasantly surprised when it comes to batteries. Here are some examples:

- I frequently go for months without driving my truck. The battery is
  often dead when I try to start it. Lead-acid batteries only get worse
  if left in a discharged state, so it’s a runaway process. Fortunately,
  I live on a hill and can often roll-start my way back onto the road. - The rechargeable NiMh batteries I use for small electronics devices
  are rated for 1000 charge cycles. I’ll bet I only get about 15–20
  cycles before noticing a serious degradation in performance. - The first set of lead-acid batteries I used with my [home-built solar
  photovoltaic
  system](https://dothemath.ucsd.edu/2012/07/my-modest-solar-setup/ "My Modest Solar Setup")
  only lasted two years before showing substantially reduced capacity. A
  newer set is still in good shape after 2.5 years, but the drop in
  performance can be pretty fast, I have found. - Lead-acid batteries for cars tend to last 5–6 years, often failing
  with little warning, in many cases resulting in being stranded. - New laptop batteries seldom fail to delight their owners in how much
  longer the charge lasts compared to the previous generation batteries.
  But give it a few years and it is not uncommon to be operating at half
  the original capacity. - Batteries left in a device for a long time can develop corrosive crud
  around the terminals, often in hard-to-clean places.

A counter-example is the occasional amazement I experience when alkaline batteries in a device that has not been utilized in *years* crackle to life after all that time—if the batteries haven’t gooped themselves up, that is.

### Energy-Power Tradeoff

The chief measure of a battery, in my mind, is how much **energy** it can store. But it makes sense to adjust this concept to the size or mass of a battery. Obviously, a more massive and voluminous battery can pack in more energy. So for a given mass (we’ll take a kilogram), we want to know how much energy a battery can store, called **specific energy**.

At low power demand (sipping rather than gulping), lead-acid batteries tend to hold about 30–40Wh per kilogram (one Watt-hour is equivalent to 3600[J](https://dothemath.ucsd.edu/useful-energy-relations/#joule "Useful Energy Relations: Joule"), or 0.001[kWh](https://dothemath.ucsd.edu/useful-energy-relations/#kilowatt-hour "Useful Energy Relations: kilowatt-hour") of energy). Ni-MH batteries score 45–60Wh/kg, and Lithium-ion gets about 120–180Wh/kg. Part of the reason for Li-ion’s better performance is that lithium itself is lightweight; by volume lead-acid has about 40% the capacity of Li-ion. Gasoline, at 36.6kWh/gal, has a specific energy of 13,800Wh/kg. Off the charts!

As power demand increases, the battery flags, and will not offer as much total energy. Obviously, the battery discharges faster under heavier power demand, but the effect is exacerbated by less actual energy available. This is best shown on a Ragone plot, in which specific energy is plotted against specific power.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/08/Ragone.png "Ragone")](https://dothemath.ucsd.edu/wp-content/uploads/2012/08/Ragone.png)

Characteristics of various battery chemistries, plus a few other technologies thrown in. Diagonal lines indicate time to discharge. The various electric vehicle goals indicate maximum power desired, but discharge times only apply if the maximum power is sustained until complete discharge, which is not the way we drive (most of us!). Plot courtesy of [V. Srinivasan](http://adsabs.harvard.edu/abs/2008AIPC.1044..283S "Srinivasan paper from which plot derived").

Note that the Internal Combustion Engine (ICE) exceeds both specific energy and power goals for vehicles (the mass must include engine weight, rather than the fuel by itself). Fuel cells provide decent specific energy, but typically insufficient power (per kilogram). Capacitors, including super-capacitors, discharge super-fast with lots of power, but have very low specific energy.

As useful as this plot is, it does not convey the whole story. While it looks like Li-ion meets the the goal for plug-in hybrid electric vehicles, this does not necessarily remain true if demanding 5,000 deep charge cycles, a ten-year lifetime, a moderately inexpensive product, etc.

### Spider Diagrams

The U.S. Department of Energy teamed up with the automotive and battery industries to define benchmark performance targets for batteries that would result in electric vehicles being competitive with ICE vehicles on a mass-produced basis. The resulting coalition was called [USABC](http://www.uscar.org/guest/teams/12/U-S-Advanced-Battery-Consortium "US Advanced Battery Consortium")/FreedomCAR, and their various target requirements are [available here](http://www.uscar.org/guest/article_view.php?articles_id=85), with a useful summary presentation [also available](http://www.scribd.com/doc/66052706/3/USABC-FreedomCAR-Battery-Requirements). Below is a subset of the target parameters pulled from these sources, and I have also thrown in the Chevrolet Volt for a side-by-side comparison to current capabilities.

|                                  |             |                     |                   |                       |
|----------------------------------|-------------|---------------------|-------------------|-----------------------|
| Characteristic                   | Hybrid Goal | Plug-in Hybrid Goal | Chevy Volt (PHEV) | Electric Vehicle Goal |
| Range on Battery (mi/km)         | 1.0/1.6     | 40/65               | 38/61             | 300/580 (?)           |
| Available Energy (kWh)           | 0.3         | 11.6                | 10.5              | 40                    |
| Specific Energy (kWh/kg)         | 0.007       | 0.097               | 0.053             | 0.2                   |
| Energy Density (kWh/L)           | 0.009       | 0.14                | 0.105             | 0.3                   |
| Specific Discharge Power (kW/kg) | 0.625       | 0.32                | 0.56              | 0.4                   |
| Power density (kW/L)             | 0.78        | 0.47                | 1.1               | 0.4                   |
| Cycle Life (cycles)              | 3,000       | 5,000 (deep)        | 2,000             | 1,000 (deep)          |
| Calendar Life (years)            | 15          | 10                  | 8                 | 10                    |
| Production Price (USD)           | \$500       | \$3,400             | \$8,000?          | \$4,000               |
| Operating Temp. Range (°C)       | −30 to 52   | −30 to 52           | −25 to 50         | −40 to 85             |

The 300 mile (580km) range for the pure electric vehicle (EV) comes from the [presentation](http://www.scribd.com/doc/66052706/3/USABC-FreedomCAR-Battery-Requirements) rather than the official USABC source, and does not look right to me based on the 40kWh battery size. Electric cars typically need 30kWh of storage for each 100 miles of driving (about what the [Volt, Leaf, and Tesla achieve](https://dothemath.ucsd.edu/2011/08/mpg-for-electric-cars/ "MPG for Electric Cars?"), based almost entirely on air resistance—not battery technology). So I would expect the 40kWh battery pack associated with the EV goal to deliver half as much range as what’s in the table.

Some of the figures for the Volt deserve explanation, since many cannot be directly looked up, and require inference and calculation. Firstly, the 2013 model battery pack has a capacity of 16kWh, but only 10.5kWh are made available so-as to avoid potentially damaging deep discharges. Meanwhile, I have no choice but to use the entire battery pack mass and volume (197kg; 100 L) in conjunction with the partial 10.5 kWh charge in calculating energy densities, because *available* energy density is what’s important. For lifetime and cycle computations, I use the 100,000 mile, 8-year guarantee on the battery, together with the estimated 37 miles per gallon (MPG) on gas alone and 98MPG for combined gas/electric. This implies an expectation that about 62,000 of the 100,000 miles will be driven under battery power. If recharges typically happen after 30 of the 38 miles are spent (corresponding to 80% of available capacity), this translates to about 2,000 deep cycles. Perhaps this is pessimistic in the sense that most guarantees correspond to a *minimum* expected performance. But offsetting this is the fact that the USABC targets are specified for *end-of-life* performance, whereas I use the beginning-of-life numbers for the Volt. General Motors estimates a 10–30% degradation at the end of 8 years (100,000 miles).

A comparison between actual performance and target performance can be cleverly displayed graphically in a “spider chart,” as illustrated below for the plug-in hybrid performance as of May 2011 (I first saw such diagrams in a presentation by Venkat Srinivasan, in 2008).

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/08/PHEV-Spider-Chart-nontech.jpg "PHEV-Spider-Chart-nontech")](https://dothemath.ucsd.edu/wp-content/uploads/2012/08/PHEV-Spider-Chart-nontech.jpg)

Figure from an [LBL news article](http://newscenter.lbl.gov/feature-stories/2011/05/19/working-to-drive-electric-vehicles-from-niche-to-mass-market/ "LBL news article") showing current battery performance relative to PHEV targets (blue line). The story is dominated by underperformance on many criteria.

We can make our own spider diagram for the Volt, based on the numbers in the table. Please excuse the sub-optimal placement of labels, etc.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/08/volt-spider-1024x768.png "volt-spider")](https://dothemath.ucsd.edu/wp-content/uploads/2012/08/volt-spider.png)

Spider chart for the Volt in relation to the USABC/FreedomCAR targets, using my estimates for several parameters, as described in the text. Power performance exceeds the values plotted, so the points are simply placed on the peripheral rim as an indication of sufficiency.

Besides looking like some sort of cool fighter jet in a dive, the diagram highlights performance deficits on several fronts. It is not terribly hard to get lots of current out of a battery, translating to more-than-adequate power performance. But all other measures fall short of the goals by varying degrees. The [APS article](http://www.aps.org/publications/apsnews/201207/electriccars.cfm "APS article on electric car batteries") intones that we should not hold our collective breaths to see a march of progress in lithium-ion technology at a level that would satisfy this (still hungry) spider. In practice, improving *one* aspect of performance tends to *decrease* another somewhere else (see the [piece by Srinivasan](http://gigaom.com/cleantech/the-three-laws-of-batteries-and-a-bonus-zeroth-law/) for more on this principle). So it’s not a simple matter of advancing on all fronts independently and incrementally.

### Full Cost of Electric Drive

Let’s say you pay \$0.10 per kWh for electricity delivered to your home. Charging the Volt battery with 10.5kWh at 90% efficiency to replace the drain from 38 miles of driving will cost \$1.17. If using gasoline alone, the same car uses about a gallon of gas to go the same distance. Let’s put the cost of that gallon at \$4.00. Electric looks pretty good, at these rates!

Now figure in the estimated price of the Volt battery at \$8,000 (a disputed number, but GM has not revealed the actual cost). If we get 62,000 miles of electric drive out of the battery, we will spend \$1950 on electricity for charging, plus \$8000 for the battery. That’s \$9,950. The same distance on gasoline would cost \$6500. Not an order-of-magnitude difference, but still gasoline currently wins.

If the price of gasoline goes up (it will; but so will electricity), and the cost of the battery goes down (it *should*), the two *may* cross. But there are other added costs to the Volt (or hybrids in general) besides just the battery. After all, hybrids can’t jettison the ICE, and require an electric drive train to boot. Even the fact that the space occupied by the battery forces bucket seats in the back of the Volt is a “cost” that must be paid.

### Beyond Cars

Batteries are, of course, useful for purposes other than transportation. While transportation hardship may be the most pressing problem in the decades following peak petroleum production, solar and wind resources cannot scale to be very large without a viable storage solution.

I worked out in [an earlier post](https://dothemath.ucsd.edu/2011/08/nation-sized-battery/ "A Nation-Sized Battery") how large a lead-acid battery would have to be to support the entire U.S. energy demand in the presence of solar/wind intermittency. It turned out that our estimates for recoverable lead in the world do not satisfy the need. Lithium and Nickel are even more constrained. It is possible that some other approach like sodium-sulfer or zinc-air can step in. But these are already relatively well-known options and have not blazed a wide path into storage over the past few decades.

### Sigh

Don’t get me wrong: even though I dwell on the shortcomings of batteries in this post, I still hold a net positive view. When it’s dark at my house, my refrigerator, television, computers, and internet goodies are all powered by [stored sunlight](https://dothemath.ucsd.edu/2012/07/my-modest-solar-setup/ "My Modest Solar Setup") in lead-acid batteries. My laptop battery gets me through many a bus ride and an occasional airplane ride. Batteries *really do work*, and provide value. Moreover, electric cars are more than a notion or fantasy: they are actually on the road getting people where they want to go. Despite their lackluster performance next to fossil fuel storage, batteries still [beat the pants off of mechanical or gravitational storage](https://dothemath.ucsd.edu/2011/09/got-storage-how-hard-can-it-be/ "Got Storage? How Hard Can it Be?").

And even though I might appear to be picking on the Chevy Volt by highlighting its deficiencies, I actually rather like the design point (electric vs. gasoline range hits the sweet spot, in my view). In fact, I was half way to buying one. By half way, I mean that if the price were cut in half, I would surely have one now.

The real point is that batteries fall pathetically short of our customary fossil fuel energy storage medium. When we wake up to a declining global availability of petroleum, we won’t *just* switch over to electric cars. We may not be able to collectively afford such a transition, given the huge up-front costs in both money *and* energy. Where will the prosperity come from? If oil shortages drive recession in the usual fashion, expensive options may be off the table.

#### Addendum

The same author of the APS article referenced above wrote an [extended version](http://www.aps.org/publications/apsnews/201208/backpage.cfm "extended APS article"), worth a look.

Hits: 2904

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2012%2F08%2Fbattery-performance-deficit-disorder%2F&linkname=Battery%20Performance%20Deficit%20Disorder "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2012%2F08%2Fbattery-performance-deficit-disorder%2F&linkname=Battery%20Performance%20Deficit%20Disorder "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2012%2F08%2Fbattery-performance-deficit-disorder%2F&linkname=Battery%20Performance%20Deficit%20Disorder "Email")[](https://www.addtoany.com/share)
