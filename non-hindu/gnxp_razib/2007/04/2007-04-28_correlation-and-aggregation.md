+++
title = "Correlation and"
full_title = "Correlation and Aggregation"
date = "2007-04-28"
upstream_url = "https://www.gnxp.com/WordPress/2007/04/28/correlation-and-aggregation/"

+++
Source: [here](https://www.gnxp.com/WordPress/2007/04/28/correlation-and-aggregation/).

Correlation and Aggregation

There are many pitfalls in the interpretation of correlation coefficients. One relatively familiar one is the problem of restriction of range. To use a common illustrative example, if we take a sample of professional basketball players and calculate the correlation between their height and some measure of basketball performance, we will probably find that the correlation is weak. This does not mean that height is not an advantage in basketball: the reason for the weak correlation is that professional basketball players are a group with a restricted range of both height and basketball performance. The influence of height is therefore less conspicuous than if we took a random sample of the general population and tried them out at basketball.

The peril I want to highlight here is less familiar, and, unlike restriction of range, it tends to increase correlations. In general terms the problem arises from the aggregation of data. If data are aggregated and averaged, in some non-random way, the correlation between the resulting average values will often be higher than for the original disaggregated data, and may well increase with the level of aggregation. Suppose we take some trait in which there is a modest correlation at the individual level – say, between education and life expectancy. If now instead of individuals we take the averages for groups of individuals (for example the inhabitants of different towns, or even entire nations), and calculate the correlation between these averages, it is common for the correlation to be higher than for the individuals. It is also likely (though not certain) that as we take the averages of larger or more wide-ranging groups, the correlation will continue to increase. Correlation is essentially a way of measuring the proportion of the variability in a certain trait that can be accounted for by its association with some other trait. If we calculate the average values of the traits for wider and wider groups, the variability (technically, the variance) of the averages themselves will be reduced, because most of the random or localised influences on the data will cancel out as the groups are widened. But as the overall variance decreases, the proportion of the remaining variance explained by more general influences (which do not cancel out) is likely to increase. Technically speaking, the covariance may remain steady while the variance to be explained declines, or the covariance may decline, but the variance declines even faster.

This is all very abstract, so I will give a practical example from George Udny Yule’s Introduction to the Theory of Statistics…

Yule notes that in England, according to the official agricultural statistics, there is a modest positive correlation between the yield per acre of wheat and potatoes \[Note 1\]. Land that is good for growing wheat is also, on average, good for growing potatoes. If we calculate the correlation between wheat and potato yields at a fairly low level of geographical aggregation – the 48 counties of England – the correlation is .2189. If we then group the counties into 24 neighbouring pairs, the correlation increases to .2963. If we further aggregate them into 12 neighbouring groups, the correlation increases dramatically (it nearly doubles) to .5757; for 6 groups the correlation is .7649, and for 3 (which Yule describes as ‘the bitter end’) it rises to .9902. (Though Yule does not say so, if we actually reduced the number to 2, the correlation would be 1 or -1, as an algebraic identity. Of course in this case calculating the correlation would be pointless). \[Note 2\]

This does not necessarily mean that other factors correlated with wheat or potato yields are disappearing as the correlation between them increases. It is possible that if we measured, say, the correlation between wheat yield and annual rainfall, the correlation (positive or negative) would similarly increase as wider areas were aggregated. When all random or local factors have been eliminated by averaging, any remaining general factors may be correlated among themselves. For example there will probably be a strong negative correlation between annual rainfall and sunshine.

Unfortunately there seems to be no general rule to predict whether, or by how much, the aggregation of data will affect correlations (except that if groups of data pairs are selected at random from the entire set of data, the correlation between the group means should be approximately the same as between individuals – see Note 3). Yule gives another example of a study where a (negative) correlation increased steadily from -.502 to -.763 when 252 geographical areas were aggregated by stages into 25, but in the same study another correlation changed relatively little, and more erratically, during the same process of aggregation.

I will not attempt to draw any practical conclusions, except to say that it is a problem that deserves to be more widely known and taken into account, especially when we find very high correlations. As Yule advises: ‘What explanation we seek in individual cases depends on the individual circumstances. We can only leave the reader with the warning to watch very carefully the possibility of grouping effects, particularly in economic investigations’. Nor is the problem confined to geographical aggregation: it could apply also to grouping by social class, occupation, educational level, or any other criteria. It should not be inferred that that the correlations resulting from grouping are invalid or meaningless, just that the value of a correlation may be relative to the method of grouping. Group correlations derived at different levels of aggregation therefore cannot safely be compared. The problem is presumably well known to statisticians, and has been discussed from time to time since the 1950s, especially in economics and sociology, under the somewhat misleading heading of ‘[ecological correlation](http://216.239.59.104/search?q=cache:U6C_scXrYdcJ:stat-www.berkeley.edu/~census/549.pdf+%22ecological+correlation%22&hl=en&ct=clnk&cd=17&ie=UTF-8)‘, but it still does not seem to be sufficiently publicised. For example, in psychometrics it could be relevant to the correlation between test results, or between test results and other criteria, such as income. This is mentioned very briefly by J. P. Guilford, Fundamental Statistics in Psychology and Education, 1950, p.355, but on a cursory search I have not found any other reference to the subject in the psychometric literature.

Note 1: examples are taken from G. U. Yule and M. Kendall, Introduction to the Theory of Statistics, 14th edition, 1950, pp.310-315. Yule distinguishes two different but related forms of the problem. In one form, which he calls the ‘Modifiable Unit’, the items to be correlated are inherently variable in scope, for example because they involve a measurement over a geographical area. In the other form, which he calls the ‘Attenuation Effect’, the ultimate units of analysis are discrete items, but the problem arises when we choose to average them and then correlate the averages.

Note 2: I assume that correlation is measured by the Pearson product-moment correlation coefficient. The correlation then equals ∑(x – Mx)(y – My)/Nσx.σy, where N is the number of paired values, and Mx and My are the means of the x and y values respectively. If there are only two x values, a and b, and two corresponding y values, c and d, the correlation comes out as (a – b)(c – d)/√(a – b)²√(c – d)². Taking positive values for the two square roots (since they represent standard deviations) the correlation will be either 1 or – 1, depending on whether (a – b)(c – d) has a positive or negative value.

Note 3: This is stated without proof by Guilford, p.216. The explanation for the result is evidently that with purely random grouping, the numerator and denominator of the correlation coefficient are both reduced in the same ratio. Suppose we divide the N individual  
pairs of correlated data at random into N/n groups of n pairs each. If we designate the deviation values (relative to the population mean) of one variable as a, b, c…, and the corresponding values of the other variable as A, B, C…, then the group means will be of the form (a + b + c…)/n and (A + B + C…)/n. In calculating the correlation between group means, each such pair of means must be multiplied together to give a product of the form (a + b + c…)(A + B + C…)/n². Expanding this gives a sum (aA + bB + cC… + aB + aC… + bA + bC…)/n². But except for the terms aA, bB, cC, etc, which are the products of the individual correlated pairs, the terms in this sum will total approximately to zero, since the factors in each product term are uncorrelated (having been chosen randomly). Since there are N/n groups, the total covariance will be ∑(aA + bB +cC…)/Nn, where (aA + bB + cC…) includes the contribution of all groups. This is 1/n times the covariance of the N individual pairs of data. But by a similar analysis the product of the standard deviations of the group means is 1/n times the product of the standard deviations of the individual values. The numerator and denominator in the correlation coefficient are therefore reduced in the same ratio, and the correlation itself is unaffected. There will of course be some fluctuation due to sampling error.

### Related Posts:

- [Basketball in
  China](https://www.gnxp.com/WordPress/2009/07/23/basketball-in-china/) - [Human inequality is not fair: NBA
  edition](https://www.gnxp.com/WordPress/2016/05/25/human-inequality-is-not-fair-nba-edition/) - [More on "variables must
  vary"](https://www.gnxp.com/WordPress/2007/01/05/more-on-variables-must-vary/) - [Steelers
  win!](https://www.gnxp.com/WordPress/2009/02/01/steelers-win/) - [Beware the causal silver
  bullet](https://www.gnxp.com/WordPress/2014/07/15/beware-the-causal-silver-bullet/) - [50 years of
  stagnation?](https://www.gnxp.com/WordPress/2009/03/04/50-years-of-stagnation/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F04%2F28%2Fcorrelation-and-aggregation%2F&linkname=Correlation%20and%20Aggregation "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F04%2F28%2Fcorrelation-and-aggregation%2F&linkname=Correlation%20and%20Aggregation "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F04%2F28%2Fcorrelation-and-aggregation%2F&linkname=Correlation%20and%20Aggregation "Email")[](https://www.addtoany.com/share)