+++
title = "The parallel lives of"
full_title = "The parallel lives of threespine stickleback"
date = "2010-03-01"
upstream_url = "https://www.gnxp.com/WordPress/2010/03/01/the-parallel-lives-of-threespine-stickleback/"

+++
Source: [here](https://www.gnxp.com/WordPress/2010/03/01/the-parallel-lives-of-threespine-stickleback/).

The parallel lives of threespine stickleback

![20081775.JPG](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/20081775.JPG?resize=200%2C69)![20081775.JPG](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/20081775.JPG?resize=200%2C69)A few days ago I pointed to a [paper](http://www.cell.com/current-biology/fulltext/S0960-9822(09)02070-3) which suggests the possible utility of looking at selection on standing genetic variation on quantitative traits to get a sense of the role of adaptation in the human genome. We humans like to think we’re a complex species, so I see no *a priori* reason why our evolutionary history should be easily reducible to spare compact dynamics. Granted, we can start with the assumption that on the order of 50,000 years before the present there was a rapid demographic expansion of anatomically modern humans out of the continent of Africa. This story is simple, and is evident in most of the genetic and genomic analyses of the past generation, as well as more traditional cladistic analyses utilizing morphological characters.  
But evolutionary process did not stop 50,000 years ago. The detailed balance of demographic, stochastic and selective parameters in shaping human evolution in a general and regionally specific sense are still to be worked out. The questions and certainly the answers are liable to be rather more complex, and possibly muddled, than those initially posed in the 1980s and later in relation to the question of humanity’s African origins.  
The rise of the [HapMap](https://en.wikipedia.org/wiki/International_HapMap_Project) and extension of the [HGDP](https://en.wikipedia.org/wiki/HGDP) data set are the first steps toward a crisper understanding. But other animals may play a role in refining our expectations as to the balance of dynamics. The domestic dog for example is a geographically differentiated species of a recent origin subject to strong selective pressures. But let us extend our gaze beyond the mammals.  
A new paper focusing on threespine stickleback has come out which shows the power of a synthetic framework in understanding evolutionary dynamics; the different parameters, as well as variation spatially and over time. [Population Genomics of Parallel Adaptation in Threespine Stickleback using Sequenced RAD Tags](http://www.plosgenetics.org/article/info:doi/10.1371/journal.pgen.1000862):

> Next-generation sequencing technology provides novel opportunities for > gathering genome-scale sequence data in natural populations, laying > the empirical foundation for the evolving field of population > genomics. Here we conducted a genome scan of nucleotide diversity and > differentiation in natural populations of threespine stickleback > (Gasterosteus aculeatus). **We used Illumina-sequenced RAD tags to > identify and type over 45,000 single nucleotide polymorphisms (SNPs) > in each of 100 individuals from two oceanic and three freshwater > populations.** Overall estimates of genetic diversity and > differentiation among populations confirm the biogeographic hypothesis > that large panmictic oceanic populations have repeatedly given rise to > phenotypically divergent freshwater populations. **Genomic regions > exhibiting signatures of both balancing and divergent selection were > remarkably consistent across multiple, independently derived > populations, indicating that replicate parallel phenotypic evolution > in stickleback may be occurring through extensive, parallel genetic > evolution at a genome-wide scale.** Some of these genomic regions > co-localize with previously identified QTL for stickleback phenotypic > variation identified using laboratory mapping crosses. In addition, we > have identified several novel regions showing parallel differentiation > across independent populations. Annotation of these regions revealed > numerous genes that are candidates for stickleback phenotypic > evolution and will form the basis of future genetic analyses in this > and other organisms. This study represents the first high-density > SNP-based genome scan of genetic diversity and differentiation for > populations of threespine stickleback in the wild. These data > illustrate the complementary nature of laboratory crosses and > population genomic scans by confirming the adaptive significance of > previously identified genomic regions, elucidating the particular > evolutionary and demographic history of such regions in natural > populations, and identifying new genomic regions and candidate genes > of evolutionary significance.

Note that the number of SNPs here are smaller than in the case of human studies; you take what you can get, and anthropocentrism in sequencing technology should be no surprise since they’re driven by the profit motive, and humans are the ones doling out hard cash. Additionally, they don’t have [haplotypes](https://en.wikipedia.org/wiki/Haplotype) here. Rather they’re focusing on the SNPs, the specific change on a base pair, and comparing them across & within populations.  
The data comes from 3 freshwater threespine stickleback populations, and 2 oceanic ones. There is a recent body of research which explores the interesting fact that freshwater and marine stickleback in the far north exhibit very different phenotypes, but the geological history of the regions populated by freshwater stickleback imply that they must have evolved only with the last 10,000 years (northern North America was glaciated). A series of genetic analyses conclude that the freshwater populations seem to have been founded repeatedly and independently. So the phenotypic similarities are examples of parallel adaptation, not the radiation of one lineage.  
In this study they’re primarily focusing on statistics such π, [nucleotide diversity](https://en.wikipedia.org/wiki/Nucleotide_diversity), H, [heterozygosity](https://en.wikipedia.org/wiki/Heterozygosity#Heterozygous), Fst and D. These can be calculated from the SNP data they have on hand.  
Here’s a table which shows π & Fst:  
![journal.pgen.1000862.t002.png](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/journal.pgen.1000862.t002.png?resize=500%2C300)![journal.pgen.1000862.t002.png](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/journal.pgen.1000862.t002.png?resize=500%2C300)  
The first two are marine populations, the last three are freshwater. Note the Fst values; remember that they’re telling you how much of the variance is *between* populations. Fst = 1 would indicate that all the variance was between populations. In the paper it is noted that:  
1) There is relatively little structure in the oceanic population. This is evident in the low Fst.  
2) There is relatively more structure between the freshwater populations, and between the freshwater and oceanic populations.  
This comports with the evolutionary history which we would infer based on geological history. Newly derived isolated populations may drift off into their own direction, and different populations which drift off in their own directions are not likely to shadow each other. This is why separation between populations is so often assumed to be a necessary and perhaps even sufficient precursor to speciation.  
But the Fst above throws in all the genomic information into one lump sum. Here’s a plot which illustrates the variance *within the genome*, π & H:  
![fish1.png](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/fish1.png?resize=500%2C437)![fish1.png](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/fish1.png?resize=500%2C437)  
There’s naturally going to be difference from region to region. Some regions exhibit more diversity, and some regions less so. Why would a region exhibit diversity? One possibility that they moot is balancing selection. In particular, balancing selection which maintains a diverse portfolio of alleles related to immunological function. Remember that immune “monocultures” are very susceptible to being wiped out by a virulent pathogen, so low frequency variants are often the highest fitness. Over the long term the constant turnover and flux of the pathogen environment has its shadow in the form of diversity on the immune loci of many complex organisms. The threespine stickleback seem no different.  
[Figure 5](http://www.plosgenetics.org/article/slideshow.action?uri=info:doi/10.1371/journal.pgen.1000862&imageURI=info:doi/10.1371/journal.pgen.1000862.g005) shows one genomic region which breaks down the patterns across the populations. In this region all populations, irrespective of ecology, show high variation, and low between population differentiation. This is a pattern one can find on immune related loci, ancient variants are often preserved from being eliminated through stochastic factors by the high fitness value at very low frequencies. One can therefore have the same the HLA profile on one loci as a chimpanzee and not one’s sibling, so diverse are these immune related genes, and so ancient are many of the variants.  
Next they wanted to look at the genomic pattern of Fst values across these populations. Remember that the Fst for human races is on the order of 0.15, that is, only 15% of the genetic variance is between population. But the Fst for Sub-Saharan Africans and Europeans is SLC24A5 is \~1, almost all the variance is between population. So it matters which gene, or genomic region, you’re looking at. In any case, here’s a chart which shows the Fst values across the genome (peaks are high Fst values):  
![journal.pgen.1000862.g006.png](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/journal.pgen.1000862.g006.png?resize=449%2C600)![journal.pgen.1000862.g006.png](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/journal.pgen.1000862.g006.png?resize=449%2C600)  
I’ve labeled for some clarity, but here’s what’s going on here:  
1) The first panel shows that there aren’t any Fst spikes when you’re comparing the two oceanic populations. We saw earlier a relatively low Fst between the two populations on average, and it turns out that there’s not much deviation from that average. Not too unexpected if there really isn’t much population structure; that is, the two ocean lineages interbreed a lot.  
2) The three subsequent panels are pairwise comparisons between a freshwater line and the average of the oceanic genomes. Now you see a lot of variance, with some huge spikes of Fst. But here’s an interesting point: **note that in many regions the high Fst values seem to coincide.** In other words, there are several regions where the Fst value differentiating freshwater and oceanic lineages is high repeatedly.  
3) The last panel shows there is definitely more between population variance in the freshwater than the oceanic case. This makes sense, the freshwater lineages have no gene flow excepting what might occur indirectly via the oceanic lineage.  
There are some genomic regions where the freshwater stickleback exhibit differences from the oceanic lineages among all three sets. These regions also have reduced genetic variation. Of course, there were some regions where not all the freshwater lineages exhibited high Fst. So it isn’t one dynamic, but a compound of several.  
The relevance of the Fst for the nature of adaptation becomes more obvious when you look at the pattern of private alleles, those variants found only within the population and not shared with others. Ocean stickleback have many more of these than the freshwater stickleback. They have a higher effective population, and have not gone through a population bottleneck, so they have much more extant variation. An analogy with Africans in human genetics might be apropos. **But in regions of high Fst between freshwater-ocean lineages it is the freshwater lineages which have private alleles in relation to the ocean lineages, but not in relation to each other.** The straightforward inference is that the freshwater lineages have a high frequency of an adaptive variant, which they share with each other. If they share the variant, and they are distinct populations, one can infer that the variant was extant in the ancestral population, though at at low frequencies. Since the N’s here are small it could be that the ocean population has many rare alleles which are not noticed in this study.  
After exploring the pattern of genomic variation, the authors looked back and focused on genes which have already been identified to have adaptive and functional significance in regions of high Fst. It was obviously useful to confirm previous work, and the alignment of the two methods reinforces the utility of each. But the previous QTL mapping was focused on particular salient traits (e.g., armor), and the researchers note that mapping the patterns of genomic variation suggest pointers to other SNPs with hitherto unexplored functional significance.  
I’ll let the authors finish:

> This work represents the first whole-genome analysis of threespine > stickleback in which high-density SNP markers reveal signatures of > selection in natural populations. The patterns we detected confirm > findings from earlier studies that used QTL analysis in controlled > crosses or research that used microsatellite markers in natural > populations to scan the genome. However, because of the dense coverage > of SNPs across the genome, and our ability to sample numerous > individuals in multiple populations, our findings are a significant > extension of previous work. The present investigation complements > these prior efforts by exposing new genomic regions that had not yet > been recognized as important in the transition from oceanic to > freshwater life histories. In particular, we find remarkably similar > patterns of conservation and differentiation between three > independently derived freshwater populations as compared to a common > oceanic ancestor. Our data support the view that these patterns are > driven in part by alleles that are repeatedly selected for in > freshwater populations, and maintained at low frequency in oceanic > populations by a balance between gene flow from freshwater and > selection against them in the ocean. Previous work supported the role > of parallel genetic evolution associated with parallel phenotypic > evolution in a small number of traits. Our data indicate that this > pattern is not limited to these traits, and that parallel phenotypic > evolution in stickleback may be underlain by extensive, genome-wide, > parallel genetic evolution.

**Citation:** Hohenlohe PA, Bassham S, Etter PD, Stiffler N, Johnson EA, et al. 2010 Population Genomics of Parallel Adaptation in Threespine Stickleback using Sequenced RAD Tags. PLoS Genet 6(2): e1000862. doi:10.1371/journal.pgen.1000862

### Related Posts:

- [Why I still lean toward a Sub-Saharan African origin
  for…](https://www.gnxp.com/WordPress/2016/02/18/why-i-still-lean-toward-a-sub-saharan-african-origin-for-modern-humanity/) - [Humans mostly out of
  Africa?](https://www.gnxp.com/WordPress/2008/03/06/humans-mostly-out-of-africa/) - [Shellfish & the human
  bottleneck](https://www.gnxp.com/WordPress/2009/12/16/shellfish-the-human-bottleneck/) - [Quantitative genetics strikes back!
  (?)](https://www.gnxp.com/WordPress/2010/02/27/quantitative-genetics-strikes-back/) - [The privileges and burdens of a novel
  inversion](https://www.gnxp.com/WordPress/2012/07/10/the-privileges-and-burdens-of-a-novel-inversion/) - [Humans like us in Sri Lanka 48,000 years
  ago](https://www.gnxp.com/WordPress/2020/06/14/humans-like-us-in-sri-lanka-48000-years-ago/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F03%2F01%2Fthe-parallel-lives-of-threespine-stickleback%2F&linkname=The%20parallel%20lives%20of%20threespine%20stickleback "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F03%2F01%2Fthe-parallel-lives-of-threespine-stickleback%2F&linkname=The%20parallel%20lives%20of%20threespine%20stickleback "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F03%2F01%2Fthe-parallel-lives-of-threespine-stickleback%2F&linkname=The%20parallel%20lives%20of%20threespine%20stickleback "Email")[](https://www.addtoany.com/share)