+++
title = "Price's First Equation"
full_title = "Price's First Equation"
date = "2010-09-05"
upstream_url = "https://www.gnxp.com/WordPress/2010/09/05/prices-first-equation/"

+++
Source: [here](https://www.gnxp.com/WordPress/2010/09/05/prices-first-equation/).

Price's First Equation

In a recent [post](https://www.gnxp.com/wp/uncategorized/the-fame-of-price) I said I would write again about the work of George Price. My main aim will be to help people read Price’s own papers. There are various ‘Price guides’ in existence, some of which are very good in their way, but I have not seen any that follow Price’s own treatment at all closely. My own old post on [‘Price’s Equation’](https://www.gnxp.com/MT2/archives/002372.html) was based mainly on an account by W. D. Hamilton, which differs in several ways from Price’s approach. \[Added: a reader has drawn my attention to a recent paper by M. van Veelen. I have now seen this, and it does follow Price’s treatment quite closely. See comments for the reference.
The published versionof the paper gives more detail than the preprint which I mention in the comments.\]

Price published only six biological papers in his lifetime, two of them co-authored (for details see References). Two of the six items (nos. 2 and 5) are on relatively technical issues. The paper co-authored with John Maynard Smith on evolutionary game theory is more general, but self-explanatory. The remaining paper, on Fisher’s Fundamental Theorem, is also important, but I would need to consider it in conjunction with Fisher’s own writings on the subject. Maybe some other time.

That leaves the 1970 paper ‘Selection and covariance’ and the 1972 paper ‘Extension of covariance selection mathematics’. Here I will deal with the 1970 paper, which is currently available online [here](http://www.cs.ucl.ac.uk/staff/wlangdon/ftp/papers/price_nature.pdf). The next post will cover the 1972 paper. A third post will contain some assessment and criticism. One of the main claims made for Price’s work is that it provides a clear way of analysing the effects of ‘group’ and ‘individual’ selection. I think these claims need to be qualified, not only for the reasons indicated in my old post on ‘Price’s Equation’, but for a further reason which only struck me recently when working through Price’s derivations using some numerical examples.

The main result of the 1970 paper, in notation which will be explained shortly, is an equation stating that:

dQ = Cov(z,q)/Z + Sz\[i\]dq\[i\]/NZ  

In words, this can be loosely translated as:

The change in frequency (if any) of a gene from one generation to the next is composed of two elements: (a) the effect of the gene on the reproductive success of the parent generation, as measured by the connection between possession of the gene and the number of offspring; and (b) the change in frequency of the gene between individual parents and their own offspring.

As presented in words, the equation may seem almost a platitude. *Of course* the change in frequency depends on these two factors: what else could it depend on? But even in these loose verbal terms, the result has some value in focusing on the two distinct, and possibly conflicting, elements.

The mathematical equation, which uses the precise statistical concept of covariance, is more important than the verbal formulation. Price himself considered it literally miraculous that someone like himself, with no training in statistics and genetics, who previously ‘did not know a covariance from a coconut’, should have discovered such a fundamental relationship (Hamilton 322-3). The equation had in fact been partially anticipated by other writers, but it was not widely known. C. A. B. Smith, an experienced geneticist and statistician, told Price ‘he had never seen anything like it before’ (Harman 210). \[Added: W. D. Hamilton has said that ‘Central to Price’s approach was a covariance formula the like of which I had never seen… The formula was easily checked to be correct, yet the approach by which it came obviously owed nothing to any previous account of selection theory I knew of.’ (Hamilton, 172)\] The Editor of *Nature* initially rejected Price’s paper as ‘too hard to understand’ (Harman 224). As late as 1997 John Maynard Smith still [claimed](http://webofstories.com/play/7297), not entirely in jest, that he ‘did not understand Price’s Theorem’.

Whether favourable or not, these reactions suggest that Price’s work is somehow obscure and mysterious. I think this is exaggerated. While it is not trivial, it is not exceptionally obscure either.

**Notation**

I shall stick as closely as possible to Price’s own notation, to facilitate comparison with his paper, but for practical reasons will avoid Greek letters and other special typography. Where Price uses capital Greek sigma to indicate summation, I will use capital S. Where Price uses capital Greek delta to indicate an increase or decrease in a quantity, I will use the letter d. Where Price uses a bar over a letter to indicate the mean (average) value of a variable, I will use the capital form of the letter; so, for example, the capital letter Z will indicate the mean value of the variable z. Where Price uses subscripts, I will use square brackets, so for example where Price has n with a subscript g, I will use n\[g\]. A forest of subscripts makes formulae more difficult to read, and subscripts can often be omitted without danger of ambiguity. However, for consistency with Price’s paper I have decided to retain them. \[Added September 21: I have now substituted asterisks for ‘primes’, which in the WordPress print format were very difficult to read.\]

**Statistical preliminaries**

Price assumes some elementary knowledge of statistics, including the concepts of mean and covariance. The mean of a set of quantities is simply the sum of their values divided by the number of items. The covariance is defined as follows. Suppose there are two variables, x and y, with n values (not necessarily different) for each variable, and each value of x is paired with a value of y in some definite way, for example because they are measurements of different properties of the same individual. Let the values of each variable be indexed with the numbers \[i\] = 1, 2, … n in such a way that paired values have the same index number. By definition the covariance between the variables for that pairing is Cov(x,y) = S(x\[i\] – X)(y\[i\] – Y)/n. The intended scope of the summation sign S is the whole of the expression following it, and a term of the sum is to be formed for each pair of x and y values with the same index number. The value of the covariance will of course depend on the particular pairing of values under consideration; if they were paired in some other way the covariance might be quite different.

An important resultused by Price is that Cov(x,y) = Sx\[i\]y\[i\]/n – XY. This was well-known in the statistical literature available to Price, but I have given a derivation in Note 1.

The covariance between two variables can be regarded as a measure of the closeness of the relationship between them. For given sets of values, if high values of x are paired with high values of y, and low values with low values, then the covariance will be relatively large. If values are paired at random, then the covariance will be close to zero, while if high values are paired with low values, then the covariance will be negative. The numerical value of the covariance is however affected by differences of scale: for example it will be larger if linear measurements are expressed in inches rather than feet. For this reason statisticians usually prefer a standardised measure, such as a correlation coefficient, which is not affected by changes of scale.

**Assumptions and definitions**

For simplicity Price assumes that a population of a species has separate generations. (Towards the end of his paper he indicates ways in which this assumption might be relaxed.) In comparing the number of individuals in different generations it is important to count them at corresponding points in their life cycle. Price does not discuss this at length, but his comments imply that the ‘offspring’ of a set of parents include all ‘zygotes conceived’. This suggests that the count of each generation should be taken immediately after conception. This makes good sense in the context of Price’s First Equation, because it makes a sharp distinction between the effect of a gene on the fitness of the individual organism and any changes in gene frequency occurring solely during the transmission of genes from parents to offspring. These two types of effect can therefore be divided neatly between the two components in the right hand side of the equation. If the count were taken at some later stage, say at the hatching of eggs, then the effect of a gene on the fitness of individuals would be smeared between the two components. (Contrast this with the current Wikipedia [account](https://en.wikipedia.org/wiki/Price_equation), which seems to assume that the ‘count’ of the second generation is taken after a process of selection on the offspring. There is no basis for this in Price’s own treatment, and it conflicts with his statement that ‘if meiosis and fertilization are random with respect to gene A, the summation term at the right will be zero except for statistical sampling effects…’, which would not be the case if the gene undergoes selection in the offspring before the second generation is counted.)

P\[1\] and P\[2\] are two generations of a species. P\[1\] contains all parents of P\[2\] members, and P\[2\] consists of all offspring of P\[1\] members. Note the distinction between ‘contains’ and ‘consists’. It is common for some individuals in one generation to have no offspring, and, as later becomes clear, it is Price’s intention to include such individuals in P\[1\]. It would in principle be possible to count P\[1\] only as a generation of actual parents, but if this were the case then the equation would exclude much of the selective effect of a gene.

N is the number of members of P\[1\]. They are to be labelled with index numbers i = 1, 2, …. N.

It is assumed that each individual has the same number of genes (zygotic ploidy) at a given locus. (Price later indicates how this assumption might be modified for more complicated cases, such as X and Y chromosomes.) The zygotic ploidy of the species for the gene of interest will be called n\[z\] (where z presumably stands for ‘zygotic’). This n must not be confused with the population number N.

The number of genes of a particular kind, A, in individual i, will be called g\[i\]. For a haploid locus g\[i\] must be 0 or 1, for a diploid locus it must be 0, 1, or 2, and so on.

The frequency of genes of a type A, in individual i, will be called q\[i\]. By ‘frequency’ Price means the proportion of A genes at the relevant locus. From the previous definitions this must be q\[i\] = g\[i\]/n\[z\]. For a haploid the frequency q\[i\] can only be 0 or 1; for diploids it could be 0, .5, or 1, and so on.

In what follows, summation is always over the N members of P\[1\], even when properties of P\[2\] are under consideration. (This is one of the distinctive features of Price’s approach, which at first may make it difficult to follow.) When variables with an \[i\] subscript are to be multiplied together, the intention is that the i’th member of one set is to be multiplied by the i’th member of the other.

Q\[1\] is the overall frequency of gene A in population P\[1\]. Since this is the total number of A genes as a proportion of all genes at the relevant locus, it isSg\[i\]/n\[z\]N, where summation is taken over all the individuals in P\[1\]. From the definition of g\[i\] and q\[i\] this also equals Sn\[z\]q\[i\]/n\[z\]N. In this expression n\[z\] is a constant and can be cancelled out, leaving Sq\[i\]/N. But from the definition of a mean this is the mean value of q\[i\] for population P\[1\]. In Price’s notation this is q with a bar over it, and in my notation Q. We therefore have Q\[1\] = Q.

We turn now to the following generation, P\[2\]. A gamete from a member of P\[1\] which contributes genes to a member of P\[2\] is termed a ‘successful gamete’. The number of successful gametes produced by individual i is designated z\[i\]. (The reason for choosing the letter z is not clear. It could stand for ‘zygote’, or ‘zygote conceived’.) This is said by Price to be the same as the number of i’s offspring. In the special case of self-fertilisation this is not true, in ordinary usage, since there are then two successful gametes but only one offspring, but this oversight (if it is one) does not affect the validity of Price’s derivation. It is assumed that the gametes contributing to P\[2\] all have the same ploidy at the locus of gene A, which will be designated by n\[g\] (where g presumably stands for ‘gametic’). Gametes are usually haploid, but diploid, triploid, etc, gametes are possible. The number of A genes among all of i’s successful gametes is designated g\*\[i\] (note the asterisk after g; asterisks are used here to designate quantities in P\[2\] compared with P\[1\]). Since individual i has z\[i\] successful gametes, with a ploidy of n\[g\], the total number of genes at the relevant locus among all of i’s successful gametes is z\[i\]n\[g\]. The frequency (proportion) of A genes at the relevant locus among all of i’s successful gametes is designated q\*\[i\]. In cases where the number of i’s successful gametes is not zero, the frequency q\*\[i\] is evidently g\*\[i\]/z\[i\]n\[g\]. When z\[i\] is zero, the concept of frequency appears not to apply, and the formula g\*\[i\]/z\[i\]n\[g\] would require division by zero, which is invalid. However, for further working Price wants q\*\[i\] to be defined even when z\[i\] is zero, and he stipulates that in this case, q\*\[i\] = q\[i\]. This seemingly strange stipulation turns out to be workable in the further stages of the derivation.

I note in passing that Price’s use of the letter ‘g’ to refer both to ‘number of genes’ and to ‘gametic ploidy’, and his use of the letter ‘z’ to refer both to ‘zygotic ploidy’ and to the ‘number of i’s successful gametes’, is unfortunate. While in their context these uses can always be distinguished, one would think that with 26 letters to choose from Price could have found clearer alternatives. The confusion is compounded when several commentators, following Steven A. Frank, use the letter ‘z’ for an entirely different purpose, and in some cases (though not that of Frank himself) assert that this was Price’s usage.

As a final group of definitions, dq\[i\] = q\*\[i\] – q\[i\], the change in frequency of A between a parent and its own offspring; Q\[2\] is the frequency of gene A in population P\[2\]; and dQ = Q\[2\] – Q\[1\], the change in the overall frequency of gene A between the two populations.

As a summary of all these definitions and equivalences, we have:

P\[1\]: the first generation, containing all parents of P\[2\], but also including any individuals with no offspring.  
P\[2\]: all offspring of members of P\[1\].  
N: the number of members of P\[1\].  
i: an index number of a member of P\[1\].  
Gene A: the particular gene type we are interested in.  
n\[z\]: the number of genes (zygotic ploidy) at the locus of gene A in a member of P\[1\].  
g\[i\]: the number of genes of type A in individual i.  
q\[i\]: the number of genes of type A as a proportion of all genes at the relevant locus in individual i.  
q\[i\] = g\[i\]/n\[z\].  
g\[i\] = n\[z\]q\[i\].  
Q: the mean value of q\[i\], by definition equal to Sq\[i\]/N.  
Q\[1\]: the overall frequency of gene A at the relevant locus in P\[1\].  
Q\[1\] = Sg\[i\]/n\[z\]N = Sn\[z\]q\[i\]/n\[z\]N = Sq\[i\]/N = Q.  
Successful gamete: a gamete from P\[1\] which contributes genes to a member of P\[2\].  
z\[i\]: the number of successful gametes produced by individual i.  
n\[g\]: the number of genes (gametic ploidy) at the locus of gene A in a gamete.  
g\*\[i\]: the number of A genes among all of i’s successful gametes  
z\[i\]n\[g\] = the total number of genes at the locus of gene A among all of i’s successful gametes.  
q\*\[i\]: the number of genes of type A as a proportion of all genes at the relevant locus among all of i’s successful gametes.  
q\*\[i\] = g\*\[i\]/z\[i\]n\[g\], when z\[i\] is not zero. When it is zero, by stipulation q\*\[i\] = q\[i\].  
dq\[i\]: the change, if any, in the frequency of gene A between individual i and i’s successful gametes.  
dq\[i\] by definition = q\*\[i\] – q\[i\].  
Q\[2\]: the frequency of gene A at the relevant locus in population P\[2\].  
dQ by definition = Q\[2\] – Q\[1\].

**Derivation**

After all the preliminaries, Price’s actual derivation of his equation is almost startlingly brief. \[Added:Hamilton (p.172) describes it as ‘like a rabbit from a conjuror’s hat’.\]The underlying aim is to find an expression for the change in the frequency of gene A between P\[1\] and P\[2\], in other words, to find dQ, using information about the number of offspring and gene frequencies of individual members of P\[1\]. We already have an expression for Q\[1\], which is Sq\[i\]/N = Q (the mean value of q\[i\]). If we can find a suitable expression for Q\[2\], dQ will therefore be Q\[2\] – Q.

From the definitions already laid down, Q\[2\] is the proportion of A genes among all genes at the relevant locus in P\[2\]. This is given by the number of all A genes in P\[2\] divided by the number of all genes at the locus: Q\[2\] = Sg\*\[i\]/Sz\[i\]n\[g\] = Sz\[i\]n\[g\]q\*\[i\]/Sz\[i\]n\[g\]. (It may be noted that in cases where z\[i\] is zero, the product z\[i\]q\*\[i\] is also zero, so these products add nothing to the total, which is why Price’s definition q\*\[i\] = q\[i\] for these cases is workable.) Since n\[g\] is a constant it may be cancelled out, giving:

Q\[2\] = Sz\[i\]q\*\[i\]/Sz\[i\] = Sz\[i\]q\*\[i\]/NZ.

This is relatively simple, but not obviously useful. Price’s next step is more ingenious, and is the key to the whole derivation. Recalling that by definition dq\[i\] = q\*\[i\] – q\[i\], and therefore q\*\[i\] = q\[i\] + dq\[i\], we can substitute q\[i\] + dq\[i\] for q\* in the above equation, which gives us Q\[2\] = Sz\[i\](q\[i\] +dq\[i\])/NZ. Using the standard rules of summation this may be rearranged as:

Q\[2\] = Sz\[i\]q\[i\]/NZ + Sz\[i\]dq\[i\]/NZ.

Price’s next piece of ingenuity is to notice that the first term on the right is related to the covariance between z and q. By one of the standard formulae for covariance (see above and Note 1), Cov(z,q) = Sz\[i\]q\[i\]/N – ZQ, therefore Sz\[i\]q\[i\]/N = Cov(z,q) + ZQ, and Sz\[i\]q\[i\]/NZ = Cov(z,q)/Z + Q.

We therefore obtain:

Q\[2\] = Cov(z,q)/Z + Q + Sz\[i\]dq\[i\]/NZ.

But Q\[1\] = Q, and dQ = Q\[2\] – Q\[1\], therefore:

dQ = Cov(z,q)/Z + Sz\[i\]dq\[i\]/NZ.

This is Price’s First Equation. It is often expressed in the form ZdQ = Cov(z,q) + Sz\[i\]dq\[i\]/N, but so far as I know Price himself did not use this form.

The ‘covariance’ term on the right hand side is a measure of the relationship between the fitness of individuals in the parent generation and their possession of one or more copies of the A gene. If the A gene has no effect on fitness, the covariance will be zero (apart from statistical fluctuations), while if it has a strong beneficial effect the covariance will be relatively high, and if the effect is adverse the covariance will be negative. As fitness is measured by the individual’s number of ‘successful gametes’, anything that affects this, such as differential survival, mating success, or fecundity, will be taken account of in the covariance term. In so far as the genotype of the parent (not the gamete) affects the fate of sperms and eggs before fertilisation, this will also count in the covariance term.

The second term on the right hand side measures the change in frequency, if any, of the A gene between individual parents and their offspring. (Individuals who have no offspring do not contribute to the second term, as in this case z\[i\] = zero.) If the count of offspring (or successful gametes) is taken immediately after fertilization, as Price seems to envisage, the effects of gene A on the fitness of the offspring themselves will not affect the second term. Changes in gene frequency between parents and offspring may occur purely by random sampling effects, in which case they will tend to cancel out in large populations. The other main factors would be any tendency for some genes to get into more gametes than others (segregation distortion or meiotic drive), any effect of the gametic genes on the viability or mating success of the gametes themselves, and gene mutation. The effects of these factors (other than chance) are usually small. Gene mutation is a rare event, and the mechanisms of heredity seem to actively work against any distortion of gene ratios in the formation of gametes (see Chapter 7 of Mark Ridley’s *Mendel’s Demon*). And, in animals at least, the genes of the gamete itself are in general inactive until after fertilization. (I do not know the position in plants.) For these reasons in practice the second term will often be small, and Price therefore gives as an approximation the following form:

dQ = Cov(z,q)/Z.

As Price points out, this equation can also be expressed in terms of regression or correlation coefficients, as Cov(z,q) = Reg(z,q)Var(q) = Corr(z,q)sd(z)sd(q), where ‘Reg’ stands for Regression, ‘Corr’ stands for Correlation, ‘Var’ stands for Variance, and ‘sd’ stands for standard deviation.

The main value of Price’s First Equation in itself, it seems to me, is in distinguishing between two types of selection that may affect the change of gene frequency between generations. One of these is selection on parents affecting the number of successful gametes produced, the other is selection (or random change) among genes in the process of gamete formation and fertilisation. The second type of change is usually unimportant, provided chance events are averaged out, but there is no a priori reason why it should be, and there is an important evolutionary question why in fact it is (see Mark Ridley’s book in general).

The first term – the Covariance term – seems to me less interesting in itself than Price and his enthusiasts believe. But I will defer general comments on the value of Price’s various equations until a later post.

As to the ‘obscurity’ of the equation and its proof, Price’s treatment may seem elaborate, and in places difficult to follow, but much of it is quite mechanical, and follows almost inevitably once one tries to derive the change in population gene frequency from data about individual gene frequencies and reproductive fitness. (A slightly simpler derivation is possible by omitting separate terms for g and g\* – see Note 2.) There are however those two flashes of ingenuity which lift it above a mere algebraic grind.

Apart from its intrinsic interest, the First Equation is also important as the prelude to the treatment in Price’s 1972 paper, where an equation is derived for ‘multi-level’ selection. It is the 1972 equation that is probably best known as ‘Price’s Equation’. At the end of the 1970 paper Price indicated that he was already working on these further developments.

There remain some biographical questions. How did Price, who had no biological training, get interested in these issues at all? And how did he hit on the particular approach of his First Equation?

Oren Harman’s biography of Price throws some light on these questions, but it is not always clear where hard evidence ends and speculation begins. I won’t discuss this further, but Harman does make one interesting claim about the equation itself. This is that Price first derived the simpler form of the equation, with just the ‘covariance’ term, and only later added the second term (Harman 220). This is entirely possible, but it is not clear whether there is any explicit documentary source for it. To see how it is possible, suppose we take the previous analysis as far as the equation:

Q\[2\] = Sz\[i\]q\*\[i\]/NZ.

Then at this point suppose we say: On average the change in gene frequencies between adults and their own offspring is usually slight, so to a good approximation, q\*\[i\] = q\[i\]. We can therefore say, approximately,

Q\[2\] = Sz\[i\]q\[i\]/NZ.

The final stage of the derivation can then proceed as before, but without the second term.

Whether this is how Price himself arrived at the simpler version of the equation I have no idea.

**Note 1**

By definition Cov(x,y) = S(x\[i\] – X)(y\[i\] – Y)/n. Expanding the right hand side by the usual rules of algebra, as applying to sums, we get (Sx\[i\]y\[i\] – Sx\[i\]Y – Sy\[i\]X + nXY)/n. (Note that the product XY has to be counted n times, once for each pair of corresponding x and y values.) But Sx\[i\]Y = nXY, and Sy\[i\]X = nYX, therefore the right hand side can be simplified to (Sx\[i\]y\[i\] – nXY)/n, or Sx\[i\]y\[i\]/n – XY, which was the required formula.

**Note 2**

Definitions and notation are as above, except that:  
a = zygotic ploidy  
b = gametic ploidy  
the terms g and g\* are omitted.

From the definitions:  
Q\[1\] = Sq\[i\]a/Na = Sq\[i\]/N = Q  
Q\[2\] = Sq\*\[i\]bz\[i\]/Sbz\[i\] = Sq\*\[i\]z\[i\]/Sz\[i\] = Sq\*\[i\]z\[i\]/NZ

The remaining stages of the derivation are as before.

**References**

Works by George Price  
1. G. R. Price, ‘Selection and covariance’, *Nature*, 227, 1970, 520-21.  
2. G. R. Price, ‘Extension of the Hardy-Weinberg law to assortative mating’, *Annals of Human Genetics*, 36, 1971, 455-58.  
3. G. R. Price, ‘Extension of covariance selection mathematics’, *Annals of Human Genetics*, 35, 1972, 485-90.  
4. G. R. Price, ‘Fisher’s Fundamental Theorem made clear’, *Annals of Human Genetics*, 36, 1972, 129-40.  
5. G. R. Price and C. A. B. Smith, ‘Fisher’s Malthusian parameter and reproductive value’, *Annals of Human Genetics*, 36, 1972, 1-7.  
6. J. Maynard Smith and G. R. Price, ‘The logic of animal conflict’, *Nature*, 246, 1973, 15-18.

Other works  
Steven A. Frank, ‘George Price’s contributions to evolutionary genetics’, *Journal of Theoretical Biology*, 175, 1995, 373-88.  
W. D. Hamilton, *Narrow Roads of Gene Land*, vol. 1, 1996.  
Oren Harman: *The Price of Altruism: George Price and the Search for the Origins of Kindness*, 2010.  
Mark Ridley: *Mendel’s Demon: Gene Justice and the Complexity of Life*, 2000 (UK edition. A US edition, which I have not seen, was published with the title *The Cooperative Gene*. )

### Related Posts:

- [The Price of
  Altruism](https://www.gnxp.com/WordPress/2010/07/21/the-price-of-altruism/) - [The Price
  Equation](https://www.gnxp.com/WordPress/2009/11/10/the-price-equation/) - [The mists of the adaptive
  fog](https://www.gnxp.com/WordPress/2008/11/18/the-mists-of-the-adaptive-fog/) - [Open Thread - October 30th,
  2010](https://www.gnxp.com/WordPress/2010/10/30/open-thread-october-30th-2010/) - [Correlation between wine quality and price
  negative?](https://www.gnxp.com/WordPress/2008/11/18/correlation-between-wine-quality-and-price-negative/) - [The Fame of
  Price](https://www.gnxp.com/WordPress/2010/08/22/the-fame-of-price/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F09%2F05%2Fprices-first-equation%2F&linkname=Price%27s%20First%20Equation "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F09%2F05%2Fprices-first-equation%2F&linkname=Price%27s%20First%20Equation "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F09%2F05%2Fprices-first-equation%2F&linkname=Price%27s%20First%20Equation "Email")[](https://www.addtoany.com/share)
