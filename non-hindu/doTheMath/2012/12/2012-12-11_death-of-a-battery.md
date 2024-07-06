+++
title = "Death of a Battery"
full_title = "Death of a Battery"
upstream_url = "https://dothemath.ucsd.edu/2012/12/death-of-a-battery/"
date = "2012-12-11"

+++
Source: [here](https://dothemath.ucsd.edu/2012/12/death-of-a-battery/).

Death of a Battery

[![Four 150 A-h 12-V golf-cart batteries](https://dothemath.ucsd.edu/wp-content/uploads/2011/09/PV-batteries-150x150.jpg "PV-batteries")](https://dothemath.ucsd.edu/wp-content/uploads/2011/09/PV-batteries.jpg)

Four golf-cart batteries used in my off-grid home PV system. Each is 12 V, 150 A-h, thus 1.8 kWh of storage.

All the metrics looked great. The 2.7-year-old lead acid batteries in my off-grid photovoltaic system appeared to have settled into a consistent mid-life performance. Monthly maintenance (equalizing, adding distilled water) promised to keep the batteries in prime condition for some time to come. Based on cycle depth, I expected another 2.5 years out of the present set of batteries. Life was good.

Then, during my absence over the course of Thanksgiving weekend, one of the batteries expired. No forewarning. Just gave up. A [previous post](https://dothemath.ucsd.edu/2012/08/battery-performance-deficit-disorder/ "Battery Performance Deficit Disorder") expressed an overall disappointment in batteries, now reinforced by this sudden nosedive.

In this post, I’ll show the metrics on my system detailing the demise of “Battery E.” The gruesome graphics are intended for mature audiences.

### Everything was Peachy

Let me first recount the status of my battery system as detailed in a [post](https://dothemath.ucsd.edu/2012/09/blow-by-blow-pv-system-efficiency/ "Blow-by-Blow PV System Efficiency: A Case Study for Storage") from September of this year.

Thus far, I have used Trojan T-1275 batteries in my PV system—each 12V, each rated at 150Ah (yielding an energy storage of 1.8kWh: just multiply voltage by charge capacity). Empirically, I found that my batteries have always behaved as if their capacity was 125Ah, from day one. During the first few years of my growing PV system, I operated with two batteries, labeled A and B. I worked them pretty hard, and they gave up around the beginning of 2010. I replaced them with two fresh batteries on 2010-02-15 (batteries C and D), and added two more in parallel a few weeks later on 2010-03-04 (E and F).

[![Four 150 A-h 12-V golf-cart batteries](https://dothemath.ucsd.edu/wp-content/uploads/2011/09/PV-batteries.jpg "PV-batteries")](https://dothemath.ucsd.edu/wp-content/uploads/2011/09/PV-batteries.jpg)

Batteries C and D at top, E and F lower. C and D are in series to make 24 V, as are E and F. These two chains are wired in parallel to each other. Looking somewhat different (E/F are T-1275+), the internal construction of all four batteries is identical.

Studying the discharge curves for every night, I found that the batteries had settled into a very stable performance, actually improving in years two and three from year one.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/09/soc-trend-1024x768.png "soc-trend")](https://dothemath.ucsd.edu/wp-content/uploads/2012/09/soc-trend.png)

Metrics ([explained elsewhere](https://dothemath.ucsd.edu/2012/09/blow-by-blow-pv-system-efficiency/ "Blow-by-Blow PV System Efficiency: A Case Study for Storage")) illustrating the settling in of the batteries in my PV system.

This is also seen in the load-corrected state-of-charge plot vs. voltage, where recent performance edged closer to matching the battery specifications—after adjusting for the realized capacity.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/09/soc-volt-1024x768.png "soc-volt")](https://dothemath.ucsd.edu/wp-content/uploads/2012/09/soc-volt.png)

Comparing best-fit performance (lines) to the manufacturer’s values (dots), it appeared that the batteries were doing better with time (more [here](https://dothemath.ucsd.edu/2012/09/blow-by-blow-pv-system-efficiency/ "Blow-by-Blow PV System Efficiency: A Case Study for Storage")).

I calculated my average daily cycle depth to be 31%, and from [cycle curves](http://www.mpoweruk.com/life.htm "lead acid battery life cycle curves"), expected 2000 cycles at this depth. But 995 days after installation, battery E fell off the cliff. So much for my rosy statement in September:

> At this point, I have sourced 1686kWh from my four batteries in 30 > months, or 422kWh each. At a de-rated 1.5kWh per battery, I have > gone through 281 full-depth equivalent cycles. In about 915 days, this > means my average cycle depth is 31% and I might expect 2000 such > cycles (5.5 years; 620 full-depth equivalent cycles) at this level. So > judging by this, I’m almost halfway done.

Oh that it were true.

### Watching the Crash

Every day, an automated script grabs data off of my solar recording apparatus, and most nights I check the day’s performance. Below is a typical plot of the five-minute resolution data. The [post on PV efficiency](https://dothemath.ucsd.edu/2012/09/blow-by-blow-pv-system-efficiency/ "Blow-by-Blow PV System Efficiency: A Case Study for Storage") details the curves, but in brief: red is solar input; cyan is the load (refrigerator cycle spikes evident), black is battery voltage (right-hand scale), green is battery state of charge (percent full), and the **yellow dots** indicate what fraction of battery current is flowing to battery chain E/F. The reference line at 50% is a useful gauge. Ideally, battery chains C/D and E/F would contribute equally to sourcing or sinking current, and the dots would always be at 50%. Minor ticks on the horizontal axis are at one-hour intervals, so it’s fairly straightforward to read the time (0.25 days is 06:00, etc.).

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/12/1208291-1024x768.png "120829")](https://dothemath.ucsd.edu/wp-content/uploads/2012/12/1208291.png)We see here that during the day, when the batteries are charging, the two chains receive nearly identical current (and therefore similar power, since their voltage is guaranteed to be the same by the magic of connective copper). In the evening, Battery E/F doesn’t contribute quite as much as C/D, but after midnight, it reaches parity, and even wiggles around depending on load variations due to the refrigerator. I am accustomed to seeing Battery E/F slightly under-perform, but not by a large margin.

Notice also the gentle slope of battery voltage decline during the night.

### Chronicling the Demise

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/12/1211181-1024x768.png "121118")](https://dothemath.ucsd.edu/wp-content/uploads/2012/12/1211181.png)November 18 was a partly cloudy day, as seen by the spiky nature in the red (solar input) curve. The battery did not get fully charged, but we see the typical dance of the yellow dots; just shy of 50% for the most part.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/12/1211191-1024x768.png "121119")](https://dothemath.ucsd.edu/wp-content/uploads/2012/12/1211191.png)November 19 was a sunny day, but the previous day’s deficit caught up to the (undersized) battery bank, causing the inverter to switch to utility input at about 04:00. During times when the current into or out of the battery is small, I do not plot the yellow dots, because they can become meaninglessly scattered when comparisons between small numbers are made. Otherwise the battery looks pretty normal: no alarms.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/12/1211201-1024x768.png "121120")](https://dothemath.ucsd.edu/wp-content/uploads/2012/12/1211201.png)Tuesday, November 20 is a picture-perfect example of what I like the PV system to look like. Sunny weather, plenty of time spent in absorb state (battery voltage plateau, while solar utilization scales back to accommodate), loads cranking away doing their thing, and the yellow dots behaving reasonably. Aside from the fact that the system is requiring 200W to maintain absorb state at the end of the cycle, things look great (absorb state took just 130W on 2012-08-29).

On Wednesday, after weather in New Mexico blocked [our attempt to shoot a
laser](http://www.utsandiego.com/news/2012/nov/19/ucsd-hit-spacecraft-orbiting-moon-laser/ "S.D. Union Tribune blurb about LRO plans") at the Lunar Reconnaissance Orbiter, I *did* scramble out of town for a weekend in the mountains. No internet. I had no way to check on the system’s performance on Wednesday. But little worry on my part. I’ve left the system essentially unattended for months while away (though checking remotely), and nothing went off the rails. I had no reason to expect anything different.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/12/1211211-1024x768.png "121121")](https://dothemath.ucsd.edu/wp-content/uploads/2012/12/1211211.png)Undetected by me, the system started showing a problem on Wednesday, November 21, when Battery E/F was only sourcing 25% of the power immediately after sunset. It also did not quite reach up to 50% in the afternoon, as it normally does. Would I have caught this problem in my often hasty scan? Who knows. I didn’t get to try.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/12/1211221-1024x768.png "121122")](https://dothemath.ucsd.edu/wp-content/uploads/2012/12/1211221.png)Thanksgiving Day, while we fussed over cooking a 12 pound turkey in a small charcoal grill, the PV system started showing serious signs of trouble. In a 24-hour average, Battery E/F only took in 42% of the input power, and sourced only 38%, dipping alarmingly near zero just after sunset.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/12/1211231-1024x768.png "121123")](https://dothemath.ucsd.edu/wp-content/uploads/2012/12/1211231.png)Over the following night and day, things went seriously ill. Around 02:00, Battery E/F began to shirk its share of running the house. It decided that 10% was enough. The battery voltage turned downward as Battery C/D stepped up to fill the gap. During most of the ensuing day (Friday, Nov. 23), Battery E/F accepted far less than its fair share of charge. Over a 24-hour period, it only accepted 31% of the total charge (about half as much as did Battery C/D), and only contributed 22% to driving loads.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/12/1211241-1024x768.png "121124")](https://dothemath.ucsd.edu/wp-content/uploads/2012/12/1211241.png)The failed battery proved itself to be practically useless the following night, and only really started accepting appreciable charge once Battery C/D reached its absorb potential and began refusing current. This time, after sunset, we see a net transfer of energy from battery C/D into battery E/F (yellow points in negative territory). Bad battery!

It was at the end of this Saturday that I returned home and checked the system. Imagine my surprise, remembering the performance from 2012-11-20 and suddenly seeing the plot above with an obviously defunct battery! It only contributed 2.2% of the outbound juice in the 24-hour period from 21:00 to 21:00.

Be advised that now the green line (percent full) has lost meaning, as the capacity is no longer that of two fully-functional battery chains in parallel, but effectively only half that.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/12/1211251-1024x768.png "121125")](https://dothemath.ucsd.edu/wp-content/uploads/2012/12/1211251.png)Around 01:00 on Nov. 25, the steeply declining battery voltage had fallen far enough to trigger the inverter’s switch to utility input. Battery E/F was effectively a drain all night. The following day (Sunday, the 25th), *some* charge managed to get dumped into Battery E/F, but not much. It was now dead weight, contributing nothing while sucking up available energy. At noon, the inverter switched back over solar/battery. That morning, I had accepted the fact that the system was seriously impaired, and disconnected the refrigerator from the PV circuit, plugging it into the utility outlet for the first time in years. So sad. The result is smoother load plots from this point forward, while my [TED plots](https://dothemath.ucsd.edu/2012/07/ted-stravaganza/ "TED-Stravaganza") are much messier than usual on account of the change. We see a net E/F drain again at night. I did not have much time to characterize the problem that day, playing catch up on work from spending a few days away, and also having to write a [blog post](https://dothemath.ucsd.edu/2012/11/this-thermal-house/ "This Thermal House") from scratch.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/12/1211261-1024x768.png "121126")](https://dothemath.ucsd.edu/wp-content/uploads/2012/12/1211261.png)Without the fridge load, Battery E/F took in a bit more juice (thanks to longer absorb cycle), but at this point is still a net drain at night.

That evening I measured batteries C through F to be 12.33, 12.39, 11.12, and 13.59V, respectively (both chains must add to the same voltage). So it’s Battery E that is the problem. Battery F is super-charged (and oozing a bit of electrolyte).

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/12/1211271-1024x768.png "121127")](https://dothemath.ucsd.edu/wp-content/uploads/2012/12/1211271.png)I worked from home the on the 27th and made occasional checks of battery voltages, to learn what I could about the dynamic charge state. At 07:45, I measured (11.91, 12.00, 10.79, 13.12) for the four batteries. At 11:40 (during a cloud passage, unfortunately), I measured (13.31, 13.37, 12.12, 14.71). Okay, so Battery F is roughly at an absorb voltage, still shy of the 15.5V equalization voltage. So I’m not absolutely toasting it.

Tired of having the dead battery act as an energy drain on the system, I finally pulled the plug on Battery E/F, disconnecting it from C/D around 18:00. Just before disconnecting, E and F measured 11.29 and 13.81V, propped up by batteries C and D (drawing power out of the good batteries). After disconnecting, they relaxed to 11.15 and 13.5, slowly creeping down. As of this writing, on 2012-12-09, the batteries have settled to 10.49 and 12.63V.

Testing the cells with a hydrometer, it is not hard to identify the weak cell, which has an off-scale-low specific density (below 1.10). For a sense of the numbers/variation, the table below lists measured values.

|          |           |           |
|----------|-----------|-----------|
| **Cell** | **Bat E** | **Bat F** |
| 1        | 1.235     | 1.275     |
| 2        | 1.235     | 1.230     |
| 3        | 1.290     | 1.275     |
| 4        | \<1.1     | 1.245     |
| 5        | 1.275     | 1.275     |
| 6        | 1.275     | 1.250     |

### The Edge of the Cliff

If I plot the fraction of juice accepted (blue) and sourced (red) from Battery E/F during 2012, We see the dramatic endgame.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/12/bat-ef-percent-1024x768.png "bat-ef-percent")](https://dothemath.ucsd.edu/wp-content/uploads/2012/12/bat-ef-percent.png)I think this plot nicely illustrates the degree to which the battery failure caught me off guard. Aside from the “while you were away” twist, the failure was **really fast**. There were no instances outside the 45–50% window the whole year, and then **bam**.

### Now the Conundrum

Okay, so I have a bad cell in a battery. Maybe the situation is salvageable. Perhaps a “battery doctor” could bring the battery back to an operable state. I’ve seen prescriptions online for how to recover some functionality from a bad cell. You can’t expect original performance, I gather. But perhaps it is possible to turn an otherwise heavy block of junk into a useful battery again.

Let me say up front that I am not a battery expert. I may be carrying misconceptions that need to be cleared up. Please correct me if I have things messed up. It’s a safe bet that when I get through this failure episode, I’ll know more than I do now.

Whether or not battery repair is possible/effective, I judge it to be a near certainty that the revived battery would be poorly matched to its brethren. We have, in my 2×2 arrangement, a series problem and a parallel problem. In series, when one battery is in worse condition than its partner, it will sit at a lower voltage in both charging and discharging scenarios. It would seem, then, that the partner in better health gets a higher absorb state (or equalization) voltage, which has the effect of keeping that battery in relatively better condition than its lesser companion. So there is a self-reinforcement going on that I imagine will ultimately go unstable, producing another cliff-edge.
Perhaps this is also why single cells in a battery (stacked in series) drive off the cliff.

The parallel problem is that if one chain is weaker than the other chain, a similar phenomenon happens. The “good” chain gets higher current during charging, better conditioning that chain while in absorb state. And then we have the power swap issue after sunset, where the weaker battery drains energy from the better battery until the two are at a similar charge state.

I am not, therefore, convinced that I want to try and revive the defective battery, almost certainly leaving me with a mismatched condition. So what’s the conundrum? Just buy a new battery!

Firstly, a new battery paired with old Battery F would produce a series mismatch problem, and also a parallel mismatch problem—assuming C, D, and F are in similar shape. To avoid the series problem, I could buy two new batteries, but this seems an unfortunate waste of battery F. For all I know, Battery E is an anomaly and I *can* expect another several years out of the other batteries. \[It’s this sort of thinking that often gets me labeled as an optimist, despite impressions you might have otherwise formed from the content of Do the Math.\]

Secondly, even biting the bullet and buying *two* new batteries will leave me with a parallel mismatch and attendant problems.

So it seems like a really bum deal! Must I replace all batteries at once?

I suspect that I am missing something here, and that a new battery in an otherwise old set may work itself out in some non-destructive way. I am still adapting to my reduced-capacity PV reality, and meanwhile needed a bloggable topic that I could cover quickly, even if the saga is incomplete. I still need to do some research, and perhaps comments will help set things straight.

### Perspective

I have written before about the disappointment inherent in batteries.
Now I have another personal example. Just when I had decided that my batteries were in their prime, crash. In our forced migration from fossil fuels over the coming century, large scale implementations of solar and/or wind are likely to transpire only in connection to energy storage solutions. With storage comes headaches, even for technologies as mature as lead-acid. Batteries will fail, and seldom at convenient times. I liken my recent experience to driving a car without a gas gauge. How tolerable will this situation be to our demanding society?
Big adjustments ahead…

*Note to readers: I will be taking a holiday break in my normal two-week cadence, so that I plan to be back on Jan. 8.*

Hits: 2479

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2012%2F12%2Fdeath-of-a-battery%2F&linkname=Death%20of%20a%20Battery "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2012%2F12%2Fdeath-of-a-battery%2F&linkname=Death%20of%20a%20Battery "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2012%2F12%2Fdeath-of-a-battery%2F&linkname=Death%20of%20a%20Battery "Email")[](https://www.addtoany.com/share)
