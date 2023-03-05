+++
title = "Demystifying Price's"
full_title = "Demystifying Price's Equation"
date = "2010-10-03"
upstream_url = "https://www.gnxp.com/WordPress/2010/10/03/demystifying-prices-equation/"

+++
Source: [here](https://www.gnxp.com/WordPress/2010/10/03/demystifying-prices-equation/).

Demystifying Price's Equation

In previous posts [here](https://www.gnxp.com/wp/uncategorized/prices-first-equation) and [here](https://www.gnxp.com/wp/genetics/prices-second-equation) I have discussed how George Price arrived at his eponymous Equation. I said that there would be one more post of comment and criticism, but it will take at least two posts to cover the points I want to make.

The present post is aimed at getting a better understanding of the ‘covariance’ element in Price’s Equation. A common reaction to this is that it is somehow mysterious and intuitively hard to grasp. There are some interesting comments in this video [talk](http://www.webofstories.com/play/7297) by the late John Maynard Smith, who claimed that he could never understand the ‘variance and covariance’ approach to population genetics. The problem was not that he could not follow the mathematics, but that he just could not *think* in those terms.

I believe that the supposed mysteriousness of Price’s Equation is largely due to the way it is usually presented and explained. I hope the following way of interpreting is intuitively more transparent and satisfying.  

First it is necessary to recall that Price’s Equation comes in several versions. Here I will deal mainly with the ‘short’ version of what I have called the First Equation, from Price’s 1970 paper, in the form:

dQ = cov(z,q)/Z.

This contains only the ‘covariance’ term of the full equation. It is valid when there is no change in gene frequency between individual parents and their own offspring, and useful as an approximation if such changes are confined to small random fluctuations in a large population. In what follows I will assume that the short version holds exactly, but the interpretation given will be applicable, with minor modifications, to the covariance term in the other versions of the Equation.

There is nothing inherently odd about a covariance being involved in measuring the effects of selection. Whenever we want to measure the strength of a relationship statistically, then a covariance is likely to be involved, either in its own right or as a component in a correlation or regression formula. In Price’s case we are interested in the relationship between the fitness of organisms and their possession of certain genes. It is not surprising that it should be possible to describe this by means of a covariance. What is more surprising is that the change in frequency of a gene can be described simply and concisely in this way.

I do not suggest that this element of surprise can be removed entirely, but I think the meaning of the covariance can be made to emerge more naturally if we reverse the process of derivation (as presented by Price) and start by considering the end-product: the change in gene frequency.

The aim is to find a way of expressing the change of frequency of a gene between two generations. I make the usual simplifying assumption of separate generations. It is also convenient to avoid complications about ploidy (whether the organism is haploid, diploid, etc.) by interpreting the population number in a given generation as the total number of genes at the relevant locus rather than the number of organisms. A ‘parent’ can therefore be interpreted as a gene in Generation 1 (G1), and an ‘offspring’ as a replica of that gene in Generation 2 (G2).

With these assumptions, let us designate the total number of genes at a locus in G1 as N, and in G2 as N\*. We designate the total number of genes of a particular type at the locus in G1 as A, and in G2 as A\*. The frequency of that gene-type (which I will call the A-type) in the population in G1 is Q = A/N, and in G2 is Q\* = A\*/N\*. The change, if any, of the frequency of the A-type gene between the two generations is therefore:

(1) dQ = Q\* – Q = A\*/N\* – A/N.

The expression A\*/N\* – A/N can be manipulated in various ways, most obviously to get a fraction with a common denominator in the form:

(2) dQ = (A\*N – AN\*)/NN\*.

However, it is more useful for comparison with Price’s Equation to find an expression with the common denominator N\*, the population number of G2 \[note 1\]. To do this we can first express N\* as a multiple of N, in the form:

(3) N\* = kN.

The coefficient k can be regarded as a measure of population growth (or decline), so, for example, if the population grows by 20% then N\* will be (1.2)N. Obviously k = N\*/N.

With this usage, Q = A/N = kA/kN = kA/N\*. Since Q\* = A\*/N\* it follows easily that:

(4) dQ = Q\* – Q = A\*/N\* – kA/N\* = (A\* – kA)/N\*.

The final expression on the right is the desired formula with N\* as the common denominator. The most interesting term in (4) is kA. From the definitions this is equal to QN\*, which is the population of G2 multiplied by the proportion of A-type genes in G1. It can be interpreted as the number of A-type genes that would be *expected* in G2 if A-type genes reproduce at the same rate as the whole population, in other words, if there is no selection for or against them. The difference between the *actual* and the *expected* number of A-type genes in G2 is equal to (A\* – kA), which can be interpreted as the surplus or deficit of A-type genes in G2 attributable to selection. When divided by N\*, this gives the difference between the actual and expected *frequencies* of A-type genes in G2. Since the ‘expected’ frequency, in the absence of selection, is simply Q (the frequency in the previous generation), this also represents the *change* in frequency between generations, Q\* – Q.

We now want to find an interpretation of Price’s Equation which mirrors the quantities expressed in (4). Suppose we consider the covariance between fitness (number of ‘offspring’) of individual genes in G1 and the frequency of the A-type in those genes (which can only be 1 or 0, since an individual gene either is or is not A-type). Using one of the standard formulae for a covariance, this can be expressed as:

(5) cov(z,q) = (Sz\[i\]q\[i\])/N – ZQ

where S is a summation sign, summation is over all members of G1, z\[i\] is the number of ‘offspring’ of the i’th gene in G1, q\[i\] is the frequency of A-type in the i’th gene in G1 (either 1 or 0), N is the ‘population’ size in G1, and Z and Q are the mean values of z and q (the totals Sz\[i\] and Sq\[i\] divided by N).

To derive Price’s Equation in its usual form we need to eliminate N from the RHS of (5). If we multiply both sides of (5) by N, and note that NZ = Sz\[i\], we can get:

(6) cov(z,q)N = Sz\[i\]q\[i\] – Sz\[i\]Q.

We are assuming that the frequency of A-type genes does not change between individual parents and offspring, so the term Sz\[i\]q\[i\] can be interpreted as the *actual* total number of A-type genes in G2. The term Sz\[i\]Q can be interpreted as the total number of A-type genes that would be *expected* in G2 if the population frequency of A-type genes does not change from G1, where the frequency is Q. The expression on the RHS can therefore be interpreted as the total *actual* number of A-type genes in G2 minus the total *expected* number of A-type genes in the absence of selection. But recalling (4) and its interpretation, this is equal to (A\* – kA) as defined earlier. Since by (4) dQ = (A\* – kA)/N\*, we can therefore divide (6) by N\* to get:

(7) dQ = cov(z,q)N/N\* = (Sz\[i\]q\[i\])/N\* – Sz\[i\]Q/N\*.

A little consideration shows that N\* = NZ = Sz\[i\], the total of all ‘offspring’ of G1, so with appropriate substitutions we can finally get:

(8) dQ = cov(z,q)/Z = (Sz\[i\]q\[i\])/Sz\[i\] – Q.

The equation dQ = cov(z,q)/Z is Price’s First Equation in its short form. This now has a natural interpretation in terms of equation (4) above. Cov(z,q)/Z, and the equivalent expression (Sz\[i\]q\[i\])/Sz\[i\] – Q, can be interpreted as the surplus or deficit of A-type genes in G2 attributable to selection, as a proportion of the total number of genes at the relevant locus in G2. The components of (Sz\[i\]q\[i\])/Sz\[i\] – Q correspond neatly to the components of Q\* – Q, since (Sz\[i\]q\[i\])/Sz\[i\] can be seen to be equal to Q\*, the total number of A-type genes in G2 as a proportion of all genes at the relevant locus, on the assumption that q\[i\] does not change between generations.

It may be thought that the concept of *covariance* has played very little part in this interpretation. It would be possible in principle to reach the equation:

(9) dQ = (Sz\[i\]q\[i\])/Sz\[i\] – Q

from the definitions and assumptions without referring to the concept of covariance at all, and it might be wondered whether the equivalence of (9) to cov(z,q)/Z is more than a curious mathematical coincidence. To see that it is more than this, we may note that a covariance itself involves a difference between actual and expected values.

If we consider in general the covariance between variables x and y, it may be represented in a variant of one of the standard formulae as:

(10) cov(x,y) = (Sx\[i\]y\[i\] – NXY)/N.

In this expression Sx\[i\]y\[i\] is the sum of the *actual* values of the products xy, for some definite pairing of the variables x and y, whereas NXY (where X and Y are the mean values of x and y) is the sum of the *expected* values of N products xy if x and y values are paired randomly \[note 2\]. The difference between these two quantities therefore represents the departure (if any) of the actual product sum from its expected value under random pairing. This may be compared with Sz\[i\]q\[i\] – Sz\[i\]Q in expression (6) above, where the first term gives the actual number of A-type genes in G2 (assuming no change in frequency between individual parents and their offspring) while the second term gives the expected number assuming no selection. ‘No selection’ is in this context another way of saying that values of z and q are paired randomly. ‘Selection’ is precisely a departure from randomness. The connection between selection and covariance is therefore not merely a formal coincidence.

The only thing that prevents the change in gene frequency being *identical* with a straightforward covariance is the possibility of a change in the size of the population between G1 and G2. The problem is then that the summation of product terms in the covariance is over members of G1 \[see note 3\], so the definition of covariance requires division by N, whereas the difference in gene frequencies requires division by N\*. As N\* = NZ, this may be achieved by dividing the covariance itself by Z. If there were no change in the size of the population, then Sz\[i\] would be N, Z would be 1, and (8) would be a straightforward covariance between z and q with N as the denominator. In a static population the covariance would therefore directly measure the effect of selection on the frequency of a gene.

In the more general case of a growing or declining population the covariance by itself would not give the right measure. If the population has grown, then the covariance would overstate the change in gene frequency, and division by Z (which in this case is greater than 1) will scale it down; and conversely if the population has shrunk. Another way of interpreting the formula is to take Z as a divisor, not of the covariance itself, but of all the z values. The various terms z\[i\]/Z can then be regarded as ‘standardised’ values of z, and the formula can be regarded strictly as a covariance between q and the standardised z. This is an interpretation suggested by Price himself in his 1972 paper, where he introduces a ‘relative selection coefficient’ which in the notation of the 1970 paper would be z\[i\]/Z. The resulting value of dQ is of course the same however we interpret it.

I hope (but doubt) that this has done something to dispel the air of mystery about Price’s Equation. There remains the question whether it is actually as useful or important as its enthusiasts claim. I will consider this in another post.

**Note 1**

It would also be possible to derive a formula with N as the denominator, but this would not lead easily to Price’s Equation in its usual form.

**Note 2**

It is perhaps obvious that if pairs of x and y values are taken at random and multiplied together the *average* value of the products, in a long run of trials, will be XY. For a more formal argument, consider the set of all possible products of x and y pairs. There are NN such products, with a total value of SxSy, since in the total every x is multiplied by every y. The mean value of all possible pairs is therefore SxSy/NN = XY. A random sample of N such pairs will therefore have an expected value of N times the mean value, or NXY.

**Note 3**

It might be wondered if there is any way of developing Price’s Equation as a covariance between properties of offspring (G2), rather than members of the parental generation (G1). I think there would be several difficulties with this, the clincher being that not all members of G1 have offspring, so that a covariance between properties of members of G2 would leave out an important part of the selective process.

### Related Posts:

- [The Price
  Equation](https://www.gnxp.com/WordPress/2009/11/10/the-price-equation/) - [The Price of
  Altruism](https://www.gnxp.com/WordPress/2010/07/21/the-price-of-altruism/) - [Levels of selection & the full Price
  Equation](https://www.gnxp.com/WordPress/2009/11/11/levels-of-selection-the-full-price-equation/) - [The mists of the adaptive
  fog](https://www.gnxp.com/WordPress/2008/11/18/the-mists-of-the-adaptive-fog/) - [Evaluating Price's
  Equation](https://www.gnxp.com/WordPress/2010/11/04/evaluating-prices-equation/) - [Price's Second
  Equation](https://www.gnxp.com/WordPress/2010/09/21/prices-second-equation/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F10%2F03%2Fdemystifying-prices-equation%2F&linkname=Demystifying%20Price%27s%20Equation "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F10%2F03%2Fdemystifying-prices-equation%2F&linkname=Demystifying%20Price%27s%20Equation "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F10%2F03%2Fdemystifying-prices-equation%2F&linkname=Demystifying%20Price%27s%20Equation "Email")[](https://www.addtoany.com/share)
