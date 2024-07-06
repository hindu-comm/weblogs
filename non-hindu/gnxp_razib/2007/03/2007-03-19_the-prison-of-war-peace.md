+++
title = "The Prison of War &"
full_title = "The Prison of War & Peace"
date = "2007-03-19"
upstream_url = "https://www.gnxp.com/WordPress/2007/03/19/the-prison-of-war-peace/"

+++
Source: [here](https://www.gnxp.com/WordPress/2007/03/19/the-prison-of-war-peace/).

The Prison of War & Peace

A few days ago I began a survey of Martin Nowak’s treatment of modern game theory in his book [Evolutionary Dynamics](https://www.amazon.com/exec/obidos/ASIN/0674023382/geneexpressio-20). Today I’m going to hit the [Prisoner’s Dilemma](https://en.wikipedia.org/wiki/Prisoner's_dilemma). Roughly, this scenario is one where two individuals are isolated, and if they both keep their mouths shut (cooperate) they get off, but, if one rats the other out while the other keeps silent, the silent partner is screwed while the snitch gets off. If *both* of them rat the other out they get a prison sentence, but a lighter one than if they had kept silent while the other ratted them out. In other words: **ratting the other person out is the “rational” option**. So, the question is, why don’t we see a war of all against all in the world around us? That is what Nowak addresses in a whole chapter, and his exploration and treatment is highly ambitious, **and it is clear that his long term aim is to characterize human action**. Nowak aims to finish the house that Robert Trivers began constructing with his theory of reciprocal altruism.

  
Here’s a payoff matrix for a Prisoner’s Dillemma:¹

|           |           |        |
|-----------|-----------|--------|
|          | Cooperate | Defect |
| Cooperate | 3         | 0      |
| Defect    | 5         | 1      |

The rows to the left are “your” strategies, while the top row indicates the strategy you play against. The integers represent your payoff. So,  
If you cooperate and the other person cooperates payoff = 3  
If you cooperate and the other person defects payoff = 0  
If you defect and the other person cooperates payoff = 5  
If you defect and the other person defects the payoff = 1  
The best **group strategy** is for both individuals to cooperate, the total payoff is 6 between the two individuals, **but**, that’s not a Nash Equilibrium, it’s rational to switch to defect and gain a payoff of 5. On the other hand, if you defect, and other individual defects, the Nash Equilibrium is attained, you can’t get a better payoff by switching to another strategy. The aggregate payoff, 2, is lower than if you cooperate, but if your opponent switches you’ll get a payoff of 5! There’s no sucker’s penalty here.  
More formally, consider the payoff (in biology it would be fitness) for the cooperative strategies as f_(C), and for the defecting strategies as f_(D). If the proportion of cooperators is given by x, then the defectors are by definition 1 – x. More formally the proportions would be multipled by the payoffs resulting in:  
f_(C) = 3 \* x + 0 \* x  
f_(D) = 5 \* (1 – x) + 1 \* (1 – x)  
Simplifying:  
f_(C) = 3 \* x  
f_(D) = 4 \* x + 1  
If x is a proportion between the interval 0 and 1, then by definition 4x + 1 \> 3x, so any way you square it, the defecting strategy is the best bet.  
So why cooperation? Well, reality is a bit more complicated. Let’s modify the scenario above, and instead of 1 round we’ll play the game for multiple rounds, defined by m. There are two strategies:  
GRIM,² where the player cooperates initially and continues to cooperate unless the other player defects, and which point it will defect permanently. And ALLD, always defect, which is pretty straightforward.  
The payoff matrix will be defined like so:

|      |            |              |
|------|------------|--------------|
|     | GRIM       | ALLD         |
| GRIM | mR         | S + (m – 1)P |
| ALLD | T + (m-1)P | mP           |

Where a generic payoff matrix uses the notation:

|     |     |     |
|-----|-----|-----|
|    | C   | D   |
| C   | R   | S   |
| D   | T   | P   |

If you read my previous post about [reciprocal altruism](https://en.wikipedia.org/wiki/Reciprocal_altruism) you know that **a particular number of iterations is necessary for recriprocation to be important**. In other words, “one off” encounters reward selfishness, repetitions reward more complex strategies, including facultative cooperation. So, for a given payoff matrix the the parameter m, the number of iterations, can be defined where GRIM can beat ALLD. Formally the condition where GRIM can resist invasion against ALLD (that is, it is an [ESS](https://en.wikipedia.org/wiki/Evolutionarily_stable_strategies)) is defined by:  
m \> (T – P)/(R – P), or, verbally  
Where m is greater than the ratio of the payoff to the defector againt a cooperator minus the simultaneous defection scenario and the payoff of simultaneous cooperation minus the simultaneous defection scenario.³ In other words, the nature of m is conditioned by the nature of the ratios of the various payoffs in each scenario. If the payoff for defection is high, then m will be higher as the numerator will increase in value. In contrast, if the payoff for cooperation is high then the denominator will increase and so m will decrease (fewer interactions necessary). But, it is important to note that **ALLD is still a Nash Equilibrium in this situation, because the payoff in the bottom right hand element is still greater than the one in the top right hand element, *switching does not pay***. So more game theoretic models must be introduced to explain how cooperation may emerge.  
There is where the famous [Tit-for-Tat](https://en.wikipedia.org/wiki/Tit-for-Tat) strategy comes into play. In the late 1970s the political scientist Robert Axelrod ran a simulated game tournament where he asked specialists in the field for strategies. Interestingly, the simplest submission, Tit-for-Tat (TFT), beat all comers. Though Tit-for-Tat exhibited weaknesses against particular strategies, no other submission was as good, on average, against all the other strategies, and so it emerged as the final victor. TFT is simple:  
1) Cooperate in round 1  
2) Do what the opponent does in all subsequent rounds (e.g., if your opponent defects in round n, defect in round n + 1, and vice versa)  
TFT is a deterministic strategy which reacts to the opponent. It may seem like such a simple idea, but Matt Ridley wrote a whole book, [The Origins of Virtue: Human Instincts and the Evolution of Cooperation](https://www.amazon.com/Origins-Virtue-Instincts-Evolution-Cooperation/dp/0140264450/ref=pd_bbs_sr_1/002-9954258-8060061?ie=UTF8&s=books&qid=1174281193&sr=8-1), which revolved around Tit-for-Tat. It is a strategy which appeals to human concepts of “fair play,” and makes nature a bit less “red in tooth and claw.”  
Here’s the payoff matrix:

|      |                 |                   |
|------|-----------------|-------------------|
|     | TFT             | ALLD              |
| TFT  | ave(m)R         | S + (ave(m) – 1)P |
| ALLD | T + (ave(m)-1)P | ave(m)P           |

It should be familiar. The main difference here is that I’ve added the *average* number of rounds, as opposed to a fixed number. But all does not end with TFT, Nowak points out that **TFT is unforgiving, so adding an error parameter into the simulation tends to result in TFT being far less effective**. In other words, TFT tends to be a poor strategy in the context of behavorial noise. This is obviously an Achilles Heal because perfection is an aspiration, not a reality, in normal biosocial systems. Additionally, it also seems that when TFT facing an “Always Cooperate” (ALLC) strategy it has no advantage, since TFT is neither a Nash Equilibrium or an ESSin this scenario. A number of mutations toward ALLC in a finite population will result in TFT’s ceding ground to this strategy over time. Thinking about it on a biological level it is plausible to accept that TFT requires more energenetic (cognitive) outlay than a simpler ALLC strategy, which is positively “dumb.” But if dumb is effective, it is often cheaper than a more sophisticated strategy which requires more mental computations (e.g., cockroaches are evolutionary winners!). So how to resolve these problems with TFT?  
There are two other strategies that Nowak introduces as alternatives to TFT. “Generous Tit-for-Tat” (GTFT) is similar to TFT, but it is more “forgiving” of “mistakes” on the part of its oppenents. While TFT will **always** defect when faced with defection, GTFT will forgive a percentage of the time mistakes made by its opponents. In other words, GTFT will cooperate an x proportion of the time when its opponent defects (presumably by mistake).  
If TFT is defined by two parameters, p & q, which represent the proportion of the time that the player cooperates in reaction to the cooperation or defection of the opponent, the elements would be:  
(1, 0), it would cooperate 100% of the time in response cooperation, and 0% of the time to defection  
GTFT on the other hand might be:  
(1, 1/3), it would cooperate 100% of the time to cooperation, and 33% of the time in response to defection (note that q is free to vary).  
Nowak ran many simulations *in silico* with various values for q & p in pairwise combinations of strategies. An interesting result he found in a subset of simulations was this:  
1) ALLD starts out dominating, but  
2) Eventually a small frequency of TFT stabilizes, and rises in frequency, dominating the system  
3) At which point GTFT begins to marginalize TFT (because there is behavorial noise in the system, mistakes)  
4) At this point, GTFT stabilizes, though it is more vulnerable to invasion by ALLD than TFT  
The parameter which defines the resistence of GTFT from invasion by ALLD is conditioned by the various values in the payoff matrix (e.g., T, R, S, P) as well as the frequency of forgiveness (e.g., 1/3). Overly generous forgiveness, or marginal payoff for cooperation, is obviously less advantageous against ALLD then more proportionate forgiveness or a greater advantage for cooperation.  
Finally, the simulations were altered so that the player knew both its own previous move, and that of its opponent. While TFT and GTFT were purely reactive, a new strategy, Win-stay or Lose-shift (WSLS) emerged from the fray and often dominated the equilibrium system. This strategy is deterministic as opposed to stochastic, as GTFT is. That is, while GTFT forgives a percentage of the time randomly, WSLS reacts precisely and exactly to the nature of the outcome of the previous round. If the previous round results in a high payoff (R or T, simultaneous cooperation, or a payoff for defection against the cooperator) it continues with the strategy, but it is a low payoff (S or P, sucker’s payoff or a low simultaneous defection strategy) it switches. WSLS is a good strategy because it can correct mistakes. For example, here are rounds of two players:  
CCCCCCCCCC*D*DCCCCC  
CCCCCCCCCCCDCCCCC  
After the “mistake,” *D*, the opponent switches to defection, at which point there is a switch back to cooperation.  
The “big picture” is illustrated at chapter’s end by a chart (which I have adapted) that shows the relationships between the various strategies, as understood now:  
![warpeace.jpg](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2007/03/warpeace.jpg?resize=313%2C345)![warpeace.jpg](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2007/03/warpeace.jpg?resize=313%2C345)In sum, a random set of strategies initially gives way to ALLD, a classic war of all against all. Then, this is defeated by the TFT strategy, which favors cooperation by simple punishment of the defectors and preferential cooperation over iteration with like minded opponents. Eventually though TFT is undermined by its unforgiving nature, and GTFT, which takes into account human folly and error can dominate TFT. Over time the generosity of GTFT can drift to ALLC, which emerges as a hypercooperative mutant which exhibits infinite forgiveness, initially unpenalized in a system of rational cooperators. But eventually an ALLD mutant or invader can disrupt this utopia, taking advantage of ALLC’s weaknesses. On occasion WSLS also enters into the picture with its hard-headed, but forgiving, strategy of always playing to win, taking advantage of suckers (like ALLC) when possible, but being fair to those who will punish such exploitation. Nowak offers that the nature of WSLS’s defeat in the face of resurgent ALLD is not well elucidated, though no doubt this is one of his current research projects. In [A Beautiful Math](https://www.amazon.com/Beautiful-Math-Theory-Modern-Nature/dp/0309101921/ref=pd_bbs_sr_1/002-9954258-8060061?ie=UTF8&s=books&qid=1174284695&sr=8-1) Nowak offers that this story is the “tale of human war and peace.” I suspect he has great plans in store for this explanatory model. If Matt Ridley could write a book, and Robert Trivers’ reputation be established, by a simple TFT paradigm, imagine the play Martin Nowak will get with this model of cycles and oscillations!  
1 – A literal Prisoner’s Dilemma should really have negative numbers for the amount of time you’d spend in prison, so the “optimal” outcome would be a payoff of 0. We’ll dispense with that.  
2 – Nowak never elaborates while “GRIM” is termed GRIM. I suspec there is some backstory that he had to cut out of the chapter because of page constraints. In general I follow his formalism where I can, but sometimes I switch the notation around if I think it would be clearer. Also, I’m not going to cover more than 2 X 2 matrices because I doubt that the formalism returns enough in terms of clarity which verbal description could not handle for the conventional audience, since I assume linear algebra isn’t going to under most peoples’ belts.  
3 – You see why formalism isn’t always a snobby conceit after reading that sentence?

### Related Posts:

- [Of rats &
  men](https://www.gnxp.com/WordPress/2009/03/25/of-rats-men/) - [Mathematical biologist Martin Nowak
  interviewed](https://www.gnxp.com/WordPress/2007/06/25/mathematical-biologist-martin-nowak-interviewed/) - [Smart people play
  nice](https://www.gnxp.com/WordPress/2008/11/10/smart-people-play-nice/) - [Martin Nowak
  profile](https://www.gnxp.com/WordPress/2007/10/15/martin-nowak-profile/) - [Alberta has no
  rats!](https://www.gnxp.com/WordPress/2009/10/29/alberta-has-no-rats/) - [Martin Nowak, man of
  God](https://www.gnxp.com/WordPress/2007/07/31/martin-nowak-man-of-god/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F03%2F19%2Fthe-prison-of-war-peace%2F&linkname=The%20Prison%20of%20War%20%26%20Peace "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F03%2F19%2Fthe-prison-of-war-peace%2F&linkname=The%20Prison%20of%20War%20%26%20Peace "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F03%2F19%2Fthe-prison-of-war-peace%2F&linkname=The%20Prison%20of%20War%20%26%20Peace "Email")[](https://www.addtoany.com/share)
