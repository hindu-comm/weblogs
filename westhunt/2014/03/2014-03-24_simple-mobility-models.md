+++
title = "Simple Mobility Models"
full_title = "Simple Mobility Models"
date = "2014-03-24"
upstream_url = "https://westhunt.wordpress.com/2014/03/24/simple-mobility-models/"

+++
Source: [here](https://westhunt.wordpress.com/2014/03/24/simple-mobility-models/).

Simple Mobility Models

Greg’s previous post reviewing Gregory Clark’s new book has generated
some interesting discussion. Reviewers elsewhere and some of our
customers have been surprised at the persistence of social class by
surname and speculated that this implies genetic transmission of class.
Does it?

A way to pursue the issue is to construct the simplest possible
competing models and to compare their predictions. This is nearly the
universal procedure in all of science. First we can construct a pure
social science model in which class i simply culturally transmitted. A
typical paper in the literature (these days about income) divides a
sample into quintiles and describes (agonizes, often) about mobility
between income quintiles. We can shorthand these, calling families under
the twentieth percentile “lower”, the next quintile “lower middle”, then
“middle”, then “upper middle”, then “upper.” We might find, then, that
15% of the sons of lower class families are lower middle class the next
generation, and so on.

### Cultural Transmission

At this point some pop social scientists and journalists rely for
interpretation on a covert assumption (or sleight of mind) that this is
equivalent to a transition between states in a Markov process, that is
that particles (i.e. families) forget their pasts. Our 15% transition
rate from lower to lower-middle is an estimate of the probability of
jumping to lower middle given a middle class family in one generation.
Now we may see that the corresponding transition probability from from
lower-middle to middle is, say, 10%. If the social structure is static
we immediately deduce that the probability that a lower class surname is
middle class after two generations is simply the product, 0.15 \*
0.10or 1.5%. Under this kind of model one’s status becomes independent
of that of the more distant ancestor and randomly distributed across
classes, assuming that all classes are reachable, eventually, from all
other classes.

The justification for the Markov assumption is, in our toy model, that
class is purely culturally transmitted some someone from a lower-middle
class family’s progress is determined by cultural transmission of
lower-middle class culture plus some error term that leads to switching
class. We do not assume family transmission, just class transmission,
because family transmission would just mimic genetic transmission.
\[This needs worked out, since there is no explicit model of what
cultural transmission really is that we know about.\]

Genetic Transmission

A simple quantitative genetic model must rely on the assumption of an
underlying normal distribution of something, EQ we can call it, that is
the additive genetic part of whatever determines income. We can impute
this since, now, we have no way to measure it. Like IQ originally, and
like our construction of AQ (‘amish quotient’) a few weeks ago, we could
come up with an estimator of it if we could measure what we think we
ought to measure. For the moment we assume that there is such a
direction in character space. An immediate problem is that income is far
from normally distributed but we can impute a mapping from the observed
income distribution to EQ. Income percentiles are well known and
published for many countries. The figure below shows data given by
Björklund and Jäntti (1997).

![Sweden](https://westhunt.files.wordpress.com/2014/03/sweden1.png?w=400&h=600 "sweden.png")

The top panel of the figure shows the conventional Lorenz for the
Swedish data: the horizontal axis is income rank and the vertical axis
is the percentile of national income at that rank, i.e. it is a
conventional cumulative distribution of income. The bottom panel has the
same vertical axis but the distribution along the horizontal axis is the
imputed normal distribution of EQ. For example the 50th percentile of
income maps to the mean of the imputed distribution, the 84th percentile
maps to +1 standard deviation of a standard normal, the 16th percentile
maps to -1 standard deviation, and so on. This figure gives us estimate
of the income of a person given his value of an underlying normally
distributed EQ. The virtue of this is that we can instantly apply a
century’s worth of quantitative genetic theory and knowledge.

Given a quantitative genetic model we know, for example, that offspring
of a couple should be distributed symmetrically around the mid-parent
value, if heritability is complete, with standard deviation of
sqrt{2}/2. If not, we add regression to the mean. If mating is
assortative we add that to the model. We can go one and on adding bells,
whistles, and coontails to the model but we start simple.

From this we can compute, and perhaps derive explicit expressions, for
the long term movement, i.e. EQ, of one’s descendants. In other words we
can test this model against the kind of data that Gregory Clark has
gathered and falsify, or not, the genetic model.

We can see right away that the pure cultural model (our version) is
falsified since status persists. Our genetic model of diffusion along an
EQ axis shows that the Markov assumption is far from satisfied. If
someone is at EQ 0.91, corresponding to the 82nd percentile, toward the
lower end of the upper class, his offspring are much more likely to fall
to the upper-middle class than is someone at EQ 1.5, corresponding to
the 93rd income percentile. On the other hand, those fallen offspring
are much closer to the upper class threshold that are offspring who
entered the upper-middle class from the middle class. They are much more
likely to diffuse back up a generation later. Once we lump people into
quintiles that Markov property vanishes along with the
pop-social-science interpretations of mobility statistics.

Since this is the sort of model that is familiar to physicists, I think
we can agree that Greg owes it to us to work out more of the details.

### References

Intergenerational income mobility in Sweden compared to the United
States. A. Björklund and M. Jäntti. The American Economic Review
(1997):1009–1018.

The Son Also Rises: Surnames and the History of Social Mobility. G.
Clark. Princeton University Press (2014).

