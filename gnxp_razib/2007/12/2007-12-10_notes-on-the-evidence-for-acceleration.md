+++
title = "Notes on the evidence"
full_title = "Notes on the evidence for acceleration"
date = "2007-12-10"
upstream_url = "https://www.gnxp.com/WordPress/2007/12/10/notes-on-the-evidence-for-acceleration/"

+++
Source: [here](https://www.gnxp.com/WordPress/2007/12/10/notes-on-the-evidence-for-acceleration/).

Notes on the evidence for acceleration

The long-awaited “acceleration paper” from [John Hawks](http://johnhawks.net/weblog/) and others has finally been [published in PNAS](http://www.pnas.org/cgi/doi/10.1073/pnas.0707650104). The claim is that humans are experiencing a burst of adaptive evolution, and the basic argument is deceptively simple: the recent increase in human population size has led, through an increased number of beneficial new mutations and an increased probability of fixation of said beneficial new mutations, to an acceleration in the rate of adaptive change in our species. The argument is motivated by population genetic theory (see Razib’s summary of that theory [here](http://scienceblogs.com/gnxp/2007/12/accelerated_adaptive_human_evo.php)); here the authors look for genomic evidence.

If you find the theoretical argument convincing (as I do), then it’s easy to accept their major conclusion. However, if you don’t find the theoretical argument convincing, the evidence presented in this paper should not convince you. Below the fold, I discuss why.

Hawks et al. have assembled a dataset of what they call “ascertained selected variants”, and apply standard methods to estimate the ages of these selection events. In their figure 1, you’ll see the age distribution they infer–one that is heavily biased towards the present. The assembly of this database is the key part of their analysis, the one most likely to lead them astray, and it is left woefully underexplored.

The method used to identify selected variants was initially introduced in the context of [a genome-wide scan](http://www.pnas.org/cgi/content/abstract/103/1/135) for natural selection in the HapMap. The statistic is based around the haplotype length surrounding an allele, and they take the top 0.5% of the scores in the distribution of this statistic as selected\[1\]. There are many questions about this method that are relevant to any downstream analyses– for example, what is the false positive rate of the test? The false negative rate? Do these things depend on allele frequency or recombination rate\[2\]? Most importantly, perhaps: **is the [statistical power](https://en.wikipedia.org/wiki/Statistical_power) to detect alleles of different ages identical?** If the test has low power to detect old sweeps and good power to detect recent ones, there you go– an artefactual acceleration. There is little discussion of these parameters in the original paper and less here. Don’t get me wrong– the areas of the genome they identify as selected are almost certainly enriched for true selective events, but how enriched? These questions are perhaps less important in a first-pass scan for selection, but if you’re going to make generalizations about selected sites, they’re essential. The claim in the paper that “demographic causes of extensive LD can be discriminated easily from those caused by adaptive selection” is not demonstrated (and is false)\[3\].

The authors seem to be partially aware of this, writing “this finding \[that few new sweeps are discovered with increased SNP density\] indicates that most events (**defined by the LDD test**) coalescing up to 80,000 years ago have been detected \[my emphasis\]”. In footnote 2, I point to a paper showing that the LDD test biases itself towards identifying sweeps in regions of the genome with a low recombination rate. Is there any reason to think that there’s a similar bias with regards to allele age? In a word: yes. Consider how they’re detecting selection– they look for alleles that are at high frequency (but not fixed) and have extensive LD around them. Since haplotype length decreases with time, **by definition, these are young alleles**. Any old allele with a strong selection coefficient has long gone to fixation and is not detected (or more carefully, there’s much less power to detect it).

The claims about the predictions of the null hypothesis of no acceleration are largely irrelevant given the above. Consider the prediction about the number of adaptive substitutions–that is, the authors claim that the number of selective events in the data predict an absurd number of adaptive substitutions between humans and chimpanzees. Now remember how these variants were identified– they’re in the 99.5th percentile of the distribution of their test statistic. Every distribution has a tail, so if they were to move their threshold a bit further to the right, surely they’d be able to narrow down the number of regions to something consistent with a constant rate. That is, **the entire argument is predicated on perfectly identifying selection in the regions of the parameter space they search**. This is a major assumption, and not one I’m willing to make without strong evidence. They provide none.

\[1\]Note that the information about selection is in haplotype structure, but the test uses unphased genotype data. Their claim that this is actually not a bug, but a feature, because of the computational intensity needed to phase genotype data is unconvincing– the phased haplotypes from the HapMap are [freely available for download](http://hapmap.org/downloads/phasing/?N=D).

\[2\][A recent review](http://www.nature.com/nrg/journal/v8/n11/abs/nrg2187.html) found that the recombination rate in regions the authors identified as being under selection is a full *one-fifth* of the genome-wide average. Unless you have some reason to believe that there’s more selection in regions of the genome with low recombination rates (you don’t), that’s strong evidence that there’s massive ascertainment bias at work here, at least along one dimension in parameter space.

\[3\] The simulations presented in the original paper presenting the method are highly questionable–they do a bootstrap-like resampling scheme from the data, which treats each site as if it were independent. In real data (selected or otherwise), nearby sites have a shared geneology, which is important to capture in any null model. There are widely-used programs [available](http://home.uchicago.edu/~rhudson1/source/mksamples.html) for simulating such samples; these should have been used.

### Related Posts:

- [Adaptive
  acceleration](https://www.gnxp.com/WordPress/2007/12/18/adaptive-acceleration/) - [HIV & cities](https://www.gnxp.com/WordPress/2008/10/03/hiv-cities/) - [More notes on
  acceleration](https://www.gnxp.com/WordPress/2007/12/15/more-notes-on-acceleration/) - [Accelerated adaptive human
  evolution?](https://www.gnxp.com/WordPress/2007/12/10/accelerated-adaptive-human-evolution/) - [How We
  Evolve](https://www.gnxp.com/WordPress/2008/09/09/how-we-evolve/) - [Coalescent
  theory](https://www.gnxp.com/WordPress/2007/12/22/coalescent-theory/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F12%2F10%2Fnotes-on-the-evidence-for-acceleration%2F&linkname=Notes%20on%20the%20evidence%20for%20acceleration "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F12%2F10%2Fnotes-on-the-evidence-for-acceleration%2F&linkname=Notes%20on%20the%20evidence%20for%20acceleration "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F12%2F10%2Fnotes-on-the-evidence-for-acceleration%2F&linkname=Notes%20on%20the%20evidence%20for%20acceleration "Email")[](https://www.addtoany.com/share)
