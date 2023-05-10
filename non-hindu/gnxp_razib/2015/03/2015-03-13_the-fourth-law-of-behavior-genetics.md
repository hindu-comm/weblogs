+++
title = "The Fourth Law of"
full_title = "The Fourth Law of Behavior Genetics"
date = "2015-03-13"
upstream_url = "https://www.gnxp.com/WordPress/2015/03/13/the-fourth-law-of-behavior-genetics/"

+++
Source: [here](https://www.gnxp.com/WordPress/2015/03/13/the-fourth-law-of-behavior-genetics/).

The Fourth Law of Behavior Genetics

![**Figure citation:** Marigorta UM, Navarro A (2013) High Trans-ethnic Replicability of GWAS Results Implies Common Causal Variants. PLoS Genet 9(6): e1003566. doi:10.1371/journal.pgen.1003566](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/03/figure3.jpg?resize=600%2C543)

The above is a figure from [The Fourth Law of Behavior Genetics](https://www.academia.edu/11395963/The_fourth_law_of_behavior_genetics?login=razibk@gmail.com&email_was_taken=true) (ungated), accepted for publication in *Current Directions in Psychological Science*. It’s an excellent overview of the intersection of behavior genetics and genomics over the past 10 years or so. The full story is outlined in the paper, fleshed out by the copious and informative citations which litter the text. The point of the above figure is to show **how robust many inferences from small effect genome-wide associations are.** In particular, there is the standard caveat that a variant which is correlated with disease X in population 1 may not be correlated with disease X in population 2. It actually turns out that **in most cases they are correlated across populations.** Above you see the correlation in effects (odds ratios) between variants and traits between East Asians and Europeans (common variants are also predictive within families).

[The Fourth Law of Behavior Genetics](https://www.academia.edu/11395963/The_fourth_law_of_behavior_genetics?login=razibk@gmail.com&email_was_taken=true) makes no sense unless you know the first three laws outlined by [Eric Turkheimer](https://scholar.google.com/citations?user=-3i13u8AAAAJ):

\* First Law. All human behavioral traits are heritable.

\* Second Law. The effect of being raised in the same family is smaller than the effect of genes.

\* Third Law. A substantial portion of the variation in complex human behavioral traits is not accounted for by the effects of genes or families.

By heritable you simply mean that some of the variation of the trait in the population is explained by variation in genes in the population (you see it in the standard parent-offspring regression). The second law refers to the fact that on many behavior genetic traits the influence of shared family environment in explaining variation can be surprisingly small. The final law points to the reality that a lot of the variation we see in people in outcomes seems pretty much random. It’s labeled non-shared environment, but we should think of it more as a noise factor. These “laws” are robust regularities which you need to take into account when considering the likelihood of any given result. What is the fourth law? It’s pretty straightforward: “A typical human behavioral trait is associated with very many genetic variants, each of which accounts for a very small percentage of the behavioral variability.” To give a concrete example, it looks like the largest effect common variants for behavioral traits explain about 10% the variance as the largest effect variant for complex disease or morphological traits, on the order of 0.01% as opposed to 0.1%.

That’s a mighty small effect. To make sense of the heritabilities estimated using classical methods that means that genetic variation is partitioned across many many genes, on the order of thousands. This is why methods to ascertain loci of effect utilizing small sample sizes (e.g., candidate gene studies) were bound to fail, because they didn’t have the power to detect true results. Rather, many of the hits were simply noise which got published because of low stringency of statistical significance.

One objection then might be that the missing heritability consists of very low frequency (i.e., far less than the 1% threshold used to define common variants in terms of minor allele frequency) mutations which have a larger effect. The authors claim that the research currently does not support that finding. That implies that high coverage whole genome sequencing at reasonable sample sizes won’t make a big difference. Second, there are the results out of the [GCTA](http://www.complextraitgenomics.com/software/gcta/) framework. I won’t go into the details, though check out the [paper](http://www.sciencedirect.com/science/article/pii/S0002929710005987) in AJHG. It’s a powerful way to explore heritabilities using genomic data across unrelated individuals that’s rapidly converging on the heritabilities estimated from classical behavior genetic methods.

Finally, in a similar vein, [Dominance Genetic Variation Contributes Little to the Missing Heritability for Human Complex Traits](http://www.cell.com/ajhg/abstract/S0002-9297(15)00009-9):

> For human complex traits, non-additive genetic variation has been > invoked to explain “missing heritability,” but its discovery is often > neglected in genome-wide association studies. Here we propose a method > of using SNP data to partition and estimate the proportion of > phenotypic variance attributed to additive and dominance genetic > variation at all SNPs (![Math > Eq](https://i0.wp.com/www.cell.com/cms/attachment/2026326785/2045312611/si1.gif?w=640)![Math > Eq](https://i0.wp.com/www.cell.com/cms/attachment/2026326785/2045312611/si1.gif?w=640)and![Math > Eq](https://i0.wp.com/www.cell.com/cms/attachment/2026326785/2045312647/si2.gif?w=640)![Math > Eq](https://i0.wp.com/www.cell.com/cms/attachment/2026326785/2045312647/si2.gif?w=640)) > in unrelated individuals based on an orthogonal model where the > estimate of![Math > Eq](https://i0.wp.com/www.cell.com/cms/attachment/2026326785/2045312611/si1.gif?w=640)![Math > Eq](https://i0.wp.com/www.cell.com/cms/attachment/2026326785/2045312611/si1.gif?w=640)is > independent of that of![Math > Eq](https://i0.wp.com/www.cell.com/cms/attachment/2026326785/2045312647/si2.gif?w=640)![Math > Eq](https://i0.wp.com/www.cell.com/cms/attachment/2026326785/2045312647/si2.gif?w=640). > With this method, we analyzed 79 quantitative traits in 6,715 > unrelated European Americans. The estimate of![Math > Eq](https://i0.wp.com/www.cell.com/cms/attachment/2026326785/2045312647/si2.gif?w=640)![Math > Eq](https://i0.wp.com/www.cell.com/cms/attachment/2026326785/2045312647/si2.gif?w=640)averaged > across all the 79 quantitative traits was 0.03, approximately a fifth > of that for additive variation (average![Math > Eq](https://i0.wp.com/www.cell.com/cms/attachment/2026326785/2045312611/si1.gif?w=640)![Math > Eq](https://i0.wp.com/www.cell.com/cms/attachment/2026326785/2045312611/si1.gif?w=640)= > 0.15). There were a few traits that showed substantial estimates > of![Math > Eq](https://i0.wp.com/www.cell.com/cms/attachment/2026326785/2045312647/si2.gif?w=640)![Math > Eq](https://i0.wp.com/www.cell.com/cms/attachment/2026326785/2045312647/si2.gif?w=640), > none of which were replicated in a larger sample of 11,965 > individuals. We further performed genome-wide association analyses of > the 79 quantitative traits and detected SNPs with genome-wide > significant dominance effects only at the*ABO*locus for factor VIII > and von Willebrand factor. All these results suggest that dominance > variation at common SNPs explains only a small fraction of phenotypic > variation for human complex traits and contributes little to the > missing narrow-sense heritability problem.

### Related Posts:

- [Behavioral genetics getting
  molecular](https://www.gnxp.com/WordPress/2007/09/22/behavioral-genetics-getting-molecular/) - [Political Behavior through the Lens of Behavior
  Genetics](https://www.gnxp.com/WordPress/2008/11/09/political-behavior-through-the-lens-of-behavior-genetics/) - [Gene surfing with David
  Dobbs](https://www.gnxp.com/WordPress/2012/12/18/gene-surfing-with-david-dobbs/) - [The genetics of
  politics](https://www.gnxp.com/WordPress/2008/11/09/the-genetics-of-politics/) - [Friends & genes &
  heritability](https://www.gnxp.com/WordPress/2011/01/19/friends-genes-heritability/) - [The power of false positives in behavior
  genetics](https://www.gnxp.com/WordPress/2011/11/23/the-power-of-false-positives-in-behavior-genetics/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2015%2F03%2F13%2Fthe-fourth-law-of-behavior-genetics%2F&linkname=The%20Fourth%20Law%20of%20Behavior%20Genetics "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2015%2F03%2F13%2Fthe-fourth-law-of-behavior-genetics%2F&linkname=The%20Fourth%20Law%20of%20Behavior%20Genetics "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2015%2F03%2F13%2Fthe-fourth-law-of-behavior-genetics%2F&linkname=The%20Fourth%20Law%20of%20Behavior%20Genetics "Email")[](https://www.addtoany.com/share)
