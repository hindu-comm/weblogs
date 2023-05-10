+++
title = "Measuring Genetic"
full_title = "Measuring Genetic Diversity Lewontin’s Other Fallacy"
date = "2005-05-04"
upstream_url = "https://www.gnxp.com/WordPress/2005/05/04/measuring-genetic-diversity-lewontin-s-other-fallacy/"

+++
Source: [here](https://www.gnxp.com/WordPress/2005/05/04/measuring-genetic-diversity-lewontin-s-other-fallacy/).

Measuring Genetic Diversity: Lewontin’s Other Fallacy

For a while now I’ve been trying to understand how genetic diversity is measured.

For example, there is the familiar finding by Richard Lewontin, replicated by many others, that in humans about 85% of total genetic diversity is found within any single population, and only 15% between different populations.

But what do such statements actually mean? How can diversity be measured and apportioned between populations?

I guess that most laymen with an interest in genetics, like myself, content themselves with a very vague understanding of such claims. A full explanation would probably be too complicated and technical for the layman to follow.

But I wanted to dig a bit deeper. While I did this mainly for my own benefit, the results may be interesting to others.

Briefly:

– the good news is, that the basic concepts and methods are not very technical. Most of the key points can be understood using only elementary algebra.

– the bad news is that there are several different ways of measuring diversity, and especially the diversity or ’distance’ between two or more populations. In general the various methods will give the same rank order of diversity, but they may give very different numerical values.

– the worse news is that some of the most widely used measures are of doubtful value. The problem is not that they are actually wrong, but that the results are ambiguous and can give a misleading impression. In particular, Wright’s FST, Nei’s GST, and similar measures (including that used by Lewontin) can seriously understate the relative importance of genetic differences between populations as compared to differences within them.

Reasons for these conclusions are given more fully in the continuation. I hesitate to go into these technical issues, because I expect to get one (or both) of two responses:

\(1\) That’s all nonsense

or

\(2\) Oh, everyone knows that!

But after a good deal of reading on the subject, I don’t think it’s all nonsense. Most of the points I make can be found somewhere in the academic literature. In particular, I was pleased to find that an eminent population geneticist has made the same key point that independently occurred to me. On the other hand, these issues do not seem to be widely discussed in the literature, and someone who had read (say) the popular works of Cavalli-Sforza, Spencer Wells, and the like, or an introductory genetics textbook, would probably not be aware that there was any serious problem about measuring diversity.

Incidentally, the main problem I discuss is quite different from that raised by Anthony Edwards in his well-known paper on ’Lewontin’s Fallacy’. I should also emphasise that I am not saying that Lewontin’s 85% figure is actually misleading, just that it may be. But to understand why, read the rest…

In measuring genetic diversity we are attempting to quantify the extent of differences within or between populations. If we were measuring diversity in continuous quantitative traits such as height, there would be a clear starting point for identifying the ’differences’ we are interested in. Given any two measurements of the same trait, we can subtract one from the other to get a raw difference or interval. These intervals are themselves quantities in the same dimension as the trait itself, and can be added, multiplied, averaged, etc, to obtain such measures of diversity as the standard deviation, the Gini coefficient, the inter-quartile interval, or the mean absolute-value deviation.

With a non-quantitative trait such as genetic material, the starting point is not so obvious. Given any two stretches of DNA, we can try to identify and list the differences between them. But are all differences equal? Are we interested in differences of single nucleotides, codons, functioning genes, or what? Is every difference to be given the same weight, or do we, for example, ignore non-coding regions or synonymous codons? This depends in part on the underlying motive for measuring diversity. The existing measures of diversity, such as Wright’s FST, were devised mainly to assist in reconstructing phylogenies and population history. For this purpose all genetic differences are potentially informative, and the tendency is to treat all differences as equal. A different approach might be appropriate for other purposes. The choice of units of analysis may also affect the size of measured diversity even if it does not affect the rank order of diversity in different populations: for example, diversity at the level of haplotypes will be larger than at the level of haplogroups, since each haplogroup is divided into many haplotypes.

However, I don’t want to linger on these issues, and will assume that a decision has been taken about the level and kind of genetic differences we are interested in. That still leaves some problems of measurement to be settled.

Once genetic material has been classified into a number of variant forms or ’alleles’ (at whatever level), it would be natural to suggest that the level of diversity within a population can be measured by the number of different alleles within that population, while the diversity between two populations can be measured by the number (and/or proportion) of alleles found in one population and not the other. This could be a workable approach in comparing different species, but within the same species the problem is that most alleles are common to most populations (except perhaps for mitochondrial or Y chromosome haplotypes). Differences are more in the frequency (proportion) of different alleles than in their simple presence or absence.

With sufficient data on the frequency of different alleles, it is possible to calculate the probability that two genes at a given locus, selected at random from the relevant population or populations, will be either identical (homozygous) or different (heterozygous). \[See note 1.\] This will give us the average expected number of genetic differences between individuals, and it is plausible that this pins down in more precise terms the vague concept of ‘diversity’. Most measures of genetic diversity are therefore based on some index of heterozygosity: the probability that two genes at a given locus, selected at random from the relevant population(s), will be different. As Lewontin puts it, ’there are various measures of the diversity of objects in a collection, all of which are equivalent to asking the probability that two objects taken at random from the collection will be of different kinds’ (Lewontin, p.120) If the frequency of a given allele in a population is p, then the probability of randomly selecting that allele twice in succession is p^2 (i.e. p-squared). \[Note 2\] If we square the relevant frequency p for each allele at the same locus, the overall probability of selecting some allele twice in succession will be the sum of all the p-squareds: Σp^2. This is the expected homozygosity of the population at that locus. Since heterozygosity is just the complement of homozygosity, the expected heterozygosity at that locus is 1 – Σp^2, which I will call H. (In the special case of a two-allele system, with frequencies p and q (= 1-p), H = 2pq \[see note 3\].) We can then average H over a number of different loci to get an estimate of average H within the population.

Intuitively, we would expect diversity to be higher, other things being equal, when there are more alleles in the system rather than fewer, and when their frequencies are evenly spread rather than concentrated in one or a few alleles. Conversely, we would expect diversity to be low when most of the frequency is concentrated in one or a few alleles. H meets these criteria of diversity rather well, and in general the level of H seems to be a reasonable way of ranking different populations with respect to their internal genetic diversity. However, this does not guarantee that differences of diversity can be numerica  
lly measured by the difference in H. Suppose for example that a population has n alleles, with equal frequencies for each allele. H will therefore be 1-n\[(1/n)^2\] = 1-1/n. Consider the following values of n and the corresponding values of H (to two places of decimals):

n\_\_\_\_H  
1\_\_\_\_0  
2\_\_\_\_.5  
3\_\_\_\_.67  
4\_\_\_\_.75  
5\_\_\_\_.8  
6\_\_\_\_.83  
7\_\_\_\_.86  
8\_\_\_\_.87  
9\_\_\_\_.89  
10\_\_\_.9  
50\_\_\_.98  
100\_\_.99

Evidently increasing the number of alleles from, say, 2 to 4 does not double the ‘diversity’ as measured by H, and increasing n beyond about 5 makes relatively little difference to H. Even increasing it tenfold from 10 to 100 only increases ‘diversity’ by 1/10. Since H cannot exceed 1, it is bound to be squeezed up against the ceiling when values of n are high. This seems intuitively unsatisfactory if we are looking for a numerical measure of diversity.

As well as differences in the number of alleles, differences in the relative frequency of alleles can also have intuitively unsatisfactory effects on H. Consider the following values of H (to two places of decimals) for different values of p, where p is the more common of two alleles in a two-allele system:

p\_\_\_\_H  
.5\_\_\_.50  
.55\_\_.50  
.6\_\_\_.48  
.65\_\_.46  
.7\_\_\_.42  
.75\_\_.38  
.8\_\_\_.32  
.85\_\_.26  
.9\_\_\_.18  
.95\_\_.10  
.99\_\_.02

Over quite a wide range of changes in gene frequency (from p = .5 up to about p = .75) ‘diversity’ changes rather slowly, but beyond this point it falls more rapidly. Suppose we are comparing diversity in 4 populations, A, B, C, and D, where p and q are in the ratios 5:5, 7:3, 8:2 and 9:1 respectively. For these ratios, H is .5, .42, .32 and .18 respectively. By the criterion of H, we will conclude that the rank order of diversity (from greater to less) is A\>B\>C\>D, which is intuitively reasonable, but we would also conclude that the difference in diversity between C and D (.32 – .18 = .14) is greater than the difference between A and B (.5 – .42 = .08). This does not seem intuitively right: in quantifying diversity at a population level the difference between a 5:5 split and a 7:3 split is surely at least as important as the difference between 8:2 and 9:1.

A further weakness of H as a quantitative measure of diversity is that it is almost bound to produce high values of H (between, say, .7 and .99) if there are more than 2 alleles at a locus, and no single allele is predominant. H cannot be less than .5 unless the most common allele has a frequency of at least .5. If there are more than a few alleles with significant shares of the population, H can hardly be less than .7. For example, if there are 4 alleles with frequencies in the ratio 30:25:25:20, H will be about .75. With 5 alleles in the ratio 25:20:20:20:15, H will be nearly .86. Such a compressed scale of measurement is likely to be inconvenient and potentially misleading. By analogy, suppose that we tried to measure climatic temperature on a new scale under which all temperatures between 0 and 60 degrees Fahrenheit had values between 0 and 90 and all temperatures above 60 degrees F were squeezed into the values between 90 and 100 on the new scale. The new scale would be unlikely to catch on!

Of course, the level of heterozygosity is interesting in itself, and if we want to define diversity by heterozygosity we are free to do so, but this doesn’t necessarily capture everything in our informal concept of diversity.

If this seems a minor technical point, reflect that if H within populations is as high as .86, then diversity between populations, measured in the most common way (Nei’s GST), cannot be more than .14, no matter how different the populations are from each other. (They could even be different species.)

But the measurement of diversity between populations is a bit more complicated than within a single population, so I will continue the analysis in a second post…

Note 1: These terms strictly apply only to genes within the same organism, but now seem also to be widely used with reference to genes in different individuals or populations. In this sense heterozygosity or homozygosity are hypothetical, referring to the probability that individuals would be hetero- or homozygous if their parental gametes were selected at random in the way specified.

Note 2: Strictly, in a finite population this is only true if we allow the same gene to be selected twice, but this does not matter unless the population is very small.

Note 3: Homozygosity = p^2 + q^2, so H = 1 – p^2 – q^2. But q = 1 – p, therefore H = 1 – p^2 – (1 + p^2 – 2p) = 2p(1-p) = 2pq.

References:  
R. Lewontin: Human Diversity, 1982

Posted by David B at [06:13 AM](https://www.gnxp.com/MT2/archives/003952.html) [](http://js-kit.com/api/static/pop_comments?ref=http://gnxp.com&path=/3952)

### Related Posts:

- [Lewontin's Paradox in the 21st
  century](https://www.gnxp.com/WordPress/2021/02/04/lewontins-paradox-in-the-21st-century/) - ["Diversity"](https://www.gnxp.com/WordPress/2006/11/10/diversity/) - [NPR on human
  variation](https://www.gnxp.com/WordPress/2008/02/22/npr-on-human-variation/) - [An ontology of genetic
  diversity](https://www.gnxp.com/WordPress/2012/09/13/an-ontology-of-genetic-diversity/) - [Complex history of archaic
  ancestry](https://www.gnxp.com/WordPress/2021/07/19/complex-history-of-archaic-ancestry/) - [85% of genetic variation is within
  groups...](https://www.gnxp.com/WordPress/2008/02/23/85-of-genetic-variation-is-within-groups/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2005%2F05%2F04%2Fmeasuring-genetic-diversity-lewontin-s-other-fallacy%2F&linkname=Measuring%20Genetic%20Diversity%3A%20Lewontin%E2%80%99s%20Other%20Fallacy "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2005%2F05%2F04%2Fmeasuring-genetic-diversity-lewontin-s-other-fallacy%2F&linkname=Measuring%20Genetic%20Diversity%3A%20Lewontin%E2%80%99s%20Other%20Fallacy "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2005%2F05%2F04%2Fmeasuring-genetic-diversity-lewontin-s-other-fallacy%2F&linkname=Measuring%20Genetic%20Diversity%3A%20Lewontin%E2%80%99s%20Other%20Fallacy "Email")[](https://www.addtoany.com/share)
