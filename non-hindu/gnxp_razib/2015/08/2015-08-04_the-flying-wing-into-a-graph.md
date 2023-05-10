+++
title = "The flying wing into a"
full_title = "The flying wing into a graph"
date = "2015-08-04"
upstream_url = "https://www.gnxp.com/WordPress/2015/08/04/the-flying-wing-into-a-graph/"

+++
Source: [here](https://www.gnxp.com/WordPress/2015/08/04/the-flying-wing-into-a-graph/).

The flying wing into a graph

If you are going to use ADMIXTURE, you really need to read the [original paper](http://www.ncbi.nlm.nih.gov/pubmed/19648217), [Fast model-based estimation of ancestry in unrelated individuals](http://www.ncbi.nlm.nih.gov/pubmed/19648217) (it’s not gated, so there’s no excuse). Though the original Jonathan Pritchard paper from 2000, [Inference of Population Structure Using Multilocus Genotype Data](http://www.genetics.org/content/155/2/945.full), is probably sufficient. Unfortunatey there’s a problem with these model-based barplots: **people have a real hard time not reifying them excessively.** Let’s call it “Plato’s revenge.” But really Plato only elaborated what’s obviously a pretty standard-issue cognitive tick: we like to think in absolute categories. This is most of the problem with “does race exist” discussions; you always need to move past the idea of Platonic constructions, which are by necessity social.

That’s what’s nice about [PCA](https://en.wikipedia.org/wiki/Principal_component_analysis). It’s a visual representation of the underlying variation in the data, and the clusters are not pre-specified. Unfortunately fixing the parameter as K = 5 magically means for most people that there are actually 5 real populations. And “most people” even includes a lot of geneticists.

So I’m going to do an experiment, and move away from model-based clustering, and use [TreeMix](http://journals.plos.org/plosgenetics/article?id=10.1371/journal.pgen.1002967) to explore data. This of course behooves us to make sure we read the [original paper](http://journals.plos.org/plosgenetics/article?id=10.1371/journal.pgen.1002967), [Inference of Population Splits and Mixtures from Genome-Wide Allele Frequency Data](http://journals.plos.org/plosgenetics/article?id=10.1371/journal.pgen.1002967). I have done so, and three elements jump out at me:

– “This Gaussian model was first introduced by Cavalli-Sforza and Edwards \[1\], and the motivation for this model is outlined in Nicholson et al. \[33\], **if the amount of genetic drift between the two populations is small** (at most on a timescale of the same order as the effective population size), then the diffusion approximation to a Wright-Fisher model…”

– “We do not model the boundaries of the allele frequencies at zero and one, nor do we consider new mutations. **This means that this model will be most accurate for alleles that were at intermediate frequency in the ancestral population.**”

– “The contribution of each parental population is weighted; **if we assume admixture occurs in a single generation….**”

What I took from the above. First, beware of highly drifted populations (they will probably generate ‘long branches’). Second, probably best to do minor allele frequency filters so that get the intermediate proportions (the common one of 0.05 would probably suffice). Finally, a lot of admixture isn’t a single event. So that might introduce some distortions in the tree (or at least representations which mislead naive humans).

This first post is something of a trial. I’m not looking to answer any questions, just exploring. I have a data set (unfortunately some of the data is not public, so I won’t be posting the Dropbox link this time) which is mostly skewed toward Northern Europeans. Using PCA I removed individuals which were outliers and generated some reasonable clusters around the centroids of particular nations (i.e., the national clusters are those with individual’s whose ancestors were all from a given nation, to the best of their knowledge).

The clusters are:

– E_Africa (HapMap Masai, with some outlier removal)  
– England (I selected individuals who were distant from the Irish, without being German)  
– Finland  
– Germany (I selected individuals which were basically North German; the Netherlands to Saxony)  
– Ireland  
– Italy (these individuals are Southern Italian; from Roman down to the Naples, but excluding Sicily)  
– Mbuti_Pygmies (HGDP)  
– Mozabite (HGDP, some outlier removal)  
– N_Amerindian (HGDP, Pima and Maya; some outlier removal)  
– S_Amerindian (HGDP, Surui and Kariatana; some outlier removal)  
– NE_Asia (HapMap and private data for Japanese and Koreans)  
– N_India (HapMap and 1000 Genomes Gujarati and Punjabis)  
– N_WestAsia (Armenians and Turks)  
– Papuan (HGDP)  
– Poland (Removed all Jews from this data)  
– Scotland (tried to remove individuals too close to Irish and English; this was not easy)  
– SE_Asia (1000 Genomes Dai and Vietnamese)  
– S_India (1000 Genomes Tamil and Telugu)  
– Spain (1000 Genomes and private data)  
– Sweden  
– S_WestAsia (private data, Saudis and Kuwaitis, pruned from those with recent African ancestry)  
– W_Africa (1000 Genomes Yoruba and Esan)  
– Yakut (HGDP)

The merged data set has 290,000 SNPs. Its missingness is 0.25% (0.0025). But there are over 5,000 individuals in the data set, and that could hide some major biases in the distribution of missingeness (e.g., the small number of HGDP Papuans could have a lot of these). So I decided to remove all SNPs that had any missingness in the data. That leaves us with \~40,000 markers. That means all 40,000 of these markers are present as calls in all 5,000 individuals in the data. For PCA 40,000 is actually pretty good, so here are the first 6….  
  
[![pc1pc2](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/pc1pc2-300x258.png?resize=300%2C258)![pc1pc2](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/pc1pc2-300x258.png?resize=300%2C258)](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/pc1pc2.png)[![PC3PC4](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/PC3PC4-300x258.png?resize=300%2C258)![PC3PC4](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/PC3PC4-300x258.png?resize=300%2C258)](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/PC3PC4.png)[![PC5PC6](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/PC5PC6-300x258.png?resize=300%2C258)![PC5PC6](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/PC5PC6-300x258.png?resize=300%2C258)](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/PC5PC6.png)The magnitude of the dimensions are: 245, 142, 34, 27, 16, and 12. The first two, which form the “wing” shape which we’re all familiar with, represent Africa vs. everyone else, and then western vs. eastern Eurasia. These are not set in stone. Remember, what PCA does is yank out independent dimensions which explain the variation in the data. If you overload the data with a particular type of variation then it could change the rank order. Or, if you throw in a very inbred group then their component is going to be very salient. **These methods depend on you not being dumb about how to interpret the data that you yourself are putting in their.** Unfortunately, it’s easy to be dumb when you don’t have much foreknowledge about the data…that’s why you are doing the analysis!

Since you can’t read the PCA plots, you should click on them. They’ll pop out into something more readable. PC 3 separates out Eurasia north to south. This is a much smaller dimension than west to east. I think that fits intuition. The fourth PC separates the Amerindian groups. Really it’s a Surui vs. non-Surui axis. I really like PC 5 and PC 6, because they show the different European clusters more visibly. The issue is that there’s very little genetic variation in Europe when judged on a world-wide scale. But the lower components are starting to capture it. I’m not going to lie, ggplot’s default color scheme is hella confusing. I’ll tell you that the two populations away from the rest are Indians, with North Indians closer to Europeans than South Indians. And way up to the top right are Papuans. One way I like to think of these sorts of patterns post hoc is that the Indians are pointing to a “ghost population.” They’re not Papuans, but they have some distant affinity to Papuans….

Next I decided to run TreeMix. First with the full 290,000 SNP data set. Then the 40,000 which are 0% missingeness. I ran them each 10 times and outputted them. I set them for 5 migrations. I’ll leave them without comment, except this: **the problem I have with TreeMix is that I’m reassured when I see a migration edge that I’m expecting, but don’t know what to make of those which are surprising**. The reason is that the algorithm can’t lie, but it can only work with the data and assumptions that go into it. When Joe Pickrell first came out with his TreeMix results there was a weird arrow going from the Amerindians to the Europeans. No one really knew what to make of this, though it wasn’t entirely surprising (something like this shows up in ADMIXTURE plots well, and I saw it in Noah Rosenberg’s microsatellite STRUCTURE work as far back as 2005). After the fact we now can make sense of it. TreeMix was showing us the impact of the “Ancestral North Eurasians” as best it could. The Amerindians of the New World have the highest proportion of this ancestry, and the people of Northern Europe some of the highest fractions in the Old World. So it drew a migration edge from the former to the latter. When you put the Mal’ta (or Yamnaya) data into TreeMix that “spurious edge” disappears….



[![FinalPool300KOut.9](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.9-300x250.jpg?resize=300%2C250)![FinalPool300KOut.9](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.9-300x250.jpg?resize=300%2C250)](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.9.jpg) [![FinalPool300KOut.10](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.10-300x250.jpg?resize=300%2C250)![FinalPool300KOut.10](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.10-300x250.jpg?resize=300%2C250)](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.10.jpg) [![FinalPool300KOut.5](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.5-300x250.jpg?resize=300%2C250)![FinalPool300KOut.5](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.5-300x250.jpg?resize=300%2C250)](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.5.jpg) [![FinalPool300KOut.6](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.6-300x250.jpg?resize=300%2C250)![FinalPool300KOut.6](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.6-300x250.jpg?resize=300%2C250)](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.6.jpg) [![FinalPool300KOut.7](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.7-300x250.jpg?resize=300%2C250)![FinalPool300KOut.7](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.7-300x250.jpg?resize=300%2C250)](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.7.jpg) [![FinalPool300KOut.8](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.8-300x250.jpg?resize=300%2C250)![FinalPool300KOut.8](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.8-300x250.jpg?resize=300%2C250)](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.8.jpg) [![FinalPool300KOut.1](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.1-300x250.jpg?resize=300%2C250)![FinalPool300KOut.1](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.1-300x250.jpg?resize=300%2C250)](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.1.jpg) [![FinalPool300KOut.2](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.2-300x250.jpg?resize=300%2C250)![FinalPool300KOut.2](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.2-300x250.jpg?resize=300%2C250)](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.2.jpg) [![FinalPool300KOut.3](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.3-300x250.jpg?resize=300%2C250)![FinalPool300KOut.3](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.3-300x250.jpg?resize=300%2C250)](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.3.jpg) [![FinalPool300KOut.4](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.4-300x250.jpg?resize=300%2C250)![FinalPool300KOut.4](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.4-300x250.jpg?resize=300%2C250)](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPool300KOut.4.jpg)  
**Here’s the 40,000 marker TreeMix output**

[![FinalPoolGenoM5Out.8](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.8-300x250.jpg?resize=300%2C250)![FinalPoolGenoM5Out.8](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.8-300x250.jpg?resize=300%2C250)](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.8.jpg)

[![FinalPoolGenoM5Out.9](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.9-300x250.jpg?resize=300%2C250)![FinalPoolGenoM5Out.9](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.9-300x250.jpg?resize=300%2C250)](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.9.jpg)

[![FinalPoolGenoM5Out.10](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.10-300x250.jpg?resize=300%2C250)![FinalPoolGenoM5Out.10](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.10-300x250.jpg?resize=300%2C250)](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.10.jpg)

[![FinalPoolGenoM5Out.5](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.5-300x250.jpg?resize=300%2C250)![FinalPoolGenoM5Out.5](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.5-300x250.jpg?resize=300%2C250)](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.5.jpg)

[![FinalPoolGenoM5Out.6](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.6-300x250.jpg?resize=300%2C250)![FinalPoolGenoM5Out.6](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.6-300x250.jpg?resize=300%2C250)](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.6.jpg)

[![FinalPoolGenoM5Out.7](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.7-300x250.jpg?resize=300%2C250)![FinalPoolGenoM5Out.7](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.7-300x250.jpg?resize=300%2C250)](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.7.jpg)[![FinalPoolGenoM5Out.2](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.2-300x250.jpg?resize=300%2C250)![FinalPoolGenoM5Out.2](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.2-300x250.jpg?resize=300%2C250)](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.2.jpg)

[![FinalPoolGenoM5Out.3](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.3-300x250.jpg?resize=300%2C250)![FinalPoolGenoM5Out.3](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.3-300x250.jpg?resize=300%2C250)](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.3.jpg)

[![FinalPoolGenoM5Out.4](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.4-300x250.jpg?resize=300%2C250)![FinalPoolGenoM5Out.4](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.4-300x250.jpg?resize=300%2C250)](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.4.jpg)

[![FinalPoolGenoM5Out.1](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.1-300x250.jpg?resize=300%2C250)![FinalPoolGenoM5Out.1](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.1-300x250.jpg?resize=300%2C250)](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/08/FinalPoolGenoM5Out.1.jpg)

### Related Posts:

- [PCA remains the swiss-army-knife to explore
  population…](https://www.gnxp.com/WordPress/2017/11/16/pca-remains-the-swiss-army-knife-to-explore-population-structure/) - [Genetic structure
  matters](https://www.gnxp.com/WordPress/2016/08/14/genetic-structure-matters/) - [Population structure, concrete and
  ineffable](https://www.gnxp.com/WordPress/2013/08/05/population-structure-concrete-and-ineffable/) - [Plato, what is he good
  for?](https://www.gnxp.com/WordPress/2007/07/02/plato-what-is-he-good-for/) - [There would have been a Plato without
  Plato](https://www.gnxp.com/WordPress/2011/08/18/there-would-have-been-a-plato-without-plato/) - [CLUMPAK, for model-based population structure
  analysis](https://www.gnxp.com/WordPress/2015/08/21/clumpak-for-model-based-population-structure-analysis/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2015%2F08%2F04%2Fthe-flying-wing-into-a-graph%2F&linkname=The%20flying%20wing%20into%20a%20graph "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2015%2F08%2F04%2Fthe-flying-wing-into-a-graph%2F&linkname=The%20flying%20wing%20into%20a%20graph "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2015%2F08%2F04%2Fthe-flying-wing-into-a-graph%2F&linkname=The%20flying%20wing%20into%20a%20graph "Email")[](https://www.addtoany.com/share)
