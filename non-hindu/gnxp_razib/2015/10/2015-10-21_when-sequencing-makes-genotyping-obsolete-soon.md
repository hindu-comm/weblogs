+++
title = "When sequencing makes"
full_title = "When sequencing makes genotyping obsolete"
date = "2015-10-21"
upstream_url = "https://www.gnxp.com/WordPress/2015/10/21/when-sequencing-makes-genotyping-obsolete-soon/"

+++
Source: [here](https://www.gnxp.com/WordPress/2015/10/21/when-sequencing-makes-genotyping-obsolete-soon/).

When sequencing makes genotyping obsolete (soon)

[![Historic_cost_of_sequencing_a\_human_genome.svg](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/10/Historic_cost_of_sequencing_a_human_genome.svg_-300x270.png?resize=300%2C270)![Historic_cost_of_sequencing_a\_human_genome.svg](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/10/Historic_cost_of_sequencing_a_human_genome.svg_-300x270.png?resize=300%2C270)](https://en.wikipedia.org/wiki/Whole_genome_sequencing)For several years there has been a nerdy debate in some labs about sequencing vs. genotyping (more precisely, doing genotyping-by-sequencing vs. going with an array). There are many [pros and cons](http://massgenomics.org/2014/03/gwas-sequencing-realities.html). If you are working on non-model organisms there may not be a good SNP array for you, so the decision is done. If you work on humans in contrast there are several options which are rather affordable. But at some point I assume that sequencing will get so cheap that that SNP array technology will be rendered obsolete, rather like what [RNA-seq](https://en.wikipedia.org/wiki/RNA-Seq) is doing to [microarrays](https://en.wikipedia.org/wiki/Microarray). Currently the cost of sequencing has not declined much for a few years, as [Illumina](https://en.wikipedia.org/wiki/Illumina_(company)) basically squeezes de facto monopoly allowable price out of customers. At some point in the near future this monopoly will break, with the current bet being on a [Nanopore](https://www.nanoporetech.com/) driven disruption of the space. Then the collapse in cost by base genome will commenceagain, until the technology gets good enough that it’s not really the rate limiter in the pipeline.

With the [announcement](http://www.unz.com/gnxp/23andme-is-back-but-a-higher-price-for-fewer-results/) that [23andMe](https://www.23andme.com/) is increasing theirprice, from \$99 to \$199, it got me to thinking about comparing sequencing vs. genotyping. You see, [23andMe](https://www.23andme.com/) uses a [SNP-chip](https://www.23andme.com/more/genotyping/). Last I checked just under one million markers, with a custom set of 30,000 added on to the standard Illumina set. They’ve got over one million people genotyped, so they’ve been at this for a long time. But is \$199 worth it for a one million markers? As regular readers know I’ve been following the progress of the small start-up [Full Genomes](https://www.fullgenomes.com/) for a while. You can get WGS elsewhere, but this group has been very proactive about attempting to cultivate a retail presence (that is, direct-to-consumer). Their prices are on their website, but below is a comparison chart:

|              |                      |          |          |                   |                                                             |
|:-------------|:---------------------|:---------|:---------|:------------------|:------------------------------------------------------------|
| **Company**  | **Service**          | **Cost** | **Time** | **User-friendly** | **How much of genome?**                                     |
| Full Genomes | 30x coverage         | \$1,850  | Months   | No                | Medical grade accuracy of whole genome                      |
| Full Genomes | 10x coverage         | \$745    | Months   | No                | Not medical grade, but probably whole genome                |
| Full Genomes | 4x coverage          | \$375    | Months   | No                | Will have gaps in genome, but most                          |
| Full Genomes | 2x coverage          | \$250    | Months   | No                | Lots of gaps in genome, but a lot of it                     |
| 23andMe      | 1 million marker SNP | \$199    | Weeks    | Yes               | Accurate genotype calls 1 million out of 5 million variants |

Basically [coverage](https://en.wikipedia.org/wiki/Deep_sequencing) is telling you how many times a marker is going to come back in the raw results. If there an error in one particular positionyou can figure that out pretty easily if you expect to have sampled it 30 times. In contrast, if you have only one read to look at for a position then if it’s not matching the reference it is highly like you’re seeing a false positive. For evolutionary genomics work low coverage is really not a major issue, because you’re curious about population wide dynamics. But if you want to make accurate calls which are medically actionable, then you need to be confident, and for that you need to have high depth on your coverage. With \>30x you’re catching almost all the variants in your genome, and so can pick up things like mutations novel to you, which wouldn’t come back on a SNP-array in most cases, since they’re ascertained on common variants.

Since I knew [Full Genomes](https://www.fullgenomes.com/)‘ cost chart I knew that their 2x sequencing is now approaching the genotyping results provided by [23andMe](https://www.23andme.com/) in terms of apples-to-oranges cost comparisons. I say apples-to-oranges, because the truth is that [Full Genomes](https://www.fullgenomes.com/) is providing a different service. It’s very much of a “rough cut,” while [23andMe](https://www.23andme.com/) is delivering turn-key personal genomics. **But, if you are comfortable with .bam and .vcf files, then now is the time to actually consider sequencing** (though from what I know [Full Genomes](https://www.fullgenomes.com/)‘ turnaround time is on the order of three to six months, while [23andMe](https://www.23andme.com/) is closer to one month). For me the sweet spot right now would be 10x, as 30x is probably overkill, especially if you already have genotype data and are comfortable with imputation….

### Related Posts:

- [Arrays on the way
  out?](https://www.gnxp.com/WordPress/2007/05/17/arrays-on-the-way-out/) - [Highly parallel genomic
  assays](https://www.gnxp.com/WordPress/2006/07/20/highly-parallel-genomic-assays/) - [Rapture for the discerning non-model
  biologist](https://www.gnxp.com/WordPress/2015/10/13/rapture-for-the-discerning-non-model-biologist/) - [On the personal genomics turning
  point](https://www.gnxp.com/WordPress/2010/05/18/on-the-personal-genomics-turning-point/) - [Next-generation
  sequencing](https://www.gnxp.com/WordPress/2007/02/18/next-generation-sequencing/) - [The Venter genome: science and
  ethics](https://www.gnxp.com/WordPress/2007/09/16/the-venter-genome-science-and-ethics/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2015%2F10%2F21%2Fwhen-sequencing-makes-genotyping-obsolete-soon%2F&linkname=When%20sequencing%20makes%20genotyping%20obsolete%20%28soon%29 "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2015%2F10%2F21%2Fwhen-sequencing-makes-genotyping-obsolete-soon%2F&linkname=When%20sequencing%20makes%20genotyping%20obsolete%20%28soon%29 "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2015%2F10%2F21%2Fwhen-sequencing-makes-genotyping-obsolete-soon%2F&linkname=When%20sequencing%20makes%20genotyping%20obsolete%20%28soon%29 "Email")[](https://www.addtoany.com/share)
