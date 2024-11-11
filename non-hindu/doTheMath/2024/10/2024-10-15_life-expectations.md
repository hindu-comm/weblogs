+++
title = "Life Expectations"
full_title = "Life Expectations"
upstream_url = "https://dothemath.ucsd.edu/2024/10/life-expectations/"
date = "2024-10-15"

+++
Source: [here](https://dothemath.ucsd.edu/2024/10/life-expectations/).

Life Expectations

<div class="wp-block-image">

![](https://dothemath.ucsd.edu/wp-content/uploads/2024/10/Kung-Bushman-people.jpg)

</div>

A while back, I came across a [fascinating paper](https://gurven.anth.ucsb.edu/sites/secure.lsit.ucsb.edu.anth.d7_gurven/files/sitefiles/papers/GurvenKaplan2007pdr.pdf) from 2007 by Gurven and Kaplan on longevity among hunter-gatherers that helped me understand aspects of what life was (and is) like outside of modernity. My interest is both a matter of pure curiosity, and to gain perspective on how desperate life feels—or doesn’t—to members of pre-agricultural (ecological) cultures.

I wrote last year about the perceived perils of early human life in [Desperate Odds](https://dothemath.ucsd.edu/2023/08/desperate-odds/), in the context that to us members of modernity, having never been weened from the teat of agricultural output, it seems like life without agriculture (and supermarkets) would be a virtual death sentence. Add to this a perceived vulnerability to predation from lions and tigers and bears (oh my!), and the mental image that emerges—as depicted by Daniel Quinn in *[Ishmael](https://www.ishmael.org/books/the-book/)*—is of a stressed and starving hunter following the tracks of elusive prey as twilight darkens, while a predator is close on his trail, audibly breathing. It feels like a knife edge of survival: everything has to go just right, but teeters on all going horribly wrong.

The core argument from the [Desperate Odds post](https://dothemath.ucsd.edu/2023/08/desperate-odds/) was that surviving to reproductive age was obviously common, or our species would wink out. This simple fact makes daily survival a near-guarantee—enough so that fear of death is not top-of-mind most of the time, allowing most brain cycles to go toward less-troubled, routine activities.

It was either in preparing that post or in connection with [A Lifetime Ago](https://dothemath.ucsd.edu/2024/01/a-lifetime-ago/) that I ran across the [aforementioned paper](https://gurven.anth.ucsb.edu/sites/secure.lsit.ucsb.edu.anth.d7_gurven/files/sitefiles/papers/GurvenKaplan2007pdr.pdf). In this post, I dig in to see what insights can be gained from survival models for various human cultures.

# The Attention-Grabber

Let’s start with the plot that caught my eye and drew me in, which is Figure 3 in the paper.

![Figure 3 from [motivating paper](https://gurven.anth.ucsb.edu/sites/secure.lsit.ucsb.edu.anth.d7_gurven/files/sitefiles/papers/GurvenKaplan2007pdr.pdf).](https://dothemath.ucsd.edu/wp-content/uploads/2024/10/life-expect-curves-1024x886.png)

Let’s see if it draws you in as well.

This plot shows life expectancy (remaining years) as a function of age for different non-agricultural groups, including some guesswork as to pre-historical human longevity, a point-making 18th Century Sweden—invisibly buried among the others—and even wild chimpanzees to make it a *real* party.

Life expectancy at birth is the y-axis intercept (left edge) for each curve, quantified as *e*₀ in the legend. Early-year mortality is visible via the initial rise in life expectancy over the first few years.

To gain familiarity with the graph, notice that the cluster of curves indicates a y-value around 25 at 40 years of age, meaning that a 40-year-old can expect (50/50 chance) to live another 25 years, to age 65. Another way to put it is that in steady-state, the population of 65-year-olds is approximately half that of 40-year-olds. Once at 5-years-old, one can expect to live to about 50–55 for most of these curves, and by age 20 it’s 55–60. These are for present-day hunter-gatherers without access to modern medicine and food, as the paper describes:

> All groups in our ethnographic sample of hunter-gatherers have had
> minimal or no exposure to modern medicine, and minimal or no inclusion
> of products of horticulture or market-derived foods in their diet.

# Digging Deeper

Okay, this plot struck me as a rich resource for learning more, so I dove in. I learned that an underlying model used in the analysis is called a Siler model (after a [1983 paper](https://onlinelibrary.wiley.com/doi/abs/10.1002/sim.4780020309)) that describes mortality rates via three components (early childhood mortality, exponentially decaying; constant low-level risk; exponentially increasing mortality with age)—represented as Equation 1 in [the paper](https://gurven.anth.ucsb.edu/sites/secure.lsit.ucsb.edu.anth.d7_gurven/files/sitefiles/papers/GurvenKaplan2007pdr.pdf), an example plot of which appears below (red curve). From this, one can derive the age distribution of the population, which is Equation 2 (with mistake: *b*₁*x* should be −*b*₁*x*). Given the age distribution (essentially a [population pyramid](https://www.populationpyramid.net/)), one can extract life expectancy by asking: at what age is the population of the age in question cut in half?

Noting that the curve for the !Kung bush-folk is buried within the raft of present-day hunter-gatherer curves, I use it as a reasonable representative. Pulling the Siler parameters listed in Table 2 of the paper, I create the following plots of survival, population distribution, and life expectancy for the !Kung.

![](https://dothemath.ucsd.edu/wp-content/uploads/2024/10/surv-kung.png)

![](https://dothemath.ucsd.edu/wp-content/uploads/2024/10/pop3-kung.png)

![](https://dothemath.ucsd.edu/wp-content/uploads/2024/10/life-kung.png)

Note that the last plot is qualitatively similar to the curves from Figure 3 in the paper (above). In the population plot, the total helps contextualize the population. In this case, it means that there are 1.0 infants (0–1 year old) per 32.8 people. A group of 100 people would therefore—statistically—have three infants and two three-year-olds (where the graph is near the 2/3 mark).

# Three Cases

The main group I am interested in understanding is present-day hunter-gatherers living ecological lives without much contamination from modernity (as noted above). This group therefore represents a (now rare) modality found at various places in the world today, for which reliable data exists—as shown in the collection of generally-similar curves from the paper. I will use the !Kung case to represent this modality.

But I am also curious about the prehistoric group, even though the model used in the paper is questionable. The curve in the figure is considerably different from the present-day hunter-gatherer groups—raising an eyebrow—and not drastically dissimilar from the wild chimpanzee curve. Color me skeptical, but I make the comparison anyway. Note that the paper has important caveats about the veracity of the prehistoric model: it might not be as brutish as depicted. Later, I give a quantitative argument that if the prehistoric curve were any lower, humans would flirt with species extinction, given reproductive timelines.

While the Siler parameters are not present in the paper for the prehistoric example, I was able to reconstruct a “reasonable” set by matching to the life expectancy outcome in the plot. Note that any effort at exactness would be pedantically silly, in this context. Here are the resulting plots.

![](https://dothemath.ucsd.edu/wp-content/uploads/2024/10/surv-prehistoric.png)

![](https://dothemath.ucsd.edu/wp-content/uploads/2024/10/pop3-prehistoric.png)

![](https://dothemath.ucsd.edu/wp-content/uploads/2024/10/life-prehistoric.png)

The third group I use for comparison is the World of 2020 (global average), as characterized by the 2022 United Nations World Population Prospects effort. In particular, the WPP provides numbers for infant mortality rate (2.8% loss by age 1), global life expectancy at birth, at 15 years, at 65 years, and at 80 years. These were sufficient to make a decent match via Siler parameters, the associated plots appearing below.

![](https://dothemath.ucsd.edu/wp-content/uploads/2024/10/surv-world.png)

![](https://dothemath.ucsd.edu/wp-content/uploads/2024/10/pop3-world.png)

![](https://dothemath.ucsd.edu/wp-content/uploads/2024/10/life-world.png)

The following table captures the Siler parameters used in this work, only the first of which comes explicitly from the motivating paper.

|             |       |       |       |          |       |
|-------------|-------|-------|-------|----------|-------|
| Group       | *a*₁  | *b*₁  | *a*₂  | *a*₃     | *b*₃  |
| !Kung       | 0.340 | 0.943 | 0.010 | 3.31E-04 | 0.077 |
| Prehistoric | 0.125 | 0.35  | 0.002 | 8.7E-03  | 0.053 |
| World 2020  | 0.04  | 0.90  | 0.001 | 2.3E-04  | 0.070 |

Siler Parameters

I don’t particularly *like* the prehistoric parameters, as they imply a lower infant mortality and constant-risk than for the !Kung. But don’t blame me: blame the plot I matched (whose prehistoric curve has a smaller step up to the peak from age zero than does the !Kung !kurve). As for constant risk, we’ll see later that the other parameters work to “cover” this, resulting in an overall higher mid-life risk than for the !Kung—so I’m less concerned about that parameter. In any case, it is not necessary to take any of this *literally* in order to still gain insights and illustrate some broad patterns.

# Key Questions

What do I want to extract from these models to help guide my thinking?

I’d want some comparative stats on likelihood of survival to particular ages. I’d like to understand something about life expectancy. I’d like to put daily risk of death in context. I’d like to know who the oldest person likely is in your band, or on the planet. What is the modal death age, beyond early life? In other words, when are you “expected” to die because your body gives out? I’d also like to know what total fertility rate (TFR) would hold the population steady for each survival model.

### Survival Rates

Let’s get right to it. First, survival odds at birth, in percent:

|             |          |          |           |           |
|-------------|----------|----------|-----------|-----------|
| Group       | To Age 1 | To Age 5 | To Age 15 | To Age 65 |
| !Kung       | 79       | 66       | 59        | 19        |
| Prehistoric | 89       | 70       | 56        | 0.4       |
| World 2020  | 97       | 95       | 94        | 66        |

Survival odds at birth, in percent

Again, I don’t take the infant mortality result literally for the prehistoric group (being better than for the !Kung), but that’s what the plot in the paper would produce if taken at face value. In all cases, ***most* newborns make it to reproductive age**, even for the just-surviving prehistoric distribution.

### Life Expectancy

How about life expectancy as a function of age, expressed as full life term rather than years remaining?

|             |          |          |          |           |           |
|-------------|----------|----------|----------|-----------|-----------|
| Group       | At birth | At Age 1 | At Age 5 | At Age 15 | At Age 65 |
| !Kung       | 29       | 44       | 52       | 55        | 74        |
| Prehistoric | 20       | 24       | 30       | 34        | 67        |
| World 2020  | 74       | 75       | 75       | 75        | 82        |

Can expect to live to this age (years) at various life (st)ages

By the time one reaches reproductive age among the !Kung, grand-parenthood can be expected, living into the mid-fifties. In the prehistoric case, once reaching reproductive age chances are pretty strong for surviving *through* the reproductive years. Note that reaching 65 in the prehistoric case is uncommon (0.4% chance, as per previous table), but once there the expectation is a couple more years of life. For the world today, mortality is so low until later in life that the needle is essentially stuck at 75 throughout the childhood years. If curious about other ages, these results can be pulled off the life expectancy graphs above (green), by adding age to years remaining.

### Mortal Peril?

How dangerous is daily life in the three groups? We express this as annual chance of survival, in percent, at the peak age (age with lowest chance of copping it).

|             |                 |          |             |
|-------------|-----------------|----------|-------------|
| Group       | Survival Chance | Peak Age | 1 in ? Odds |
| !Kung       | 98.9            | 10       | 34,000      |
| Prehistoric | 98.0            | 11       | 18,000      |
| World 2020  | 99.9            | 8        | 250,000     |

Chance of surviving, in percent, at “golden” age, and daily chance of survival

All these are pretty darned high, but we now see how even the very low *a*₂ value used in the prehistoric model does not translate to a free pass—the balance of the model appropriately yielding the lowest annual survival chance. In all cases, the safest time to be alive is roughly at age 10. The “odds” column is the **daily chance** of coming to life’s end at the golden age. In the worst case, it’s one chance in 18,000 (0.0056%). I would put forth that odds this low translate into *little daily concern* for death. You just go about the business you know well. Sure, you’re careful and alert, but it’s not a life of knife-edge terror—as conveyed in Quinn’s characterization of typical attitudes—and **I think that’s hugely important**! Don’t let fear of what we don’t *personally* know incorrectly color what the *actual* experience is like. We ought to be honest and admit that *we know almost nothing about it*.

### Elders

How old is the oldest person in your group likely to be? How much longer might that person expect to live? I use two different group sizes in this case: 150 and 1 million. The former represents a typical moderately-large clan size, deliberately chosen to align with [Dunbar’s number](https://en.wikipedia.org/wiki/Dunbar%27s_number). The second group size tries to get at prehistoric human population, so that the age represents the oldest person on Earth, given a million people.

|             |        |         |       |         |
|-------------|--------|---------|-------|---------|
| Group       | In 150 | Live To | In 1M | Live To |
| !Kung       | 82     | 85      | 100   | 101     |
| Prehistoric | 59     | 62      | 79    | 80      |
| World 2020  | 96     | 99      | 115   | 116     |

Oldest person in group, and how old you’d expect them to get

An octogenarian is not unusual among the !Kung, and if the world were populated by a million such people, it would likely contain a 100-year-old. The table suggests that the world has hosted 80-year-old humans for quite some time (relevant to the [Lifetime Ago post](https://dothemath.ucsd.edu/2024/01/a-lifetime-ago/)). Also interesting is that the oldest person in a group of 150 people is expected to live another 3 years for each of the disparate groups, while out of a million people it’s down to a year (a more extreme outlier).

Incidentally, to arrive at these numbers, I ask: at what age is the cumulative population beyond that age down to half-a-person. You’ve then got a 50/50 chance of encountering a live person at that age within the group.

### Seven Generations

I’ll take a brief detour from the statistical tables to point out that knowing grandparents was commonplace throughout human existence, and even great-grandparents were not rare. A person living to old age would therefore have direct personal knowledge of three generations prior, their own generation, and three generations following (their own great-grandchildren). That’s seven generations. We hear about various Indigenous cultures practicing “seventh generation” consideration, and I wonder if the origin of that number is based on direct personal knowledge. An elder has direct access to the experiences and stories of individuals along such a span of lifetimes.

### Modal Death

What is the most popular age for dying, beyond childhood? This is a different question than life expectancy. This is the age at which the population pyramid is tapering most steeply: where the largest attrition rate within the population occurs as failing physiology begins to dominate.

|             |           |
|-------------|-----------|
| Group       | Modal Age |
| !Kung       | 66        |
| Prehistoric | 32        |
| World 2020  | 81        |

Mode of death-age distribution, beyond childhood

The !Kung result is commensurate with the same investigation in [the paper](https://gurven.anth.ucsb.edu/sites/secure.lsit.ucsb.edu.anth.d7_gurven/files/sitefiles/papers/GurvenKaplan2007pdr.pdf), which concludes that people appear to be built to last about 7 decades, when conditions allow. Modern health care has extended that by about 15 years, but not really night-and-day different: a 20% change, for something like (at least) 1000% more per-capita resource use and extinction-level ecological destruction: a *very steep* price.

Meanwhile, note that the *ultimate* chance of death is exactly the same (100%) in all three modalities.

### Fertility

Finally, what total fertility rate (TFR) would support a steady population given the various survival models? While the result is not very sensitive to the choice of age-specific distribution of reproducing women, I adopted a simple model that ramps up linearly from ages 12 to 21, hangs steady until 31, then ramps back down toward zero at age 41. But again, the total is *far* more significant than how it gets spread among ages (i.e., hard to get changes greater than a few-percent via realistic alterations to the age-specific distribution).

|             |     |
|-------------|-----|
| Group       | TFR |
| !Kung       | 4.0 |
| Prehistoric | 5.1 |
| World 2020  | 2.3 |

Total Fertility Rate necessary to maintain steady population

The theoretical TFR for “replacement” in the complete *absence* of mortality through reproductive age would be 2.07 to account for the fact that male babies outnumber females by the ratio 1.07:1. We often hear that replacement is 2.1, which accounts for the male/female asymmetry and a smidge of mortality—appropriate for affluent countries. But the actual number for the world as it is right now, given its survival rates, is 2.26—with regional variation of course.

In any case, if only half of babies survive to reproductive age, the TFR needs to roughly double from today’s replacement value into the 4–5 ballpark in order to hold population steady—as the tables reflect. To me, this implies a lower-bound life expectancy at birth of about 20 years (meaning half make it to 20), as it takes until about that age to have enough children to just hold population steady. Thus, the prehistoric curve in the paper seems to be close to the worst-case lower bound for the merest *survival* of the human species. Some periods and locations were probably like this, but other places and times would have been less difficult.

Another hint along these lines is that the frontal cortex of the brain (the closest we get to wisdom) has not finished developing until the late twenties. Why would evolutionary processes bother if humans did not routinely achieve such ages?

# Reflections

How one looks at these tables depends on mindset. If it’s a matter of which one looks peachiest without applying broader considerations, well no doubt the world of 2020 offers the longest lives, lowest infant mortality, etc. If only it were a menu (subject of [last post](https://dothemath.ucsd.edu/2024/10/your-order-please/)). But, as I have stressed in other places, modernity is a fleeting apparition whose self-termination is an inevitable consequence of unsustainable, non-ecological living.

The question for me then becomes: is a different lifestyle that bears some similarity to past ways **tolerable**? I’m not saying that I know we will identically replicate hunter-gatherer styles in the coming millennia, although I would be unjustified in ruling that out. After all, modernity will leave a mark. We’ve learned some things that will stick. In that sense, the !Kung and other present-day hunter-gatherers might be more representative of survival statistics in an age when we have greater understanding of hygiene, disease transmission, the importance of clean water, etc. Some of those gains will not be easily lost.

So, could I tolerate a world in which a 10-year-old has a 1/34,000 (0.003%) chance of dying on any given day, where the oldest person in my clan is in her 80’s, and where I’m likely to live to 60 once into adulthood? Sure: seems less than harrowing. At age 54, I can reflect that the gift of life I have *already* experienced has been satisfying: i need not be greedy. If the foregoing scenario means halting the sixth mass extinction and setting up for a long tenure of ecological living for humans on this planet, the price seems fair to me (and who am I to protest, in any case, in defiance reality?). The last group on each of the “menus” (tables) above represents a false and fleeting “choice” that carries the price of colossal failure, mass extinction, and self-termination—souring the appeal.

**New Feature**: Subscribe to receive e-mail notices of new posts (info absolutely not shared!). But note that it may be some days before I get the e-mail server properly configured—so please be patient and assume you’ll get notifications eventually.

<div class="tnp tnp-subscription">

<div class="tnp-field tnp-field-firstname">

First name

</div>

<div class="tnp-field tnp-field-surname">

Last name

</div>

<div class="tnp-field tnp-field-email">

Email

</div>

<div class="tnp-field tnp-field-button" style="text-align: left">

</div>

</div>

Views: 2746

<div class="addtoany_share_save_container addtoany_content addtoany_content_bottom">

<div class="a2a_kit a2a_kit_size_32 addtoany_list" a2a-title="Life Expectations" a2a-url="https://dothemath.ucsd.edu/2024/10/life-expectations/">

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2024%2F10%2Flife-expectations%2F&linkname=Life%20Expectations "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2024%2F10%2Flife-expectations%2F&linkname=Life%20Expectations "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2024%2F10%2Flife-expectations%2F&linkname=Life%20Expectations "Email")[](https://www.addtoany.com/share)

</div>

</div>
