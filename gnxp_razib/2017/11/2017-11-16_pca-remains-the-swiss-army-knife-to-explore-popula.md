+++
title = "PCA remains the"
full_title = "PCA remains the swissarmyknife to explore population structure"
date = "2017-11-16"
upstream_url = "https://www.gnxp.com/WordPress/2017/11/16/pca-remains-the-swiss-army-knife-to-explore-population-structure/"

+++
Source: [here](https://www.gnxp.com/WordPress/2017/11/16/pca-remains-the-swiss-army-knife-to-explore-population-structure/).

PCA remains the swiss-army-knife to explore population structure

> genotype-based methods? >
> — Razib Khan (@razibkhan) [November 15, > 2017](https://twitter.com/razibkhan/status/930828965916311553?ref_src=twsrc%5Etfw)

  
I put up a poll without context yesterday to gauge people about what methods they preferred when it came to population genetic structure.\* **PCA came out on top by a plural majority.** More explicitly model-based methods, such as Structure/Admixture, come in right behind them. Curiously, the oldest method, pairwise Fst comparisons (greater Fst means more variance partitioned between the groups), and Treemix, the newest method, have lower proportions of adherence.

Why is PCA so popular? Unlike Treemix or pairwise Fst you don’t have to label populations ahead of time. You just put the variation in there, and the individuals shake out by themselves. Pairwise Fst and Treemix both require you to stipulate which population individuals belong to *a priori*. This means you often end up using PCA or some other method to do a pre-analysis stage. Structure/Admixture model-based methods make you select the number of distinct populations you want to explore, and often assume an underlying model of pulse admixture between populations (Treemix does this too when you have an admixture edge).

PCA is also better at smoking out structure than Structure/Admixture for the same number of markers, and, it’s pretty fast as well. This is why the first thing I do when I get population genetic data where I want to explore structure is do a PCA and look for clusters and outliers. After this pre-analysis stage, I can move onto other methods.

**Further reading:**

- [Population Structure and
  Eigenanalysis](http://journals.plos.org/plosgenetics/article?id=10.1371/journal.pgen.0020190)
  (PCA) - [Inference of Population Structure Using Multilocus Genotype
  Data](http://www.genetics.org/content/155/2/945) )(the original
  “Structure paper”, useful for explaining why this method because so
  popular in comparison to Fst based NJ-trees and PCA) - [Estimating and interpreting *F_(ST)*: The impact of rare
  variants](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3759727/)
  (pairwise *F_(ST)*) - [Inference of Population Splits and Mixtures from Genome-Wide Allele
  Frequency
  Data](http://journals.plos.org/plosgenetics/article?id=10.1371/journal.pgen.1002967)
  (the “Treemix paper”)

\* I stipulated “genotyped-based” methods to set aside some of the new-fangled techniques, which often assume phasing and analysis of haplotypes, such as Chromopainter or explicit local ancestry deconvolution (some local ancestry deconvolution does not require phased haplotypes, but the most popular do).

### Related Posts:

- [Ancestry analysis
  quickstart](https://www.gnxp.com/WordPress/2020/07/17/ancestry-analysis-quickstart/) - [Population Pairwise Fst on 250,000
  SNPs](https://www.gnxp.com/WordPress/2021/10/28/pairwise-fst-on-250000-snps/) - [How to look at population
  structure](https://www.gnxp.com/WordPress/2016/10/03/how-to-look-at-population-structure/) - [How South Asian populations relate to each
  other](https://www.gnxp.com/WordPress/2018/01/25/how-south-asian-populations-relate-to-each-other/) - [Ashkenazi Jews are more European in
  ancestry](https://www.gnxp.com/WordPress/2009/09/04/ashkenazi-jews-are-more-european-in-ancestry/) - [Buddy, can you spare an
  SNP?](https://www.gnxp.com/WordPress/2007/09/20/buddy-can-you-spare-an-snp/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F11%2F16%2Fpca-remains-the-swiss-army-knife-to-explore-population-structure%2F&linkname=PCA%20remains%20the%20swiss-army-knife%20to%20explore%20population%20structure "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F11%2F16%2Fpca-remains-the-swiss-army-knife-to-explore-population-structure%2F&linkname=PCA%20remains%20the%20swiss-army-knife%20to%20explore%20population%20structure "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F11%2F16%2Fpca-remains-the-swiss-army-knife-to-explore-population-structure%2F&linkname=PCA%20remains%20the%20swiss-army-knife%20to%20explore%20population%20structure "Email")[](https://www.addtoany.com/share)
