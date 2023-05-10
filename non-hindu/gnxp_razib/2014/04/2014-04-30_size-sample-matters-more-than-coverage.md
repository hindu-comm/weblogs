+++
title = "Size matters more than"
full_title = "Size matters more than coverage"
date = "2014-04-30"
upstream_url = "https://www.gnxp.com/WordPress/2014/04/30/size-sample-matters-more-than-coverage/"

+++
Source: [here](https://www.gnxp.com/WordPress/2014/04/30/size-sample-matters-more-than-coverage/).

Size (sample) matters more than coverage

![[**Credit**](https://en.wikipedia.org/wiki/File:Historic_cost_of_sequencing_a_human_genome.svg)](https://i0.wp.com/www.unz.com/wp-content/uploads/2014/04/Historic_cost_of_sequencing_a_human_genome.svg_-300x270.png?resize=300%2C270)

We live in an age where it’s almost anachronistic to talk about “-omics.” When a technology becomes seamless in our day to day life it becomes unworthy of notice. That being said we’re still in the phase of genomics where a lot of the details of “best practices” are being hashed out (the proliferation of “pipelines” for relatively pedestrian tasks makes that clear). Recently I stumbled upon two papers which I thought would be useful to give a little more coverage to, [Population genomics based on low coverage sequencing: how low should we go?](http://onlinelibrary.wiley.com/doi/10.1111/mec.12105/full)and [Assessing the Effect of Sequencing Depth and Sample Size in Population Genetics Inferences](http://www.plosone.org/article/info%3Adoi%2F10.1371%2Fjournal.pone.0079667). At issue here is coverage versus sample size. By [coverage](https://en.wikipedia.org/wiki/Shotgun_sequencing#Coverage) I mean the expected number of reads that will hit a nucleotide. If you have 100**×** you’ll expect to get 100 hits on a base, and if you have 1**×** you’re only getting one hit. Because of variation lots of positions are going to be above or below your expected coverage. Why this matters on the most prosaic level is that there is going to error in the results you get back from sequencing, and if you have many hits on the same position you can distinguish true from false polymorphism. For many projects people today seem to prefer on the order of 30**×**.

![**Citation:** Fumagalli M (2013) Assessing the Effect of Sequencing Depth and Sample Size in Population Genetics Inferences. PLoS ONE 8(11): e79667. doi:10.1371/journal.pone.0079667](https://i0.wp.com/www.unz.com/wp-content/uploads/2014/04/journal.pone_.0079667.g001-300x276.png?resize=300%2C276)

As the second paper is open access I’ll refer to its results, which are broadly in agreement with the first. When attempting to estimate simulated (so the author knows the “true” values) population genetic statistics or population substructure **increasing sample size at even 1-2**x** coverage gave much more bang for the buck than ratcheting up coverage.** The methodology employed a trade off between sample size and coverage, so that (sample size)x(coverage) remained invariant. It actually wasn’t totally surprising for me in relation to population structure, since noisy and error prone data can still be quite useful assuming there isn’t a systematic bias (i.e., the error is random, so you’re left to thousands of useful markers after employing stringent quality control). But it did surprise how much of an effect there was in standard population genetic statistics of diversity. And the problems in that domain only increase when you have a rapidly growing population so that there is an excess of rare variants (like humans), rather than a constant population size.\*

Finally, obviously this is a conclusion geared toward biologists focusing on population-scale dynamics, whether it be molecular ecologists or population geneticists. But as sequencing becomes more ubiquitous, and money remains finite, these sorts of balancing acts between coverage versus sample size will come more to the fore.

\* Also, the author observes that instead of employing a hard cut off of some sort in variant calling, but utilizing a probabilistic model such as in [ANGSD](http://popgen.dk/wiki/index.php/ANGSD), you can get a lot more juice out of low coverage.





### Related Posts:

- [When sequencing makes genotyping obsolete
  (soon)](https://www.gnxp.com/WordPress/2015/10/21/when-sequencing-makes-genotyping-obsolete-soon/) - [The Illumina
  whole-genome-sequence](https://www.gnxp.com/WordPress/2009/07/05/the-illumina-whole-genome-sequence/) - [Rapture for the discerning non-model
  biologist](https://www.gnxp.com/WordPress/2015/10/13/rapture-for-the-discerning-non-model-biologist/) - [The \$2,000 "whole
  genome"](https://www.gnxp.com/WordPress/2015/01/10/the-2000-whole-genome/) - [Batch effects in the 1000 Genomes
  data?](https://www.gnxp.com/WordPress/2019/05/04/batch-effects-in-the-1000-genomes-data/) - [Nebula Genomics, 12-hour
  sale](https://www.gnxp.com/WordPress/2021/07/24/nebula-genomics-12-hour-sale/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2014%2F04%2F30%2Fsize-sample-matters-more-than-coverage%2F&linkname=Size%20%28sample%29%20matters%20more%20than%20coverage "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2014%2F04%2F30%2Fsize-sample-matters-more-than-coverage%2F&linkname=Size%20%28sample%29%20matters%20more%20than%20coverage "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2014%2F04%2F30%2Fsize-sample-matters-more-than-coverage%2F&linkname=Size%20%28sample%29%20matters%20more%20than%20coverage "Email")[](https://www.addtoany.com/share)
