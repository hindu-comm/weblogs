+++
title = "The HGDP in the"
full_title = "The HGDP in the postascertainment era"
date = "2018-07-30"
upstream_url = "https://www.gnxp.com/WordPress/2018/07/30/the-hgdp-in-the-post-ascertainment-era/"

+++
Source: [here](https://www.gnxp.com/WordPress/2018/07/30/the-hgdp-in-the-post-ascertainment-era/).

The HGDP in the post-ascertainment era

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/07/41qapuvdFL._SX331_BO1204203200_.jpg?resize=175%2C262&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/07/41qapuvdFL._SX331_BO1204203200_.jpg?resize=175%2C262&ssl=1)](https://www.amazon.com/exec/obidos/ASIN/0521539870/geneexpressio-20/)In the 1990s there was a huge debate around the “Human Genome Diversity Project” (HGDP). By the HGDP I don’t mean what you probably know as the HGDP panel, but a more ambitious attempt to genotype tens of thousands of individuals across the world. In the end activists “won”, and the grand plans came to naught. If you want to read about it, [The Human Genome Diversity Project: An Ethnography of Scientific Practice](https://www.amazon.com/exec/obidos/ASIN/0521539870/geneexpressio-20/ref=as_at?creativeASIN=0521539870&linkCode=w61&imprToken=HDBfw7fzY71wCCxR00-Jyw&slotNum=0) has a scholarly viewpoint, though you can also just ask someone who was involved with the human population genetics community in the 1990s (this not a large set of scholars).

Ultimately the HGDP became the samples from L. L. Cavalli-Sforza’s dataset which you read about in [The History and Geography of Human Genes](https://www.amazon.com/exec/obidos/ASIN/0691029059/geneexpressio-20/ref=as_at?creativeASIN=0691029059&linkCode=w61&imprToken=GAMmUeEsNpUWirutorXv6A&slotNum=214). This is what drives the [HGDP Browser](http://hgdp.uchicago.edu/cgi-bin/gbrowse/HGDP/). It’s also the data set at the heart of papers like [Worldwide Human Relationships Inferred from Genome-Wide Patterns of Variation](http://science.sciencemag.org/content/319/5866/1100). Here is the abstract:

> Human genetic diversity is shaped by both demographic and biological > factors and has fundamental implications for understanding the genetic > basis of diseases. We studied 938 unrelated individuals from 51 > populations of the Human Genome Diversity Panel at **650,000 common > single-nucleotide polymorphism loci.** Individual ancestry and > population substructure were detectable with very high resolution. The > relationship between haplotype heterozygosity and geography was > consistent with the hypothesis of a serial founder effect with a > single origin in sub-Saharan Africa. In addition, we observed a > pattern of ancestral allele frequency distributions that reflects variation in population dynamics among geographic regions. This data set allows the most comprehensive characterization to date of human genetic variation.

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/10/historyandgeography.jpeg?resize=195%2C258&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/10/historyandgeography.jpeg?resize=195%2C258&ssl=1)](https://www.amazon.com/exec/obidos/ASIN/0691029059/geneexpressio-20/ref=as_at?creativeASIN=0691029059&linkCode=w61&imprToken=GAMmUeEsNpUWirutorXv6A&slotNum=214)These SNPs though were ascertained on European populations. That is, the genetic variation tended to be genetic variation found in Europe. This is a problem, and one reason that the [Human Origins Array](http://www.genetics.org/content/early/2012/09/06/genetics.112.145037.short) was developed. The ascertainment problem was [really obvious](https://www.nature.com/articles/nature08795) when researchers were looking at Khoisan genomes, and noticed how much variation they had that wasn’t being captured on SNP-arrays.

Today, we’ve finally moving beyond the era where ascertainment is so much of an issue. At the SMBE meeting earlier this month [Anders Bergstrom](https://www.sanger.ac.uk/people/directory/bergstrom-anders) presented results from the HGDP **using whole-genome analysis.** When you look at the whole genome, you obviate the problem with selecting a biased subset of the variation. You can look at all the variation, or vary the variation you want to look at.

Bergstrom & company will have a paper on the whole-genome analysis of the HGDP in the near future. I assume it will be somewhat like the [1000 Genomes paper](https://www.nature.com/articles/nature15393), but I bet you the SNP count will be higher, because they have Khoisan in their samples (along with Mbuti, etc.). Anders shared with me some of the preliminary data that the [Sanger Institute has generated](https://www.sanger.ac.uk/).

Below the fold I plotted a PCA of the HGDP data. First, the classic SNP-chip data. Second, SNPs pulled out of the WGS which are very high quality calls (though they may still have wrong calls), but have a minor allele frequency of at least 1% (\~1.5 million). You immediately notice the Eurasian compression along PC 1. Finally, using \~15 million SNPs that had no missingness in the data, you see you PC 2 being defined by San Bushmen vs. non-San-Bushmen, while Mbuti Pygmies along with Biaka clearly are the furthest along PC 1 excepting the San. There are 6 San Bushmen in the data. If there are SNPs which are very distinct to this group, and not polymorphic in other populations, then my 1% cut-off would actually remove that variation.

It’s an interesting world we live in, thanks to research groups like the[Sanger Institute](https://www.sanger.ac.uk/), [Estonian Biocentre](http://evolbio.ut.ee/), and the [1000 Genomes Project](http://www.internationalgenome.org/), as well as tools such as [PLINK](https://www.cog-genomics.org/plink/1.9/). Analysis that took decades in the 20th century can now be whipped out in a matter of hours. Better analyses in fact.

![650,000 SNPs (European ascertained)](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/07/hgdp.png?resize=640%2C465&ssl=1)



![1.5 million SNPs, 1% or more minor allele frequency](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/07/WGS_LD_01.png?resize=640%2C465&ssl=1)

￼

![15 million SNPs, 0 “no calls”](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/07/WGS.png?resize=640%2C465&ssl=1)



### Related Posts:

- [The HGDP made less
  racist!](https://www.gnxp.com/WordPress/2011/08/17/the-hgdp-made-less-racist/) - [HGDP Selection
  Browser](https://www.gnxp.com/WordPress/2008/11/10/hgdp-selection-browser/) - [HGDP browser is
  out!](https://www.gnxp.com/WordPress/2008/11/10/hgdp-browser-is-out/) - [Signals of recent positive selection in a worldwide
  sample…](https://www.gnxp.com/WordPress/2009/03/24/signals-of-recent-positive-selection-in-a-worldwide-sample-of-human-populations-again-sort-of/) - [Personal Genome
  Project](https://www.gnxp.com/WordPress/2007/12/03/personal-genome-project/) - [The Human Genome Diversity Project at
  high-coverage!](https://www.gnxp.com/WordPress/2020/03/25/the-human-genome-diversity-project-at-high-coverage/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2018%2F07%2F30%2Fthe-hgdp-in-the-post-ascertainment-era%2F&linkname=The%20HGDP%20in%20the%20post-ascertainment%20era "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2018%2F07%2F30%2Fthe-hgdp-in-the-post-ascertainment-era%2F&linkname=The%20HGDP%20in%20the%20post-ascertainment%20era "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2018%2F07%2F30%2Fthe-hgdp-in-the-post-ascertainment-era%2F&linkname=The%20HGDP%20in%20the%20post-ascertainment%20era "Email")[](https://www.addtoany.com/share)
