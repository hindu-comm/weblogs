+++
title = "Inferring demographic"
full_title = "Inferring demographic history from lower coverage population genomic data sets"
date = "2016-03-09"
upstream_url = "https://www.gnxp.com/WordPress/2016/03/09/inferring-demographic-history-from-lower-coverage-population-genomic-data-sets/"

+++
Source: [here](https://www.gnxp.com/WordPress/2016/03/09/inferring-demographic-history-from-lower-coverage-population-genomic-data-sets/).

Inferring demographic history from lower coverage population genomic data sets

[![ukmss-36009-f0003](https://i0.wp.com/www.unz.com/wp-content/uploads/2016/03/ukmss-36009-f0003.jpg?resize=545%2C600)![ukmss-36009-f0003](https://i0.wp.com/www.unz.com/wp-content/uploads/2016/03/ukmss-36009-f0003.jpg?resize=545%2C600)](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC3154645/)

The above is what I have flippantly referred to as “standard PSMC plot you always see” from the origin [paper](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC3154645/) which debuted the method. Basically PSMC uses the pattern of variation over a good quality whole genome to infer the population history of that individual’s genealogy. All of use unique snowflakes do after all reflect the combined histories of our ancestors.

But in the over 4 years since that paper was published science has moved on. Heng Li, the first author, even has a post up, [Alternatives to PSMC](http://lh3.github.io/2014/07/20/alternatives-to-psmc/), which states that:

> PSMC is okay, but now there are better models and implementations at > least in theory.[MSMC](https://github.com/stschiff/msmc), which has > recently been[published in Nature > Genetics](http://www.nature.com/ng/journal/vaop/ncurrent/full/ng.3015.html), > not only extends PSMC to multiple haplotypes, but also improves PSMC > for a diploid genome. It precalculates transition matrices over long > runs of homozygosity and becomes fast enough to perform whole-genome > inference without binning the input like PSMC. More importantly, for a > diploid genome, MSMC implements the PSMC’ model. It is a better > approximation to the coalescent-with-recombination model by allowing > non-effective recombinations. It is able to give a much better > estimate of the recombination rate. I was lazy when I was working on PSMC. I knew PSMC’ is better, but I skipped that because its derivation is more complicated and because PSMC worked well to infer other parameters. >
> Another important tool > is[dical](http://sourceforge.net/projects/dical/)by Kelly Harris et > al. It also uses better model and has a[time complexity linear in the > number of states](http://arxiv.org/abs/1403.0858). This is a significant advantage over the PSMC implementation whose time complexity is quadratic in the number of states. Dical runs much faster.

Probably the best place to start on perusing software for demographic inference is this [list](http://www.nature.com/nrg/journal/v16/n12/fig_tab/nrg4005_T1.html) from [Methods and models for unravelling human evolutionary history](http://www.nature.com/nrg/journal/v16/n12/full/nrg4005.html).

In an ideal world you’d have awesome data and infinite computational power. But these Markovian coalescent models take a long time to run, and [Stephan Schiffels](https://scholar.google.com/citations?user=6FZPsI4AAAAJ&hl=en) has told me that you probably need 20× [coverage](https://en.wikipedia.org/wiki/Deep_sequencing) to get MSMC to work for you. This is just too high a standard for many population genomic projects, though it is probably necessary for really good phasing using sequence data (conditional on genetic diversity, etc.).

A new paper in *PLOS GENETICS* seems to offer the rest of us hope. [Inferring Population Size History from Large Samples of Genome-Wide Molecular Data – An Approximate Bayesian Computation Approach](http://journals.plos.org/plosgenetics/article?id=10.1371/journal.pgen.1005877):

> Molecular data sampled from extant individuals contains considerable > information about their demographic history. In particular, one > classical question in population genetics is to reconstruct past > population size changes from such data. Relating these changes to > various climatic, geological or anthropogenic events allows > characterizing the main factors driving genetic diversity and can have > major outcomes for conservation. Until recently, mostly very simple > histories, including one or two population size changes, could be > estimated from genetic data. This has changed with the sequencing of > entire genomes in many species, and several methods allow now > inferring complex histories consisting of several tens of population > size changes. However, analyzing entire genomes, while accounting for > recombination, remains a statistical and numerical challenge. These > methods, therefore, can only be applied to small samples with a few > diploid genomes. **We overcome this limitation by using an approximate > estimation approach, where observed genomes are summarized using a > small number of statistics related to allele frequencies and linkage > disequilibrium. In contrast to previous approaches, we show that our > method allows us to reconstruct also the most recent part (the last 100 generations) of the population size history.** As an illustration, we apply it to large samples of whole-genome sequences in four cattle breeds.

So first, they focus on AFS and LD. Second, because the sample size is increased they catch more recent coalescent events, which is critical to obtain power to detect recent demographic events. If you are interested in population genomics, that is pretty essential. Within the paper they admit MSMC’s precision and utility in very specific ranges of time and instances, but suggest that their method’s ability to use larger population sizes makes it practically more useful

Finally, because they use unphased data it seems that you don’t need very whole quality sequences. The cattle in their empirical data set were 13×, which is a reasonable coverage for whole genome results.

The software is called [PopSizeABC](https://forge-dga.jouy.inra.fr/projects/popsizeabc/) and available for [download](https://forge-dga.jouy.inra.fr/projects/popsizeabc/).

### Related Posts:

- [Whole genomes as a window onto the
  past](https://www.gnxp.com/WordPress/2014/06/23/whole-genomes-as-a-window-into-the-past/) - [Two pulses of white admixture in American
  slaves?](https://www.gnxp.com/WordPress/2012/07/09/two-pulses-of-white-admixture-in-american-slaves/) - [The 1000 Genomes
  Paper](https://www.gnxp.com/WordPress/2015/09/30/the-1000-genomes-paper/) - [Endless Tigers Most
  Beautiful](https://www.gnxp.com/WordPress/2017/12/11/endless-tigers-most-beautiful/) - [Inferring demographic
  history](https://www.gnxp.com/WordPress/2009/10/23/inferring-demographic-history/) - [The Simons Genome Diversity
  Project](https://www.gnxp.com/WordPress/2015/10/01/the-simons-genome-diversity-project/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2016%2F03%2F09%2Finferring-demographic-history-from-lower-coverage-population-genomic-data-sets%2F&linkname=Inferring%20demographic%20history%20from%20lower%20coverage%20population%20genomic%20data%20sets "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2016%2F03%2F09%2Finferring-demographic-history-from-lower-coverage-population-genomic-data-sets%2F&linkname=Inferring%20demographic%20history%20from%20lower%20coverage%20population%20genomic%20data%20sets "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2016%2F03%2F09%2Finferring-demographic-history-from-lower-coverage-population-genomic-data-sets%2F&linkname=Inferring%20demographic%20history%20from%20lower%20coverage%20population%20genomic%20data%20sets "Email")[](https://www.addtoany.com/share)
