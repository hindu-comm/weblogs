+++
title = "The greater fool theory"
full_title = "The greater fool theory 1 A mostly verbal mathematical model"
date = "2009-08-19"
upstream_url = "https://www.gnxp.com/WordPress/2009/08/19/the-greater-fool-theory-1-a-mostly-verbal-mathematical-model/"

+++
Source: [here](https://www.gnxp.com/WordPress/2009/08/19/the-greater-fool-theory-1-a-mostly-verbal-mathematical-model/).

The greater fool theory 1: A mostly verbal mathematical model

Here is [a brief description of the idea](https://en.wikipedia.org/wiki/Greater_fool_theory) that price bubbles are caused by people buying something, not necessarily because they think it’s worth anything, but because they think they can find an even greater fool to buy it at a higher price. This continues until no more such fools can be found, and this bust drives prices back down to what they were before the boom began.

I didn’t see any references to mathematical models of the theory at Wikipedia or through Googling around a bit, so I made one up today at Starbucks since I didn’t have anything to read to pass the time. Because I’m not an economist, I don’t know how original it is, or how it compares with alternative models of the greater fool theory (if they exist). So, this is intended just as an exercise in modeling, explaining the model, and hopefully shedding some light on how the world works. I’ve kept most of the exposition straightforward and largely verbal, so that you don’t need to know much math at all to understand what the model says and what its implications are.

In part 1, I lay out the logic of the model and explain enough of it to show that it is capable of producing a single round of boom-and-bust for price hype. Part 2 will provide more mathematical detail about how the dynamics unfold, a phase plane analysis, and graphs of how the variables of interest would change over time, to better wrap your brain around what the model predicts.

This is a dynamic model, or one that tracks how things change over time — after all, we want to see how price, the number of fools, etc., evolves. It is made of several differential equations, and all these equations say is what causes something of interest to go up or go down over time. (You may recall that the sign of a derivative tells you whether a function is increasing or decreasing, and the magnitude says by how much.) I’ll only explain what is absolutely necessary for the reader to see what’s going on, with the less necessary math being confined to footnotes.

First, we set up the basic picture before we write down equations. My version of the greater fool theory goes like this. There is a population of people, and during a price bubble they can fall into three mutually exclusive groups: suckers (S), who are susceptible to joining in on the bubble; investors (I), who currently own the speculative stuff (such as a home bought for speculation); and those who are retired from the bubble (R), who used to be investors but have gotten rid of their investment. And of course there is the price of the thing — I model only the extra price that it enjoys due to hype (P), above its fundamental value, since this is the only component of price that changes radically during the bubble.

I set the population to be fixed in size during the bubble, since growth or decline is negligible over the handful of years that the bubble lasts. I also set the amount of speculative stuff to be fixed, which is less general — supply should shoot up to meet the rising demand during a bubble. So, this model is restricted to cases where you can’t produce lots more of the stuff, relative to how much already exists, on the time-scale of the bubble’s boom stage (say, 5 years or less). Or perhaps no more of it will be produced at all, such as video game consoles from decades ago that the original manufacturers will never bring back into production, but which nostalgic fans have taken to buying and selling speculatively (like NEC’s TurboDuo). Last, the amount of stuff that each investor has is the same across all investors and stays constant — say, if each investor always owned just one speculative home.

At the start of the bubble, there is a certain number of early investors. In order to sell their stuff, they need to meet a sucker to sell it to. When they meet — and I assume the two groups are moving around independently of each other — there is a probability that the sale will be made. If they make a deal, the sucker is now an investor, and the former investor is now retired. In this model, retireds do not again become suckers — they consider themselves lucky to have found a greater fool and stay out of the bubble for good afterward. That’s the extent of how people change between groups.

As for price hype, again I’m not an economist, so the exact formula may differ from what’s standard. I take it to respond positively to demand — namely, the number of suckers — and that there is a multiplier that serves as a reality check. This reality check should be weak at the start when most non-investors are suckers, and should be strong near the end when most non-investors are retired. In other words, the price hype at the beginning is a near total distortion — nearly 0% accurate — whereas the price hype near the end is nearly 100% accurate. This will make more sense once we write down formulas.

Now we get to the differential equations for how these things change. We write down one equation for each variable whose values we’re tracking over time. I use apostrophes to denote the derivative with respect to time (i.e., rate of change):

S’ = -aSI

Since suckers can only lose members (by turning into investors), there is only one term, and it shows how suckers decline (negative sign). Remember, retireds do not go back into the pool of potential buyers. And investors either make a sale and go into the retired group, or they sit on their stuff in hope of selling, so they never contribute to the growth of suckers. Thus, there is no growth term. The parameter a shows the probability that, when a sucker and an investor meet, the investor will transfer his stuff to the sucker. (“Parameter” is another word for “constant,” in contrast to a variable that changes.) The reason we use the product of S and I is that this is essentially the rate at which the two groups encounter each other when they move around independently of each other. \[1\]

I’ = aSI – aSI = 0

Investors both grow and decline, so one term is positive and the other negative. They grow by having a sucker join their ranks, which as we saw above happens at rate aSI. However, each time that happens, the investor loses his stuff and becomes retired. That happens at the same rate, and the negative sign just shows that this causes I to decline. When we simplify, we get I’ = 0 — that is, the number of investors does not change over time. That makes sense because each bundle of stuff always has an owner, regardless of how it may change hands, somewhat like the game of hot potato. When something doesn’t change, it is constant, so whenever we see I from now on, we’ll know that this is just another parameter, not a variable that changes. In particular, it refers to the initial number of early investors who get the bubble going.

R’ = aSI

Retireds never join the suckers again. And recall the mindset of a retired person — they knew the stuff was junk and are glad to have gotten through the selling process, so they cannot be sold the stuff again to become investors once more. Thus, there is no way for them to lose numbers. They grow by former investors making a sale and becoming retired, which once again happens at rate aSI.

Here’s the neat thing: notice that S’ + R’ = -aSI + aSI = 0. The sum of the two derivatives equals zero, and since taking a derivative shows the distributive property, this also means that (S + R)’ = 0. That is, the sum of suckers and retireds does not change over time. This makes sense since, if the number of investors stays constant, the leftovers — suckers and retireds — is constant, regardless of how each separate group grows or shrinks. We can take this further to note that S’ + I’ + R’ = 0, which means (S + I + R)’ = 0. That is, the combined size of all three groups does not change over time — which is just what we claimed by keeping total population size constant. (Otherwise, each group would have birt  
h and death terms, aside from the terms that show how their members switch between groups.)

We’ll call this constant total population size N. So, S + I + R = N. Now, I is just a constant, so we’ll move it to the other side: S + R = N – I. We have two variables, S and R, but we just wrote an equation connecting them, so we can re-write one in terms of the other. I’ll choose R, but it doesn’t matter. So, R = N – I – S, and anywhere we see R, we can replace it with N – I – S. In other words, we’ve removed R from our focus — we can always get it from knowing what the variable S is, as well as the two parameters N and I. That means the equation for R’ only gives us redundant information, and we can ignore it. We can also ignore the I’ equation, since it just tells us that I is constant, and we’re only interested in things that change. So we’re left with just the S’ equation.

Now we move on to the price hype formula and how it changes over time. First, the formula for price as a function of demand and the reality check, since hype is never totally irrational and at least tries to take stock of reality:

P = bS(R / Rmax) = bS(R / (N – I))

Demand is driven by the number of suckers — the ones who eventually want to get in on the bubble — and the parameter b says how strongly demand responds to the number of suckers. The multiplier (R / Rmax) provides a reality check. If you landed from Mars and only knew the number of suckers, you would also want to know how many retireds there were — if there were few retireds, that would tell you the bubble had only just begun, so that hype is likely to be high and to go even higher short-term. Thus, this filter should not let much of the demand information through. Indeed, when R is very low compared to Rmax, the multiplier is near 0.

However, if you saw that there were many retireds, that would say the bubble was near its bust moment, and that the information from demand is very accurate by this point. Indeed, when R is near Rmax, the multiplier is near 1 and the filter lets just about all of the demand information through. What is Rmax? It is the value when no one is a sucker and everyone is retired, aside from the constant number of investors. Looking above at the equation S + R = N – I, we see that when there are no suckers, R = N – I.

Now we need to find the differential equation for how P changes over time. Using the product rule for derivatives \[2\], we get:

P’ = (abI / (N – I)) \* S(2S + I – N)

Since a, b, I, and N – I are always positive, and since S is positive except for the very end of the bubble when it is 0, in the meantime, whether price hype shoots up or crashes down depends on whether the term 2S + I – N is positive or negative. It is positive and price hype grows when S exceeds (N – I) / 2, which is half the size of non-investors. It is negative and price hype declines when S is below (N – I) / 2. It is 0 and price hype momentarily stalls out when S is exactly (N – I) / 2.

Because the bubble starts with all non-investors being suckers, S is initially N – I, which is greater than (N – I) / 2. So at first the price hype shoots up. However, remember that S only declines — as more and more of the suckers are drawn into the bubble (some of whom may also make sales and become retireds), S will inevitably fall below (N – I) / 2 and price hype will start to contract.

When S inevitably reaches 0 — when all non-investors are out of the bubble for good — then P = 0 (recall that P = bS(R / Rmax)). Moreover, at that time P’ = 0 too. Thus, at the end, price hype has completely evaporated and it will stay that way. This is a single round of boom-and-bust for price hype.

In this post, I’ve shown how some pretty simple “greater fool” dynamics can lead to a boom-and-bust pattern for price hype. You can quibble with all of the assumptions I’ve made, but the model shows that the greater fools theory is a viable explanation for price bubbles. I’ve relaxed some of the assumptions to see if it makes a difference, like making the decline of S be a saturating rather than linear function of S, and so far they don’t seem to affect things qualitatively. A more realistic model would have P appear in the equation for S’ — that is, to have price hype affect the probability of making a sale. Or rather, the trend of prices (P’ ) should affect sale probability — if suckers see that price hype is increasing, they should want to get in on the bubble, and to stay put if price hype is dropping. Also, allowing retireds to re-enter the pool of suckers would be more general and would almost certainly lead to sustained cycles of boom-and-bust, rather than a single round. But that’s for another slow afternoon.

In part 2, I’ll go into more mathematical detail about how we see what states this system is at rest in, and whether they are stable to disruptions or not. I’ll look more at the formula for the maximum level of price hype, and interpret that in real-world terms in order to see what things will give us larger-amplitude bubbles. I’ll provide a picture of the phase plane, which shows what the equilibrium points are, and how the variables will change in value on their way from their starting values to the final ones. I’ll also have a couple of graphs showing how the number of suckers and retireds, and the amount of price hype, change over time.

\[1\] Draw one person at random, and the chance that they’re a sucker reflects S. Draw another one at random, and the chance that they’re an investor reflects I, since the draws are independent. The chance of doing both is just the product of the two separate probabilities.

\[2\] P’ = (bS(R / Rmax))’ = (b / (Rmax)) (S’ \* R + S \* R’)  
A little algebra, which you can confirm by hand or using Maple, gives the equation in the main body for P’.

### Related Posts:

- [Math convinces
  Dawkins](https://www.gnxp.com/WordPress/2008/01/01/math-convinces-dawkins/) - [Formalization &
  process](https://www.gnxp.com/WordPress/2007/12/31/formalization-process/) - [Open Thread,
  2/8/2015](https://www.gnxp.com/WordPress/2015/02/08/open-thread-282015/) - [Hey Canada](https://www.gnxp.com/WordPress/2010/03/03/hey-canada/) - [Math = conservative, Verbal =
  liberal](https://www.gnxp.com/WordPress/2006/06/30/math-conservative-verbal-liberal/) - [Movies; watch, and
  don't](https://www.gnxp.com/WordPress/2008/08/23/movies-watch-and-dont/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F08%2F19%2Fthe-greater-fool-theory-1-a-mostly-verbal-mathematical-model%2F&linkname=The%20greater%20fool%20theory%201%3A%20A%20mostly%20verbal%20mathematical%20model "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F08%2F19%2Fthe-greater-fool-theory-1-a-mostly-verbal-mathematical-model%2F&linkname=The%20greater%20fool%20theory%201%3A%20A%20mostly%20verbal%20mathematical%20model "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F08%2F19%2Fthe-greater-fool-theory-1-a-mostly-verbal-mathematical-model%2F&linkname=The%20greater%20fool%20theory%201%3A%20A%20mostly%20verbal%20mathematical%20model "Email")[](https://www.addtoany.com/share)
