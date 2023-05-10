+++
title = "Notes on Sewall Wright"
full_title = "Notes on Sewall Wright Wright's Fstatistics"
date = "2008-05-20"
upstream_url = "https://www.gnxp.com/WordPress/2008/05/20/notes-on-sewall-wright-wright-s-f-statistics/"

+++
Source: [here](https://www.gnxp.com/WordPress/2008/05/20/notes-on-sewall-wright-wright-s-f-statistics/).

Notes on Sewall Wright: Wright's F-statistics

Several of my previous notes have touched on the subject of Sewall Wright’s F-statistics. The best known of these is FST, which is very widely used as a measure of the genetic divergence between sub-populations of a species. My aim in this note is to trace the evolution of the F-statistics in Wright’s work.

**Why F?**

A preliminary question is one of terminology. What, if anything, does the letter ‘F’ stand for? One plausible answer is that it stands for ‘fixation’, since among other things the F-statistics can be used to measure the rate at which alleles tend to be ‘fixed’. Wright himself in his later writings sometimes refers to F as an ‘index of fixation’.

Plausible though this may be, it does not seem to be the origin of Wright’s use of the letter F. This first appeared in his series of papers on ‘Systems of Mating’ in 1921, where he uses the letter F (in its lower-case form ‘f’) as a symbol for the ‘correlation between uniting gametes’ and as a measure of inbreeding. Although the word ‘fixation’ does occur in these papers, Wright does not say that ‘f’ stands for ‘fixation’. The banal truth seems to be that by the time Wright needed a symbol to represent the correlation between uniting gametes, the letters a to e had already been allocated to other purposes, so that f was the first available letter in the alphabet.

**F as correlation between uniting gametes**

Wright’s primary use of F (or f) is to designate the correlation between uniting gametes. The general idea of a correlation between gametes is now somewhat unfamiliar. If there are varying types of gametes in the population, uniting gametes may be said to be positively correlated if the same types tend to be paired together at mating, or negatively correlated if dissimilar types are paired. If the different alleles at a locus in the population are given notional numerical values, such as 0 and 1, a correlation coefficient for the correlation between pairs of uniting gametes can be calculated in the usual way. (For a fuller explanation see my [post](https://www.gnxp.com/blog/2008/04/notes-on-sewall-wright-measurement-of.php) on Wright’s measurement of kinship.) The resulting correlation coefficient is F.

**Heterozygosis and the correlation between gametes**

Also in 1921 Wright points out that the correlation between uniting gametes is connected with the proportion of heterozygotes in the population. Whether an individual is heterozygous at a locus is determined by the gametes (egg and sperm) of its parents which unite to form a zygote at fertilization. If they are identical at that locus, the offspring is homozygous, otherwise it is heterozygous. The proportion of heterozygotes (the level of heterozygosis) among the offspring, over and above the level expected with random mating, can be calculated from the correlation between uniting gametes, and vice versa. In SM1 Wright calculates that the percentage of heterozygosis is (1/2)(1 – f), where f is the correlation between uniting gametes. (This is stated without full proof, but I have checked it, calculating the correlation by the method of notional values.) This formula is only valid for the special case where there are two alleles with equal proportions of 1/2 in the population, but Wright soon (in 1922) generalised it to the case of two alleles with proportions of p and q = (1 – p), in which case the formula is 2pq(1 – f). He also began to use upper-case F, rather than f, as his preferred notation.

**F as a measure of inbreeding in a population**

A positive correlation between uniting gametes can arise in two ways (apart from mere sampling error): by assortative mating between similar phenotypes, or by mating between genetic relatives, in other words by inbreeding. Wright deals with both inbreeding and assortative mating, but gives more attention to inbreeding. If assortative mating is excluded, then F can be used as a measure of the average degree of inbreeding in a population.

If the correlation between gametes is due solely to inbreeding, then the formula 2pq(1 – F) for the percentage of heterozygosis in a population can be given a simple interpretation in terms of Malecot’s concept of Identity by Descent. The two genes at a locus in an individual are either Identical by Descent (IBD) from a common ancestor, or they are, by assumption, drawn randomly from the gene pool. In the first case they are certainly identical. In the second case, applying the familiar Hardy-Weinberg formula, they have a probability of (1 – 2pq) of being identical. Therefore if we interpret F as the probability that the two genes are IBD, on average for the population, the total probability that they are identical is F + (1 – F)(1 – 2pq) = 1 – 2pq(1 – F). Subtracting this from 1 to get the probability of heterozygosity we get the required formula 2pq(1 – F).

**F and the inbreeding of individuals**

The degree of inbreeding in a class of individuals (e.g. all offspring of matings between siblings) can be derived from an analysis of the way in which they are bred. The coefficient of inbreeding then measures the correlation between any pair of alleles at the same locus in an individual belonging to that class.

The level of inbreeding in an offspring can be derived from the correlation between the uniting gametes of its parents, which in turn can be derived from the correlation between the parents themselves, in accordance with Wright’s method of path analysis. The full method would involve considerations of dominance, heritability, and so on, but the coefficient of inbreeding is usually derived using a simplified method devised by Wright himself and expounded in several papers of the early 1920s (see especially paper 2 in ESP).

In the simplest case, for the offspring of half-siblings who are not themselves inbred, Wright’s formula gives a coefficient of inbreeding of 1/8. This is the same as the figure derived by the methods of Malecot for the probability in this case that the two genes at a locus in the offspring are identical by descent. In Malecot’s approach this result is derived from explicit assumptions about probabilities. It is assumed that each gene in an offspring has a probability of 1/2 of coming from either parent, and – very importantly – that there is an independent probability of 1/2 that the same gene is inherited by any other offspring of the same parent. This is an assumption which is usually empirically correct (with certain exceptions such as sex chromosomes), but it is not logically necessary. For example, if surviving offspring came in pairs, each member of which received genes from complementary chromosomes in the parent, such pairs of offspring would have a lower correlation with each other than the usual calculations would suggest.

It is therefore worth asking what features of Wright’s approach take the place of the explicit probability assumptions in Malecot’s system. The first key assumption, that each gene in an offspring has a probability of 1/2 of coming from either parent, is explicitly stated as a biological assumption (with the exception of sex-linked genes) in Wright’s derivation of the path coefficient between offspring and parent. The other key assumption, that there is an independent probability of 1/2 that the same gene is inherited by any other offspring, does not seem to be explicitly stated. In SM1 Wright only directly calculates the correlation between parent and offspring. All other correlations, such as those between siblings, are derived indirectly from the parent-offspring correlation by the method of path analysis. The assumption of independent probabilities for each offspring seems to be built into the general assumptions of path analysis. In a late discussion of the principles of path analysis Wright emphasised that ‘The validity of the system requires t  
hat any variable that enters into the system as a common factor back of two or more dependent variables, or as an intermediary in a chain, vary as a whole. If one part of a composite variable…. is more significant in one relation than in another, the treatment of the variable as if it were a unit may lead to grossly erroneous results’ (EGP vol. 1 p.300). Fortunately, the assumption appears to be consistent with the usual pattern of genetic inheritance. Apart from special cases such as sex-linked genes, or MZ twins, it seems that each surviving offspring has an equal and independent probability of receiving any given allele from the same parent. This is despite the fact that during the formation of gametes the precursor-cells of the gametes are formed in pairs with complementary alleles from different chromosomes in the parent. In the case of eggs, only one of the proto-eggs formed from the same parental cell usually survives. In the case of sperms, so many sperms are produced in total that the chance of two sperms derived from the same parental cell both ending up in surviving offspring is negligible.

**F as a measure of inbreeding relative to a foundation stock**

One of Wright’s original motives in devising his F statistics was to measure the effect of continued inbreeding over a number of generations. In agricultural (and laboratory) practice it is common for animals to be bred systematically over long periods using close relatives, e.g. mating sisters with brothers, or daughters with their fathers. With such practices the level of inbreeding among the offspring rises over the generations, and the level of heterozygosis declines. Wright’s F-statistics provide a convenient method of measuring this process, superior to the previous ad hoc methods. The result of a number of generations of inbreeding within an inbred line can be summarised in the average F within that line, relative to the foundation stock (the population from which the inbred line is derived). The cumulative decline of heterozygosis since the inception of the line can then be calculated using the formula 2pq(1 – F). But this should raise questions about the precise meaning of F in such a case. F is in principle always a correlation coefficient, and could if necessary be expressed in terms of the Pearson product-moment formula. This requires the mean and standard deviation of the relevant statistical population to be specified. But what is the mean in the present case? The correlation is said to be ‘relative to the foundation stock’, so this appears to be the relevant statistical population, but the foundation stock no longer exists, and the correlated pairs are not part of it. So what is going on? Is F a legitimate correlation coefficient at all when more than one generation is involved?

This puzzled me until I paid proper attention to page 169 of SM5. This gives the key to the mystery. Rather than just considering the correlation within a single inbred line, we must consider an indefinitely large (actual or hypothetical) ensemble of lines, all separately inbred according to the same system (e.g. sibling mating) for the same number of generations, and all derived from the same ‘foundation stock’. The mean gene frequencies for the entire ensemble (or a large random sample thereof) should then be the same as in the foundation stock (in the absence of selection and mutation), but will vary within each particular inbred line according to the chance variations resulting from the reproductive process. F will therefore measure the average correlation within each such line as compared with the values of the foundation stock. Such a correlation coefficient will usually be hypothetical, since no such ensemble actually exists, but in principle it has a clear meaning consistent with the general method of correlation.

**The story so far**

The uses of F (or f) identified so far were all first described in Wright’s ground-breaking ‘Systems of Mating’ in 1921. The different uses therefore cannot be put in a chronological sequence. Logically, however, the sequence is as follows:

a\) F as the correlation between uniting gametes. This is always the fundamental conception.

b\) F as a measure of average inbreeding in a population. In this sense it is closely connected to the level of heterozygosis.

c\) F as a measure of inbreeding in an individual. In this sense it is closely connected to the measurement of relatedness.

d\) F as a measure of continued inbreeding in a line relative to a foundation stock – see the last paragraph.

**F in natural populations**

As developed by Wright in 1921, the concept of F was heavily influenced by the circumstances of agricultural stock breeding, where mating is carried out in accordance with some deliberate plan. (Wright was employed in agricultural research for the US Department of Agriculture at the time – see Provine, chapter 4). The next major step was Wright’s application of F to the measurement of genetic drift in natural random-mating populations. It is clear from Provine’s biography that Wright first took this step around 1925, but the results were not fully published until the major paper on ‘Evolution in Mendelian Populations’ in 1931.

I have discussed genetic drift in a previous [post](https://www.gnxp.com/blog/2008/05/notes-on-sewall-wright-genetic-drift.php), and will not repeat that discussion here. The essential point is that in any finite population, over the course of time, there will be a tendency, purely by chance, for some lines of ancestry to be relatively successful, while others dwindle and eventually die out. The result is that, in the absence of selection or mutation, fewer alleles will account for a larger proportion of genes in the population, and the level of heterozygosis will decline.

As a result of genetic drift, F tends to increase at a rate of approximately 1/2N per generation, where N is the size (strictly, the ‘effective’ size) of the random mating population. But F is still in principle the correlation between uniting gametes. Since the correlation between uniting gametes within a random mating population is zero, how can there be an increasing value of F?

The answer is again that F is a correlation relative to the baseline of a ‘foundation stock’. Wright does not, so far as I know, explain what exactly this means in the case of a natural random mating population, but I think we can understand it by analogy with the case of inbred agricultural breeding lines. We are to imagine that from a specified generation onwards a population is allowed to evolve by random genetic drift in a large number of hypothetical different ways. Within each of the resulting hypothetical descendent populations there will be a correlation between uniting gametes relative to the entire ensemble of hypothetical outcomes. The average of these correlations is constantly increasing. It is conceivable that in some cases the actual observed value of F – the correlation between uniting gametes within an actual population relative to that in the foundation stock – would be negative, but the expected average F is always positive.

**F in subdivided populations**

If a number of subgroups of a population breed within themselves in full or partial isolation from each other, the gene frequencies within them will tend to diverge from each other as a result of selection or genetic drift. Within each such subgroup, individuals will tend to be more similar to each other than to individuals randomly selected from other subgroups or from the entire population. Within the groups, individuals will therefore be positively correlated with each other relative to the entire population.

Wright developed a system of F-statistics to analyse the structure of subdivided populations. This is one of his major contributions to population genetics after the fundamental paper EMP of 193  
1. The best-known of the F-statistics is FST, where S and T should ideally be subscripts, and stand for ‘subpopulation’ and ‘total population’. The expression FST is possibly first used in a paper of 1950 (ESP p.585), but the underlying concept was first developed in a paper of 1943 on ‘Isolation by Distance’. (I will cite this from the reprint in ESP, but it may be available online [here](http://www.pubmedcentral.nih.gov/picrender.fcgi?artid=1209196&blobtype=pdf). I downloaded it successfully once, but on another occasion got an error message.)

Wright considers a population subdivided into a number of subpopulations of equal size, within which mating is random, and with two alleles at a locus. He shows, by a relatively simple but ingenious proof (ESP p.403), that in this case the correlation between uniting gametes within each subpopulation, relative to the total, is equivalent to Vp/pq, where Vp is the variance of the gene frequencies of the subpopulations (i.e. the mean square of their deviations from the frequency in the total population), and p and q are the frequencies in the total population. In 1943 this correlation is simply called F, but it is in fact the measure later known as FST. Wright recommends that the square root of F could usefully be taken as a measure of the genetic divergence between populations. (Of course, the rank order will be the same whether we take F itself or its square root as the measure.) It may also be noted that Vp/pq cannot be negative, as both the numerator and denominator are necessarily positive or at least zero. In general, a correlation coefficient may be either positive or negative, but in this case F measures the correlation due to the average differences between the gene frequencies of subpopulations, regardless of sign, and these cannot be less than zero.

In the same 1943 paper, and in subsequent papers of the 1940s, Wright developed methods for dealing with correlations within hierarchically subdivided populations, where mating within each division may or may not be random. His terminology varied somewhat, but by 1950 he seems to have settled on the following (with IT, IS, and ST as subscripts):

FIT: inbreeding coefficient of individuals relative to the total population  
FIS: inbreeding coefficient of individuals relative to the subpopulation  
FST: correlation between random gametes drawn from the subpopulation relative to the total population. (If mating is in fact not random within the subpopulation, this is a hypothetical correlation.)

Wright shows that these measures are related by the equation FST = (FIT – FIS)/(1 – FIS). (For a relatively simple proof see EGP vol. 2 p.294-5, but note that the left square bracket in Equation 12.14 on that page is in the wrong place: it should be immediately before the first occurrence of qT.) It may be seen that if FIS is zero, in other words if mating within subpopulations is random, then FST = FIT. This is as it should be, since in this case the only source of correlation between individuals is the division of the population into subpopulations. FST then accounts for the entirety of the correlation within the total population, which is FIT.

Wright’s F-statistics are still widely used or alluded to, but are seldom understood in their original sense as correlation coefficients. Inbreeding within individuals is now usually explained by means of Malecot’s Identity by Descent, while FST is usually explained in a way more appropriate to Masatoshi Nei’s GST. Wright’s work was however clearly the inspiration and foundation for the work of these later geneticists.

A few cautions about the use of FST may be useful.

a\) Wright originally intended FST to be calculated as an average over a large number of subpopulations. In theory, it would be possible to calculate it for as few as two subpopulations, in which case, if they are of equal size, FST is d^2/pq, where d is the deviation of the subpopulation frequencies from the frequency in the total population. So far as I know, Wright himself never used it in this way.

b\) FST is calculated from gene frequencies on a locus-by-locus basis. It may well vary from one locus to another. To get an indication of the extent of evolutionary divergence between subpopulations, it is desirable to take the average FST over a large number of loci.

c\) FST is not simply proportional to the length of time or number of generations that two subpopulations have been diverging. Other factors such as the amount of migration between them and the size of the populations are also relevant. Small populations diverge by genetic drift far more quickly than large ones.

d\) Wright intended FST mainly to be used for genes that are not subject to significant natural selection. Genes that are under selection may diverge either more or less in different subpopulations than an average FST would suggest.

References:

William B. Provine: Sewall Wright and Evolutionary Biology, 1986.

Sewall Wright: Evolution: Selected Papers, edited and with Introductory Materials by William B. Provine, 1986. (ESP)

Sewall Wright: Evolution and the genetics of populations, 4 vols., 1968-1978. (EGP)

### Related Posts:

- [Notes on Sewall Wright: Wright's
  F-statistics](https://www.gnxp.com/WordPress/2008/05/20/notes-on-sewall-wright-wrights-f-statistics/) - [Sewall Wright & genetic
  drift](https://www.gnxp.com/WordPress/2008/05/09/sewall-wright-genetic-drift/) - [Sewall Wright & the Shifting Balance
  Theory](https://www.gnxp.com/WordPress/2008/10/23/sewall-wright-the-shifting-balance-theory/) - [Sewall Wright & the Shifting Balance Theory (part
  II)](https://www.gnxp.com/WordPress/2008/11/09/sewall-wright-the-shifting-balance-theory-part-ii/) - [Notes on Sewall Wright: the Adaptive
  Landscape](https://www.gnxp.com/WordPress/2008/09/01/notes-on-sewall-wright-the-adaptive-landscape/) - [Notes on Sewall Wright: Population
  Size](https://www.gnxp.com/WordPress/2008/06/06/notes-on-sewall-wright-population-size/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F05%2F20%2Fnotes-on-sewall-wright-wright-s-f-statistics%2F&linkname=Notes%20on%20Sewall%20Wright%3A%20%20Wright%27s%20F-statistics "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F05%2F20%2Fnotes-on-sewall-wright-wright-s-f-statistics%2F&linkname=Notes%20on%20Sewall%20Wright%3A%20%20Wright%27s%20F-statistics "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F05%2F20%2Fnotes-on-sewall-wright-wright-s-f-statistics%2F&linkname=Notes%20on%20Sewall%20Wright%3A%20%20Wright%27s%20F-statistics "Email")[](https://www.addtoany.com/share)
