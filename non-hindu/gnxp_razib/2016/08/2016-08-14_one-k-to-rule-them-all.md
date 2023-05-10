+++
title = "One K to rule them"
full_title = "One K to rule them all?"
date = "2016-08-14"
upstream_url = "https://www.gnxp.com/WordPress/2016/08/14/one-k-to-rule-them-all/"

+++
Source: [here](https://www.gnxp.com/WordPress/2016/08/14/one-k-to-rule-them-all/).

One K to rule them all?

[![Rosenberg_1048people_993markers](https://i0.wp.com/www.unz.com/wp-content/uploads/2016/08/Rosenberg_1048people_993markers.jpg?resize=220%2C538)![Rosenberg_1048people_993markers](https://i0.wp.com/www.unz.com/wp-content/uploads/2016/08/Rosenberg_1048people_993markers.jpg?resize=220%2C538)](https://web.stanford.edu/group/rosenberglab/papers/popstruct.pdf)A friend recently emailed to ask about the best way to pick a proper “K” value when inferring structure. *K* just being the parameter which defines how many putative ancestral populations you have in your model to explain some data on genetic variation. Obviously some value of *K* are more informative than others of population history.

For example, if you had 100 Swedes and 100 Yoruba Nigerians, to model the population structure you could select *K* = 2 or *K* = 50. The algorithm would produce results in the latter case, but you “know” *a priori* that really *K* = 2 is a really good model of the population history in a straightforward interpretable sense. There’s just not that much more juice to squeeze with many clustering methods out of this sort of data.

But it’s harder when you have population structure in organisms which we don’t know much about aside from the genetic data. How does one “objectively” select a *K*. The most common method is outlined in a 2005 paper, [Detecting the number of clusters of individuals using the software structure: a simulation study](http://onlinelibrary.wiley.com/doi/10.1111/j.1365-294X.2005.02553.x/full):

> The identification of genetically homogeneous groups of individuals is > a long standing issue in population genetics. A recent Bayesian > algorithm implemented in the software structure allows the > identification of such groups. However, the ability of this algorithm > to detect the true number of clusters (K) in a sample of individuals > when patterns of dispersal among populations are not homogeneous has > not been tested. The goal of this study is to carry out such tests, > using various dispersal scenarios from data generated with an > individual-based model. We found that in most cases the estimated ‘log > probability of data’ does not provide a correct estimation of the > number of clusters, K. However, using an ad hoc statistic ΔK based on > the rate of change in the log probability of data between successive K > values, we found that structure accurately detects the uppermost > hierarchical level of structure for the scenarios we tested. As might > be expected, the results are sensitive to the type of genetic marker > used (AFLP vs. microsatellite), the number of loci scored, the number > of populations sampled, and the number of individuals typed in each > sample.

There’s an old saying, “garbage in, garbage out.” The method of *ΔK* is useful as far as it goes, but as inputs it takes the log likelihoods from the Structure program. For Admixture you can look at [cross-validation](http://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-12-246). But these statistics are subject to various assumptions and approximations (in addition, some of the priors within the clustering algorithms are gross simplifications).

This is one reason I was excited about [Estimating the Number of Subpopulations (K) in Structured Populations](http://www.genetics.org/content/203/4/1827):

> A key quantity in the analysis of structured populations is the > parameter K, which describes the number of subpopulations that make up > the total population. Inference of K ideally proceeds via the model > evidence, which is equivalent to the likelihood of the model. However, > the evidence in favor of a particular value of K cannot usually be > computed exactly, and instead programs such as Structure make use of > heuristic estimators to approximate this quantity. We show—using > simulated data sets small enough that the true evidence can be > computed exactly—that these heuristics often fail to estimate the true > evidence and that this can lead to incorrect conclusions about K. Our > proposed solution is to use thermodynamic integration (TI) to estimate > the model evidence. After outlining the TI methodology we demonstrate > the effectiveness of this approach, using a range of simulated data > sets. We find that TI can be used to obtain estimates of the model > evidence that are more accurate and precise than those based on > heuristics. Furthermore, estimates of K based on these values are > found to be more reliable than those based on a suite of model > comparison statistics. Finally, we test our solution in a reanalysis > of a white-footed mouse data set. The TI methodology is implemented > for models both with and without admixture in the software > MavericK1.0.

The [website for MavericK 1.0](http://www.bobverity.com/home/maverick/what-is-maverick/) is informative if you don’t have academic access.

Unfortunately, and probably not surprisingly, this method is **not scalable to genomic data sets.** E.g., they’re looking that 10, 20 or 50 loci. A “modest” human genotyping array will provide you with tens of thousands of loci (SNPs). A “standard” array will provide you with on the order of 500,000 SNPs.

But the conclusion of the paper is worth keeping in mind:

> Finally, it is important to keep in mind that when thinking about > population structure, we should not place too much emphasis on any > single value of K. The simple models used by programs such as > Structure and MavericK are highly idealized cartoons of real life, and > so we cannot expect the results of model-based inference to be a > perfect reflection of true population structure (see discussion in > Waples and Gaggiotti 2006). Thus, while TI can help ensure that our > results are statistically valid conditional on a particular > evolutionary model, it can do nothing to ensure that the evolutionary > model is appropriate for the data. Similarly—in spite of the results > in Table 2—we do not advocate using the model evidence (estimated by > TI or any other method) as a way of choosing the single “best” value > of K. The chief advantage of the evidence in this context is that it > can be used to obtain the complete posterior distribution of K, which > is far more informative than any single point estimate. For example, > by averaging over the distribution of K, weighted by the evidence, we > can obtain estimates of parameters of biological interest (such as the > admixture parameter a) without conditioning on a single population > structure. **Although one value of K may be most likely a posteriori, > in general a range of values will be plausible, and we should > entertain all of these possibilities when drawing conclusions.**

Amen!

### Related Posts:

- [How much informative "structure" is in the HGDP data
  set?](https://www.gnxp.com/WordPress/2014/06/06/how-much-informative-structure-is-in-the-hgdp-data-set/) - [Admixture analysis isn't wrong, it
  misleads](https://www.gnxp.com/WordPress/2016/09/19/admixture-analysis-isnt-wrong-it-misleads/) - ["Multiregionalism vs. Out of
  Africa"](https://www.gnxp.com/WordPress/2010/04/21/multiregionalism-vs-out-of-africa/) - [More genetic structure of human
  populations](https://www.gnxp.com/WordPress/2009/05/16/more-genetic-structure-of-human-populations/) - [PCA remains the swiss-army-knife to explore
  population…](https://www.gnxp.com/WordPress/2017/11/16/pca-remains-the-swiss-army-knife-to-explore-population-structure/) - [Population structure, concrete and
  ineffable](https://www.gnxp.com/WordPress/2013/08/05/population-structure-concrete-and-ineffable/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2016%2F08%2F14%2Fone-k-to-rule-them-all%2F&linkname=One%20K%20to%20rule%20them%20all%3F "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2016%2F08%2F14%2Fone-k-to-rule-them-all%2F&linkname=One%20K%20to%20rule%20them%20all%3F "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2016%2F08%2F14%2Fone-k-to-rule-them-all%2F&linkname=One%20K%20to%20rule%20them%20all%3F "Email")[](https://www.addtoany.com/share)
