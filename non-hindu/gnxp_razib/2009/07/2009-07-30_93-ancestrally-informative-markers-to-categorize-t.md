+++
title = "93 ancestrally"
full_title = "93 ancestrally informative markers to categorize them all"
date = "2009-07-30"
upstream_url = "https://www.gnxp.com/WordPress/2009/07/30/93-ancestrally-informative-markers-to-categorize-them-all/"

+++
Source: [here](https://www.gnxp.com/WordPress/2009/07/30/93-ancestrally-informative-markers-to-categorize-them-all/).

93 ancestrally informative markers to categorize them all

[An ancestry informative marker set for determining continental origin: validation  
and extension using human genome diversity panels](http://www.biomedcentral.com/1471-2156/10/39):

> **Results**  
> In this study, genotypes from Human Genome Diversity Panel populations > were used to further evaluate a 93 SNP AIM panel, a subset of the 128 > AIMS set, for distinguishing continental origins. Using both > model-based and relatively model-independent methods, we here confirm > the ability of this AIM set to distinguish diverse population groups > that were not previously evaluated. This study included multiple > population groups from Oceana, South Asia, East Asia, Sub-Saharan > Africa, North and South America, and Europe. In addition, the 93 AIM > set provides population substructure information that can, for > example, distinguish Arab and Ashkenazi from Northern European > population groups and Pygmy from other Sub-Saharan African population > groups.  
> **Conclusion**  
> These data provide additional support for using the 93 AIM set to > efficiently identify continental subject groups for genetic studies, > to identify study population outliers, and to control for admixture in > association studies.

AIM = ancestrally informative markers. You are probably aware of the fact that most variance on any given gene is found within populations, and not between. Therefore, the chestnut of conventional wisdom that 85% of variance is within races, and 15% is between races. But not all genes are created equal. For example, on [SLC24A5](https://en.wikipedia.org/wiki/SLC24A5) almost all the variance among Europeans and Africans is between the races; if you know the state of *SLC24A5*, then you can establish with a high degree of certainty whether the person is African or European in origin if these are your only two options (Asians and Africans cluster on *SLC245*, though if you find the “European” variant you can be assured of an individual’s provenance, at least partially, from North Africa or Western Eurasia). The logic then is that a small number of highly population informative markers (i.e., those markers which are good at distinguishing between populations) can allow one to discern population stratification within medical studies. If, for example, you are looking for disease susceptibility alleles and different populations have different disease susceptibilities, then naturally those alleles which are correlated with particular populations will show up on an association (though the “causal” connection is population identity in terms of both disease and allele). This is why Ashkenazi Jewish genetics are of more than genealogical interest, if Jews have a unique suite of genetic diseases (this is true) then it might best to exclude them from studies using other Europeans. Sniffing out of this sort of “cryptic” structure isn’t that hard, in the early 2000s Neil Risch et al. pointed out that as [few as 20 AIMs may be sufficient](http://genomebiology.com/2002/3/7/comment/2007) to distinguish continental populations.  
This study uses 93 markers to distinguish [HGDP](https://en.wikipedia.org/wiki/Human_Genome_Diversity_Project#Current_status) groups, along with a few other supplemental populations which were not well represented in HGDP sample. For example, since the government of India was rather restrictive of genetic research when the HGDP population samples were being collected the “South Asians” are generally from Pakistan. A [study which surveyed Indian Americans](http://www.plosgenetics.org/article/info:doi/10.1371/journal.pgen.0020215) (that is, Americans whose family are of Indian origin) provided the data to “plug” that whole. Clusters were displayed through two primary methods, [Structure](http://pritch.bsd.uchicago.edu/software.html) and principal component analysis charts.

  
![1471-2156-10-3932struct.png](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/1471-2156-10-3932struct.png?resize=324%2C872)![1471-2156-10-3932struct.png](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/1471-2156-10-3932struct.png?resize=324%2C872)  
(I’ve reformatted this figure a bit)  
![1471-2156-10-3935pc.png](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/1471-2156-10-3935pc.png?resize=500%2C581)![1471-2156-10-3935pc.png](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/1471-2156-10-3935pc.png?resize=500%2C581)  
These figures aren’t too special, you’ve seen better. But, **instead of tens thousands of SNPs these are just 93 markers.** So the bang-for-the-buck is rather big. Both the Structure and PC charts aligned with intuition and previous findings. In fact they compared their results to those of 3,500 random SNPs (remember, *randomly* selected markers will show a lot less between population variance, so less bang-for-the-buck).  
![1471-2156-10-3933rsquar.png](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/1471-2156-10-3933rsquar.png?resize=500%2C571)![1471-2156-10-3933rsquar.png](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/1471-2156-10-3933rsquar.png?resize=500%2C571)  
The r² is the square of the correlation, and describes how much of the variation of Y can be explained by variation of X. As you can see the 93 AIMs don’t do too badly when judged against 3,500 random markers. This check is necessary because local adaptation can give a distorted impression of total genome content if selection is driving allele frequencies toward convergence among disparate populations. Consider if *LCT*, the locus which controls lactase persistence, were used. It seems as if there is a fair amount of ecologically driven variance at odds with the rest of the genome on some genes which exhibit a lot of between population variance, so one must be aware of this problem.  
But there’s a big exception: **the 93 AIMs don’t seem too good at classifying the South Asians as a distinct group when set against more markers.** In other words, these 93 AIMs don’t seem too “ancestrally informative” when it comes to brown folk. At K = 5 (five putative ancestral populations) the admixture of South Asians is rather evident in the Structure chart. They note that using a 85% cut-off for ancestry within a “South Asian” cluster results in in only 25% of South Asians in their own category (at K = 6). Dropping to 50% increases the proportion to 60%. South Asians should of course be excluded from studies which are majority European because there are clear genetic differences. I just assume that part of the issue is that these ancestrally informative markers were selected in the context of a much larger literature which relied on Europeans, African Americans and East Asians (combined with the fact that South Asians are closer to Europeans & Middle Easterners than other population clusters, but still distinctive).  
**Cite:** BMC Genetics 2009, 10:39 doi:10.1186/1471-2156-10-39  
**Related:** [Genetic maps](https://www.google.com/cse?cx=017254414699180528062:uyrcvn__yd0&q=genetic+map+site:http://scienceblogs.com/gnxp/&sa=Search).

### Related Posts:

- [Genetic Map of East
  Asia](https://www.gnxp.com/WordPress/2008/12/07/genetic-map-of-east-asia/) - [Admixture analysis isn't wrong, it
  misleads](https://www.gnxp.com/WordPress/2016/09/19/admixture-analysis-isnt-wrong-it-misleads/) - [More genetic structure of human
  populations](https://www.gnxp.com/WordPress/2009/05/16/more-genetic-structure-of-human-populations/) - [More markers, or more
  populations?](https://www.gnxp.com/WordPress/2010/07/02/more-markers-or-more-populations/) - [From genome-wide data to insights into human
  population…](https://www.gnxp.com/WordPress/2009/02/14/from-genome-wide-data-to-insights-into-human-population-structure/) - [Single markers tell you only a bit about individual
  ancestry](https://www.gnxp.com/WordPress/2015/01/22/single-markers-tell-you-only-a-bit-about-individual-ancestry/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F07%2F30%2F93-ancestrally-informative-markers-to-categorize-them-all%2F&linkname=93%20ancestrally%20informative%20markers%20to%20categorize%20them%20all "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F07%2F30%2F93-ancestrally-informative-markers-to-categorize-them-all%2F&linkname=93%20ancestrally%20informative%20markers%20to%20categorize%20them%20all "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F07%2F30%2F93-ancestrally-informative-markers-to-categorize-them-all%2F&linkname=93%20ancestrally%20informative%20markers%20to%20categorize%20them%20all "Email")[](https://www.addtoany.com/share)
