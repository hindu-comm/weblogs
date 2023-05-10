+++
title = "Buddy, can you spare a"
full_title = "Buddy, can you spare a genetic distance statistic?"
date = "2013-07-20"
upstream_url = "https://www.gnxp.com/WordPress/2013/07/20/buddy-can-you-spare-a-genetic-distance-statistic/"

+++
Source: [here](https://www.gnxp.com/WordPress/2013/07/20/buddy-can-you-spare-a-genetic-distance-statistic/).

Buddy, can you spare a genetic distance statistic?

![Sewall Wright  
**Credit:** University of Wisconsin, Madison](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/07/150px-Sewall_Wright.jpg?resize=150%2C183 "150px-Sewall_Wright")

You have probably heard or read that **most genetic variation is **within** races, not *between* races.** This assertion has led, in my opinion, to unwarranted inferences. Often bracketed under [“Lewontin’s Fallacy”](https://en.wikipedia.org/wiki/Human_Genetic_Diversity:_Lewontin's_Fallacy#Lewontin.27s_argument), the basic intuition is that if most variation is within races, then races as a taxonomic unit are without utility or substantive basis. This is disputable. In plain English, though most genetic variation may be within races (i.e., not diagnostic of racial identity), the variation **across** races is quite systematic because that variation reflects deep population history. In this way of thinking population or racial substructure are simply reflections of the tips of the [tree](https://en.wikipedia.org/wiki/Phylogenetic_tree)which has been shaped by history.

**But these discussions are ultimately predicated upon a *statistic*,** [F_(ST)](https://en.wikipedia.org/wiki/Fixation_index#FST_in_humans). F_(ST) is generally considered one of the fixation indices pioneered by the American evolutionary geneticist [Sewall Wright](https://en.wikipedia.org/wiki/Sewall_Wright#Population_genetics). What Wright’s F_(ST) aims to capture is the relative amount of genetic variance which is due population substructure. In regards to human races out of the total genetic variation \~15% of it can be inferred simply by looking at population substructure (F_(ST) \~0.15), with the balance not being due to population structure. But this is an *average* value. At [rs1426654](http://hgdp.uchicago.edu/cgi-bin/alfreqs.cgi?pos=46213776&chr=chr15&rs=rs1426654&imp=true) in *SLC24A5* when comparing Europeans and Africans almost all of the variation is **between** the populations, because the allele frequencies are disjoint. But what if I told you that Wright’sF_(ST) is quite a bit woollier than you might think?

![**Citation:** Patterson, Nick, Alkes L. Price, and David Reich. “Population structure and eigenanalysis.” PLoS genetics 2.12 (2006): e190.](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/07/GeneticDistance-300x211.png?resize=300%2C211 "GeneticDistance")

The issue here is that **measuring genetic distance is not like measuring acceleration or length**. Acceleration is a clearly defined phenomena with a first order relationship to material entities, while length is a physical property of concrete objects. What population genetics is attempting to do is formalize and render abstract phenomena whose ultimate basis are not constrained by human preconceptions or easily amenable to intuitions, and may be nested within other abstruse constructions. In most cases what “genetic distance” really is is a way for humans to be able to conceptualize easily patterns of variation which are the outcome of complex historical processes. Often the interest of population geneticists is not in taxonomy as such, but the historical events which can be inferred by the classifications.

Wright’s F_(ST)is useful because it gives you a number. And, due to its age it is also easy to compute using single marker data, as was prevalent before the molecular revolution of the 1960s. Today I much prefer visualizations of genetic relationships such as can be found in principal component analysis, or the ubiquitous bar plots of explicit population model clustering (e.g.,*Admixture*or*Structure*). But if you are submitting a paper for peer review you may still be asked to provideF_(ST), meaning that this is still a relevant statistic.\*

This is why a new preprint in *Genome Research* is very important for scientists working in this area, [Estimating and interpreting F_(ST): the impact of rare variants](http://genome.cshlp.org/content/early/2013/07/16/gr.154831.113.abstract.html). I had a short conversation with [Gaurav Bhatia, the first author](http://www.hsph.harvard.edu/alkes-price/ashg-talks/), at ASHG 2012, so I was waiting for this preprint to come out. In the text **the authors provide explicit guidelines for ‘best practices’ on using and computing F_(ST).** This is needed. I myself have shied away from using F_(ST)much because I have seen that different methods give different results. Yes, qualitatively coherent, **but it is not reassuring as F_(ST) purports to a precise quantity.**

The problem seems to be that F_(ST)emerged in an earlier pre-genomic era, and with genome-wide dense SNP data biases, distortions, and inconsistencies across different F_(ST) frameworks are starting to emerge. As an empirical result the authors point out that [a recent paper](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC3303124/) has claimed that F_(ST) \< 0.10 for human populations using 1000 Genomes data. This is lower than the values inferred from HapMap3. Why? One possibility is that the 1000Genomes data is enriched for rare variants, which are likely to have emerged after the divergence of the populations from a common ancestor. This is problematic because many variants of F_(ST) are predicated on a divergence from a common ancestor, and so should be evaluating shared variation (the authors observe that highly heterozygous alleles with a bias toward private alleles can paradoxically result in very low F_(ST)). Because of the importance of taking into account shared and diverged population history the authors recommend ascertaining the SNPs in an outgroup, if possible (if not, then make the ascertainment strategy explicit and sample different genomics regions to get a sense of possible biases or distortions).

Additionally, there are problems with unequal sample sizes, as well as using pooled SNPs so as to compute individual distance values and taking the average of the results. They term the latter “average of ratios” (the ratio between the variance components), and conclude that this will underestimate the F_(ST,)and that that is what occurred in the 1000 Genomes paper above. Rather, they recommend that taking the ratio of the average variances across the SNPs are less biased. This is where the pre-genomic origins of F_(ST) show, as this would not be an issue in an age of few markers. But with the copious data from the 1000 Genomes these distortions can be amplified and result in genuine confusions about the biological history of a population.

Finally, they make explicit recommendations as to the form of F_(ST) to use:

Hudson estimator \>Weir and Cockerham \> Nei

All this goes to show that even in established science it is important check your premises. Too oftenF_(ST)is simply a black-box, one of the elements which you have to check off. But it is a tool which should be used with subtle understanding.

**Addendum:** [Alkes Prices’ software](http://www.hsph.harvard.edu/alkes-price/software/) page has some great resoruces. And there’s a new version of *Eigensoft*! I know what I’m going to do this weekend….

**Citation:** *Genome Research*, Estimating and Interpreting FST: the Impact of Rare  
Variants, Gaurav Bhatia1, Nick Patterson2, Sriram Sankararaman, Alkes L. Price. doi:10.1101/gr.154831.113  
\* In F_(ST) is still useful in many cases as part of a broader population genetic toolkit.

### Related Posts:

- [Richard Dawkins accepts the usefulness of
  race](https://www.gnxp.com/WordPress/2012/05/04/richard-dawkins-accepts-the-usefulness-of-race/) - [Origin of the
  races](https://www.gnxp.com/WordPress/2007/09/08/origin-of-the-races/) - [Race: maybe it's
  agriculture](https://www.gnxp.com/WordPress/2012/03/02/race-maybe-its-agriculture/) - [A genetic test to tell you what "population" you
  are?](https://www.gnxp.com/WordPress/2008/12/15/a-genetic-test-to-tell-you-what-population-you-are/) - [Race: A Social Destruction of a Biological
  Concept](https://www.gnxp.com/WordPress/2010/01/28/race-a-social-destruction-of-a-biological-concept/) - [No cheat left
  behind](https://www.gnxp.com/WordPress/2006/03/26/no-cheat-left-behind/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F07%2F20%2Fbuddy-can-you-spare-a-genetic-distance-statistic%2F&linkname=Buddy%2C%20can%20you%20spare%20a%20genetic%20distance%20statistic%3F "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F07%2F20%2Fbuddy-can-you-spare-a-genetic-distance-statistic%2F&linkname=Buddy%2C%20can%20you%20spare%20a%20genetic%20distance%20statistic%3F "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F07%2F20%2Fbuddy-can-you-spare-a-genetic-distance-statistic%2F&linkname=Buddy%2C%20can%20you%20spare%20a%20genetic%20distance%20statistic%3F "Email")[](https://www.addtoany.com/share)
