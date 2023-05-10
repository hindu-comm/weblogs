+++
title = "Price's Second Equation"
full_title = "Price's Second Equation"
date = "2010-09-21"
upstream_url = "https://www.gnxp.com/WordPress/2010/09/21/prices-second-equation/"

+++
Source: [here](https://www.gnxp.com/WordPress/2010/09/21/prices-second-equation/).

Price's Second Equation

In a previous [post](https://www.gnxp.com/wp/uncategorized/prices-first-equation) I discussed what I called Price’s First Equation, as contained in George Price’s 1970 paper ‘Selection and covariance’. The present post deals with the 1972 paper ‘Extension of covariance selection mathematics’ (so far as I know, not currently available free online.) The main result of the 1972 paper is often known simply as Price’s Equation, but to avoid ambiguity I will call it Price’s Second Equation. As in the previous post, my aim will be to help people follow Price’s own derivation, which uses the relatively unfamiliar concept of a weighted covariance. Comment and criticism will be reserved for another post. This one won’t be easy reading, but people who aren’t interested in the technical details may still find a few points worth noting.

  
Price’s First Equation, in the notation explained previously, stated that:

dQ = Cov(z,q)/Z + Sz\[i\]dq\[i\]/NZ

This equation breaks down the change in frequency (if any) of a gene from one generation to the next into two components: (a) the effect of the gene on the reproductive success of members of the parent generation; and (b) the change in frequency of the gene between individual parents and their own offspring.

In the 1970 paper Price said that he was working on an extension of this approach to the problem of group selection. The First Equation itself can be applied to groups rather than individuals, with only slight changes of definition and interpretation, provided the groups are all of the same size.

The main technical contribution of the 1972 paper is to show how the Equation can be generalised to groups of differing size.

**Notation**

As previously, I will avoid Greek letters and other special typography, which may not be compatible with some browsers. Where Price uses Greek capital sigma to indicate summation, I will use capital S. In the 1972 paper capital sigma always has a subscript i, which can be taken as implied here. Where Price uses Greek capital delta to indicate an increase or decrease in a quantity, I will use the letter d. Where Price uses a bar over a letter to indicate the mean (average) value of a variable, I will use the capital form of the letter; so, for example, the capital letter W will indicate the mean value of the variable w. Where Price uses subscripts, I will use square brackets, so for example where Price has w with a subscript i, I will use w\[i\]. It would be possible to shorten the formulae by omitting most ‘subscripts’, and making some other notational changes, but I have decided to stick as closely as possible to Price’s formulae to facilitate comparison. I have however replaced ‘primes’ by asterisks, as I found that when I first posted this the primes came out inconsistently (and difficult to read).
The expression cov(x,y) stands for the covariance between x and y. (See the previous post for the meaning of ‘covariance’.) The numbers \[A1\], \[A2\], etc, are Price’s own numbered equations or definitions. Other numbers in brackets are my own.

**Weighted averages and covariances**

The 1972 paper uses the concepts of weighted average and weighted covariance. The concept of a weighted average (mean) is relatively familiar, and was treated in standard works on statistics available to Price (e.g. Yule and Kendall, 332). Consistently with the usual treatment, Price defines the weighted average of a variable x as:

\[A1\] ave\[w\]x = (Sw\[i\]x\[i\])/Sw\[i\]

where and w\[i\] stands for a ‘weight’ or ‘weighting variable’. Price mentions two well-known properties of weighted averages: if all w\[i\] are equal, then the weighted average has the same value as the ordinary (unweighted) average; and if all w\[i\] are multiplied by the same constant, the value of the weighted average is unchanged. Another fairly obvious property is that provided all weights are positive (as is usually assumed), then the weighted average will fall somewhere within the range of the x values.

Weighted averages have various uses. For example they may be used to give different weight to data that differ in reliability or importance. Perhaps the most common use of weighted averages is to calculate an overall average when averages are known for subgroups of a population but not for the total population itself. If the sizes of the subgroups are used as the weighting factors, the resulting weighted average will be the same as the unweighted average for the total population. For example, if we know the average score of pupils on a test in the various schools of a city, but not the average in the city as a whole, the averages for each school may be weighted by the number of pupils taking the test to obtain the average for the city.

Price states an important result about weighted averages, which he would have known from the textbooks (e.g. Yule and Kendall, 334):

\[A7\] ave\[w\]x = X + cov(w,x)/W.

It can be seen that the weighted average will be greater than the ordinary average if the covariance between the weights and the values of x is positive, and less than the ordinary average if it is negative.

The concept of a weighted *covariance* is much less familiar than that of a weighted average, and on consulting several pre-1972 statistics textbooks I have not found it discussed. Price however treats it as an established concept (see also his more technical paper of 1971), and defines it as:

\[A2\] cov\[w\](x,y) = \[Sw\[i\](x\[i\] – ave\[w\]x)(y\[i\] – ave\[w\]y)\]/Sw\[i\].

This can be compared with the standard formula for an ordinary covariance, cov(x,y) = \[S(x\[i\] – X)(y\[i\] – Y)\]/N. It can be seen that in the weighted covariance the product terms are all weighted by their corresponding w\[i\]’s, the ordinary averages of x and y are replaced by their weighted averages, and Sw\[i\] replaces the population number N.

Price states the following equivalence, which is important in his subsequent derivation:

\[A6\] (Sw\[i\]x\[i\]y\[i\])/Sw\[i\] = cov\[w\](x,y) + (ave\[w\]x)(ave\[w\]y).

It can be seen that this corresponds to (Sx\[i\]y\[i\])/N = cov(x,y) + XY for ordinary covariances. Proving it from the definitions is just a tedious algebraic grind, which I will omit.

As in the case of weighted averages, the formula for weighted covariance can be applied to cases where the covariance is known for each of the subgroups of a population but not for the total population. But just weighting the covariance within groups by the size of the groups would not necessarily give an accurate covariance for the population as a whole. Covariance in the whole population is relative to the population averages, and these may be different from the group averages. It is quite possible for the population covariance to be greater or less than any of the group covariances, or even to be different in sign \[see Note 1\]. Suppose, for example, that the ‘groups’ are human males and females. It is likely that within each group the covariance between height and hair length is small but positive, because other things being equal taller individuals in each group are likely to have slightly longer hair, whereas in the total human population the covariance may be negative, because men tend to be taller but to have shorter hair than women. Part of the total population covariance thus only becomes apparent when calculated by reference to the average values for the population as a whole. The weighted covariance formula \[A2\] allows for this by using weighted averages for the whole population as the ‘baseline’ from which deviations are measured. It can be shown that when this is done, and group sizes are used for weighting, then the weighted covariance in accordance with \[A2\] is equal to the ordinary (unweighted) covariance for the population.

Price also defines weighted versions of variance, standard deviation, regression, and correlation, but I will not make use of these.

**Further definitions**

The main derivation in the paper begins with some further definitions. Price gives hints as to what his new terms are intended to designate, but it is probably best in the first instance to regard them as purely formal symbols.

The term p is used to represent the numerical value of some property of population members.

By definition:

\[A8\] dp\[i\] = p\*\[i\] – p\[i\],

d(ave\[w\]p) = ave\[w\*\]p\* – ave\[w\]p.

Price then says that the term s will be called a ‘selection coefficient’, and by definition s\[i\] = w\*\[i\]/w\[i\]. (In my notation there would be an ambiguity between S as a summation sign and S as the unweighted average of s, but the latter does not occur in the derivation.)

It might be thought that the definitions at \[A8\] are formally defective, as the terms d and \* (‘prime’ in Price’s text) have not been previously defined in the paper, and one undefined term is therefore defined by reference to another. However, in the subsequent working the derivations are always carried out strictly in accordance with the definitions, and the result is an equation that is formally valid even though it contains terms that have not yet been fully interpreted. It thus provides a schema that allows valid inferences to be made whatever interpretations are given to the undefined terms.

**Derivation**

As in the 1970 paper, after all the preliminary definitions and assumptions have been set out, the actual derivation of the main result is quite brief. I will set out the various steps more fully than the paper, as Price tends to combine three or four operations in each step, which saves space but leaves the reader to do much of the work.

It will first be convenient to note some equivalences which follow easily from the definitions:

\(1\) p\*\[i\] = p\[i\] + dp\[i\] (from \[A8\])

\(2\) w\[i\]s\[i\] = w\*\[i\] (from the definition ofs\[i\])

\(3\) Sw\[i\]s\[i\] = Sw\[i\](ave\[w\]s) (from \[A1\])

\(4\) ave\[w\*\]p\* = ave\[w\]p + d(ave\[w\]p) (from \[A8\]).

Now, substituting w\* and p\* for w and x in \[A1\], we have:

\(5\) ave\[w\*\]p\* = (Sw\*\[i\]p\*\[i\])/Sw\*\[i\].

Using the equivalence (1) we can substitute p\[i\] + dp\[i\] for p\*\[i\], giving:

\(6\) ave\[w\*\]p\* = \[Sw\*\[i\](p\[i\] + dp\[i\])\]/Sw\*\[i\].

Following the usual rules for summation we can split the expression on the right into two parts, giving:

\(7\) ave\[w\*\]p\* = (Sw\*\[i\]p\[i\])/Sw\*\[i\] + (Sw\*\[i\]dp\[i\])/Sw\*\[i\].

Then substituting w\[i\]s\[i\] for w\*\[i\] in the first term on the right, as permitted by (2), we have:

\[A10\] ave\[w\*\]p\* = (Sw\[i\]s\[i\]p\[i\])/(Sw\[i\]s\[i\]) + (Sw\*\[i\]dp\[i\])/Sw\*\[i\].

Using the equivalence (3) we can substitute Sw\[i\](ave\[w\]s) for (Sw\[i\]s\[i\]) in the denominator of the first term on the right, giving:

\(8\) ave\[w\*\]p\* = (Sw\[i\]s\[i\]p\[i\])/Sw\[i\](ave\[w\]s) + (Sw\*\[i\]dp\[i\])/Sw\*\[i\].

But by \[A6\], substituting s and p for x and y, we have:

\(9\) (Sw\[i\]s\[i\]p\[i\])/Sw\[i\] = cov\[w\](s,p) + (ave\[w\]s)(ave\[w\]p).

We can therefore substitute cov\[w\](s,p) + (ave\[w\]s)(ave\[w\]p) into (8), getting for the first term on the right:

\(10\) \[cov\[w\](s,p) + (ave\[w\]s)(ave\[w\]p)\]/(ave\[w\]s),

which can be simplified to:

\(11\) cov\[w\](s,p)/ave\[w\]s + ave\[w\]p.

Equation \[A10\] as a whole is therefore equivalent to:

\(12\) ave\[w\*\]p\* = cov\[w\](s,p)/ave\[w\]s + ave\[w\]p + (Sw\*\[i\]dp\[i\])/Sw\*\[i\].

By \[A1\] the final term on the right is equivalent to ave\[w\*\]dp, so we also have:

\(13\) ave\[w\*\]p\* = cov\[w\](s,p)/ave\[w\]s + ave\[w\]p + ave\[w\*\]dp.

But by (4) we have ave\[w\*\]p\* = ave\[w\]p + d(ave\[w\]p), so we can subtract ave\[w\]p from both sides of (13) to get:

\[A11\] d(ave\[w\]p) = cov\[w\](s,p)/ave\[w\]s + ave\[w\*\]dp.

This is the basic form of Price’s Second Equation. Price also proposes a simplification by defining a ‘relative selection coefficient’, s\[i\]/ave\[w\]s. He designates this by s with a tilde above it, which I will represent by \[s\~\]. With this convention \[A11\] can be presented as:

\[A12\] d(ave\[w\]p) = cov\[w\](\[s\~\],p) + ave\[w\*\]dp.

The Second Equation is as yet just a formal identity, with no specific interpretation. As Price emphasises, it is an identity for all values of w\[i\], p\[i\], w\*\[i\], and p\*\[i\]. The equation will therefore be valid whatever values or symbols are substituted for these terms.

**Application to group selection**

The main application which Price himself makes of the equation is to the issue of group selection. He supposes that a large population is subdivided into a number of subpopulations or groups. For simplicity he assumes that generations are non-overlapping and that there is no interbreeding or migration between groups. (He also tacitly assumes sexual reproduction, though it would be easy to adapt the model to cover asexual or self-fertilising reproduction.) He then makes certain definitions:

n\[i\] is the population of group G\[i\] in the parent generation.

n\*\[i\] is the population of group G\[i\] in the offspring generation.

s\[i\] = n\*\[i\]/n\[i\]. Price notes that this is the mean number of offspring per parent generation member of group G\[i\], when each parent is given credit for half of each offspring conceived (assuming sexual reproduction). Without this proviso the mean number of offspring per member would be overstated, since each offspring would be counted twice, once for each parent.

p\[i\] is the frequency of gene A in group G\[i\] in the parent generation.

p\*\[i\] is the frequency of gene A in group G\[i\] in the offspring generation. Price does not specify whether p\[i\] and p\*\[i\] are frequencies of gene A at a particular locus or among all genes in the genome, but this does not matter provided the same approach is taken for each generation.

P is the frequency of gene A in the total population of the parent generation.

P\* is the frequency of gene A in the total population of the offspring generation.

dP = P\* – P (by definition).

Price notes that ‘it can easily be seen’ that P = ave\[n\]p\[i\], and P\* = ave\[n\*\]p\*\[i\]. This does indeed follow from the definition of weighted average. It further follows from the definition of d(ave\[w\]p) in \[A8\] (substituting n for w) that:

dP = d(ave\[n\]p).

The final step is to note that n and n\* can be substituted for w and w\* respectively in all the previous formal derivations, up to \[A12\], which is possible because s\[i\] (in its ‘group’ interpretation) is defined as n\*/n, corresponding to w\*/w in the previous working. Equation \[A11\] can therefore be validly restated in the form:

dP = d(ave\[n\]p) = cov\[n\](s,p)/ave\[n\]s + ave\[n\*\]dp

and equation \[A12\] in the form:

\[A15\] dP = d(ave\[n\]p) = cov\[n\](\[s\~\],p) + ave\[n\*\]dp.

That completes the main part of the derivation. It is of course a very roundabout way of reaching a result on group selection, and later authors have generally gone straight to an interpretation in terms of groups and gene frequencies. Price’s approach does however have the advantage that his equations \[A1 – A12\] are extremely general, and can in principle be applied to many other problems.

Price goes on to discuss the interpretation of group selection in the light of the Second Equation. I will reserve comments on this for another post. However, while the technical details are still fresh on the page, it may be useful to look at some issues of terminology.

Price himself refers to the term cov\[n\](s,p)/ave\[n\]s) as a covariance or weighted covariance, and later authors have usually called it the Covariance term. It is however an odd kind of covariance, and there might be doubts whether it has all the statistical properties of an ordinary (unweighted) covariance, notably for the purposes of correlation and regression. It involves a combination of group and individual properties: summation is ostensibly over the groups, as the \[i\]’s are index numbers for groups, but the averages from which deviations are measured are the averages for the total population, and the product sum is divided by Sn\[i\], which is the total population number, not the number of groups.

I think any doubtscan be alleviated by keeping in mind that the weighted covariance, when the weights are the numbers in the groups, is equal to the ordinary covariance for the total population, and has all the usual properties of a covariance in that context. One may still balk at claims of conceptual ‘transparency’. I suggest that purely for the purpose of thinking about group selection it might be better to assume that group sizes are initially equal, so that the covariance term does not need to be weighted at all. The covariance term can then be interpreted simply as a covariance between properties of groups.

The second term, ave\[n\*\]dp, also raises a problem. It has become customary to call it the Expectation term, though this terminology was not used by Price himself and seems to have been introduced by Hamilton in 1975 \[Hamilton, 332\]. The problem is that ‘Expectation’ or ‘Expected value’ has a traditional meaning in probability theory (see e.g. von Mises, 148; Hacking, 80). In this usual sense, Expectation involves values (utilities) multiplied by probabilities, whereas Price’s term has nothing to do with either utilities or probabilities: it is simply a weighted average of the changes in frequency within groups. It might be better to call it the Transmission term, since it measures the fidelity of transmission of a property between generations. There are some other problems in interpreting it, but I will discuss these in a further post.

Note 1

I have not seen this stated, but it can be shown that if a population is divided into groups, then the covariance between traits in the whole population equals the weighted mean of the covariance *within* groups, plus the weighted covariance *between* the group means, using group sizes as the weights. (This corresponds to the better known additive property of within-group and between-group variances.) If the covariance between group means is negative, this may be enough to offset or reverse a positive covariance within groups, or vice versa.

**References**

Works by George Price

G. R. Price, ‘Selection and covariance’, *Nature*, 227, 1970, 520-21.

G. R. Price, ‘Extension of the Hardy-Weinberg law to assortative mating’, *Annals of Human Genetics*, 36, 1971, 455-58.

G. R. Price, ‘Extension of covariance selection mathematics’, *Annals of Human Genetics*, 35, 1972, 485-90.

Other works

Steven A. Frank, ‘George Price’s contributions to evolutionary genetics’, *Journal of Theoretical Biology*, 175, 1995, 373-88.

Ian Hacking: *An Introduction to Probability and Inductive Logic*, 2001.

W. D. Hamilton: *Narrow Roads of Gene Land*, vol. 1, 1996.

Richard von Mises: *Probability, Statistics and Truth*, Dover edn., 1981.

G. Udny Yule and M. Kendall: *An Introduction to the Theory of Statistics*, 14th edn., 1950.

### Related Posts:

- [The Price
  Equation](https://www.gnxp.com/WordPress/2009/11/10/the-price-equation/) - [Demystifying Price's
  Equation](https://www.gnxp.com/WordPress/2010/10/03/demystifying-prices-equation/) - [Levels of selection & the full Price
  Equation](https://www.gnxp.com/WordPress/2009/11/11/levels-of-selection-the-full-price-equation/) - [The mists of the adaptive
  fog](https://www.gnxp.com/WordPress/2008/11/18/the-mists-of-the-adaptive-fog/) - [Price's First
  Equation](https://www.gnxp.com/WordPress/2010/09/05/prices-first-equation/) - [George Price, Group Selection, and
  Altruism](https://www.gnxp.com/WordPress/2011/04/10/george-price-group-selection-and-altruism/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F09%2F21%2Fprices-second-equation%2F&linkname=Price%27s%20Second%20Equation "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F09%2F21%2Fprices-second-equation%2F&linkname=Price%27s%20Second%20Equation "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F09%2F21%2Fprices-second-equation%2F&linkname=Price%27s%20Second%20Equation "Email")[](https://www.addtoany.com/share)
