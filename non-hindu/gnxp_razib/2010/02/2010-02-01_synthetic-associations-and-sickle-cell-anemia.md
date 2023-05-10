+++
title = "\"Synthetic associations\""
full_title = "\"Synthetic associations\" and sickle cell anemia"
date = "2010-02-01"
upstream_url = "https://www.gnxp.com/WordPress/2010/02/01/synthetic-associations-and-sickle-cell-anemia/"

+++
Source: [here](https://www.gnxp.com/WordPress/2010/02/01/synthetic-associations-and-sickle-cell-anemia/).

"Synthetic associations" and sickle cell anemia

[Last week](https://www.gnxp.com/blog/2010/01/bold-prediction-synthetic-associations.php), I made a silly error in describing a problem in the sickle cell anemia example given by [Dickson et al. (2010)](http://www.plosbiology.org/article/info:doi/10.1371/journal.pbio.1000294) as an empirical example of the phenomenon they call “synthetic association”. So allow me to take a mulligan, and re-try this:

The authors performed an association study in African-Americans, using \~200 individuals with sickle cell anemia as cases, and \>7,000 controls. From their description, they simply performed a logistic regression of disease status on common polymorphisms genome-wide. This turned up a large (\~2.5Mb) region surrounding HBB (known to harbour the rare disease-causing mutation) as highly associated with the phenotype. This large region of association stands in contrast, they argue, to the known patterns of linkage disequilibrium in the region, which extends over a few kilobases at most.

This observation, they argue, is an empirical example of how associations due to rare variants can lead to large blocks of associations at common variants. This effect is due to the fact that haplotypes surrounding rare variants are longer and have had little time to be broken up by recombination. Under certain genetic models, this effect of “synthetic associations” is plausible, however, this example is a poor one for making their case.

The reason is that individuals with sickle cell anemia have two chromosomes of African ancestry in the region of HBB, while individuals without sickle cell anemia have approximately the background distribution of European and African chromosomes at the locus–\~20% European and \~80% African. To put it another way, let X_d be number of chromosomes of African ancestry of an individual some distance d from HBB (X can be 0, 1, or 2), and Y be the number of chromosomes of African ancestry of an individual at HBB. In the cases, they’ve conditioned on the fact that Y=2, while in the controls they have not. **P(X_d) != P(X_d \| Y =2)**, so much of their association is likely due simply to differences in ancestry between the cases and controls in the HBB region (recall that admixture linkage disequilibrium in African-Americans [extends for megabases](http://www.nature.com/nrg/journal/v6/n8/full/nrg1657.html)).

More concretely, any SNP near the HBB locus that happened to be fixed for opposite alleles in Europe and Africa would have a whopping 20% allele frequency difference between cases and controls in their analysis, attributable simply to differences in local ancestry. That’s the extreme (and unlikely) situation, but alleles with more modest allele frequency differences between populations will show the same effect.

To some extent, this is their point–the haplotype carrying the causal mutation is long. But the effect in this case is massively exaggerated by admixture, and the presentation of this exaggerated effect is misleading.

### Related Posts:

- [A bold prediction: "synthetic associations"
  are…](https://www.gnxp.com/WordPress/2010/01/26/a-bold-prediction-synthetic-associations-are-not-a-panacea/) - [Defining "synthetic associations"
  down](https://www.gnxp.com/WordPress/2010/02/22/defining-synthetic-associations-down/) - [Synthetic associations and all
  that](https://www.gnxp.com/WordPress/2011/01/18/synthetic-associations-and-all-that/) - [Genetic background & medicine, HIV &
  differences…](https://www.gnxp.com/WordPress/2009/07/21/genetic-background-medicine-hiv-differences-between-blacks-whites/) - [Common versus rare variants,
  again](https://www.gnxp.com/WordPress/2010/04/17/common-versus-rare-variants-again/) - [Common disease-common variant hypothesis taken down a
  notch…](https://www.gnxp.com/WordPress/2010/01/25/common-disease-common-variant-hypothesis-taken-down-a-notch-again/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F02%2F01%2Fsynthetic-associations-and-sickle-cell-anemia%2F&linkname=%22Synthetic%20associations%22%20and%20sickle%20cell%20anemia "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F02%2F01%2Fsynthetic-associations-and-sickle-cell-anemia%2F&linkname=%22Synthetic%20associations%22%20and%20sickle%20cell%20anemia "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F02%2F01%2Fsynthetic-associations-and-sickle-cell-anemia%2F&linkname=%22Synthetic%20associations%22%20and%20sickle%20cell%20anemia "Email")[](https://www.addtoany.com/share)
