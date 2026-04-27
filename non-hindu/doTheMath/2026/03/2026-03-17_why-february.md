+++
title = "Why February?"
full_title = "Why February?"
upstream_url = "https://dothemath.ucsd.edu/2026/03/why-february/"
date = "2026-03-17"
+++
Source: [here](https://dothemath.ucsd.edu/2026/03/why-february/).

Why February?

[![](https://dothemath.ucsd.edu/wp-content/uploads/2026/03/Cork-stone-circle.jpg)](https://dothemath.ucsd.edu/wp-content/uploads/2026/03/Cork-stone-circle.jpg)

An old calendar (by Vreijs from [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:County_Cork_-_Drombeg_stone_circle_-_20150328102444.jpg))

In a bit of a break from heavy topics, we’re going to look at why February is so weird. The average month is 30.4 days, sensibly splitting into either 30 or 31. A seven-to-five distribution of 30-day months and 31-day months would get most years right, or an even split gets leap years. Why, then, does February jump the shark to 28? The weirdness doesn’t stop there, because in every year divisible by four February has 29 days: still unique among months. Yet this special treatment does not apply to century years. Except every 400 it does. February is the month that takes up all the slack in trying to fit a rigid integer-based system onto a more nuanced reality. And the choice of February is not *entirely* arbitrary. It would make less sense to abuse June or August in the same way, for reasons we’ll address.

All of this was inspired by equinoxes (thus the timing of the post: equinox happens Friday). More viscerally, all this was inspired by lengthening days. Living at latitude 48°, the days here go from just over 8 hours long to just over 16 hours long through the course of the year. Around this time, it’s quite dramatically noticeable how quickly day length is changing—by almost a half-hour per week at my latitude.

# When is Equinox?

We’ll gain significant insight into the vagaries of calendars by asking when, exactly, is the equinox (or solstice)? First, equinox is defined not as the time when day and night are each 12 hours (as the name suggests), but as the time when the sun crosses the extension of Earth’s equator in its annual sinusoidal wandering. Equinoxes can be thought of as when Earth is at 0° or 180° in its orbit around the sun—relative to the intersection of ecliptic and equatorial planes—while solstices happen at 90° and 270°. Incidentally, today (March 17) is the date at my latitude when day and night are both 12 hours. On the equinox itself, my day length is 12 hours and 11 minutes. The asymmetry has to do with atmospheric refraction (lifting the apparent sun above the horizon when the geometric sun is below) and definition of sunrise/sunset as when the *top* of the sun touches the horizon, not the center.

Equinoxes and solstices are always *approximately* around the 21^(st) of months that are multiples of three. But sometimes it’s the 20^(th) and sometimes the 22^(nd) or even 23^(rd). And it’s not always the same date from one year to the next.

Here’s a table of [upcoming dates and times](https://www.astropixels.com/ephemeris/soleq2001.html) (in UTC, or Greenwich):

|      |           |           |           |           |
|------|-----------|-----------|-----------|-----------|
| Year | March Eq. | June Sol. | Sept. Eq. | Dec. Sol. |
| 2026 | 20 14:46  | 21 08:25  | 23 00:06  | 21 20:50  |
| 2027 | 20 20:25  | 21 14:11  | 23 06:02  | 22 02:43  |
| 2028 | 20 02:17  | 20 20:02  | 22 11:45  | 21 08:20  |
| 2029 | 20 08:01  | 21 01:48  | 22 17:37  | 21 14:14  |

The pattern is that times get about 6 hours later each year, then snap back about 18 hours after a leap-year insertion. A plot over a longer period showing when equinoxes land will start to reveal the regularity.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2026/03/eq-2000-2050.png)](https://dothemath.ucsd.edu/wp-content/uploads/2026/03/eq-2000-2050.png)

Dots represent the day of month (and fraction thereof) for equinoxes: blue for March; red for September. Note that these are in Universal Time (Greenwich), so you’d need to adjust for your time zone (subtract 7 hours or 0.3 days—shift the dots down—for Pacific Daylight Time, for instance; see my earlier [rant about Daylight Savings](https://dothemath.ucsd.edu/2025/03/daylight-ravings-time/)). Generally, then, around the present year, the March equinox will be on March 20 (Greenwich)—occasionally poking into March 19 late in the day in the U.S. In September, the equinox straddles September 22 and 23; leaning earlier in the U.S. The choice of which day to call “equinox” (or “solstice”) on a calendar is fraught with unstated assumptions about time zone, and ought not be taken literally or definitively.

The trends in the plot are telling: a steady march to later times for four years in a row followed by a slightly-overcompensating reset on years divisible by four (leap years, of course). I say overcompensating because each 4-year cycle gets a little lower (earlier) on the plot. The plot indicates that in the U.S., the vernal equinox is going to dip into March 19 on leap years for the next little while, when lowering dots by about 0.2–0.3 days. Meanwhile, the autumnal equinox will be September 22 unless late in the leap-year cycle (like 2027, 2031, etc.). In the 2040s all the equinoxes in the U.S. will be on September 22. Kids will get the wrong idea.

The two-and-a-half day split between the two would be more extreme were it not for February being as short as it is. In fact, it could stand to be a bit shorter, still. More on why later.

For completeness, here is a plot of the solstice dates in June (blue) and December (red).

[![](https://dothemath.ucsd.edu/wp-content/uploads/2026/03/sol-2000-2050.png)](https://dothemath.ucsd.edu/wp-content/uploads/2026/03/sol-2000-2050.png)

These two overlap, and the 21^(st) is often a decent guess for either—but not always, of course.

# How Long is a Year?

A year is 365 days, right? Except when it’s 366. On average, our calendar says it’s 365.25 days. Is that for real? Does the Earth orbital period and rotation period really line up to the integer ratio of 1461 to 4? Oh, that we should be so lucky. Of course it doesn’t! The [tropical year](https://en.wikipedia.org/wiki/Tropical_year) is currently 365.242189 days, but that number is slowly getting smaller (as days lengthen very slightly due to tidal friction).

But we pretend it’s 365.25, right?

The plots above illustrate what happens. If we underestimate year length at 365 days, the dots quickly march up, around a quarter of a day (6 hours) each year. During a person’s lifetime, the calendar would get off by the better part of a month. Can’t have that. What would birthdays even *mean*? (I’m not sure why they’re treated as significant, anyway.)

Conversely, overestimating year length to be 365.25 results in a slower downward trend that even in this 50-year view accumulates to about 0.4 days of drift.

We can do better if we ignore leap years once per century: in 1700, 1800, etc. Now we’ve got 365.24 days per year, effectively. But this adoption underestimates the year again (by much less than before), so we can expect a slow upward creep. That’s why every 400 years we keep the usual leap-year schedule. Leap year gets canceled in 1700, 1800, 1900, but not in 2000 or 2400. Now we’re at 365.2425 days. To do any better, we’d need to eliminate three more leap years over the course of 10,000 years. Maybe drop the leap day in the year 3000, 6000, etc. But guess what: I’d lay money on the notion that we won’t be keeping precise calendars that long (and that’s not necessarily a bad thing)!

Anyhow, this is a good time to show the longer-term trend of equinox dates.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2026/03/eq-1600-2400.png)](https://dothemath.ucsd.edu/wp-content/uploads/2026/03/eq-1600-2400.png)

Now we see the century-long down-trend (from pretending 365.25 is right) being corrected once per century by leaving out a leap year in 1700, etc.—allowing the rapid up-sweep in the absence of leap years to rocket up for another four years before putting the brakes back on. But you can see that the overall trend is still slowly up (top crests are rising), which is where the preservation of leap year in 2000 comes in. But it’s not quite enough to stabilize the trend. The top of the crest at 2300 is very slightly lower than the top at 1900, which is where elimination of three leap years in 10 millennia would come in.

# Other Stuff Going On

Even if we nailed down a system to get the current tropical year right, earth rotation is slowing on [an unpredictable trajectory](https://en.wikipedia.org/wiki/%CE%94T_(timekeeping)). As day length increases by a few milliseconds per century (accumulating to minute-scale time slips over a century), the tropical year computes to fewer days. Within about 3,000 years, the year is down to 365.2420 days, so our tidy 3,000-year scheme to fix 365.2425 down to 365.2422 fails to hit the moving target. On longer time scales, Earth’s orbit migrates as well.

Here again, the actual universe does what it wants, oblivious to our compulsion to impose integer order.

# But February?

Right. I promised to address February. Part of the job is done, as to why leap years are inserted—the extra day sensibly goes onto the shortest month, leaving it shortest, still. We also get why February is left alone every 100 years, except not every 400.

But why is February so short? I mean, getting months to add to 365 could be done by a sequence like 31, 30, 30, 31, 30, 31, 30, 30, 31, 30, 31, 30 (phased however we like; needn’t start this sequence in January). We could get our occasional 366 by promoting one of the 30 pairs to 31 (could still be February).

Here’s the thing, though. Earth travels an elliptical orbit around the sun. At an eccentricity of 0.0167, the perihelion-half of the orbit (swinging through 180°) takes only 178.75 days, while the “back” 180° takes 186.5 days.

When is perihelion? It’s [typically around January 3–4](https://astropixels.com/ephemeris/perap2001.html), plus or minus a day or so. And, indeed, the way the month lengths are stacked, it’s 181 (or 182) days between the same date in September and March when passing through January, and 184 days across July. In other words, by putting a significantly foreshortened month on the perihelion side, the calendar nods to the reality that Earth zips around the sun faster through these months.

Because the date of the equinox in September is about 2.4 days after that in March (most easily seen in first plot for 2030 and 2040, for instance), the equinoxes are actually 178.6 (181 minus 2.4) and 186.4 (184 plus 2.4) days apart, closely mirroring the time advertised above for a 180° turn on either side of the orbit (not exact because perihelion and solstice dates are two weeks apart).

To perhaps better mirror the asymmetry inherent in Earth’s orbit, one could imagine a scheme where all perihelion-side months are 30 days and all aphelion-side months are 31 days (in a ratio 7 to 5 to get 365 days; changing an edge-case to 31 for leap years). Centering the 30-day months on January achieves the result (closer to orbital reality) that dates in March and September are 184/185 days and 181 days apart depending on which side you run through. In this scheme, leap year might add a day to April.

# Give it a Rest

I’m not seriously proposing an improved calendar. Indeed, calendars are a form of insisting that our wild universe adheres to a rigid plan. How’s that working out? Now, it makes all the sense in the world to pay close attention to seasonal cycles—as many plants and animals do. What arbitrary, artificial labels do is of far less relevance to the Community of Life, and those cousins of ours usually have the right of things.

# Bonus

Although the plot below is tailored to my latitude (48°), the tick marks work for anyone: the right-hand set is distorted to accommodate Earth’s elliptical orbit so that the same solar declination obtains on either side at the same height.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2026/03/sym-year-410x1024.png)](https://dothemath.ucsd.edu/wp-content/uploads/2026/03/sym-year.png)

Mirror dates (and day lengths for my latitude).

I use this diagram to appreciate milestones in the changing year, in terms of day length (0% to 100% is just a day-length scale from the minimum to maximum day length). The universal utility of this diagram is that, for instance, the analog of today (March 17) is September 25, or April 21 maps to August 20/21. In other words, day length, lighting angles, etc. will be the same on these dates. This aspect works anywhere in the world. To customize to your location, you could use a [blank version](https://dothemath.ucsd.edu/wp-content/uploads/2026/03/sym-year-blank.png) and [this site](https://www.timeanddate.com/sun/), which I find to be highly informative (select your location and then mouse-over to watch data change).

Views: 1982

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2026%2F03%2Fwhy-february%2F&linkname=Why%20February%3F "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2026%2F03%2Fwhy-february%2F&linkname=Why%20February%3F "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2026%2F03%2Fwhy-february%2F&linkname=Why%20February%3F "Email")[](https://www.addtoany.com/share)
