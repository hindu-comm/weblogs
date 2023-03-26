+++
title = "Buddy can you spare a"
full_title = "Buddy can you spare a selective sweep"
date = "2012-10-21"
upstream_url = "https://www.gnxp.com/WordPress/2012/10/21/buddy-can-you-spare-a-selective-sweep/"

+++
Source: [here](https://www.gnxp.com/WordPress/2012/10/21/buddy-can-you-spare-a-selective-sweep/).

Buddy can you spare a selective sweep

***The Pith:** Natural selection comes in different flavors in its genetic constituents. Some of those constituents are more elusive than others. That makes “reading the label” a non-trivial activity.*

As you may know when you look at patterns of variation in the genome of a given organism you can make various inferences from the nature of these patterns. But the power of those inferences is conditional on the details of the real demographic and evolutionary histories, as well as the assumptions made about the models one which is testing. When delving into the domain of population genomics some of the concepts and models may seem abstruse, but the reality is that such details are the stuff of which evolution is built. A new paper in *PLoS Genetics* may seem excessively esoteric and theoretical, but it speaks to very important processes which shape the evolutionary trajectory of a given population. The paper is titled [Distinguishing between Selective Sweeps from Standing Variation and from a *De Novo* Mutation](http://www.plosgenetics.org/article/info:doi/10.1371/journal.pgen.1003011). Here’s the author summary:

> Considerable effort has been devoted to detecting genes that are under > natural selection, and hundreds of such genes have been identified in > previous studies. Here, we present a method for extending these > studies by inferring parameters, such as selection coefficients and > the time when a selected variant arose. Of particular interest is the > question whether the selective pressure was already present when the > selected variant was first introduced into a population. **In this > case, the variant would be selected right after it originated in the > population, a process we call selection from a *de novo* mutation. We > contrast this with selection from standing variation, where the > selected variant predates the selective pressure.** We present a > method to distinguish these two scenarios, test its accuracy, and > apply it to seven human genes. We find three genes, ADH1B, EDAR, and > LCT, that were presumably selected from a de novo mutation and two > other genes, ASPM and PSCA, which we infer to be under selection from > standing variation.

The dynamic which they refer to seems to be a reframing of the conundrum of detecting [hard sweeps vs. soft sweeps](http://www.ncbi.nlm.nih.gov/pubmed/20178769). In the former you case have a new mutation, so its frequency is \~1/(2N). It is quickly subject to natural selection (though stochastic processes dominate at low frequencies, so probability of extinction is high), and adaptation drives the allele to fixation (or nearly to fixation). In the latter scenario you have a great deal of extant genetic variation, present in numerous different allelic variants. A novel selection pressure reshapes the frequency landscape, but you can not ascribe the genetic shift to only one allele. **It is no surprise that the former is easier to model and detect than the latter**. Much of the evolutionary genomics of the 2000s focused on hard sweeps from *de novo* mutations because they were low hanging fruit. The methods had reasonable power to detect them (as well as many false positives!). But of late many are suspecting that hard sweeps are not the full story, and that much of evolutionary genetic process may be characterized by a combination of hard sweeps, soft sweeps (from standing variation), various forms of [negative selection](https://en.wikipedia.org/wiki/Negative_selection_(natural_selection)), not to mention the plethora of possibilities which abound in the domain of [balancing selection](https://en.wikipedia.org/wiki/Balancing_selection).

Many of the details of the paper may seem overly technical and opaque (and to be fair, I will say here that the figures are somewhat difficult to decrypt, though the subject is not one that lends itself to general clarity), but the major finding is straightforward, and illustrated in figure 4 (I’ve added labels):

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/10/journal.pgen_.1003011.g004.jpg?resize=600%2C237)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/10/journal.pgen_.1003011.g004.jpg?resize=600%2C237)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/10/journal.pgen_.1003011.g004.jpg)

– The y-axis represents the frequency of the selected allele(s) at the initial start of the selection phase

– The x-axis frequency represents a population scaled selection coefficient:*α =*4*Ns.* Recall that *N* is the population size, and *s* is the standard selection coefficient, which measures the relative fitness difference between an individual/gene against the population median. A selection coefficient of 0.10 (10% increased fitness) is strong. One of 0.01 (1%) is modest.

What the results above, derived from simulations using particular parameters relevant to population genetic models and the output statistics (e.g., iHS, EHH, Tajima’s D), show you is that it is easier to differentiate forms of selection when:

– For standing variation the selected variants are present at a higher initial frequency when selection initiates. This is not relevant for *de novo* mutation, where the frequency is very low by definition. Remember that the latter case is actually a subset of the former. If the standing variation model has a parameter which varies in frequency, as the proportion converged upon 1/(2*N*) you just get the *de novo* scenario.

– The stronger the selection event, the greater the power to detect and correctly assign selection for standing variation. This is rather straightforward on first blush. The main exception seems to be in panel e, where increased strength of selection decreases the ability to differentiate the models when the adaptive phase initiates when the initial allele frequency is low. I assume here you have a situation where it is difficult to distinguish the two models, as *de novo* and standing variation are converging. Note that it is easier to assign a hard sweep from a *de novo* mutation when the final frequency (or the frequency you are attempting to detect) is lower. Why? Probably because as the mutation fixes you are removing much of the variant genomic information you need to infer the trajectory of the selected variant (this is true for iHS).

All this may seem abstract. But what you need to do to make some sense of this is to visualize the trajectory of the evolutionary dynamics in temporal and concrete terms. For example, a *de novo* mutation which drives adaptation will rapidly expand in the population over time. Because of this phenomenon there will be a hitchhiking event where the flanking regions of the favored allele also rise in frequency. This generates a extended region of homogeneity in the genome, in direction proportion of the frequency of the [haplotype](https://en.wikipedia.org/wiki/Haplotype). This block of homogeneity eventually decays as genetic recombination breaks apart the physical association of the markers which were found together on the original mutant by chance. This is why the power to detect these events declines over time; the perturbation decays, and the genome reverts to equilibrium. In contrast selection against standing variation is more complex, and therefore more difficult to detect, as it does not produce a clear and distinct signal as often. You may have numerous alleles dispersed across wide regions of the genome amenable to being driven up in frequency by adaptive pressures. This generates a mass action shift in variants, but does not entail the production of wide and distinctive homogeneous blocks across the genome. Rather, you have a larger number of alleles subject to less intensive individual selection. Though some of the same consequences are entailed asin the *de novo* mutation case, the magnitude will be sharply attenuated in any given region of the genome.

Though the conceptual & methodological issues here are of interest in and of themselves (e.g., can you trust the Approximate Bayesian Computation framework to generate simulations which give useful results?), there are also some analyses of real human genes. These are not revolutionary, they’re loci which have been analyzed before. But methods need to be judged against reality at some point, and this is an attempt. The table below shows their results.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/10/gene.jpg?resize=594%2C190)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/10/gene.jpg?resize=594%2C190)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/10/gene.jpg)

Some of these genes should be familiar to you. If not, see the function column. I do want to mention that *EDAR* has been [implicated in hair thickness in East Asians](http://hmg.oxfordjournals.org/content/17/6/835.abstract?etoc). The most amusing aspect of this gene is that it can turn [mice into Asians](https://www.gnxp.com/blog/2008/06/edar-again.php), at least in their hair form. Obviously they focused on single populations. They note in the methods that more populations would introduce demographic complexities into their simulations, and it seems likely that they were already pushing the realistic boundaries of computations which you might want to run routinely in a laboratory. But, this simplification might explain some ambiguity with *ADH1B*, which has been found in West Asia as well (forgoing the straightforward model in all likelihood of one single sweep in East Asia). An important issue then may be the population sensitivity of these methods. One could imagine that selection at a gene is easy to discern in population A, but not population B. One population may shift to a different phenotype through standing variation, while another was subject to a hard sweep from *de novo* mutation. The devil here is in the details. There may not be one narrative to rule them all.

The most important result from this paper was its exploration of the reasonable parameter space over which one can make robust inferences about the specific variety of selection which is operative (or lack thereof). In the near future computational power and a surfeit of empirical data sets will make it so that there will be great temptation to generate reams of results in a blind fashion utilizing off the shelf techniques. But techniques without subtly and human judgment can lead to confusion and falsity. It is useful to know the scenarios where one would expect large numbers of false positives or low statistical power, *a priori*. That way you may save yourself a great deal of time after the fact.

As for soft vs. hard sweeps. This isn’t simply a question of interest and relevance to population geneticists and genomicists. The nature of adaptation is a question of deep importance across evolutionary biology. The balance between these two phenomena are important in characterizing the mode and tempo of evolution. It may be that in fact the ratio varies as a function of the tree of life, so that evolution may operate with slightly different rules contingent upon taxon.

**Citation:** Peter BM, Huerta-Sanchez E, Nielsen R (2012) Distinguishing between Selective Sweeps from Standing Variation and from a De Novo Mutation. PLoS Genet 8(10): e1003011. doi:10.1371/journal.pgen.1003011

### Related Posts:

- [The dam of ancient DNA starts to
  break](https://www.gnxp.com/WordPress/2013/01/21/the-dam-of-ancient-dna-starts-to-break/) - [Pop gen; more robust than you'd
  think](https://www.gnxp.com/WordPress/2016/07/24/pop-gen-more-robust-than-youd-think/) - [A fly's life: adventures in experimental
  evolution](https://www.gnxp.com/WordPress/2010/09/16/a-flys-life-adventures-in-experimental-evolution/) - [Genetic stochasticity &
  environments](https://www.gnxp.com/WordPress/2007/01/22/genetic-stochasticity-environments/) - [Fitness is still a
  bugger!](https://www.gnxp.com/WordPress/2015/02/01/fitness-is-still-a-bugger/) - [Sweeping through a fly's
  genome](https://www.gnxp.com/WordPress/2011/02/23/sweeping-through-a-flys-genome/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F10%2F21%2Fbuddy-can-you-spare-a-selective-sweep%2F&linkname=Buddy%20can%20you%20spare%20a%20selective%20sweep "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F10%2F21%2Fbuddy-can-you-spare-a-selective-sweep%2F&linkname=Buddy%20can%20you%20spare%20a%20selective%20sweep "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F10%2F21%2Fbuddy-can-you-spare-a-selective-sweep%2F&linkname=Buddy%20can%20you%20spare%20a%20selective%20sweep "Email")[](https://www.addtoany.com/share)