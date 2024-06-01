+++
title = "My Chicken of an EV"
full_title = "My Chicken of an EV"
upstream_url = "https://dothemath.ucsd.edu/2015/08/my-chicken-of-an-ev/"
date = "2015-08-25"

+++
Source: [here](https://dothemath.ucsd.edu/2015/08/my-chicken-of-an-ev/).

My Chicken of an EV

[![Yes, that's my chicken atop my car.](https://dothemath.ucsd.edu/wp-content/uploads/2015/08/cmax-chick-300x201.jpg)](https://dothemath.ucsd.edu/wp-content/uploads/2015/08/cmax-chick.jpg)

Yes, that’s my chicken atop my car.

A little over two years ago, my wife and I entered a new phase of life in two respects: we got three chickens, and we got a [plug-in hybrid vehicle](https://dothemath.ucsd.edu/2013/08/man-bites-ev-will-ev-bite-back/ "Man Bites EV: Will EV Bite Back?"). They have more in common than I would have thought. We see flagging performance in both (egg-laying and battery capacity). We knew the chickens would only last/live for something like 4 years. It’s looking like the EV battery may be similar! Both are happiest pipkining around: plodding about at a leisurely pace. And perhaps like some children, they both disappoint us at times, but we are fond of them all the same. They’re good girls, we tell ourselves.

It may come as no surprise to you that I’ve been collecting data (yes, on both “experiments,” but I’ll spare you egg masses and laying schedules). It takes a little time to do, but recording/resetting the trip meter for every charge, noting charge time and energy delivered, and convincing the wife to go along does pay off, as you will hopefully be convinced.

From the data, I see that the battery capacity is at about 85% of its original condition. While extrapolation is highly risky, it would seem that I can expect zero capacity on the scale of six years, based on its accelerating decline. At this point, we have put about 500 full-cycle-equivalent charges on the battery in about 700 charge events (just shy of one per day, typically about 70% depth). So perhaps it’s not surprising: few batteries can withstand more than 1–2000 charge cycles before giving out.

Want to see some data?

Basics first. The car is a 2013 Ford C-Max Energi, with a nominal electric range of about 20 miles, plus a gasoline range around 600 miles. The 7.5kWh battery provides nominally about 5.5kWh of capacity for the user. The following plot shows the historical usage profile for our vehicle.

[![gasoline vs. electrical consumption over time](https://dothemath.ucsd.edu/wp-content/uploads/2015/08/cmax_traj-1024x768.png)](https://dothemath.ucsd.edu/wp-content/uploads/2015/08/cmax_traj.png)

Gasoline vs. on-board electrical consumption over time

The horizontal axis tallies gasoline usage in gallons, while the vertical axis is the electrical energy used, in [kWh](https://dothemath.ucsd.edu/useful-energy-relations/#kilowatt-hour "Useful Energy Relations") (as reported by the car: charging supplies 22% more than this). Road trips shoot over to the right, while long stints of around-town driving are more vertical tracks. Color coding signifies progress through time (the same scheme is used for many of the plots to follow). Soon after getting the car, we took a ~4000 mile road trip to the Pacific Northwest (charges along the way), and a more recent one to Yosemite. The black line represents an approximate parity between EV driving and gasoline driving. Traveling a total of 24,200miles using 280 gallons means a literal MPG of 86 (37km/L).

### MPGe

Rather than focusing on miles per literal gallon of gas, the car also reports MPGe: miles per gallon-equivalent. Reverse-engineering, it uses a conversion of about 33kWh per gallon of gasoline, which is consistent with the thermodynamic [lower heating value of gasoline](https://en.wikipedia.org/wiki/Gasoline_gallon_equivalent "Wikipedia: Gasoline Energy").

Looking only at “pure EV” trips in our car, we get the following scatter relationship between kWh reported used by the car and miles driven. The upper, middle, and lower black lines correspond to 170, 140, and 110MPGe, respectively.

[![cmax_pure-ev](https://dothemath.ucsd.edu/wp-content/uploads/2015/08/cmax_pure-ev-1024x768.png)](https://dothemath.ucsd.edu/wp-content/uploads/2015/08/cmax_pure-ev.png)

So 140MPGe is typical for us. Note a greater preponderance of blue (early) points at lower MPGe, and more red (recent) above the center line: we’re driving more efficiently over time. The direct conversion of 140MPGe is 4.27 miles per kWh, or 23.4kWh/100mi (a suggested metric in this [old post on EV MPG](https://dothemath.ucsd.edu/2011/08/mpg-for-electric-cars/ "MPG for Electric Cars?")). But we should not be so hasty to declare this a marvelous feat.

Firstly, charging efficiency (at a 3.4kW rate) for our car is around 82%. By this, I mean that Delivering 5.0kWh from the wall outlet results in only 4.1kWh kept/used by the battery. That’s not a bad energy efficiency, as batteries go (note that energy efficiency is always lower than *charge* efficiency, which just counts charges—electrons—ignoring the fact that charging takes place at higher voltage than discharging). So the true effective efficiency is 113MPGe, or 29kWh/100mi, which is in line with other EVs. The same (our) car on gasoline tends to get about 47MPG, so EV mode uses about 40% as much energy as would gasoline to propel the car (far less wasted as heat). If the electric drive is 80% efficient (guessing), this implies a 32% efficiency in gas/hybrid mode.

Also, I should remind readers that electricity doesn’t come out of wall sockets without some less-than-perfectly-efficient process behind the scenes. A coal plant at 33% efficiency needs three times as much thermal energy as the amount delivered in the form of electricity. So the 40% EV miracle goes up in a puff of smoke, now taking 20% *more* thermal energy compared to direct burning of gasoline, and producing an even larger toll on climate change, given coal’s higher carbon intensity. If your power is coming from solar, wind, or hydro, then fine. Fossil fuels: flirting with break-even.

Note that the upper right end of the plot above has no (recent) red points. The battery capacity is fading.

One more point before leaving the topic of MPGe. Our car has trained us to be more efficient drivers. The biggest effect happened over the first few months, but we see a slower improvement since then as well. The plot below tells the story.

[![cmax_mpge](https://dothemath.ucsd.edu/wp-content/uploads/2015/08/cmax_mpge-1024x768.png)](https://dothemath.ucsd.edu/wp-content/uploads/2015/08/cmax_mpge.png)

This is the only plot for which dot color is *not* tied to the timeline. In this case, it represents the fraction of the trip energy provided by electricity. Dark blue is effectively gasoline-only, while dark red is pure EV mode. We see a steep initial “training” curve, especially in the EV-only points. One anomalous cyan point sits on the lower line. The car was in the shop at this time, and I can’t figure out what they did to use so much battery juice for not very many miles. I also detect a seasonal variation: more efficient in summer.

### Decline

Okay, now for the bad news. We used to frequently pull into the garage on battery “fumes,” and note 5.5kWh delivered by the car battery. But we have not seen this for many months now. Time to plot up all our hard-earned data. The plot below shows the energy expended on pure-EV trips (or collections of small trips) that ended with an estimated remaining range of three miles or less. For those trips with some range remaining, the “full” capacity was estimated by adding estimated range divided by 5.5 miles per kWh, which is the empirically-determined (optimistic) range estimate scaling the car seems to use. In other words, if we use 4.7kWh and have 3 miles left, I report this as 5.2kWh total capacity. The curve looks no different (just sparser) when including only points with 0 or 1 miles remaining.

[![Unmistakable decline in battery capacity](https://dothemath.ucsd.edu/wp-content/uploads/2015/08/cmax_est_kwh-1024x768.png)](https://dothemath.ucsd.edu/wp-content/uploads/2015/08/cmax_est_kwh.png)

Unmistakable decline in battery capacity

In the early days, 5.0–5.5kWh was the rule. Now it’s 4.4–4.8kWh. The black curve is a fit-by-eye parabola that does a fair job of capturing the initially-flat behavior. But it may have been even flatter initially, and falling more steeply than the curve suggests now. In any case, that particular curve hits 80% in early 2016 (2.6 years in), 50% after 4 years of service, and would be dead within 6 years of purchase. I hope I’m wrong.

Could it be that the car is simply reporting less energy used by the battery, but that the actual energy has not changed? After all, we seem to be getting better mileage. Is this an illusion also connected to under-reporting of energy used on-board?

Short answer: no. I had hoped for something like this. We not only keep track of charge times, but [our electricity monitoring system](https://dothemath.ucsd.edu/2012/07/ted-stravaganza/ "TED-Stravaganza") also tells us how much we’re actually delivering. Comparing initial charge efficiency to recent efficiency shows no change at the few-percent level.

### Economics

Although there is a generous warranty on the battery (8 years or 100,000 miles; 10 years or 150,000 miles in CA and some other states), this does not apply to gradual capacity loss, since this is considered to be normal wear and tear. So if the \$4,400 battery cost crops up in four years, my cost analysis (\$3/gal gasoline, \$0.15/kWh electricity, 5,000 miles/year in EV mode) indicates a propulsion cost savings of \$100 per year (about 15% savings on yearly total propulsion cost, assuming 10,000 miles total per year). Compared to the \$1100/year in battery premium cost, this saving is practically invisible/meaningless. Batteries becoming twice or even four times cheaper will not offset the differential.

### Take Away

While obligated to point out the financials, I am the last to feel enslaved by a strict dollars-and-cents analysis. There are other reasons to go for an EV: reduced reliance on petroleum, solar charge capability, quiet, efficient, support of a nascent technology, etc. For me, energy is a hobby. I buy an expensive car and expensive solar batteries because I want to learn more about their pros and cons. In part, I am glad that I can export what I learn to the people. Most folks do not have the financial or technical capabilities to look into possibly-hyped technologies and report, free of financial agenda.

I am not yet personally convinced that we will see an EV revolution. Gasoline price fluctuations are a short-term killer of long-term planning. Batteries still do, and likely always will, [disappoint](https://dothemath.ucsd.edu/2012/08/battery-performance-deficit-disorder/ "Battery Performance Deficit Disorder"). I am learning similar lessons on the nickel-iron battery front. We may have to face the fact that gasoline has been the ultimate transportation fuel, and the economists’ picture of universal substitutability may not apply. If EVs can never really outperform gasoline in cost, ease/simplicity, convenience, and robustness—and if they remain expensive to own and maintain, from where will the prosperity derive for us to all have such marvelous toys?

Meanwhile, I will continue to enjoy my EV and my chickens while they last, as a lifestyle choice. The cost per egg or cost per mile certainly do not justify them. So we need be satisfied by other reasons.

Hits: 2495

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2015%2F08%2Fmy-chicken-of-an-ev%2F&linkname=My%20Chicken%20of%20an%20EV "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2015%2F08%2Fmy-chicken-of-an-ev%2F&linkname=My%20Chicken%20of%20an%20EV "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2015%2F08%2Fmy-chicken-of-an-ev%2F&linkname=My%20Chicken%20of%20an%20EV "Email")[](https://www.addtoany.com/share)
