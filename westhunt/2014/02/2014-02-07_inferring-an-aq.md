+++
title = "Inferring an AQ"
full_title = "Inferring an AQ"
date = "2014-02-07"
upstream_url = "https://westhunt.wordpress.com/2014/02/07/inferring-an-aq/"

+++
Source: [here](https://westhunt.wordpress.com/2014/02/07/inferring-an-aq/).

Inferring an AQ

Back in December Greg and I
[posted](https://westhunt.wordpress.com/2013/12/21/assortative-mating-class-and-caste/)
a draft of a paper on assortative mating, class, and caste. We asked for
input and we got a lot, for which we are grateful. In that manuscript we
described a thought experiment in which the rate of boiling off of young
Amish each generation might act like truncation selection in favor being
Amish, whatever that might be. We suggested that one might construct an
“Amish Quotient” inductively by analogy with the way that IQ was
discovered and developed, purely from correlations among observable
traits. Pie in the sky but all is fair with thought experiments.

A week later an undergraduate student of mine, Michael Weight, walked
into my office with a 1970 paper from the *American Anthropologist*
(Wittmer 1970) reporting on a personality test given to 25 young Amish
men and 25 Rural Indiana men as controls. We were able to obtain
Wittmer’s 1968 doctoral dissertation from Indiana State University with
the raw data, scores on the PF16 personality test. I have never had much
faith in personality tests but, with nothing better, Weight thought it
was worth a look. The PF16 was developed in mid-century by Raymond
Cattell without modern machinery of multivariate analysis: this is
perhaps and advantage rather than a disadvantage. On the other hand the
test is proprietary so it would be very difficult for an unlicensed
practitioner to try to make sense of it. The output is in the form of
scores on 16 variables, and the supposed key to interpreting these
variable is widely available.

In the spirit of exploratory data analysis Weight computed a correlation
matrix from the 50 young men by the 16 PF16 scores and looked at the
first pair of principal components. The are what Steve Hsu calls “lossy
compression” of the original data, yielding an optimum (in the sense of
least squares) picture of the differences among the subjects and, in the
dual space, of the differences among the variables.

Here is the result: each letter is the placement of an individual
subject in the PCA space. The “a”s are young Amish men while the “n”s
are young non-Amish men. There is almost a complete separation between
the two groups: a Fisher discriminant analysis between the two group
misclassified two of 50 subjects with its hit-miss table.d There are
black circles around the two Amish men misclassified by the discriminant
function.

There is a paucity of comparable PF16 data on the internet, probably
because so much of it is proprietary, used in personnel selection.
Weight did find one paper giving PF16 scores for a sample of managers as
well as a random sample in the UK. The group average manager is shown on
the figure with the large ‘m’ while the average random Englishman is
shown with a large ‘e’. We entered the UK group means into the data
table 12 times each so all three groups, Amish, non-Amish, and UK
managers and random people were given roughly equal weight.
Interestingly the UK random sample group is right in the center of the
generic Indiana non-Amish. The UK managers, all of whom were finalists
for high management positions, are more distant from the Amish.

I am not sure that this is much evidence in support of our selection by
boiling off hypothesis about gene-culture coevolution among the Amish,
but we certainly have failed to falsify it. We wonder especially why
generic Indiana young men are so similar to citizens of the UK yet so
different from Amish young men who likely live right down the road.

![Eandm](https://westhunt.files.wordpress.com/2014/02/eandm.png?w=600&h=328 "eandm.png")  
A convenient property of PCA is that we can look at the differences
among the variables (called “factors”) on the same axes. This figure
plots the two-dimensional reduced space of the PF16 variables, labeled
from “a” to “q4.” Since the axes are the same we see right away that
Amish men are high on factor g and low on factor q1. From the standard
interpretations given for the PF16 tests Amish men, relative to their
neighbors, are “..exacting in character, dominated by sense of duty,
persevering, responsible, playful.” He is also “conscientious and
moralistic.” His low q1 score suggests he is also “confident in what he
has been taught to believe, and accepts the ‘tried and true'”. He is
“cautious and compromising in regard to new ideas”. He “tends to oppose
and postpone change, is inclined to go along with tradition, is more
conservative in religion and politics, and tends not to be interested in
analytical ‘intellectual’ thought.”

![Loadings](https://westhunt.files.wordpress.com/2014/02/loadings.png?w=600&h=464 "loadings.png")

### References

Bartram, D. The personality of UK managers: 16PF norms for short-listed
applicants. Journal of Occupational and Organizational Psychology,
65(2):159–172, 1992.

Wittmer, J. A Comparison of the Variability of Perceived Parental
Behavior Characteristics and Personality Traits of Twenty-five Non-Amish
and Twenty-five Amish Youth, Between the Ages of Eighteen and Twenty,
from the same Community. Dissertation, Indiana State University, 1968.

Wittmer, J. Homogeneity of Personality Characteristics: A Comparison
between Old Order Amish and Non-Amish1. American Anthropologist,
72(5):1063–1068, 1970.

