+++
title = "The games matrices play"
full_title = "The games matrices play"
date = "2007-03-15"
upstream_url = "https://www.gnxp.com/WordPress/2007/03/15/the-games-matrices-play/"

+++
Source: [here](https://www.gnxp.com/WordPress/2007/03/15/the-games-matrices-play/).

The games matrices play

As I’ve said before I’ve been reading Martin Nowak’s [Evolutionary Dynamics](https://www.amazon.com/exec/obidos/ASIN/0674023382/geneexpressio-20). Nowak is a mathematical biologist, and a lot of his research program deals with game theory, so it isn’t a surprise that several chapters in this book address exclusively game theoretic concepts. In the first chapter to tackle game theory head on Nowak covers a lot of ground, starting with the basics of frequency dependent strategies and pushing all the the way to some heavy theoretical ecology in regards to predatory-prey models. I’m going to pass over the more complex aspects of the chapter (e.g., Rock-Paper-Scissor strategies which involve 3 X 3 matrices), and just focus on the foundation: **fixed strategy two player games**.

  
The basic logic is simple. Consider the canonical [Hawk vs. Dove](https://en.wikipedia.org/wiki/Game_of_chicken#Hawk-Dove) game which the great evolutionary biologist J.M. Smith made famous, it is a classic frequency dependent dynamic in regards to **phenotype**. Assume for example you have a population of birds which share food when they encounter each other. In this scenario both birds get a smaller benefit than if they had found the food source alone, but they gain fitness nonetheless. Now, imagine what happens if a new morph emerges within a population, an aggressive form which challenges the dovish variant whenever it encounters food simultaneously. The doves will give ground, resulting in a gain for the hawk, and no fitness increase for the dove. When doves meet each other they gain half as much benefit as when they encounter food sources alone, but for a hawk the presence of a dove or a singular food encounter is irrelevant. On the other hand, **meeting another hawk is problematic, as two aggressive birds are going to enter into conflict**. Now the hawk strategy incurs a cost. If one emerges as a victor then one might still gain some food even after incurring the cost of the fight, but in a loss one not only loses the nutritional benefit, but one has expended energy in vain. The implication is clear: **as the hawk morph increases in frequency, taking advantage of the vulnerable dove morph, they begin to encounter more and more fellow hawks, and the increase in proportion of these encounters results in an average decrease in the fitness of the hawk strategy**. In contrast, doves do not enter into fights, so they do not incur the energetic costs of the fights. Eventually the frequency of hawks and doves should enter into a stable state in relation to the various costs and benefits which emerge from the combinations of the encounters.  
More formally, one can state:  
d(strategy 1)/dt = (proportion of strategy 1) X (proportion of strategy 2) X (fitness of strategy 1 as a function of proportion of strategy 1 – fitness of strategy 2 as a function of strategy 1)  
Verbally: the change in the proportion of strategy 1 with respect to time is a function of the product of the proportion of strategy 1 and the proportion of strategy 2 and difference in fitness of the two strategies conditional upon their proportions. When the change equals 0 then you have reached an equilibrium point, which can occur when the fitnesses are equal (and so they cancel out in the equation above) or one of the strategies is extinct.  
Get it? Well, perhaps not…which is why the models are presented in a graphical matrix format. Here is a generic 2 X 2 matrix which shows a two player game with two strategies:

|     |     |     |
|-----|-----|-----|
|    | A   | B   |
| A   | a   | b   |
| B   | c   | d   |

The small letters are payoffs. One can read them like so:  
a = the payoff to A when it plays against A  
b = the payoff to A when it plays against B  
c = the payoff to B when it plays against A  
d = the payoff to B when it plays against B  
Therefore, I generally read from the leftmost column toward the right. Additionally, feel free to reread what I just wrote up there, you need to know what a, b, c and d mean pretty well to make sense of what I’m going to say below without scratching your head if this is new to you. Now, the payoff matrix above maps onto this system of linear equations:  
fitness of A = a X (proportion of strategy A) + b X (proportion of strategy B)  
fitness of B = c X (proportion of strategy A) + d X (proportion of strategy B)  
Fitness has an obvious relationship to payoff, e.g., consider the food resources above. The payoffs are essential in determining the nature of evolutionary dynamics here. There are four primary outcomes here:  
1) A dominates B (so B goes extinct). Here the payoff of a \> c and b \> d.  
2) The inverse, where B dominates A, so a \< c and b c and b \< d. In this scenario A is the best response to A and B is the best response to B, so the final state will be determined by the initial condition (there is also an unstable equilibrium in the middle of the system). This is equivalent to a positive frequency dependence.  
4) A & B can stably coexist where a d. This is the situation where the best response to a strategy is the other strategy, e.g., A to B has a higher payoff than B to B, and vice versa. The equilibrium proportion will be determined by the the relations of the payoffs. This is basically a negative frequency dependence.  
Next, let’s move to the famous [Nash Equilibrium](https://en.wikipedia.org/wiki/Nash_Equilibrium), a non-cooperative game where the stable final state is where neither party can gain a better outcome by defecting. For the above generic payoff matrix here are the conditions for the Nash Equilibrium:  
1) A is a strict Nash Equilibrium if a \> c.  
2) A is a Nash Equilibrium if a \>= c.  
3) B is a strict Nash Equilibrium if d \> b.  
4) B is a Nash Equilibrium if d \>= b.  
A mathematical point is that if there are a set of pure strategies there may not be a Nash Equilibrium amongst those pure strategies, but, there will be at least one if you included in mixed strategies (e.g., facultative switching). I take that to mean that nature is filled with Nash Equilibriums (this is true from what I know).  
Here is a payoff matrix that illustrates the famous [Prisoner’s Dilemma](https://en.wikipedia.org/wiki/Prisoner's_dilemma):

|     |     |     |
|-----|-----|-----|
|    | A   | B   |
| A   | 3   | 0   |
| B   | 5   | 1   |

If both players choose “A” (A against A) then they gain a payoff of 3. But, if one player “defects” to B, then they gain 5, while the other has a sucker’s payoff of 0. So what to do? The Nash Equilibrium here is simple: both should pick B, because switching to A from this strategy is irrational. Though the payoff is lower than if they both chose A, one can not guarantee that the other player will also play A, while there is at least some payoff (1) if one chooses B, and the possibility of a larger one (5) if the other player chooses A.  
OK, to something more explicitly biological, the famous [Evolutionarily Stable Strategy](https://en.wikipedia.org/wiki/Evolutionarily_stable_strategy) (ESS). This is a strategy which resists invasion by another strategy, e.g., A resisting the mutant B. Going back to our payoff matrix above, if either a \> c, or, a = c and b \> d, then A can resist invasion by B. Note, this holds only for infinitely large populations and infinitesimally small numbers of an invader. A strict Nash Equilibrium is an ESS by definition.  
Finally, I want to end this with the payoff matrix of the Hawk vs. Dove game which I started out with. Here it is:

|     |         |     |
|-----|---------|-----|
|    | H       | D   |
| H   | (b-c)/2 | b   |
| D   | 0       | b/2 |

This means that:  
1) Playing Dove against Hawk results in a payoff of 0.  
2) Playing Hawk against Dove results in a benefit, b.  
3) Playing Dove against Dove results in a benefit divided in half, b/2.  
4) Playing Hawk against Hawk results in a benefit minus the cost of the fight divided by 2, (b – c)/2. The division by 2 is because both Hawks are equally strong so there is a 1/2 expectation of gaining the leftover from the benefit minus the cost.  
The relationship between benefit and cost can then be used to determine the equilibrium proportions.  
There are many other “games” out there, and this is just the beginning. Obviously one can employ “mixed” strategies, which are not fixed across interactions, and, there can be more than two strategies. The maths are more complex, but no less important, especially in theoretical ecology. But the general insights of **frequency dependence can be extrapolated outside of behavior and into genetics as well**. Consider the [MHC](https://en.wikipedia.org/wiki/Major_histocompatibility_complex) loci, among the most polymorphic amongst animals with an adaptive immune system. These alleles are essential to the [Red Queen Hypothesis](https://en.wikipedia.org/wiki/Red_Queen_Hypothesis), an arms race amongst organisms and their pathogens, and frequency dependent effects over millions of years have resulting in a never ending game as rare alleles are always a necessary part of the immune toolkit.  
**Addendum:** Most of the equations above are modified from [Evolutionary Dynamics](https://www.amazon.com/exec/obidos/ASIN/0674023382/geneexpressio-20).

### Related Posts:

- [Mathematical biologist Martin Nowak
  interviewed](https://www.gnxp.com/WordPress/2007/06/25/mathematical-biologist-martin-nowak-interviewed/) - [Martin Nowak
  profile](https://www.gnxp.com/WordPress/2007/10/15/martin-nowak-profile/) - [Martin Nowak, man of
  God](https://www.gnxp.com/WordPress/2007/07/31/martin-nowak-man-of-god/) - [Martin Nowak interview
  (translated)](https://www.gnxp.com/WordPress/2007/06/25/martin-nowak-interview-translated/) - [Evolution of
  Cooperation](https://www.gnxp.com/WordPress/2006/05/01/evolution-of-cooperation/) - [Group & kin
  selection](https://www.gnxp.com/WordPress/2007/04/13/group-kin-selection/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F03%2F15%2Fthe-games-matrices-play%2F&linkname=The%20games%20matrices%20play "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F03%2F15%2Fthe-games-matrices-play%2F&linkname=The%20games%20matrices%20play "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F03%2F15%2Fthe-games-matrices-play%2F&linkname=The%20games%20matrices%20play "Email")[](https://www.addtoany.com/share)
