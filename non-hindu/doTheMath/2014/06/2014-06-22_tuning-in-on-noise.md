+++
title = "Tuning in on Noise?"
full_title = "Tuning in on Noise?"
upstream_url = "https://dothemath.ucsd.edu/2014/06/tuning-in-on-noise/"
date = "2014-06-22"

+++
Source: [here](https://dothemath.ucsd.edu/2014/06/tuning-in-on-noise/).

Tuning in on Noise?

[![xkcd-904](https://dothemath.ucsd.edu/wp-content/uploads/2014/06/xkcd-904-225x300.png)](https://dothemath.ucsd.edu/wp-content/uploads/2014/06/xkcd-904.png)It’s a bit off-topic for the series, but I can’t even go to Google now without being reminded of the World Cup and soccer this, soccer that. (Apologies to non-Americans who know the sport as football—but don’t get me started on football!) I have often wondered: given characteristic low score values, is soccer anything more than Poisson noise? When discussing this with colleagues, one pointed me to this [XKCD comic](http://xkcd.com/904/), reproduced at right.

Any random process that produces discrete events in some time interval, with uniform probability per unit time follows a Poisson distribution. When the number of events becomes large, the distribution tends toward a Gaussian (normal) distribution.

My thesis is that soccer is an amalgam of random processes whose net effect produces rare events—those more-or-less unpredictable events spread more-or-less uniformly in time. Whether a good or bad bounce off the bar, a goal keeper who may or may not prevent a goal, a referee who may or may not see an illegal action, a pass that may or may not be intercepted, and on and on: the game is full of random, unpredictable events. So I expect soccer to behave similarly to a Poisson process and follow a Poisson distribution. By extension, I will claim that the attention devoted to the World Cup is founded on flimsy numerology and might even be called a tremendous waste of time and money.

Normally I allow comments on Do the Math for ten days after each post. I’ve tackled some controversial topics and stirred up emotional responses. Yet I predict that the outrage generated by my insinuation that watching soccer is a waste of time will absolutely dwarf the reactions to my saying that we may not be looking at a [space-faring future](https://dothemath.ucsd.edu/2011/10/why-not-space/ "Why Not Space?"), or that indeed we may face [collapse of civilization](https://dothemath.ucsd.edu/2012/02/the-way-is-shut/ "The Way is Shut"). To the extent that this (untested) prediction is true, it would seem that soccer is more important than the fate of the world, in the eyes of many. Scary, if true. \[After reconsideration, I enabled comments, but I won’t have time to vet and respond with my usual level of attention.\]

But getting back to soccer numerology, my question becomes: given a final score (which is taken to be the ultimate “truth” of the match) how likely is it that the victor is *actually* a better team?

## Expectations and Subtleties

One could imagine other measures of a team’s prowess in a game besides final score, like how many shots on goal, what fraction of the time a team’s offense keeps the ball downfield, how many goals the keeper directly prevented, etc. But it’s the final score that dictates the fate of the team in the series. So I’ll go with the measure that has actual consequences and most directly influences the high emotions of the fans.

But what is the truth of the situation? If team A were to play team B many times, what would the outcomes be? In this hypothetical situation, we want to compare the teams as they are at one moment in time, ignoring fatigue, changes in roster, injuries, evolving strategies, etc. that would happen if we *actually* had the teams play many games in series. What I’m after is a measure of the capabilities of the team at an instant in time: a snapshot. We will characterize this as the expectation value, or *X_(A)* for team A and *X_(B)* for team B. These measures can be thought of as the average score the team would acquire in repeated trials (matches), and in general will not be confined to integers, like the actual scores are.

Now, the value *X_(A)* is not a universal characteristic of team A. It’s only valid when playing team B. If a World Cup team (A) played a high school team (B), we would not be surprised by a score of 83 to 0, and if played multiple times, we may find that *X_(A)*=68.3 and *X_(B)*=0.7. Each instance would produce random numbers near these averages. But if the same team (A) plays another World Cup team, we might see *X_(A)*=2.3 and *X_(B)*=1.9, so that a 2:2 tie would not surprise us. Then when team A encounters World Cup team C, we might find that *X_(A)*=1.3 and *X_(C)*=0.8. While team A will still often prevail against team C, perhaps team C’s defense is able to shut down team A’s offense more effectively than is the case for team B. Different strengths and weaknesses make the expectation values depend on the particulars of the match-up. And we can’t necessarily apply transitive properties. For instance, we could have *X_(A)\>*X_(B) when A plays B, *X_(B)\>*X_(C) when B plays C, yet *X_(C)\>*X_(A) when A plays C—based on the peculiarities of cross-team “chemistry.” And even *X_(A) compared to *X_(B) could change over time if the teams *actually* played each other multiple times in a series or season.********

All this is to say that I get the subtleties (at least some of them). I am not saying that I can reduce the entire sport to algorithmic expectations. That’s why I want to focus on **a particular game** resulting in **a particular score**. Given that there are *some* “true” expectation values for that match-up, how much meaning can we place in the final score given random fluctuations?

## Poisson Statistics

First, a look at the math of Poisson statistics. If I have an expected (average) outcome of *X* (traditionally labeled *&lambda*), what are the chances that in a given trial (game) I get *N* as a result, where *N* is an integer? Under Poisson statistics, the answer is:

> p(N)=X^(N)e^(−X)/N!

where *e* represents the exponential function, and *N!* is *N*-factorial, or *N*(*N*−1)(*N*−2)…1 (e.g., 4!=24). Some relevant examples appear in the table below.

|     |         |         |         |         | |-----|---------|---------|---------|---------| | *N* | *X*=0.7 | *X*=1.0 | *X*=2.0 | *X*=2.4 | | 0   | 0.496   | 0.368   | 0.135   | 0.091   | | 1   | 0.348   | 0.368   | 0.271   | 0.218   | | 2   | 0.122   | 0.184   | 0.271   | 0.261   | | 3   | 0.028   | 0.061   | 0.180   | 0.209   | | 4   | 0.005   | 0.015   | 0.090   | 0.125   | | 5   | 0.001   | 0.003   | 0.036   | 0.060   | | 6   | 0.000   | 0.001   | 0.012   | 0.024   |

Each column (when extended to all *N*) sums to 1.0, as probability should. Note all “teams” above may score zero by chance, even if “expected” to score 2.4 in a game. Sure, the probability of zero is reduced to 9% for the *X*=2.4 team, but it will happen. The point is that the Poisson distribution is pretty spread out, but in a sensible way: the team with an expectation of 0.7 has essentially no chance of scoring 6 by dumb luck, while the 2.4 team (coincidentally) has a 2.4% chance of doing so.

We can turn the Poisson distribution around, and ask: if a team scores *N* points, what is the probability (or more technically correct, the probability density) that the underlying expectation value is *X*? This is more relevant when assessing an actual game outcome.

An example appears in the plot below. The way to read it is: if I have an expectation value of \<*value on the horizontal axis*\>, what is the probability of having 2 as an outcome? Or inversely—which is the point—if I have an outcome of 2, what is the probability (density) of this being due to an expectation value of \<*value on the horizontal axis*\>?

## [![inverse-poisson](https://dothemath.ucsd.edu/wp-content/uploads/2014/06/inverse-poisson-1024x768.png)](https://dothemath.ucsd.edu/wp-content/uploads/2014/06/inverse-poisson.png)Example Application

By applying this inversion to both teams’ final scores, we can assess the frequency that the winning team is actually better (i.e., has a higher expectation value) than the losing team. We form a two-dimensional parameter space comprised of all values of *X_(A)* and *X_(B)*, and for each one can assess the joint probability of getting the score *N* to *M*. The joint probability is found by multiplying the individual probabilities. Figuring joint probabilities in this way assumes independence of the two scores, which is certainly open to criticism. Don’t mistake this independence for claiming that the teams have no effect on each other: the expectation values embody this dynamic, and are particular to the match-up. This independence is basically saying that the expectation values do not change as a result of how many goals the other team winds up scoring in the game. Maybe a team is galvanized by the others’ score, or maybe demoralized. This would impact independence, but I can think of lots of scenarios in which it would go either way, so will not bias in one particular direction.

If you’re on board and keen to see the results, skip ahead. But if you still want a feel for how this scheme works in practice, an illustrative table appears below for the case of a 2 to 1 final score.

|          |       |       |       |      |      |        | |----------|-------|-------|-------|------|------|--------| | *X* vals | 1     | 2     | 3     | 4    | 5    | totals | | 1        | 6.77  | 4.98  | 2.75  | 1.35 | 0.62 | 16.47  | | 2        | 9.96  | 7.33  | 4.04  | 1.98 | 0.91 | 24.22  | | 3        | 8.24  | 6.06  | 3.35  | 1.64 | 0.75 | 20.04  | | 4        | 5.39  | 3.97  | 2.19  | 1.07 | 0.49 | 13.11  | | 5        | 3.10  | 2.28  | 1.26  | 0.62 | 0.28 | 7.54   | | 6        | 1.64  | 1.21  | 0.67  | 0.33 | 0.15 | 4.00   | | 7        | 0.82  | 0.60  | 0.33  | 0.16 | 0.08 | 1.99   | | totals   | 35.92 | 26.43 | 14.59 | 7.15 | 3.28 | 87.37  |

The winning team’s expectation value increases along the left hand side, and the losing team’s expectation value runs along the top. This table captures 87% of the possibilities; had I extended in both directions (to larger expectation values) and sampled less coarsely, we would have gotten 100%. The way to interpret this table is that if the final score was 2 to 1, the chances that the expectation values were actually 2 vs. 1—in line with the final score—is 10%. The chances that the roles are reversed, and the expectation values were 1 vs. 2 is 5%. There is a 2% chance that the losing team had an expectation of 4 while the winning team had an expectation of 2, making this a dramatic upset. The most probable “truth” is an expectation of 2 vs. 1, in accordance with the actual score. Looking at the totals, the most probable expectation for team A (winner) is 2, while for team B the most likely expectation score is 1—again in accordance with expectation.

If we sum the probabilities in the table where the winning team’s expectation is indeed higher than the losing team’s (correct game outcome), splitting the probabilities when the expectations are matched, we get 58.5% (though out of 87% total, so we might expect about 67% if we had extended the table. The implication is that a 2 to 1 score is correctly interpreted as a statement of dominance two-thirds of the time.

## Calculated Results

But the above example is a bit coarse-grained. A more thorough exploration of parameter space would include fractional expectation values. So get ready for the full deal. In the table that follows, each row represents a score for a non-tie game (from which all we can conclude is that each team has a 50% chance of being better than the other). Following are percent chances that the winning team is truly better than the losing team. The second column examines every expectation value between 0 and 16 in steps of 0.01, uniformly weighted. That’s 1600 cases for each team, for a total of 2.6 million test cases. You’ll forgive me for not including the table associated table this time. It does not pay to extend beyond expectations of about 16, because the Poisson inverse probability is pretty much dead by this time.

|        |         |              |              |              | |--------|---------|--------------|--------------|--------------| | Score  | Uniform | μ=1.5, σ=2.0 | μ=2.0, σ=2.0 | μ=2.0, σ=1.5 | | 1 to 0 | 75.1    | 73.1         | 72.7         | 71.2         | | 2 to 1 | 68.7    | 66.4         | 66.1         | 64.9         | | 2 to 0 | 87.6    | 84.7         | 84.3         | 82.4         | | 3 to 2 | 65.6    | 63.3         | 63.1         | 62.1         | | 3 to 1 | 81.2    | 77.6         | 77.2         | 75.4         | | 3 to 0 | 93.8    | 91.1         | 90.7         | 88.9         | | 4 to 3 | 63.7    | 61.4         | 61.2         | 60.4         | | 4 to 2 | 77.3    | 73.5         | 73.1         | 71.6         | | 4 to 1 | 89.1    | 85.1         | 84.7         | 82.8         | | 4 to 0 | 96.9    | 94.7         | 94.4         | 92.9         | | 5 to 4 | 62.3    | 60.1         | 59.9         | 59.3         | | 5 to 3 | 74.6    | 70.7         | 70.4         | 69.0         | | 5 to 2 | 85.5    | 81.0         | 80.6         | 78.9         | | 5 to 1 | 93.7    | 90.1         | 89.7         | 87.9         | | 5 to 0 | 98.4    | 96.8         | 96.5         | 95.4         | | 6 to 5 | 61.2    | 59.1         | 59.0         | 58.4         | | 6 to 4 | 72.5    | 68.7         | 68.4         | 67.2         | | 6 to 3 | 82.8    | 78.0         | 77.6         | 76.1         | | 6 to 2 | 91.0    | 86.6         | 86.1         | 84.4         | | 6 to 1 | 96.5    | 93.5         | 93.1         | 91.6         | | 6 to 0 | 99.2    | 98.0         | 97.8         | 96.9         |

So far, we have considered no prior information on likely expectation values for a team. We have let the low scores effectively kill the chances of the actual expectation being very large (it would be unlikely indeed for a team with *X_(A)*=45 to end up scoring 3 points in a game). So the calculation converges without needing to assume any priors. But we can do better than this. We already have a sense for typical soccer game scores. We can model this reasonably with a Gaussian distribution whose mean, *μ* might be around 2, and whose standard deviation, *σ*, may be similar. Such a distribution would slightly disfavor a team’s average score from getting too low or too high.

Three test-case distributions for a team’s expected average score, *X_(A)*, appear in the plot below.

[![soccer-dist](https://dothemath.ucsd.edu/wp-content/uploads/2014/06/soccer-dist-1024x768.png)](https://dothemath.ucsd.edu/wp-content/uploads/2014/06/soccer-dist.png)



The final three columns in the huge table above correspond to these three cases. What we find is that the probability of the winning team actually being better is not terribly sensitive to any weighting we might apply to favor “reasonable” expectation values. In general, the reliability of final scores correctly picking the winner *decreases* when “realistic” expectation values are considered.

Therefore, given a final score, you can look at this table and see how meaningful the score is in the face of Poisson statistics. A 3:2 score gives the winning team only a 5-in-8 chance of actually being a better team—in the absence of any additional information. But that’s the criterion for advancing: the score is paramount, and no other considerations are entertained.

## Reflection

Personally, I don’t find this to be very impressive. Even a 6:1 blowout leaves a 7% chance that it was a statistical fluke. More typical scores are even less decisive.

Maybe some force within the game operates to squelch Poisson variation. This can be true in sports where a scoring event on the part of one team gives control to the other team for a time. But control flips back and forth so many times in soccer that it’s hard to spot a mechanism that kills statistical variation. It’s a good random machine. Sure, you can have a team whose offense is not often in control of the ball. This (and other factors) may suppress the expectation value, but does it remove the randomness? I would be skeptical.

Admittedly, I don’t follow soccer—in part because I suspect it boils down to watching well-executed random events. It could be that team A beating team B by 2:1 is a pretty repeatable event. What I *have* seen (and I have been to a World Cup game) seems to amount to a series of low-probability scoring attempts, where the reset button (control of the ball) is hit repeatedly throughout the game. I do not see a lot of long-term build-up of progress. One minute before a goal is scored, the crowd has no idea/anticipation of the impending event. American football by contrast often involves a slow march toward the goal line. Basketball has many changes of control, but scoring probability per possession is considerably higher. Baseball is a mixture: as bases load up, chances of scoring runs ticks upward, while the occasional home run pops up at random. Alas, for soccer, I can’t easily get past the smell of Poisson.

Oh geez: now *I’ve* wasted time on the World Cup too!

Hits: 1231

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2014%2F06%2Ftuning-in-on-noise%2F&linkname=Tuning%20in%20on%20Noise%3F "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2014%2F06%2Ftuning-in-on-noise%2F&linkname=Tuning%20in%20on%20Noise%3F "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2014%2F06%2Ftuning-in-on-noise%2F&linkname=Tuning%20in%20on%20Noise%3F "Email")[](https://www.addtoany.com/share)