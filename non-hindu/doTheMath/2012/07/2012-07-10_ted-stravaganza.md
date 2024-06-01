+++
title = "TEDStravaganza"
full_title = "TEDStravaganza"
upstream_url = "https://dothemath.ucsd.edu/2012/07/ted-stravaganza/"
date = "2012-07-10"

+++
Source: [here](https://dothemath.ucsd.edu/2012/07/ted-stravaganza/).

TED-Stravaganza

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-wash-150x150.png "ted-wash")](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-wash.png)My wife calls it spying. I call it data. To-may-to, To-mah-to. It’s true that I know what she’s been up to (electrically) while I’m away. And it’s true that I can access this information anywhere in the world that has an internet connection. But domestic surveillance is not my aim (cameras and microphones would be far more informative in that regard). I just care about the energy angle.

In this post, I will present example results from monitoring and recording my home electricity use, demonstrating the marvelous secret world it reveals. My interest lies in putting numbers on my own behaviors, and in characterizing the appliances in my house. Some of this rubs off on my wife, and some of it rubs her the wrong way. But as I explained in [an earlier post](https://dothemath.ucsd.edu/2012/03/the-phantoms-ive-killed/ "The Phantoms I’ve Killed"), I kept a note she once wrote that said: “Okay, TED’s pretty cool.”

Who is TED? TED is [The Energy Detective](http://www.theenergydetective.com/ "TED Main Page"). That same [earlier post](https://dothemath.ucsd.edu/2012/03/the-phantoms-ive-killed/ "The Phantoms I’ve Killed") told the story of TED’s tortured journey to our home—a tale of excitement, rejection, and ultimate acceptance.

This post is not meant to convey anything deep and meaningful about the energy challenges we face, except for the fact that those challenges provided a background motivation for me to explore and monitor energy data in my home (it should be obvious by now that I’m a data-holic). Rather, I will simply showcase a number of data captures from TED so you can see for yourself the interesting hidden behaviors of appliances, and develop some intuition about how much of a toll various devices take.

### TED Basics

I should spend a little time telling you a bit about TED. At the heart of TED are two *current*-measuring clamps that each encircle power lines delivering two phases of AC electricity into the home. Tying into a two-phase circuit breaker via wire, it also knows the *voltages* of the two phases. *Power* is current times voltage, so TED simply accumulates the instantaneous current times voltage for each of the two phases. Out pops Watts, measured once per second.

The data are communicated through the electrical wires themselves—via the same wires that connect TED to the breaker. A communication unit inside the house plugs into any outlet to receive the information and relay it via ethernet to the (separately furnished) home networking equipment. Configuration of the router can allow password-protected access to TED from outside the home. An optional display receives wireless communication from the plugged-in communication device—albeit over a pathetically short range in my unit—and presents (among other options) the instantaneous power usage of the house in Watts.

I [discussed before](https://dothemath.ucsd.edu/2012/03/the-phantoms-ive-killed/ "The Phantoms I’ve Killed") methods for using the utility meter on the side of the house to gauge power draw, but the methods are indirect and slow. Nothing beats a real-time reading *in the house*. Suddenly many curiosities may be satisfied. All the integrated devices (lighting, fans, air conditioning, electric ovens/stoves, hot tubs, etc.) that are not available for measurement via the Kill-A-Watt are now fair game. One useful exercise is to turn off breakers one by one during a quiet period in order to discover which circuits harbor [phantoms](https://dothemath.ucsd.edu/2012/03/the-phantoms-ive-killed/ "The Phantoms I’ve Killed")—making it considerably easier to track them down in the house.

Moreover, TED data are stored automatically so that periodic retrieval can result in an uninterrupted record of electrical activity in the house. My favorite!

At one-second resolution, TED keeps the last ~65 minutes of data. I only export the one-second data after some particularly informative event, like a washing machine cycle. For one-minute resolution, TED stores a little over two days’ worth (this is what I routinely collect). I should note that the lower-resolution data is *accumulated*, rather than sampled. So usage that comes and goes within the course of a minute (or is activated/deactivated some time within the minute) is properly accounted/prorated. Hourly activity is recorded for the last hundred days or so, and daily and monthly totals are accumulated for longer than the 1.5 years over which I have owned my unit.

A web interface allows you to see what’s happening in real time; export data; configure the unit; or graph recent results. Example screenshots follow.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-dash.gif "ted-dash")](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-dash.gif)

TED “dashboard” showing a variety of useful quick-look items. Note that the month-to-date peak power occasionally flips out (every few weeks) and reports a maximum power in excess of 32 kW, even though the recorded data does not reflect the anomaly. Average daily use and projected usage are based on the month to date, becoming more reliable as the month progresses and more days are added to the average.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-24-hr.gif "ted-24-hr")](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-24-hr.gif)

Activity over the last 24 hours, plotted. Voltage (uninteresting) is in red, and power (super-interesting) is in blue. Spikes are generally brief microwave usages (like the one at about 19:30). The activity around 17:00 is a circular saw, and skulking low around 19:00 (just before the microwave spike) is the bed-warmer test shown later in more detail.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-daily.gif "ted-daily")](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-daily.gif)

The last 15 days show our household using about 1.5 kWh per day of utility electricity. In the summer, we supplement this with typically about 4 kWh of off-grid solar input, most of which runs the attic fan during the hottest (and happily, sunniest) part of the day.

### TED Funhouse

Okay, let’s take a look at examples of TED data captures. I will be using units of Watts and Watt-hours (Wh) to describe the results. For example, consuming electricity at a rate of 30W for 10 minutes (one-sixth of an hour) accumulates 5Wh, or 0.005kWh in more familiar billing terms.

My TED data records are especially clean because many of the periodic/variable power draws in my house are serviced by the off-grid solar installation: refrigerator, computers, wireless and modem, entertainment console, etc.

#### Getting Warmed Up

As a rule of thumb, electrical devices designed to generate *heat* are power hogs—simply because significant thermal energy tends to cost a lot of Joules. Two exceptions in our house are a heating pad and a heated mattress pad: targeted, small-scale heat.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-heater.png "ted-heater")](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-heater.png)

Heating pad (initial long pulse, becoming choppy thermostatic cycling), followed by a space heater run for a little over three minutes.

The plot above shows a heating pad turned on (at minute 7), staying on for about half-an-hour. In this time, the pad averaged 30W (48W when on). A heating pad on your lap, in your chair, or for your feet can eliminate the discomfort of sitting/working in a cold environment. Compare this to a space heater, seen in the latter part of the plot, running for just over three minutes. Despite running for only about one-tenth as long, the space heater accounts for 85% of the above-baseline power expenditure pictured here (84Wh for the space heater vs. 15Wh for the heating pad). We also see from this example the stability of the TED data: the baseline is flat, and the top of the space heater pulse is pretty flat also, showing very little fractional wavering (and what wavering there *is* may just as likely be attributed to actual variation in the heater).

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-bed.png "ted-bed")](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-bed.png)

Mattress pad heater (also barely visible around 19:00 in the 24 hour plot above). The heater was turned on one click at minute 16, then advanced another click every five minutes starting around minute 36. The pad automatically comes on full-scale for the first four minutes to pre-charge the thermal mass.

The mattress pad, like the heating pad, is about as modest as it gets when it comes to energy for heating. The pad we have has dual controls for each side of the bed, and this test represents only one side. The maximum scale is 30W per side, with five equal steps of about 6W. Now that the vertical scale only extends to about 70W, we can see the TED measurement dithering at the 1W level. In this case, I evaluated the baseline to be at 38.5W, and the test consumed 10.7Wh above baseline activity.

#### Garage Door Opener

This one will make appearances in some of the forthcoming examples, so let’s get it out of the way.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-garage.png "ted-garage")](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-garage.png)

Opening and closing of the garage door, showing also the light (a compact fluorescent) staying on for about five minutes each time.

Raising the door required 1299J, or 0.36Wh, while the light (staying on for 290 seconds) consumed 4263J (1.18Wh), so that *the light accounts for more than three-quarters of the total expenditure*. Imagine what an incandescent would do! On the way down, the closing action required 951J. All together, the opening and closing cost 2.95Wh—even when the light was allowed to stay on. It is often easy to turn off the light manually, so why not make it a habit? One lesson from these small numbers: opening and closing the garage door is not a serious energy concern.

#### Domestic Service

Okay, let’s get busy. About a year ago, I made stairs to ascend the bank at the back of my yard. I cut the stringers out of four 2×12 10-foot boards, accommodating 9 stairs per stringer, making for 18 saw cuts per board. The 65-minute capture caught the tail end of the first set (board), followed by the next three complete sets.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-sawing.png "ted-sawing")](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-sawing.png)

Four sets of stair stringers (the last three fully captured) were cut with a circular saw, consisting of 18 high-power cuts each.

The time in between cutting periods accounts for measurement and layout work. Measure twice; cut once. The activity shown in the plot represents 370Wh of work. If the saw peaks at 1800W, that means the saw was on for an integrated 740 seconds out of the 65 minute span, or 19% of the time. Considering that the cutting phase totals 27 minutes, the actual saw-on time during the cutting phase was about 46%, which seems reasonable. As I cut the wood, I didn’t consider that my efficiency was being quantified by TED. But I happen not to mind spying on myself…

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-mower.png "ted-mower")](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-mower.png)

The dominant activity visible here is use of an electric lawn mower, but the sequence starts with laptop activity, the garage door and light, mowing three sections of yard, more garage door action, then back to the laptop.

This sequence shows a variety of actions, starting with laptop use (generally wiggly/variable). Normally our computers are powered by the off-grid solar setup, but sometimes a change of venue might put one of them on utility power. After opening the garage door, I failed to turn the light off manually. Three sections of yard were mowed, costing 57Wh at a typical power of 600W. After the mowing was done, the mower was wheeled into the garage, tripping the light—promptly turned off this time—then the garage door was closed and the light turned off immediately after. Naturally, I had to wake up the laptop to export the data from TED.

#### Furnace

Our gas furnace uses natural gas at a rate of about 75,000Btu/hr (22kW). But the air handling adds 600W to this. Below are two furnace cycles in our house (rarely used: part of the test described in [an earlier post](https://dothemath.ucsd.edu/2012/03/home-heating-for-the-hardy/ "Home Heating for the Hardy")).

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-furnace.png "ted-furnace")](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-furnace.png)

Two furnace cycles, showing remarkable consistency. The individual actions are detailed below.

First, the furnace’s internal blower turns on, followed by ignition of the gas about 30 seconds later. After another 30 seconds, the main house blower turns on (accompanied by an initial surge/spike). After about six minutes, the gas turns off, as does the internal blower. The main blower continues for another couple of minutes to deliver residual heat to the house. All told, each cycle is using about 80Wh of energy (perhaps 240Wh of fossil thermal energy at a power plant, if operating at 33% efficiency). Meanwhile, the energy expended in gas is about 2400Wh. So approximately 10% of the expended energy is on the electrical side, or as little as 3% if the source is solar, wind, or hydroelectric—without the typical heat-engine loss.

Another useful measure that comes from such analysis is that, for my house, each Therm of energy (29.3kWh) delivered by natural gas burned in the furnace is accompanied by 1kWh of on-site electrical expenditure.

#### Appliances

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-fridge-dvd.png "ted-fridge-dvd")](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-fridge-dvd.png)

One refrigerator cycle plus an hourly hiccup from the DVD player.

This series corresponds to a time when the photovoltaic system’s battery was low (cloudy/rainy period), so all household power is reported by TED. It’s much noisier than usual. After the refrigerator cycle (characteristically higher power at first), the DVD player woke up wondering what time it was, and checked for cable service we no longer have to get the answer. It does this every hour, spending 13 minutes at 8W, costing about 40Wh per day. Normally, this system is on solar, and I have plenty of juice to cover it, so don’t really care. But maybe I should address it all the same.

But this data set is rather boring, yes? Let’s move on.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-wash.png "ted-wash")](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-wash.png)

Front-load washing machine cycle.

The clothes washer makes quite the rich TED subject. Firstly, our washer consumes **6W** to sit *doing absolutely nothing* if left plugged in. Criminal! 6W may sound like a pittance, but when our utility electricity baseline is around 40W (as seen in many of these TED plots), 6W becomes substantial. Over the course of a year, it adds up to \$6, or about one sizable burrito. So the first event we see in the plot is a little step corresponding to plugging in the machine. Then it’s a tumble, stop; tumble, stop sequence over and over as the machine practices the art of washing clothes. Later on, the soapy water is spun out, rinsed, and spun again, in cyclic fashion. At the end, things get serious as the drum spins up to 1000 rotations per minute or thereabouts to wring the clothes dry.

In total, the process consumed 132Wh of energy.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-all-hell.png "ted-all-hell")](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-all-hell.png)

Clothes washer, rice cooker, and microwave; all mixed together.

Okay, want a bit of chaos? Here we have a clothes washing cycle starting two minutes in. The rice cooker is turned on at ten minutes, was on for 16 minutes, off for three (for some reason), then on for another 6. Also thrown in are short microwave cooking invocations at minutes 26, 35, 39, and 41.

Out of the total 420Wh represented in this cacophony (above baseline), 183Wh is attributable to the rice cooker, operating at 500W. We’ll assume 132Wh for the clothes washer—as was the case before. It looks like the microwave ran a total of about four minutes at 1740W for 116Wh. Adding these up, I get 430Wh, which is close enough to 420 to satisfy me. Maybe the microwave ran twenty seconds less than my crude estimate, or the washing machine does not do exactly the same thing every time (could investigate…).

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-dishes.png "ted-dishes")](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-dishes.png)

Dishwasher, plus a bit of microwave (twice).

Finally, we have the dishwasher. Unfortunately, my tardy initiation of data export resulted in my missing the first three minutes of the dishwashing activity. But I know when it started based on the one-minute-sampled data (and set the left-hand extent of the axis to correspond to this time, for visual effect). The microwave oven makes two appearances, roughly compensating the unaccounted dishwasher energy at the beginning of the record. In total, this capture represents 660Wh of energy expended. I don’t have much insight into the meanings of the various pulses, other than the general observation that the early big pulses must represent the wash phase, and the later period must involve rinsing and possibly heating—though we generally don’t use the high temperature wash option and turn off heated dry.

### Cloudy Periods

As mentioned before, a number of our electrical devices are supported by the off-grid solar installation at our house. But during cloudy or rainy periods, my undersized battery bank will drain to the point that the smart inverter switches to utility input. During these times, the activity recorded by TED may be more typical of “normal” households, albeit still at modest scale.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-busy.png "ted-busy")](https://dothemath.ucsd.edu/wp-content/uploads/2012/07/ted-busy.png)

Two days of data when the solar input was mostly bypassed (solar re-engages at day 348.4). Local midnight corresponds to X.00 days, so that X.50 is noon and X.75 is 6 PM.

The refrigerator forms the visually dominant feature of this sequence, tirelessly cycling on and off. It can be easier to look at the bottom envelope of activity to sense the overall usage pattern. I note refrigerator defrost cycles at 346.94 and 348.36 days—corroborated by the longer cooling cycle after each heat pulse (see [post on heat pumps](https://dothemath.ucsd.edu/2012/06/heat-pumps-work-miracles/ "Heat Pumps Work Miracles")). Most spikes are due to the microwave (or sometimes similar-power toaster oven). I recognize the lopsided signature of a clothes-washing cycle at 348.53, and the tell-tale two-horned visage of the dishwasher at 347.87. We hosted a dinner on the evening of day 347 (though the guests were likely unaware of the day number), which accounts for a higher-than-normal evening energy use (compare to evenings before and after), as well as the use of the dishwasher.

### Summary Table

As a matter of convenience, I gather the results of the various measurements represented throughout this post. I crudely estimate the daily impact of each, based on our usage patterns—some of which are seasonal, and some of which don’t really apply to us (like the furnace, which we almost never use).



|                                      |                 |               |                              | |--------------------------------------|-----------------|---------------|------------------------------| | **Activity**                         | **Energy (Wh)** | **Daily Use** | **Notes/Conditions**         | | Garage Door Open                     | 0.36            | 1.4           | 2 open/close per day         | | Garage Door with Light               | 1.5             | 6.0           | 2 open/close per day         | | Mowing Small Lawn                    | 57              | 8             | weekly, summer months        | | Clothes Washer Cycle                 | 132             | 30            | at 1.5 loads per week        | | Rice Cooker                          | 180             | 50            | at twice per week            | | Heating Pad, 1 hour                  | 30              | 90            | at 3 hr/day in winter        | | Sawing 40 ft of Stair Stringers      | 370             | —             | not habitual                 | | Microwave, 5 minutes                 | 150             | 150           | 5 min/day                    | | Furnace Blower, 1 cycle              | 80              | 160           | at 20 cycles/day (if used)   | | Mattress Pad, full-blast, both sides | 60              | 240           | 8 hr/day, half-blast, winter | | Space Heater, 1 hour                 | 1400            | 280           | at 12 minutes/day, winter    | | Refrigerator, 1 cycle                | 20              | 1000          | efficient (40 W) fridge      |

### Postlude

As I disclosed at the beginning, I was not aiming for any momentous conclusion in this post. And maybe a post with plot after plot of energy activities in my home is of little interest to people outside my household—and maybe only to half of those within, come to think of it. But hey, I learned something from each one of them, and hope the plots are worthwhile to others as well.

There are many appliances I *don’t* have, so cannot show. And our usage is modest enough that we seldom have lots of things happening at once. So it’s not as hard to disentangle events in these plots as it might be for more active households.

I would still like to test our almost-never-used air conditioning unit sometime and see how the thermal performance of our house in cooling mode compares to heating mode, and what kind of efficiency leverage we’re getting from the heat pump. I know many in the U.S. will cringe to hear it, and I’m not saying this to be mean, but we have yet to see temperatures this year in San Diego that call for cooling. Our July 4 was a cold and windy day. No wonder the fireworks all went off in a 15 second frenzy: they couldn’t stand the cold and wanted to hurry up the show!

### Okay—Irresistible Aside

If you haven’t heard about it, a technical glitch caused the coordinated fireworks displays across San Diego to fire all at once during this year’s July 4^(th) celebration. I was at a party where we managed to get atop a local hill in time to see the Sea World fireworks a bit later, but missed the municipal debacle. So I had to watch a [youtube video](http://www.youtube.com/watch?v=lrPCEubDZ9A) (or see [here for a view of three displays in one frame](http://www.youtube.com/watch?v=JuJHfkXEI-o)). All I can say is that had I been close at hand to one of the accelerated displays, I would have been laughing so hard I might have had trouble breathing for the next several minutes. Many spectators were deeply disappointed and complained bitterly. But this would have been the **best fireworks display of my life**, and one I would never forget—unlike all the rest that become boring by the end and then fade into obscurity. **Awesome!**

Hits: 1173

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2012%2F07%2Fted-stravaganza%2F&linkname=TED-Stravaganza "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2012%2F07%2Fted-stravaganza%2F&linkname=TED-Stravaganza "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2012%2F07%2Fted-stravaganza%2F&linkname=TED-Stravaganza "Email")[](https://www.addtoany.com/share)
